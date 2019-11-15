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
### Structure of OpenWRT source code
```mermaid
graph TD
A[Buildroot Root dir] --> |Before built1| B[Tools]
A[Buildroot Root dir] --> |Before built2| C[Toolchain]
A[Buildroot Root dir] --> |Before built3| D[Include]
A[Buildroot Root dir] --> |Before built4| E[Scripts]
A[Buildroot Root dir] --> |Before built5| F[Target]
A[Buildroot Root dir] --> |Before built6| G[Package]
A[Buildroot Root dir] --> |After Built1| I[bin]
A[Buildroot Root dir] --> |After built2| K[build_dir]
A[Buildroot Root dir] --> |After built3| K[staging_dir]
A[Buildroot Root dir] --> |After built4| K[dl_dir]
A[Buildroot Root dir] --> |After built5| K[feeds_dir]
```



































----------------------------------------------------------------------------------
Author: Duy. Ho
Date: 14/11/2019
email:duyhohung.work@gmail.com
