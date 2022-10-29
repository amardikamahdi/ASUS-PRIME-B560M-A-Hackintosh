# ASUS-PRIME-B560M-A-Hackintosh

## *Take a note that this is may not be working on your setup, so DWYOR*

## The setup specs

| Component | Type | Reference |
| ------ | ------ | ----- |
| Motherboard | ASUS PRIME B560M-A (LGA-1200) | https://www.asus.com/motherboards-components/motherboards/prime/prime-b560m-a/
| Processor | Intel Core i3-10105F | https://ark.intel.com/content/www/id/id/ark/products/203474/intel-core-i310105f-processor-6m-cache-up-to-4-40-ghz.html
| iGPU | - | - |
| dGPU | AMD Radeon RX 560 (Buffin) | https://www.amd.com/en/products/graphics/radeon-rx-560 |
| RAM | TFORCE DELTA RGB DDR4 (8 X 4)  | https://www.teamgroupinc.com/en/product/delta-rgb-ddr4 |
| Audio Codec | Realtek ALC897 (Built-in with Motherboard) | https://www.asus.com/motherboards-components/motherboards/prime/prime-b560m-a/
| Trackpad | - | - |
| Storage | Digital Alliance NVME DA930E 128GB | https://digitalalliance.co.id/produk/m-2-pro-nvme-128gb/ |
| Wireless LAN | Broadcom BCM94360CS2 with PCIe Adapter | https://www.amazon.com/Broadcom-Bcm94360cs2-Bcm94360cs2ax-Bluetooth-Wireless/dp/B00PDNDQ0K
| Ethernet | Intel Ethernet Connection 1219-V (Built-in with Motherboard) | https://www.asus.com/motherboards-components/motherboards/prime/prime-b560m-a/

## Current version of this Opencore setup : 0.8.5

## Installation
Clone this repo
```sh
git clone https://github.com/pussy-cats/ASUS-PRIME-B560M-A-Hackintosh.git
```
Then you can use your EFI Mounter, im personally using [MountEFI][MountEFI]

## What is working and not working?
```sh
Well, i can tell you almost everything works out of the box, even iServices if you choose the right SMBIOS
```

## Notes (Read this)

- Im using [Opencore] bootloader for this to be working. I have tested using Debug version of [Opencore] for bug-free this config, so i hope this config doesn't hurt your hardware

- SMBIOS use in this EFI is **iMacPro1,1** so you can generate your own using [GenSMBIOS] and then [follow this guide][SMBIOSGuide]

> Take a note that from the step above, **you only need to know how to input your SMBIOS to your config, not following the SMBIOS there as i dont have any iGPU, so **iMacPro1,1** is selected**.

- This config has integrated SecureBootModel to iMacPro1,1, so if you are running issues like can't boot, try to change this value of section on your **config.plist**

> Misc->Security->SecureBootModel = Disabled

- Last, **DWYOR!**

## Credits
- Acidanthera - for their beatiful [Opencore]
- Corpnewt - for their beautiful [GenSMBIOS] and [MountEFI]
- Dortania - for their beautiful [guide of Hackintosh][Dortania]
- [My Guru(s) at Hackintosh Lover Indonesia][HackintoshLoverIndonesia] - for their knowledgements so i can make it this far and set this beautiful config

[//]: #
[MountEFI]: <https://github.com/corpnewt/MountEFI>
[Opencore]: <https://github.com/acidanthera/OpenCorePkg>
[GenSMBIOS]: <https://github.com/corpnewt/GenSMBIOS>
[SMBIOSGuide]: <https://dortania.github.io/OpenCore-Install-Guide/config.plist/comet-lake.html#platforminfo>
[Dortania]: <https://dortania.github.io>
[HackintoshLoverIndonesia]: <https://t.me/HackintoshLover>
