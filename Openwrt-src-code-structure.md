-----------------------------------------------------------------------------
#Tutorials for Openwrt source code structure
----------------------------------------------------------------------------
##**General source structure:**

1. Before building

 - /config : Configuration file for **make menuconfig**

 - /include: Makefile configurations file

 - /package: Main packages makefile and configuration (patches). The OpenWRT Makefile has its own syntax, different from the conventional Makefile of Linux make tool.

 - /scripts: extra scripts through build process (and Openwrt package management)

 - /target: makefile and configuration for building imagebuilder, kernel and the toolchain built by buildroot

 - /toolchain: makefile and configuration for building the toolchain. It contains all the build instruction to fetch the kernel headers, the C library, the bin-utils, the compiler ifself and the debugger. If you add a new architecture, you would add a configuration for 

the C library here.

 - /tools : extra tools used throughout the build process

2. After building:

 - bin: where the firmware image will be generated and all .ipk package files will be generated

 - dl: Where the user-space package tarballs will be downloaded.

 - build_dir: where all user-space tools and kernel module and other module will be cross-compiled. It contains a wide range of architecture.

 - staging_dir: Where the cross-compilation tools will be installed.

 - feeds: It contains other module which is not the main package.

## The process of OpenWRT image building (step by step):

1. Download the cross-compilation tools, kernel headers,etc,....

2. Set up the staging directory ( staging_dir/). this is where the cross-compilation toolchain will be installed. If you want to use the same cross-compilation toolchian for other purposes, sush as compile the third-party applications, you can find the cross-compiler tools in this directory and then use arch-linux-gcc to compile your application.

3. Create the download directory (dl/ by default). This is where the tarballs will be downloaded.

4. Create the build_dir/. This is where user-space tools will be compiled.

5. Create the target directory (build_dir/target-arch/root by default) and the target filesystem skeleton. This directory will contain the final root filesystem.

6. Install the user-space packages to the root filesystem and compress the whole root file system with suitalbe format. The result firmware image is generated in bin/.

##




























----------------------------------------------------------------------------------
Author: Duy. Ho
Date: 14/11/2019
email:duyhohung.work@gmail.com
