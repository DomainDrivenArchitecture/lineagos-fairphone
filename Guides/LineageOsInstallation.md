# Install LineageOS on Fairphone

## 1. Check your prerequisites on your computer
[ ] adb and fastboot are installed?  
[ ] you have downloaded bootimage (img) and LineageOS (zip)?  
[ ] you have the unlock code (in case of Fairphone 3)?  
[ ] you have a usb cable prepared?  
[ ] you are prepared to erase all the data on your fairphone?  

## 2. Unlock your fairphone

Unlocking will allow us to overwrite the boot-loader.
1. Navigate to "Settings - About phone"
1. Press 7 times “Build number” to enable Developer mode
1. Navigate to "Settings - System – Advanced – Developer options"
1. Enable OEM unlocking with unlock your code
1. Navigate to "Settings - System – Advanced – Developer options"
1. Enable USB Debugging

## 3. Connect via usb

For overwriting your fairphones boot-loader we will need connection to your pc.
1. Connect your computer & fairphone via usb
1. On your fairphone allow the usb connection
1. Type `adb devices` on your computer. The result should show something like   
   ```
   List of devices attached
   <SerialNumberOfYourPhone>	device
   ```

## 4. Install LinegaeOS recovery image

If this step goes wrong your fairphone may remain broken. So be shure, your phone has at least 50% battery.
1. Reboot your fairphone to bootloader mode: Type `adb reboot bootloader` on your computer.
1. Fairphone should show the bootloader screen.  
1. Type `fastboot devices` on your computer. The result should show something like
   ```
   <SerialNumberOfYourPhone>	fastboot
   ```
1. Type on your computer `fastboot oem unlock`.
1. Install fastboot image by typing `fastboot flash recovery <image_filename.img>` on your computer (<image_filename.img> is the img-file you have downloaded in 1.).
1. Type on your computer `fastboot oem lock`.

OEM unlocking / locking will erase all data, so we should ensure to do the lock again.

## 5. Install LineageOS

This step is no more dangerous. You can retry as often you want to. The LineageOs boot-loader will verify your binaries.
1. Reboot your fairphone again to bootloader mode: Type `adb reboot bootloader` on your computer.
1. Your fairphone now boots to the new LineageOS recovery image. Then start the recovery mode.   
[<img src="img/start.jpg" width="300" height="400">](img/start.jpg)[<img src="img/recovery.jpg" width="300" height="400">](img/recovery.jpg)

1. Choose Factory Reset - Format Data/Factory Reset  
[<img src="img/reset.jpg" width="300" height="400">](img/reset.jpg)[<img src="img/format.jpg" width="300" height="400">](img/format.jpg)
1. Return to main menu
1. Apply update - Apply from ADB  
[<img src="img/apply.jpg" width="300" height="400">](img/apply.jpg)[<img src="img/sideload.jpg" width="300" height="400">](img/sideload.jpg)
1. Type `adb sideload <lineagos.zip>` on your computer (<lineagos.zip> is the zip-file you have downloaded in 1.).  
[<img src="img/done.jpg" width="300" height="400">](img/done.jpg)  

### 5.1 Optional installation of Google Apps

If you can't abstain from the Google Apps or the Google Play Store there exist packages with various scopes, you will find a package comparison here: [https://github.com/opengapps/opengapps/wiki/Package-Comparison](https://github.com/opengapps/opengapps/wiki/Package-Comparison). You have to install Google Aps in front of first the first start wizzard.
1. Download the favored version from [here](https://opengapps.org/).
1. Install the gapps the same way, you installed LineageOs: `adb sideload <gapps.zip>`

## 6. Start LineageOS

First start of your new LineageOS - hurray.
1. Return to main menu
1. Choose Reboot system, then your phone should start with the new LineageOS.
1. Walk through the initial LineageOS setup.

## 7. Download the F-Droid App-Store

For installing more software we recommend F-Droid 
1. Use the browser on your Fairphone to download F-Droid: [https://www.f-droid.org/](https://www.f-droid.org/)
1. Visit the download-folder and install F-Droid (accept the warning).
1. Now you can install Apps like DeltaChat, NextCloud, Fennec, Tusky, k9 (...) through the F-Droid Store.
1. Open Fennec and install privacy badger as add-on.
