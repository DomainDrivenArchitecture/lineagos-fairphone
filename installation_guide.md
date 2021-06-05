Lineageos
=========
Angelegt Freitag 05 Juni 2021

On Your Fairphone:
- Save your data!
- Unlock the Bootloader:
	- Find IMEI number (Settings - About phone)
	- Find serial number (Settings - About phone - Model and Hardware)
	- enter them [here][bootloader] and get your unlock code. 
	   
	- enable Developer mode (press 7 times “Build number” [Settings - About phone])
	- enable OEM unlocking with unlock code (System – Advanced – Developer options)





On Your Computer:
- install fastboot and adb (sudo apt install adb fastboot)


Desktop
-------
* sudo apt install adb fastboot
* adb
	* adb install *.apk
	* adb push
	* adb shell

Vorbereitung - Bootstrap
------------------------
1. lineagos img image ->  ~/cloud/meissa/09_organisation/99_SystemAdministration/Lineageos xx/bootstrap
2. lineagos zip -> xx/sideload
3. gapps pico -> xx/sideload
4. apks aktualisieren:
	a. https://apkpure.com/de/dr-ft/com.sturmkind.drift/download?from=details
	b. https://apkpure.com/de/db-navigator/de.hafas.android.db/download?from=details
	c. https://apkpure.com/de/google-text-to-speech/com.google.android.tts
5. DeltaChat Backupen (in Downloads)

Installieren
------------
1. lineageos + gapps nano 
	a. https://wiki.lineageos.org/devices/FP3/adb%20devices%20finds%20phone%20but%20fastboot%20notinstall
	b. fastboot devices / fastboot oem unlock /
2. Lookl Bootloader -  fastboot oem lock
3. Initialisieren
4. Dateien per usb überspiele, apk installieren
5. Entgoogeln1:
	a. anderen DNS eintragen: dns2.digitalcourage.de
	b. Datenschutz + Standort einstellen
	c. druckerservice aus
	d. Telefonnummern suche aus
6. Hintergrund einrichten
7. Fdroid Installation
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
8. deltachat-backup + Files unter: ~/cloud/meissa/09_organisation/99_SystemAdministration/Lineageos auf das Smartphone kopieren
9. nextcloud einrichten
	a. cloud.prod.meissa-gmbh.de
	b. smart-jem
10. davx5 - crm einrichten
	a. https://meissa.h.opencrm.eu/carddav.php/principals/jem
	b. jem
11. tusky
	a. https://social.meissa-gmbh.de
	b. jem
12. email
13. tts
14. fennec
	a. Einstellungen anpassen!
	b. privacy badger einrichten
15. google captive portal MIT adb einrichten (https://www.kuketz-blog.de/android-captive-portal-check-204-http-antwort-von-captiveportal-kuketz-de/)
adb shell 'settings put global captive_portal_http_url "http://captiveportal.kuketz.de"'
adb shell 'settings put global captive_portal_https_url "https://captiveportal.kuketz.de"'
adb shell 'settings put global captive_portal_fallback_url "http://captiveportal.kuketz.de"'
adb shell 'settings put global captive_portal_other_fallback_urls "http://captiveportal.kuketz.de"'
# Test it
adb shell 'settings get global captive_portal_https_url'

[bootloader]: https://www.fairphone.com/en/bootloader-unlocking-code-for-fairphone-3/
