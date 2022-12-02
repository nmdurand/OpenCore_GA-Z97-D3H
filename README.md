# OpenCore configuration for GA Z97 D3H

This is my OpenCore config, used with:
- A GA-Z97-D3H motherboard
- An Intel i5 Haswell processor
- [OpenCore v0.8.6](https://github.com/acidanthera/OpenCorePkg/releases/tag/0.8.6)
- macOS Monterey (12.6.1) at the time of writing

## BIOS settings
I used [this repo](https://github.com/korzhyk/OpenCore_GA-H97M-D3H) to help with the BIOS settings (I just changed the suggested *EHCI Hand-off* setting):
- *Save & Exit → Load Optimized Defaults* **[Yes]**
- *BIOS Features → Fast boot* **[Disabled]**
- *BIOS Features → VT-d* **[Enabled]**
- *BIOS Features → Windows 8 Features* **[Windows 8 WHQL]**
- *BIOS Features → CSM Support* **[Disabled]**
- *Peripherals → Initial Display Output* **[IGFX]**
- *Peripherals → XHCI Mode* **[Enabled]**
- *Peripherals → Intel Processor Graphics Memory Allocation* **[64M]**
- *Peripherals → XHCI Hand-off* **[Enabled]**
- *Peripherals → EHCI Hand-off* **[Disabled]**
- *Peripherals → Super IO Configuration → Serial Port A* **[Disabled]**

## USB Mapping
You probabily need to create your own USBMap kext. I had a hard time with this, since some of the USB2 ports wouldn't show at all in the USBMap tool.
Check out the [motherboard specs](https://www.gigabyte.com/fr/Motherboard/GA-Z97-D3H-rev-10#ov) to see which ports you are actually using and follow the guide to [USB mapping](https://dortania.github.io/OpenCore-Post-Install/usb/intel-mapping/intel.html).