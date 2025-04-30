# EFI for chipset H610M, CPU i5-13400F, GPU RX 6650 XT and Wifi Fenvi Broadcom BCM4360 (aka BCM94360)

## Machine Hardware
CPU MODEL: 			13th Gen Intel(R) Core(TM) i5-13400F Raptor Lake

GPU MODEL:			[AMD/ATI] Navi 23 [Radeon RX 6650 XT / 6700S / 6800S] (rev c1)

CHIPSET:			H610M K DDR4

AUDIO MODEL:			ALC897 Analog [ALC897 Analog]

NETWORK WIFI:			Broadcom Inc. and subsidiaries BCM4360 802.11ac Dual Band Wireless Network Adapter (rev 03)

NETWORK LAN:			RTL8111/8168/8211/8411 PCI Express Gigabit Ethernet Controller

DISK INFO:			CT1000P3PSSD8


## Before Install 
Use folder EFI-Install, as this is a small version make to only the install process.
Also:
- Change SMBIOS Information.
- Copy WhateverGreen.kext to kext folder 
- Open config.plist with proper-tree
- File › OC Clean Snapshot
- Disable NootRx.kext
- Save config.plist

## After Install
User folder EFI-after-install, this version has all kexts needed to work GPU and Wifi.
This version is intended to be bootable directly to MacOS, if you want to see the picker and other disks like with Windows, change:
- Misc › Boot › ShowPicker to true
- Misc › Security › ScanPolicy to 0

Also:
- Change the SMBIOS information to the one created before
- This version already has NootRx.kext enabled 
- Remember to ResetNvram. If ShowPicker is Disabled: After start the computer press ESC to enter on the picker screen, than press space and choose ResetNvram
- After the first boot with this version of EFI, download and install OpenCore Legacy Patcher. Then run the Post-Install Root Patch and reboot.
- Map (on windows) the USBs as described here https://github.com/USBToolBox/tool then replace the UTBMap.kext on kext folder.

## TODO
- Fix sleep issues.

## other tool and files
- pack-activate-wifi-bt-BCM94360-sonoma.zip the files inside are already on the EFI-after-install
