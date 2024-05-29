# Thinkpad P50 Hackintosh-ing made (sorta) easy / [OpenCore only]

---

This guide will run you through the process of setting up your machine to a fully working MacOS install using Dortania's guide and my own experience. I will not distribute any Kexts/EFIs or will be able to help with quirks due to the different specifictions of this laptop.

# Thanks to the people at the [r/Hackintosh Discord Server](https://discord.gg/Wxam8aH) for helping me get through the process of setting up OC (OpenCore) and to get more of an understanding towards Hackintoshing.

# I will reference [midi1996's P50 OpenCore Guide](https://github.com/midi1996/P50-opencore-hackintosh/) throughout this guide, without them I wouldn't even have started this journey <3

---

## QUICK DISCLAIMER: 
This guide was made primarily for educational purposes. Using this guide does not guarantee a perfectly working machine, neither does it guarantee to keep you safe from data loss. This means that neither the author (me), people/guides mentioned (directly or indirectly) can be held responsible for any data loss, harm or damages to your machine. By following this guide you completely and fully agree to be held responsible for your own damages, etc. It is advised to only do this when you have no deadlines, enough time and patience to dabble into the arts hackintoshing the P50.

---

## My specifications:
* Model: Lenovo ThinkPad P50 (20EN)
* CPU: Intel Core i7-6820HQ @ 2.7Ghz
* GPUs:
  * Intel HD 530
  * Nvidia Quadro M2000M (disabled and won't work. NVidia support has been dropped since High Sierra)
* RAM: 32GB
* Storage:
  * 512GB M.2 SSD
    * macOS
  * 512GB SATA M.2 SSD
  	 * Windows (Mostly now virtualized in MacOS using VMware Fusion Bootcamp)
* WiFi Card: *shipped with* Intel Wireless Dual Band 8360 (for vPro), replaced with third party BCM94360CS2.
* Display: 4k Panel, running @ 1080p/4k 
* Audio: ALC298
* USB-C/TB3
  * Disabled in BIOS as it's currently very picky
* OSes: macOS 13.6.x - Windows 11
* Panel Calibrator: Pantone X-Rite
  * Doesn't work and won't work, using older Spyder calibrator

---

## Currently working:
The System currently works fine as is. If not still a bit sligtly iffy.
* Battery Status
* Wifi (Completely fine after replacing the Wifi Card.)
* Bluetooth*
* Trackpad
* Trackpoint
* Volume/Brightness control
* AirDrop*
* Airplay*
* Continuity*
* Handoff*
* Messages/Facetime**
* GPU Acceleration (again, limited to only integrated)
  * QE/CI Support
  * HEVC decoding
* USB-A Ports
  * including 10W charging, even in sleep mode (only for the Always-On Port)

*: These all are relying on the wifi card present. It is possible to patch in the original Intel card (Wifi/Bluetooth) using specific Kexts but this means it will be unreliable, has no AirDrop, Continuity, etc. Please refer here to the [Dortania OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide/).
**: This only works if you have setup the SMBIOS correctly including your Apple ID.
