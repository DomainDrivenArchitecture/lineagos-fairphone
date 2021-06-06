Ungoogle Fairphone
=========
Angelegt Freitag 05 Juni 2021

Install LineageOS on Fairphone
---------------------------------
1. Save you Data and Unlock Bootloader (on Your Fairphone)
- Find IMEI number (Settings - About phone)
- Find serial number (Settings - About phone - Model and Hardware)
- enter them [here][bootloader] and get your unlock code. 
- enable Developer mode (press 7 times “Build number” (Settings - About phone))
- enable OEM unlocking with unlock code (System – Advanced – Developer options)
- enable USB Debugging (System – Advanced – Developer options)

2. Install and download dependencies (on Your Computer)
- install fastboot and adb (sudo apt install adb fastboot)
- Download LineageOS .img and .zip files [here][LineageOS]
- connect Fairphone via USB with computer
- Reboot bootloader (adb reboot bootloader)

3. Prepare Phone (on Your Fairphone)
- start phone in Recovery mode
- choose Factory Reset - Format Data/Factory Reset
- apply update - Apply from ADB

4. Install LineageOS (on Your Computer)
- adb sideload <lineagos.zip>

5. Apply LineageOS (on Your Fairphone)
- apply update

6. TODO: bootlock your phone

Install Apps
------------
2.1. [Here][apkpure] you can download Apps which you can install via the computer on your phone (adb install example.apk).



Remove Google-dependencies
-----------------------------
3.1. enter new DNS: dns2.digitalcourage.de (Settings - Network and Internet - Private DNS)

3.2. Check Privacy Settings and GPS

3.3. Switch off Print Service (Settings - Connected devices - Connection preferences - Printing)

3.4. (Switch off Companion Device Manager? )

3.5. Fdroid Installation
	a. deltachat (import backup von oben)
	b. nextcloud
	c. osmand
	d. davx5
	e. icsx5
	f. fennec
	g. LibreraReader
	h. QRScanner
	i. tusky
	j. AudioAnchor
	k. Aegis
	l. CoronaTracking
	m. editor

3.6. deltachat-backup + Files unter: ~/cloud/meissa/09_organisation/99_SystemAdministration/Lineageos auf das Smartphone kopieren

3.7. nextcloud einrichten
	a. cloud.prod.meissa-gmbh.de
	b. smart-jem

3.8. davx5 - crm einrichten
	a. https://meissa.h.opencrm.eu/carddav.php/principals/jem
	b. jem

3.9. tusky
	a. https://social.meissa-gmbh.de
	b. jem

3.10. email

3.11. tts

3.12. fennec
	a. Einstellungen anpassen!
	b. privacy badger einrichten

3.13. google captive portal MIT adb einrichten (https://www.kuketz-blog.de/android-captive-portal-check-204-http-antwort-von-captiveportal-kuketz-de/)
adb shell 'settings put global captive_portal_http_url "http://captiveportal.kuketz.de"'
adb shell 'settings put global captive_portal_https_url "https://captiveportal.kuketz.de"'
adb shell 'settings put global captive_portal_fallback_url "http://captiveportal.kuketz.de"'
adb shell 'settings put global captive_portal_other_fallback_urls "http://captiveportal.kuketz.de"'
# Test it
adb shell 'settings get global captive_portal_https_url'

[bootloader]: https://www.fairphone.com/en/bootloader-unlocking-code-for-fairphone-3/
[LineageOS]: https://download.lineageos.org/FP3
[apkpure]: https://apkpure.com
