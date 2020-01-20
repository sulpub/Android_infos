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
