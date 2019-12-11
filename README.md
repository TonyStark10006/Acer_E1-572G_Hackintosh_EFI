# Acer E1-572G Hackintosh EFI Folder

Laptop model: Acer E1-572G-54204G50Mnkk

All equipments and features work well except bluetooth, the specs as below

> * Chipset:    		Intel HM87
> * CPU: 				Intel i5 4200U Haswell with IGPU HD4400
> * Audio: 				Realtek ALC282 V2
> * Ethernet:			Broadcom BCM57786
> * WireLess Network:	Qualcomm AR9565


## Usage
1. 10.14+,  copy the EFI folder to the EFI partition, copy ext/AirPortAtheros40.kext to S/L/E/IO80211Family.kext/Contents/Plugins/, repair the permissions and rebuild the caches.

2. 10.13.*, copy the EFI folder to the EFI partition, repair the permissions and rebuild the caches.

3. 10.12.6 and below, copy the EFI folder to the EFI partition, then remove /EFI/CLOVER/drivers64UEFI/apfs.efi.
repair the permissions and rebuild the caches, done.

## Tips: 
### wireless network cards of Qualcomm were no longer supported on 10.14 Mojave, follow [this guide](http://bbs.pcbeta.com/viewthread-1790406-1-1.html) to refind them.
#### 1. notice
+ install the 10.13 - 10.13.3
    + (1 copy the ext/IONetworkingFamily.kext and ext/IO80211Family.kext to S/L/E
    + (2 copy the relevant ext/apfs.efi(e.g. 10.13.3 apfs.efi) to /EFI/CLOVER/drivers64UEFI, repair the permissions and rebuild the caches.
    
+ install the 10.13.4+
    + (1 copy the ext/IO80211Family.kext to S/L/E
    + (2 copy the relevant ext/apfs.efi to /EFI/CLOVER/drivers64UEFI, repair the permissions and rebuild the caches.

+ install 10.14+
    + copy ext/AirPortAtheros40.kext to S/L/E/IO80211Family.kext/Contents/Plugins/ & repair the permissions and rebuild the caches & reboot to enable wireless card. file comes from [this repo](https://github.com/athlonreg/Enable-AR956X-AR946X-AR9485-in-your-hacintosh), it's modifed for AR956X matched 10.13 from [insanelymac](https://www.insanelymac.com/forum/topic/312045-atheros-wireless-driver-os-x-101112-for-unsupported-cards/?page=20) but also worked on 10.14

#### 2. explanation
ext/IO80211Family.kext for WIFI<br>
ext/IONetworkingFamily.kext for ethernet<br>
IntelGraphicsFixup.kext for resolving safari crash problem while watching online video<br>
some useful efi drivers maybe clover needed also has placed in ext folder.


### Credits
[Apple Inc.](https://www.apple.com)<br/>
[RehabMan](https://bitbucket.org/RehabMan)<br/>
[DalianSky](https://blog.daliansky.net)<br/>
Special thanks to the enthusiastic commenters on [pcbeta](http://bbs.pcbeta.com) & [tonymacx86](https://www.tonymacx86.com)