# Dell-XPS-13-9370-Hackintosh 
Hi Everyone this is my Dream Laptop Hackintosh Build that I am putting together. Im grateful to share this efi for those who have this specific niche model of DELL XPS 13 9370 :)

Im pushing hard to make this a very nice top of the line dualbooting daily work driver but i will say its like 90% of the way done and is a little more finicky then my first build but it works.

Dortania opencore post/blog helped me alot awhile back so I give them the credit for info but I really built this from scratch every step of the way


This is a Opencore build 
* **MacOS Version** Big Sur

# What's working?
* **SMBIOS**: MacBookPro15,4 (Kaby Lake R) Intel 8th Gen I7-8650U Quad Core 
* **Audio**: AppleALC.kext alcid=20 NVRAM patch, working on headphones patch at the moment 
* **Graphics Acceleration**: Integrated Intel UHD 620 stolemen/stoelmen patch Platform_id was added for PCI
* **Wifi**: Intel based onboard card non removal. Heliport and itlwm.kext modification needed for your network to connect but it works on this laptop no issues
* **Bluetooth** Intel IntelBluetoothInjector/IntelBluetoothFirmware Kexts because somehow this is a intel card on this board specification need to check bluetooth audio and see it if works since i need to work on aux/jack
* **Mapped Thunderbolt**: USBMap.kext is used and was configured with USBMaptool and are mapped out correctly but does not allow hotswapping usb on the left side ports right side is the only friend we can plug and unplug and it will work normal , left side only works if plugged in at boot, neat trick is use a usb hub and u can plug and unplug stuff with that and it will always stay working aslong as the hub has something in use.
* **CPU Power Management**: CPUFriend and CPUFrienddataprovider kext is managing the tdp usage its prebuilt from someone who post a similar model just slightly different specs but seems to work well. 
* **OpenCore Boot** Windows 11 and macos was installed on same M.2 NVME drive split into 2 different partitions and formatted accordingly
* **Keyboard**: VoodooPS2Controller.kext 
* **Touch-Screen/4kDisplay** Working well use 2 fingers to scroll pinch and zoom is nice. UIscale was adjusted for the 4k display and man its super clean
* **Apple Services** this is working when I setup UDID and proper serial number/MAC Address
* **BACKLIT KEYBOARD Brightness control** Key Works As should to dim 

# What's not working?
* Trackpad is on the frits at the moment ive had no life from it whatsoever on mac os, works perfect in windows so its not broken, i believe its conflict of kexts and ssdt but still testing because touchscreen is nice but still want a regular mouse .
* USB c Ports on the left side only work if u have something plugged into them at boot, either ports on the left side but device needs to be powered off the usb insereted for it to work correctly then boot into macos
* Mic not working
* Goodix Fingerprint hasnt been setup but i will say its not working for now 
* WebCam shows up in device list but no way to interact with it. 
* Aux JAck but im working on a fix 
