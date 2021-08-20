# X260-Opencore-Hackintosh

## Introduction

Files and steps related to Hackintosh-ing a Thinkpad X260 laptop using Opencore bootloader.
Before using any of these files, make sure you have similar hardware.
> *Though your cases may vary..*

## This modifies Big Sur to work in my environment.

## My Specs

💻 **Laptop**
* Brand       :	Lenovo Thinkpad X260
* BIOS version: R02ET74W 1.47
* Monitor     : 12,5" TN panel 1920x1080 HD
* Battery     : Dual = 3-cell 23Whr internal + 6-cell 72Whr external
  > My _new_ internal battery only recognize with 17Whr max capacity in Windows 10, despite doing many workaround.
  > Sometimes _Lenovo Vantage_ shows 25% wears in my internal battery information.
  > But still, I get satisfying battery life from both Windows and macOS, which is 10+ hours for doing simple tasks.
* Processor   :	Intel® CORE ™ i5-6300U 2,4GHz vPro
* iGPU        :	Intel® Skylake GT2 [HD Graphics 520]
* dGPU        :	-
* RAM         :	1 x 8 GB, DDR4, 2133MHz, PC17000
* Audio Codec :	Realtek ALC293
* Keyboard    : Japan layout
* Trackpad    : Synaptics 2104 SMBus
  > Trackpad_Clickpad: touchpad with three physical button
* Storage     :	TOSHIBA 128GB SSD 2,5"
* Card Reader  : Realtek RTS522A PCI Express Card Reader
* Web Cam      : 720p
* Wireless LAN : Intel ® Dual Band Wireless-AC 8260 (with bluetooth)
* Ethernet     : Intel Ethernet Connection I219-LM
* Bootloader   : OpenCore 0.6.8
* OS Version   : ```macOS Big Sur 11.5.2 (Build 20G95)```


**Other Hardware:**
  > Which I used daily with this hackintosh machine
* 45Watts AC adapter


**BIOS Settings**
* Enable  : Swap Fn - Ctrl, trackpad, trackpoint, card reader, Intel TPM (set to _inactive_), Execution Prevention, Intel Virtualization Technology, Intel VT-d Feature
* Disable : Always on usb, WiGig, WWAN, Anti Theft, Intel SGX, Computrace, Device Guard, Secure Boot,
* Boot    : include only _ATA Drive_ & _FD HDD_, UEFI only, CSM = No

***Worked***
- [x] iGPU with external monitor
  ~~> only work after waking from sleep~~ change VGA-to-miniDP adapter with VGA-to-HDMI. Work without enter sleep and wake.
- [x] CPU power management
- [x] Backlight
  > Backlight control will be activated once it goes to sleep.
- [x] Webcam
- [x] Sound: speaker, microphone
- [x] Wifi
- [x] Ethernet / LAN
- [x] Bluetooth
- [x] All USB Ports
- [x] Battery notification: charging, full charge, etc
- [x] Trackpad, trackpoint, 3 physical button, & gesture (Trackpad showed in System Preferences)
- [x] ~~Keyboard --remap with [Karabiner-Elements](https://karabiner-elements.pqrs.org)~~ now use SSDT-KBRD & ThinkpadAssistant from MSzturc
- [x] Power management
- [x] iMessage, Facetime, Appstore
- [x] DRM Support, tested based on [Dortania Opencore Post Install](https://dortania.github.io/OpenCore-Post-Install/universal/drm.html#testing-drm)
- [x] Card reader
- [x] Logitech Pebble mouse with Bluetooth connection
- [x] Handoff (& universal clipboard)

**_not yet_ Worked or May Not Work**
* Handoff and Universal Clipboard are the only supported Continuity features (opens new window).
* Instant Hotspot from iPhone can be recognized but may likely fail to connect.

**Steps will written down in seperate .md files**

**Source:**
* celerond256, GitHub [X260-Opencore-Hackintosh] (https://github.com/celerond256/X260-Opencore-Hackintosh)
* Picel Media Group, Youtube Channel [Belajar bareng cara install Hackintosh Catalina (OpenCore) di Lenovo T440p](https://youtu.be/zdcPPpd-g8I)
* Hackintosh Telegram group, [H4CK1NTOSH L0V3R](https://t.me/HackintoshLover)
* MSzturc, Github [Lenovo-T460-OpenCore](https://github.com/MSzturc/Lenovo-T460-OpenCore)
* Opencore preparations [Dortania Getting Started](https://dortania.github.io/getting-started/)

