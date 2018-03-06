# Acer_E1-572G_Hackintosh_EFI

PC model is Acer E1-572G-54204G50Mnkk

all equitments and features work well except bluetooth, the specs below

> * chipset:    		intel HM87
> * cpu: 				intel haswell i5 4200u
> * Audio: 				Realtek ALC282 V2
> * Ethernet:			Broadcom BCM57786
> * WireLess Network:	Qualcomm AR9565


## Usage
1. for 10.12.6 below, copy the EFI directory to the EFI partition, then copy the ext/IO80211Family.kext to S/L/E, repair the permissions and rebuild the caches, done.

tips: if install the high sierra (10.13.* ), copy the ext/IONetworkingFamily.kext to S/L/E after the first step, repair the permissions and rebuild the caches.

ext/IO80211Family.kext for WIFI, ext/IONetworkingFamily.kext for ethernet.
