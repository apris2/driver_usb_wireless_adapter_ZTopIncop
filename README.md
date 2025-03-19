
# Driver WiFi ZTopInc  

This repository is a fork of [driver_wifi_ztopinc](https://codeberg.org/sallecta/driver_wifi_ztopinc.git). Modifications have been made to improve compatibility with **Ubuntu 24.04.2 LTS** and **Linux kernel 6.11.0-19-generic**.  

## Changes  
- Fixed an issue in `usb.c` at line 1114 and other related sections.  
- Ensured compatibility with **Ubuntu 24.04 (Noble)**.  
- Adapted the driver for **Linux kernel 6.11.0-19-generic**.  
- Added support for **ZTopInc 802.11n NIC** (**ID: 350b:9101**).  

## Installation  

### Install Dependencies  
Before building the driver, install the necessary packages:  

```bash
sudo apt update
sudo apt install dkms build-essential git
```

### Clone the Repository and Build the Driver  
Run the following commands to clone this repository, navigate to the directory, and compile the driver:  

```bash
make
sudo insmod ./zt9101_ztopmac_usb.ko cfg=./wifi.cfg
```

### Troubleshooting  
If you encounter module signature errors, try disabling **Secure Boot** in your BIOS.  

## System Information  
- **Device**: ZTopInc 802.11n NIC (**ID: 350b:9101**)  
- **OS**: Ubuntu 24.04.2 LTS (Noble)  
- **Kernel**: 6.11.0-19-generic  

---

