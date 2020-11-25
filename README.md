# OptiHack5070
Dell Optiplex 5070 Hackintosh OpenCore

First and foremost, thanks to everyone involved who put this together. The guide at https://dortania.github.io/OpenCore-Install-Guide/ is fanatastic and you should read through it. Twice. 

My efforts to get a Dell Optiplex 5070 fully working using Opecore bootloader. Included is the entire package, with SSDTime dumps and USBMap.kext.

i7 9700
Realtek ALC225 Using Layout 11 (IRQ patch is required).
Intel UHD Graphics 630 reporting 1536 MB -- Monitor reporting 100Hz, 1440p/.
I had read SATA may be an issue but it works fine in Big Sur 11.0.1.


Not working: 

Sleep seems to cause a kernel panic. 

Currently working:

As far as I can tell, everything else


Things to do, besides get sleep working: 

Disable CGF lock in the bios
