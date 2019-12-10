--------------------------------------------------------------------------------
# Tutorial for develop OpenWRT source
-------------------------------------------------------------------------------
 This tutorial is designed for OpenWRT routers. It allows you to have standard procedure to develop OpenWRT with OpenWRT source code.

1. Using quilt to apply new patch or edit patch after modifying OpenWRT source code

	1.1. Introduction

 	Patches is the way for us to apply and update the difference between OpenWRT source code and Linux kernel sorce code, between this platform and other platform, this version vs other versions.

	Quilt is a tool of bthe built system for easy patch management.
	1.2. Prepare for quilt configuration

	In order to let quilt creates pathes in the prefered format, a configuration file .quiltrc containg common diff and patch options must be created in the home directory.
       
	Ex: duyho/home/~ :
          
	```shell
	cat > ~/.quiltrc <<EOF
	QUILT_DIFF_ARGS="--no-timestamps --no-index -p ab --color=auto"
	QUILT_REFRESH_ARGS="--no-timestamps --no-index -p ab"
	QUILT_SERIES_ARGS="--color=auto"
	QUILT_PATCH_OPTS="--unified"
	QUILT_DIFF_OPTS="-p"
	EDITOR="nano"
	EOF
	``` 

2. Patching a Package

	- Prepare package source directory:

	```shell
	make package/example/{clean,prepare} V=s QUILT=1
	```

	- Open new terminal to access the build_dir directory:

	```shell
	cd build_dir/target-aarch64-cotex-a53/linux-cotexa53/linux-4.19.81/
	```

	- Understand the patches, first list patches in series

	```shell
	quilt series
	```

	- Show current patches in series

	```shell
	quilt top
	```

	- Show files in current patch

	```shell
	quilt files
	```

	- Show the difference in patches
	
	```shell
	quilt diff
	```

	- Tell quilt you want to make a new patch

	```shell
	quilt new 0xx-fix_something.patch
	```

	3 first number is:

	|Options for 3 first number| Desciptions                                 |
	| ------------------------ | :-----------------------------------------: |
	|          0xx             | upstream backports                          |
	|          1xx             | code awaiting upstream merge                |
	|          2xx             | kernel build/config/headers patches         | 
	|          3xx             | architecture specific patches               |
	|          4xx             | mtd related patches (subsystem and drivers) |
	|          5xx             | filesystem related patches                  |
	|          6xx             | generic network patches                     |
	|          7xx             | network / phy driver patches                |
	|          8xx             | other drivers                               |
	|          9xx             | uncategorized other patches                 |

	- If, we has created a patches before, we just advance to this patch that needs to be edited:

	quilt push xxx-fix_something.patch

	- Add and Edit the patch files simply

	Ex:
	```shell
	quilt edit package/feeds/luci/luci-app-ipsecvpn
	```

	- Review the changes

	```shell
	quilt diff
	```

	- update the current patch with the change made

	```shell
	quilt refresh
	```

	- Change back to the toplevel directory ( /OpenWRT/)

	```shell
	cd ../../../
	```

	- Update the package

	```shell
	make package/feeds/luci/update V=s
	```

	- Build the package

	```shell
	make package/example/{clean,compile} package/index V=s
	```

# Note: Base-file (root/etc/...) is in OpenWRT/Package. Package and feeds is in OpenWRT/packages

3. Adding or editting the kernel patches

	- Prepare kernel tree

	```shell
	make target/linux/{clean,prepare} V=s QUILT=1
	```

	- Enter the source tree

	```shell
	cd build_dir/target-*/linux-*/linux-*
	```

	- Create the new patch for editting the kernel source code

	If it is the common patches for all architecture:

	```shell
	quilt new generic/010-main_code_fix.patch
	```

	- Patches in platform folder should made with ( /build_dir/target-aarch64../linux...)

	```shell
	quilt new platform/010-main_code_fix.patch
	```

	- Edit the source

	```shell
	quilt edit ./net/ipv4/esp4.c
	```

	- review the change and refresh to update patches

	```shell
	quilt diff
	quilt refresh
	```

	- Build the source:
	
	```shell
	make target/linux/{compile,install} V=s
	make package/index
	make target/linux/update
	```
# NOTE: source file of linux kernel in /build_dir/target../linux../linux.../
	 
