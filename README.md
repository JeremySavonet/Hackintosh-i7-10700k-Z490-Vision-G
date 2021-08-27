# Hackintosh-i7-10700k-Z490-Vision-G

**Latest working macOS**: 11.5.2

**Current OpenCore**: 0.6.3

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
- 32GB RAM - 3200 MHz DDR4 (Corsair LPX)
- 1TB Samsung 970 EVO NVMe PCIe SSD (macOS Partition) + 1TB Seagate HDD (Windows Partition)
- Sapphire Pulse RX 5600 XT
- Noctua NH-U12S
- LG UltraFine 27UK670-B 27" 4K
   
**SMBIOS**: iMac20,2

The system dual boots Windows 10 on a separate drive

## What works
- macOS Catalina / Big Sur
- WiFi
- Audio
- HDMI from internal graphics
- dGPU
- All USB ports
- 2.5Gbit Ethernet
- iCloud related (iMessage, Facetime, etc)
- Logic Pro X (no stability issue)
- Temperature monitoring
- DRM content (Netflix, Spotify)
- Shutdown/Reboot
- Sleep/Wake-up (issue with my display: needs to be power-off and on) => **FIXED BY ADDING BOOT-ARGS: igfxonln=1**

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
- SMC**
- DAGPM
- USBInjectAll

## Drivers used:
- OpenCanopy.efi for GUI
- OpenRuntime.efi
- HFSPlus

## Issues:

No known issue for now. A little bit long to boot after OC menu (around: 22sec before logging screen)

## Installation

- Create a USB stick with MacOS on it (follow OC tutorial for that)
- Copy the my EFI folder to the EFI partition of your USB stick
- Edit the <CHANGEME> in config.plist for serial number using [this](https://github.com/corpnewt/GenSMBIOS)

## Thanks/Credits
- [SchmockLord](https://github.com/SchmockLord/Hackintosh-Intel-i9-10900k-Gigabyte-Z490-Vision-D)
- [rursache](https://github.com/rursache/Hackintosh-i9-10900k-Z490-Vision-G)
- [artvandelay750](https://github.com/artvandelay750/Hackintosh-Z490-Gigabyte-VisionG)
