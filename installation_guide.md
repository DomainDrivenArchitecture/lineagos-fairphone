Ungoogle Fairphone
=========
Angelegt Freitag 05 Juni 2021

Install LineageOS on Fairphone
------------------------------
1.1. Save you Data and Unlock Bootloader (on Your Fairphone)
- Find IMEI number (Settings - About phone)
- Find serial number (Settings - About phone - Model and Hardware)
- enter them [here][bootloader] and get your unlock code. 
- enable Developer mode (press 7 times “Build number” (Settings - About phone))
- enable OEM unlocking with unlock code (System – Advanced – Developer options)
- enable USB Debugging (System – Advanced – Developer options)

1.2. Install and download dependencies (on Your Computer)
- install fastboot and adb (sudo apt install adb fastboot)
- Download LineageOS .img and .zip files [here][LineageOS]
- connect Fairphone via USB with computer
- Reboot bootloader (adb reboot bootloader)

1.2.1 Optional installation of Google Play Store
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

2.3. Now you can install Apps like DeltaChat, NextCloud, Fennec, Tusky...

2.4 Dont forget to check again the predefined settings (additional install a privacy badger).

2.5 If you are interested in how a specific App is tracking you. You can use the [exodus][privacy] platform to check.


Remove Google-dependencies
--------------------------
3.1. enter new DNS: dns2.digitalcourage.de (Settings - Network and Internet - Private DNS)

3.2. Check Privacy Settings and GPS (especially browser-settings from Fennec).

3.3. Switch off Print Service (Settings - Connected devices - Connection preferences - Printing)

3.4. Google captive portal check mit [Kuketz][kuketz] einrichten bzw ersetzen. Dafür FP wieder mit dem Computer verbinden und erneut mit Hilfe von adb folgende Kommandos ausführen.
- adb shell 'settings put global captive_portal_http_url "http://captiveportal.kuketz.de"'
- adb shell 'settings put global captive_portal_https_url "https://captiveportal.kuketz.de"'
- adb shell 'settings put global captive_portal_fallback_url "http://captiveportal.kuketz.de"'
- adb shell 'settings put global captive_portal_other_fallback_urls "http://captiveportal.kuketz.de"'

Um zu testen ob ob die Einstellungen übernommen wurden folgendes eingeben:
- adb shell 'settings get global captive_portal_https_url'



[bootloader]: https://www.fairphone.com/en/bootloader-unlocking-code-for-fairphone-3/
[LineageOS]: https://download.lineageos.org/FP3
[apkpure]: https://apkpure.com
[Fdroid]: https://www.f-droid.org/
[kuketz]: https://www.kuketz-blog.de/android-captive-portal-check-204-http-antwort-von-captiveportal-kuketz-de/
[GApps]: https://opengapps.org/
[privacy]: https://reports.exodus-privacy.eu.org/de/
