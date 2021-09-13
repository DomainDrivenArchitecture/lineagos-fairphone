# Install LineageOS on Fairphone

## 1. Check your prerequisites on your computer
[ ] adb and fastboot are installed?  
[ ] you have downloaded bootimage (img) and LineageOS (zip)?  
[ ] you have the unlock code (in case of Fairphone 3)?  

## 2. Unlock your fairphone
1. Navigate to "Settings - About phone"
1. Press 7 times “Build number” to enable Developer mode
1. Navigate to "Settings - System – Advanced – Developer options"
1. Enable OEM unlocking with unlock your code
1. Navigate to "Settings - System – Advanced – Developer options"
1. Enable USB Debugging

## 3. Connect via usb
1. Connect your computer & fairphone via usb
1. On your fairphone allow the usb connection
1. Type `adb devices` on your computer. The result should show something like   
   ```
   List of devices attached
   <SerialNumberOfYourPhone>	device
   ```

## 4. Install LinegaeOS recovery image
1. Reboot your fairphone to bootloader mode: Type `adb reboot bootloader` on your computer.
1. Fairphone should show the bootloader screen.  
1. Type `fastboot devices` on your computer. The result should show something like
   ```
   <SerialNumberOfYourPhone>	fastboot
   ```
1. Type on your computer `fastboot oem unlock`.
1. Install fastboot image by typing `fastboot flash recovery <image_filename.img>` on your computer (<image_filename.img> is the img-file you have downloaded in 1.).
1. Type on your computer `fastboot oem lock`.

## 5. Install LineageOS
1. Reboot your fairphone again to bootloader mode: Type `adb reboot bootloader` on your computer.
1. Your fairphone now boots to the new LineageOS recovery image. Then start the recovery mode.   
[<img src="/doc/start.jpg" width="300" height="400">](/doc/start.jpg)[<img src="/doc/recovery.jpg" width="300" height="400">](/doc/recovery.jpg)

1. Choose Factory Reset - Format Data/Factory Reset  
[<img src="/doc/reset.jpg" width="300" height="400">](/doc/reset.jpg)[<img src="/doc/format.jpg" width="300" height="400">](/doc/format.jpg)
1. Return to main menu
1. Apply update - Apply from ADB  
[<img src="/doc/apply.jpg" width="300" height="400">](/doc/apply.jpg)[<img src="/doc/sideload.jpg" width="300" height="400">](/doc/sideload.jpg)
1. Type `adb sideload <lineagos.zip>` on your computer (<lineagos.zip> is the zip-file you have downloaded in 1.).  
[<img src="/doc/done.jpg" width="300" height="400">](/doc/done.jpg)  

### 5.1 Optional installation of Google Apps
If you can't abstain from the Google Apps or the Google Play Store there exist packages with various scopes, you will find a package comparison here: https://github.com/opengapps/opengapps/wiki/Package-Comparison
1. Download the favored version from [here](https://opengapps.org/).
1. Install the gapps the same way, you installed LineageOs: `adb sideload <gapps.zip>`

## 6. Start LineageOS
1. Return to main menu
1. Choose Reboot system, then your phone should start with the new LineageOS.
1. Walk through the initial LineageOS setup.

## 7. Download the F-Droid App-Store
1. Use the browser on your Fairphone to download F-Droid: https://www.f-droid.org/
1. Visit the download-folder and install F-Droid (accept the warning).
1. Now you can install Apps like DeltaChat, NextCloud, Fennec, Tusky, k9 (...) through the F-Droid Store.
1. Open Fennec and install privacy badger as add-on.
