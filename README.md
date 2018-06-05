# Acer_E1-572G_Hackintosh_EFI

PC model: Acer E1-572G-54204G50Mnkk

All equipments and features work well except bluetooth, the specs below

> * Chipset:    		Intel HM87
> * CPU: 				Intel i5 4200U Haswell
> * Audio: 				Realtek ALC282 V2
> * Ethernet:			Broadcom BCM57786
> * WireLess Network:	Qualcomm AR9565


## Usage
1. 10.13+, copy the EFI folder to the EFI partition, repair the permissions and rebuild the caches.

2. 10.12.6 and below, copy the EFI folder to the EFI partition, then remove /EFI/CLOVER/drivers64UEFI/apfs.efi.
repair the permissions and rebuild the caches, done.

Tips: 
+ if install the 10.13 - 10.13.3
    + (1 copy the ext/IONetworkingFamily.kext and ext/IO80211Family.kext to S/L/E
    + (2 copy the ext/apfs.efi to /EFI/CLOVER/drivers64UEFI, repair the permissions and rebuild the caches.
    
+ if install the 10.13.4+
    + (1 copy the ext/IO80211Family.kext to S/L/E
    + (2 copy the ext/apfs.efi to /EFI/CLOVER/drivers64UEFI, repair the permissions and rebuild the caches.

ext/IO80211Family.kext for WIFI, ext/IONetworkingFamily.kext for ethernet, some useful efi drivers maybe clover needed also has placed in ext folder.
