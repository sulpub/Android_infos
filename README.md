# Android Informations

## Android Debug Bridge

Here is the list of ADB command for Android device. Before using it, it's necessassy to activate the developer mode on your Android device.

### ADB list commands

### adb help

Command to list all the command use by adb software.

### adb start-server

This command ensures that a server is still running.

### adb kill-server

The purpose of this command is to shut down the ADB server. Once this command typed, you will have to re-launch the adb devices command to bring the adb server back online.

### adb logcat

This command allows you to view the device-specific or emulator-specific log.

### adb devices

This command displays the list of emulators (launched via the Android SDK) and devices connected via USB to the computer and which can be administered with the ADB.


### adb wait-for-device

This command blocks all execution until a device or an emulator is connected.

 ### adb get-state
 
This command lets you know the status of the connected device or emulator in the desired time: offline (offline), bootloader, normal (device).

### adb get-serialno

This command obtains the serial number of the connected device.

### adb -s "device"  "command"

This command allows you to apply a specific command to one of the terminals listed.
Ex : adb -s emulator-5554 install apk_to_install.apk

### adb install "path_file_apk"

This command allows when we are in possession of the .apk file of an application, to be able to install it on the connected device or emulator.

### adb pull "path_file_on_android_device" "path_file_on_the_computer"

This command allows you to move a file located on a device or an emulator to the computer directly without going through the management of the memory card.

### adb push "path_file_on_the_computer" "path_file_on_android_device"

This command allows you to move a file on the computer to the connected device or emulator without going through the management of the memory card.

### adb -s "device" shell

This command opens a shell command entry, as if we were on the Linux terminal. This way we can use the basic Linux shell commands.
Ex : adb -s emulator-5554 shell

### adb-shell-terminal

    adb -s -d "device" shell "commande shell"

Cette commande permet d'utiliser les commandes shell basiques de Linux directement sur le terminal sélectionné, sans passer par l'application Terminal Emulator. 
Ex :  adb -s emulator-5554 shell ls

### adb install "path_file_apk_to_install".apk

This command, by indicating the entire path to the .apk file to install, allows you to install the desired application on the phone connected to the computer or on the emulator directly. This can be useful for testing your application before final deployment on the Play Store.

Ex : adb install C:/adb/testfile.apk

### adb uninstall aplication_name.apk

This command allows you to delete a package from the device or the emulator without going through the graphical interface. It is also possible to use the "-k" parameter in order to keep the application cache if in the future you want to reuse it.

### adb bugreport

This command allows you to report all data from the device or emulator that may have been included in the bug report.

### adb reboot "mode_you_want"

This command reboots (NDLR: restart) your device or the emulator in the desired mode. This is often used to flash a new ROM or a new .zip package.
Ex : adb reboot recovery or adb reboot bootloader.


## LINEAGEOS on Nexus 7 (2013)

Before run the upgrade, change the partition of the NEXUS 7 with this link : https://forum.xda-developers.com/nexus-7-2013/orig-development/repartition-nexus-7-2013-repartition-t3844386 [[REPARTITION] Nexus 7 (2013) Repartition [FLO/DEB] [16GB/32GB] [UA TWRP]]

Download :
 1. Repartitioning package: flo-deb_clamor_repartition.zip (https://forum.xda-developers.com/devdb/project/dl/?id=30499)
 2. Recovery flo: twrp-3.3.1-1_UA-flo.img (https://forum.xda-developers.com/devdb/project/dl/?id=31667)
 2. Recovery deb: twrp-3.3.1-1_UA-deb.img (https://forum.xda-developers.com/devdb/project/dl/?id=31668)

ROMs : pitrus- for Android 10 for NEXUS 7 (2013)
- **NEXUS 7 LTE version**: deb package (https://lineageos.wickenberg.nu/deb/)
- **NEXUS 7 Wi-Fi version**: flo package (https://lineageos.wickenberg.nu/flo/)

Magisk (root nexus): https://forum.xda-developers.com/apps/magisk/official-magisk-v7-universal-systemless-t3473445

Open GApps (use version 10 nano for google application) : https://sourceforge.net/projects/opengapps/files/arm/

### How to flash LineageOS and Open GApps

1. Move any files you want to keep to your computer or flash drive via a USB OTG cable – ! Or you will lose them !
2. Download your LineageOS Rom and GApps Package,
3. Boot into Recovery Mode (Hold volume up and Power button until you see TWRP's splash screen),
4. Wipe > Advanced Wipe > Select On (enable tick) for Dalvik / Art Cache, System, Data, Internal Storage, Cache,
5. Swipe to Wipe at Bottom of Screen,
6. Back to Main start screen,
7. Wipe > Format Data,
8. Type 'Yes' and press blue checkmark at the bottom-right corner,
9. Go Back to Main Start Screen,
10. Move your LineageOS Rom and GApps Package to the internal storage,
11. Install > select a zip file to flash (optionally, Add More Zips > select another zip file to flash),
11. After you have finished installing the Rom and GApps > Wipe Cache/Dalvik > Swipe to Wipe,
12. Reboot System! Enjoy!

Source : (https://forum.xda-developers.com/nexus-7-2013/development/rom-lineageos-17-1-t4038425)
