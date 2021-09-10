
# Install LineageOS on Fairphone

## 1. check your prerequisites on your computer
[ ] adb and fastboot are installed? \
[ ] you have downloaded bootimage (img) and LineageOS (zip)? \
[ ] you have the unlock code (in case of Fairphone 3)?

- enable Developer mode (press 7 times “Build number” (Settings - About phone))
- enable OEM unlocking with unlock code (Settings - System – Advanced – Developer options)
- enable USB Debugging (Settings - System – Advanced – Developer options)

1.2. Download and install dependencies (on Your Computer)
- install fastboot and adb (sudo apt install adb fastboot)
- Download LineageOS .img and .zip files [here][LineageOS]
- connect Fairphone via USB with computer
- Reboot bootloader (adb reboot bootloader)

1.2.1. Optional installation of GooglePlay Store
- If you can't abstain from the Play Store there exist a minimum Google installation, (pico) Open GApps.
- Download the favored version from [here][GApps].

1.3. Prepare Phone (on Your Fairphone)
- start phone in Recovery Mode
- choose Factory Reset - Format Data/Factory Reset
- apply update - Apply from ADB

1.4. Install LineageOS (on Your Computer)
- adb sideload <lineagos.zip>
- optional: adb sideload <gapps.zip>

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
