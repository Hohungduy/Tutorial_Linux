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
A --> |Before built2| C[Toolchain]
A --> |Before built3| D[Include]
A --> |Before built4| E[Scripts]
A --> |Before built5| F[Target]
A --> |Before built6| G[Package]
A --> |After Built1| I[bin]
A --> |After built2| K[build_dir]
A --> |After built3| K[staging_dir]
A --> |After built4| K[dl_dir]
A --> |After built5| K[feeds_dir]
```
```mermaid
graph TD
A[Christmas] -->|Get money| B(Go shopping)
B --> C{Let me think}
C -->|One| D[Laptop]
C -->|Two| E[iPhone]
C -->|Three| F[Car]
```


































----------------------------------------------------------------------------------
Author: Duy. Ho
Date: 14/11/2019
email:duyhohung.work@gmail.com
