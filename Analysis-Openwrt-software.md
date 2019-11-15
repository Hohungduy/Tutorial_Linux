-----------------------------------------------------------------------------------
# The analysis of OpenWRT software architecture
----------------------------------------------------------------------------------

## General

OpenWRT is a Linux release version used in embedded system. OpenWRT has four part:
the boot load program (boot loader), Linux Kernel, file system (actual in Linux kernel), user-space application.

|   UCI  |  OPKG  |   User Programs  |
| :----- | :----: | ---------------: |
|          BusyBox                   |
|          uClibc                    |
|          Linux kernel              |

 - UCI: is a interface provided by OpenWRT for configuration of user space and managenment system, it it a C language library which can be easily integrated into user-space application and it give us an great opportunity to save the system configuration information to the user through the change application file in *** etc/config **. Through command line or LuCI web interface, we can easily modify UCI configuration file.

 - OPKG: download package tools

 - User programs: usually exists in the form of .ipk software

 - BusyBox is the root file system of OpenWRT and the file carrier for OPnWRT to run, BusyBox usually kept the system command, the system configuration file, the library that user application needs and 3rd-party application.

 - ulIbc is a software library of OpenWRT os

## Construction of OpenWRT system

OpenWRt is Linux release version used for embedded device particular router, the mirror on OpenWRT

|  U-Boot (512 kb) | linux kernel (5 MB) |    Rootfs (122 MB)    |
| :--------------- | :-----------------: | --------------------: |


