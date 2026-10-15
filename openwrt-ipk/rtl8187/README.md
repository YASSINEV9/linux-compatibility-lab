# RTL8187 Driver for OpenWrt

## Target Device
Netgear R6220

## USB Wi-Fi Adapter
Alfa RTL8187

## Target Configuration
- OpenWrt: 24.10.2
- Target: ramips/mt7621
- Architecture: mipsel_24kc
- Kernel: 6.6.93

## Required Package
kmod-rtl8187

## Status
Custom IPK build required. The package must match the exact kernel ABI and dependencies.

## Dependencies
- kmod-eeprom-93cx6
- kmod-mac80211
- kmod-usb-core
