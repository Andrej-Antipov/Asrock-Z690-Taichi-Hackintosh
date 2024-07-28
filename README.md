# Asrock-Z690-Taichi-Hackintosh

EFI OpenCore Folder

## Hardware configuration:
* CPU: i5-13600kf RaptorLake (Undervolted)
* MB: Asrock Z690 Taichi
* RAM: 2x16Gb DDR5 PATRIOT VIPER VENOM 7000
* LAN: Intel 219 1Gbit
* LAN: Killer 3100 2,5Gbit
* LAN: X540T2 10Gbit local net (only works in PCI-e slot 4)
* TB: Maple Ridge 2 type-c ports (hotplug working)
* GPU: Radeon RX5700 Sapphire Pulse 8Gb
* GPU: Radeon RX6800XT Asrock Taichi 16Gb
* SSD: 1Tb Netac NV7000 NVME M2 (PCI-e 4.0) - Mac OS 13
* SSD: 2Tb Netac NV7000 NVME M2 (PCI-e 4.0) - Windows 11
* WIFI/BT: bcm943602CS in M2 A/E keys NGFF adapter or PCI-E adapter (OCLP patch)
* WIFI: onboard ax1675 with AirportItlwm.kext (Ventura/Sonoma)
* BIOS: [v20.07 beta](https://www.asrock.com/mb/Intel/Z690%20Taichi/index.ru.asp#BIOS)
* Display: LG 4K 60 Hz HDR via Display Port (27UK650-W)

### BIOS setup: 

* Default and Overclocking with undervolting
* ACPI disable all wake options

MacOS terminal. Disable darkwake options:

sudo pmset tcpkeepalive 0

Sonoma+:  disable CSPNEvaluation darkwake 

mkdir -p /System/Library/FeatureFlags/Domain/

open /System/Library/FeatureFlags/Domain/

put into this folder powerd.plist

### Mac OS Monterey and Ventura EFI OpenCore loader 1.0.1
### Mac OS Sonoma, Sequoya beta with EFI OpenCore loader 1.0.1 and legacy Broadcom WiFi patch

FileVault2 and some Intel LAN not working in Sonoma with the OCLP patch!
 
* All mac os futures are working including DRM playback and sleep/wake S3
* Clover has issue with update under T2 mac models

Wifi legacy patch Sonoma, Sequoya beta. [OCLP](https://drive.google.com/file/d/1poXc2ZGHqONZTQKSdnTMutIrU6v9UOKp/view?usp=sharing)
