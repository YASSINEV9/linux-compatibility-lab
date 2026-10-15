# RTL8187 IPK Package Installation on OpenWrt

## Target Device
- Router: Netgear R6220
- USB Wi-Fi adapter: Alfa RTL8187
- Target OpenWrt version: 24.10.x

## 1. Transfer the IPK Package

From Windows PowerShell:

    scp "C:\path\to\kmod-rtl8187.ipk" root@192.168.1.1:/tmp/

Replace the path and router IP with your actual values.

## 2. Connect via SSH

    ssh root@192.168.1.1

## 3. Verify the Package

    ls -lh /tmp/kmod-rtl8187.ipk
    uname -r
    ubus call system board

## 4. Install the Package

OpenWrt 24.10 normally uses APK as its package manager, so a legacy IPK package may not be directly installable.

Check compatibility and package format before proceeding. Do not rename an IPK file to APK.

## 5. Verify the Driver

    find /lib/modules -iname '*rtl8187*'
    dmesg | tail -50

## Important
The package must match the router's architecture, kernel ABI, and firmware version. Successful installation and driver operation must be tested on the actual device.
