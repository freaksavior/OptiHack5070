# OptiHack5070
Dell Optiplex 5070 Hackintosh using OpenCore 0.6.3.

Find the latest [OpenCore Release](https://github.com/acidanthera/opencorepkg/releases)
 

First and foremost, thanks to everyone involved who put this together. The [OpenCore Install Guide]( https://dortania.github.io/OpenCore-Install-Guide)
 is fanatastic and you should read through it. Twice. 

My efforts to get a Dell Optiplex 5070 fully working using Opecore bootloader. Included is the entire package, with SSDTime dumps and USBMap.kext.

-----------------------------------------------------------------------
OS                             Version 11.0.1 (Build 20B29)

Kernel                         Darwin 20.1.0 x86_64

RAM                            16.00 GB

Model Identifier               iMac19,1

CPU                            Intel(R) Core(TM) i7-9700 CPU @ 3.00GHz

Intel Generation               Coffee Lake

Platform ID                    0x3E9B0007

Board ID                       Mac-AA95B1DDAB278B95

FW Version                     1037.140.50.0.0

Serial Number                  

Hardware UUID                  

System ID                      

ROM                            

Board Serial Number            

VDA Decoder                    Fully Supported

-----------------------------------------------------------------------

Serial Info

-----------------------------------------------------------------------

Country                        China (Quanta Computer)

Year                           2019

Week                           10.29.2019-11.03.2019

Line                           805 (copy 1)

Model                          iMac (Retina 5K, 27-inch, 2019)

Model Identifier               iMac19,1

Valid                          Possibly

-----------------------------------------------------------------------

IGPU

-----------------------------------------------------------------------

GPU Name                       Intel UHD Graphics 630 (Desktop 9 Series)

GPU Device ID                  0x3E988086

Total VRAM                     1536 MB

Free VRAM                      0 MB

Quartz Extreme (QE/CI)         Yes

Metal Supported                Yes

Metal Device Name              Intel(R) KBL Unknown

Metal Default Device           Yes

Metal Low Power                Yes

Metal Headless                 No

-----------------------------------------------------------------------

Realtek ALC225 Using Layout 11 (IRQ patch is required).

Not working: 

Sleep seems to cause a kernel panic. 

Currently working:

As far as I can tell, everything else


Fixed:
-----------------------------------------------------------------------

Disable CGF lock via GRUB boot64.efi.

Please refer to the following two guides:

https://dortania.github.io/OpenCore-Post-Install/misc/msr-lock.html#turning-off-cfg-lock-manually

https://github.com/JimLee1996/Hackintosh_OptiPlex_9020

Bios 1.7 has a lock location of

`0x4DAC6   One Of: CFG Lock, VarStoreInfo (VarOffset/VarName): 0x5BE, VarStore: 0x1, QuestionId: 0x333, Size: 1, Min: 0x0, Max 0x1, Step: 0x0 {05 91 B6 03 B7 03 33 03 01 00 BE 05 10 10 00 01 00}`

