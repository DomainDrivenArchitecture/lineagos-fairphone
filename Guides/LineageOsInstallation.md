
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
1. Type `adb devices` on your computer. The result should show sth like   
   ```
   List of devices attached
   A209VYM20201	device
   ```

## 4. Install LinegaeOS recovery image
1. Reboot your fairphone to bootloader mode: Type `adb reboot bootloader` on your computer.
1. Fairphone should show the bootloader screen.
1. Type `fastboot devices` on your computer. The result should show sth like
   ```
   A209VYM20201	fastboot
   ```
1. Type on your computer `fastboot oem unlock`.
1. Install fastboot image by typing `fastboot flash boot <image_filename.img>` on your computer (<image_filename.img> is the img-file you have downloaded in 1.).
1. Type on your computer `fastboot oem lock`.

## 5. Install LineageOS
1. Reboot your fairphone again to bootloader mode: Type `adb reboot bootloader` on your computer.
1. Your fairphone now boots to the new LineageOS recovery image.
1. Choose Factory Reset - Format Data/Factory Reset
1. Return to main menu
1. Apply update - Apply from ADB
1. Type `adb sideload <lineagos.zip>` on your computer (<lineagos.zip> is the zip-file you have downloaded in 1.).

### 5.1 Optional installation of Google Apps
If you can't abstain from the Google Apps or the Google Play Store there exist packages with various scopes, you will find a package comparison here: https://github.com/opengapps/opengapps/wiki/Package-Comparison
1. Download the favored version from [here][GApps].
1. Install the gapps the same way, you installed LineageOs: `adb sideload <gapps.zip>`

## 6. Start LineageOS
1. Return to main menu


1.5. Apply LineageOS (on Your Fairphone)
- apply update

1.6. Lock the Bootloader again (on Your Computer)
- adb reboot bootloader
- fastboot flashing lock

Install Apps
------------
2.1. [Here][apkpure] you can download Apps which you can install via the computer on your phone (adb install example.apk).

2.2. Download F-Droid Store [here][Fdroid].

2.3. Now you can install Apps like DeltaChat, NextCloud, Fennec, Tusky (...) through the F-Droid Store.

2.4. Dont forget to check again the predefined settings (additional install a privacy badger).


Remove Google-dependencies
--------------------------
3.1. enter new DNS: dns2.digitalcourage.de (Settings - Network and Internet - Advanced - Private DNS).

3.2. Check Privacy Settings and GPS (especially browser-settings from Fennec).

3.3. Switch off Print Service (Settings - Connected devices - Connection preferences - Printing).

3.4. Replace Google captive portal check with [Kuketz][kuketz]. Therefore, connect your Fairphone with your computer and execute following adb commands:
- adb shell 'settings put global captive_portal_http_url "http://captiveportal.kuketz.de"'
- adb shell 'settings put global captive_portal_https_url "https://captiveportal.kuketz.de"'
- adb shell 'settings put global captive_portal_fallback_url "http://captiveportal.kuketz.de"'
- adb shell 'settings put global captive_portal_other_fallback_urls "http://captiveportal.kuketz.de"'

In order to test the settings, if they were correctly adopted, you can type in:
- adb shell 'settings get global captive_portal_https_url'



[bootloader]: https://www.fairphone.com/en/bootloader-unlocking-code-for-fairphone-3/
[LineageOS]: https://download.lineageos.org/FP3
[apkpure]: https://apkpure.com
[Fdroid]: https://www.f-droid.org/
[kuketz]: https://www.kuketz-blog.de/android-captive-portal-check-204-http-antwort-von-captiveportal-kuketz-de/
[GApps]: https://opengapps.org/
