
# Driver WiFi ZTopInc for Linux  

This repository provides a **Linux WiFi driver** for the **ZTopInc 802.11n USB wireless adapter NIC** (**ID: 350b:9101**) , ensuring compatibility with **Ubuntu 24.04 LTS** and **Linux kernel 6.11.0-19-generic**.  

It is a fork of [driver_wifi_ztopinc](https://codeberg.org/sallecta/driver_wifi_ztopinc.git) with **fixes and kernel support improvements**.  

## Features & Fixes  
- **Fixed** an issue in `usb.c` at line 1114 and related sections.  
- **Optimized** for **Ubuntu 24.04 (Noble)** and **Linux kernel 6.11.0-19-generic**.  

## Installation Guide  

### Step 1: Install Dependencies  
Before compiling the **Linux WiFi driver**, install the required packages:  

```bash
sudo apt update
sudo apt install dkms build-essential git
```

### Step 2: Clone, Build, and Load the Driver  
Run the following commands to clone this repository, navigate to the directory, and compile the driver:  

```bash
make
sudo insmod ./zt9101_ztopmac_usb.ko cfg=./wifi.cfg
```

### Step 3: Troubleshooting  
If the driver fails to load due to **module signature errors**, disable **Secure Boot** in your BIOS.  

## System Compatibility  
- **Device**: ZTopInc 802.11n USB Wireless Adapter (**ID: 350b:9101**)  
- **OS**: Ubuntu 24.04.2 LTS (Noble)  
- **Kernel**: 6.11.0-19-generic  
- **Supported Architectures**: x86_64  

## Images  
![ZTopInc WiFi Adapter](https://github.com/apris2/driver_usb_wireless_adapter_ZTopIncop/raw/main/IMG1.jpg)  
![ZTopInc WiFi Adapter](https://github.com/apris2/driver_usb_wireless_adapter_ZTopIncop/raw/main/IMG2.jpg)  

---  
