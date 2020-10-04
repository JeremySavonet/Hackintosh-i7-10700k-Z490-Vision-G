# Hackintosh-i7-10700k-Z490-Vision-G

**Latest working macOS**: 10.15.7

**Current OpenCore**: 0.6.1

**Z490 vision G bios version**: F7

<p align="center">
  <img src="https://github.com/JeremySavonet/Hackintosh-i7-10700k-Z490-Vision-G/blob/main/screenshot/mac-info.png" />
</p>

<p align="center">
  <img src="https://github.com/JeremySavonet/Hackintosh-i7-10700k-Z490-Vision-G/blob/main/screenshot/hw-over.png" />
</p>

## Complete hardware specs:
- Intel i7 10700k 3.8GHz
- Gigabyte Z490 Vision G
- DWA-131E1 (USB wifi dongle for now)
- 32GB RAM - 3200 MHz DDR4 (Corsair LPX)
- 1TB Samsung 970 EVO NVMe PCIe SSD (macOS Partition) + 1TB Seagate HDD (Windows Partition)

**SMBIOS**: iMac20,2

The system dual boots Windows 10 on a separate drive

## What works
- macOS Catalina
- WiFi
- Audio
- HDMI from internal graphics 5DP not tested)
- All USB ports
- 2.5Gbit Ethernet
- iCloud related (iMessage, Facetime, etc)
- Logic Pro X (no stability issue)
- Temperature monitoring
- DRM content (Netflix, Spotify)
- Shutdown/Reboot
- Sleep/Wake-up (issue with my display: needs to be power-off and on) => FIXED BY ADDING BOOT-ARGS: igfxonln=1)

## BIOS config:
**Disable**
- Fast Boot
- CSM
- Secure Boot

**Enable**
- EHCI/XHCI Hand-off
- Above 4G decoding

## Kexts used:
- AppleALC (audio)
- Lilu + Whatevergreen (Audio helper, DRM support, IGPU helper)
- VirtualSMC + addons (you cannot boot without this + temperature support)
- FakePCIID
- FakePCIID_Intel_I225-V (ethernet)
- FakePCIID_Intel_HDMI_Audio (optional, support for audio via HDMI)

## Drivers used:
- OpenCanopy.efi for GUI
- OpenRuntime.efi
- HFSPlus

## Issues:

No known issue for now. A little bit long to boot after OC menu (around: 22sec before logging screen)

## Thanks/Credits
- [SchmockLord](https://github.com/SchmockLord/Hackintosh-Intel-i9-10900k-Gigabyte-Z490-Vision-D)
- [rursache](https://github.com/rursache/Hackintosh-i9-10900k-Z490-Vision-G)
