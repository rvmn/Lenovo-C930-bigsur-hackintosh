# Lenovo-C930-bigsur-hackintosh
Hackintosh config for Lenovo C930 laptop on BigSur (OpenCore)

Important:

You need to unlock CFG:

Unzip the RU.zip file to an empty FAT32 formatted USB disk, or unzip elsewhere and copy the BOOT folder to your EFI folder. Boot from it then press Enter to start. Press Alt + '=' and open CpuSetup. Go to 03 on left and 0C on top and press 00, then press Enter. Then press Ctrl + W to write to BIOS and wait for a confirmation message. Done!

More info on CFG Locks: https://dortania.github.io/OpenCore-Post-Install/misc/msr-lock.html#what-is-cfg-lock


Important 2:  

In the BIOS disable Secure Boot and Intel SGX (disables fingerprint reader)

Works:

- Everything that can on Mac: Touchscreen, trackpad, 4K-screen (@48Hz though), AppStore (Use GenSMBIOS on config.plist), Battery, Graphics, Wifi, Bluetooth, Sound (though no bass), Sleep.

Usage:

See tutorials for making a USB installer (gibmacOS) or use CarbonCopyCloner to copy a live Mac installation to USB.

Then copy the EFI dir to the EFI partition.

Use GenSMBIOS to update the serial to your own serial so there will be no weird serial conflicts in the appstore (https://github.com/corpnewt/GenSMBIOS). Use MacBookPro14,1 as model.

Postinstall:

Alt-key is used as Command-key by default. You can switch by going to System Prefs -> Keyboard -> right-bottom button: 'Special keys' and switching alt and command.

Connect WIFI: Start HeliPort app (see postinstall) and in sysprefs set it to autostart (Users -> Login Items) and hide the wifi icon in the top panel (Dock and menu -> Wifi).

Multiboot: Use refind if you want to multiboot your system. Smartest is to install windows first and linux first, then clone mac to drive and copy opencore to EFI, then install refind.

Credits:

@navaira    https://www.tonymacx86.com/threads/guide-lenovo-yoga-c930-13ikb-4k-i7-8550u-99-working-updated-7-feb.270421/

@Mrqeque and @JianGaming https://www.tonymacx86.com/threads/guide-dell-inspiron-15-7573-catalina-10-15-7-oc-0-6-0-i7-8550u-4k-uhd-620-best-100-simple-setup.305350/page-33

