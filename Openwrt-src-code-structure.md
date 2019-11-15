-----------------------------------------------------------------------------
#Tutorials for Openwrt source code structure
----------------------------------------------------------------------------
1. General source structure:

 - /config : Configuration file for **make menuconfig**

 - /include: Makefile configurations file

 - /package:packages makefile and configuration

 - /scripts: extra scripts through build process

 - /target: makefile and configuration for building imagebuilder, kerneland the toolchain built by buildroot

 - /toolchain: makefile and configuration for building the toolchain

 - /tools : extra tools used throughout the build process

```mermaid
graph TD;
A[Buildroot Root dir] --> B[Tools];
A[Buildroot Root dir] --> C[Toolchain]
A[Buildroot Root dir] --> D[Include]
A[Buildroot Root dir] --> E[Scripts]
A[Buildroot Root dir] --> F[Target]
A[Buildroot Root dir] --> G[Package]
A[Buildroot Root dir] --> |After Built| I[bin]
A[Buildroot Root dir] --> |After built| K[build_dir]
A[Buildroot Root dir] --> |After built| K[staging_dir]
A[Buildroot Root dir] --> |After built| K[dl_dir]
A[Buildroot Root dir] --> |After built| K[feeds_dir]
```



































----------------------------------------------------------------------------------
Author: Duy. Ho
Date: 14/11/2019
email:duyhohung.work@gmail.com
