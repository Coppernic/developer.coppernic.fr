OS
==

All OS packages can be found on [copperpro website](https://copperpro.coppernic.fr/copperpro-downloads/)

Here are procedures for upating OS on Coppernic’s devices

### Prerequisites

* You shall have adb installed on your computer.
* You should be familiar with adb and how to install OS on Android platform

C-five
------

- Copy os update file on a SD card
- Insert the SD card to the device
- Press power and vol + button and place the battery at the same tile
- Hold power and vol + button until you get in the recovery menu
- Press Volume Up / Down to select “sd update” then press Power Button
- Press Volume Up / Down to select the correct update file
- Press Power Button to execute Update
- Waiting for “Install from sdcard complete” appear.
- Press power button to reboot device

C-One
-----

- Copy “update….zip” file to a SD card
- Insert the SD card to the device
- Press Power button and select “Reset”
- Hold P1 & Volume up button until you get in the recovery menu
- Press Volume Up / Down to select “sd update” then press Power Button
- Press Volume Up / Down to select “update…zip” file
- Press Power Button to execute Update
- Waiting for “Install from sdcard complete” appear.
- Press HW Reset button.

ID Platform
-----------

### OTA

This method uses OTA (Over The Air) package.

* Get OTA package from copperpro website
* Reboot IdPlatform on recovery mode : `adb reboot recovery`
* On recovery page, select **adb update**
* On your computer, run `adb sideload [PACKAGE_FILE]` (Replace [PACKAGE_FILE] by the name of your package)
* When update is complete, reboot device

### Fastboot

If previous method fails, try this one. It uses fastboot package.

* Get fastboot package from copperpro website
* Unzip package and go in unzipped folder
* Reboot IdPlatform on fastboot mode : `adb reboot fastboot`
* On your computer, run `flash.sh` script
    * If you are a Windows user, then feel free to update the flash script.
