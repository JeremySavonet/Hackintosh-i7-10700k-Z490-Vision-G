# Hackintosh-i7-10700k-Z490-Vision-G

**Latest working macOS**: 10.15.7

**Current OpenCore**: 0.6.1

![About this mac](screenshot/mac-info.png)

![HW overview](screenshot/hw-over.png)


Complete hardware specs:
- i7 10700k 3.8GHz
- Gigabyte Z490 Vision G
- DWA-131E1
- 32GB RAM - 3200 MHz DDR4
- 1TB Samsung 970 EVO NVMe PCIe SSD (macOS Partition) + 1TB Seagate HDD (Windows Partition)

**SMBIOS**: iMac20,2

The system dual boots Windows 10

## What works
- macOS Catalina
- WiFi
- Audio
- HDMI from internal graphics 5DP not tested)
- All USB ports
- 2.5Gbit Ethernet
- Everything iCloud related (Drive, iMessage, Facetime, unlock with Apple Watch, etc)
- Temperature monitoring
- DRM content (Netflix, ATV+, Airplay 2 mirroring etc)
- Shutdown/Reboot
- Sleep/Wake-up (issue with my display: needs to be power-off and on)

## Kexts used:
- AppleALC (audio)
- Lilu + Whatevergreen (Audio helper, DRM support, IGPU helper)
- VirtualSMC + addons (you cannot boot without this + temperature support)
- FakePCIID
- FakePCIID_Intel_I225-V (ethernet)
- FakePCIID_Intel_HDMI_Audio (optional, support for audio via HDMI)
- DAGPM (better dGPU performance for 5700xt: here for futur use)

## Drivers used:
- OpenCanopy.efi for GUI
- OpenRuntime.efi
- HFSPlus

## Thanks/Credits
- [SchmockLord](https://github.com/SchmockLord/Hackintosh-Intel-i9-10900k-Gigabyte-Z490-Vision-D)
- [rursache](https://github.com/rursache/Hackintosh-i9-10900k-Z490-Vision-G)
