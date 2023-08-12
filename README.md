# Opencore-Aspire-E15
Opencore on an Intel i3-4005U, HD Graphics 4000

Opencore config for my old laptop.
Current OC version: 0.9.4
Current macOS Version: 12.6.7

### Hardware
- RAM: 4GB DDR3
- HDD: 500GB something
- CPU: Intel i3-4005u
- Ethernet: Realtek RTL8111
- Audio: Realtek ALC283
- WiFi & Bluetooth: itlwm + IntelBluetoothFirmware works
### Installation
1. Download the latest release
2. Download propertree and edit EFI/OC/config.plist
    1. Change PlatformInfo -> MLB, ROM, SystemUUID and SystemSerialNumber using [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS)
3. Create the macOS Installer USB-Stick using [this](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/) guide. You don't need to create the EFI, that work have I done already. 
4. Update the BIOS settings according to [this](https://dortania.github.io/OpenCore-Install-Guide/config-laptop.plist/haswell.html#intel-bios-settings) guide. 
5. Insert USB and boot! When entering the macOS Recovery, click Disk Utility, format your Disk as APFS/GUID and then install macOS.

### Working
- iServices
- Davinci Resolve
- Audio
- GPU Acceleration
- WiFi + Bluetooth (non-native wifi)
- all Continuity features exept AirDrop (because of intel wifi and BT)
- USB Ports
- Shutdown and Restart (sometimes shutdown is a reboot, dortania guide didn't help. ACPI aml files are included to test, but disabled by default)
- CPU temp


### Not working
- Sleep
- Shutdown (not always)
