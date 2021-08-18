Ungoogle Fairphone
=========
Erstellt Freitag 05 Juni 2021

LineageOS auf dem Fairphone istallieren
------------------------------
1.1. Datensicherung und Bootloader entsperren (Auf dem Fairphone)
- Sichere alle relevanten Dateien vom Smartphone auf dem Computer
- Finde die IMEI Nummer (Einstellungen - Über das Telefon)
- Finde die Seriennummer (Einstellungen - Über das Telefon - Modell)
- beide Nummern [hier][bootloader] eingeben und Entsperrungscode generieren.
- Entwicklereinstellungen aktivieren (drücke 7 mal "Build-Nummer"(Einstellungen - Über das Telefon))
- OEM-Entsperrung mit unlock code aktieren (Einstellungen - System - Erweitert - Entwickleroptionen)
- USB-Debugging aktivieren (Einstellungen - System - Erweitert - Entwickleroptionen)

1.2. Abhängigkeiten runterladen und installieren (Auf dem Computer)
- fastboot und adb installieren (sudo apt install adb fastboot)
- LineageOS .img und .zip Dateien [hier][LineageOS] herunterladen
- Fairphone über USB mit Computer verbinden
- Reboot bootloader (adb reboot bootloader)

1.2.1. Optionale installation des GooglePlay Stores
- Wenn auf eine bestimte Google Services nicht verzichtet werden kann, exisiert eine minimale Google Installation, (pico) Open GApps.
- Favorisierte Version kann [hier][GApps] heruntergeladen werden.

1.3. Das Smartphone vorbereiten (Auf dem Fairphone)
- starte Smartphone im Recovery Modus
- wähle Factory Reset - Format Data/Factory Reset
- Update anwenden - Apply from ADB

1.4. LineageOS installieren (Auf dem Computer)
- adb sideload <lineagos.zip>
- optional: adb sideload <gapps.zip>

1.5. LineageOS installieren (Auf dem Fairphone)
- apply update

1.6. Den Bootloader wieder sperren (Auf dem Computer)
- adb reboot bootloader
- fastboot flashing lock


Apps installieren
------------
2.1. [Hier][apkpure] können apks heruntergeladen werden, die dann über den Computer auf dem Smartphone installiert werden können (adb install example.apk).

2.2. Den F-Droid Store [hier][Fdroid] herunterladen.

2.3. Über den F-Droid Store können jetzt Apps wie DeltaChat, NextCloud, Fennec, Tusky (...) installiert werden.

2.4. Denke daran, die Einstellungen manuell durchzugehen und anzupassen (zusätzlich sollte ein privacy badger installiert werden).


Google Abhängigkeiten entfernen
--------------------------
3.1. trage eine neue DNS ein: dns2.digitalcourage.de (Einstellungen - Netzwerk und Internet - Erweitert - Privates DNS).

3.2. Privatsphäre-Einstellungen und GPS durchgehen (besonders in der Browsereinstellungen von Fennec).

3.3. Druckerservices ausschalten (Einstellungen - Verbundene Geräte - Verbindungseinstellungen - Drucken - Standarddruckdienst)

3.4. Den Google Captive portal check durch [Kuketz][kuketz] ersetzen. Dafür Fairphone mit Computer verbinden und folgende Kommandos ausführen:
- adb shell 'settings put global captive_portal_http_url "http://captiveportal.kuketz.de"'
- adb shell 'settings put global captive_portal_https_url "https://captiveportal.kuketz.de"'
- adb shell 'settings put global captive_portal_fallback_url "http://captiveportal.kuketz.de"'
- adb shell 'settings put global captive_portal_other_fallback_urls "http://captiveportal.kuketz.de"'

Zum testen ob die neuen Einstellungen übernommen wurden, prüfe mit:
- adb shell 'settings get global captive_portal_https_url'



[bootloader]: https://www.fairphone.com/en/bootloader-unlocking-code-for-fairphone-3/
[LineageOS]: https://download.lineageos.org/FP3
[apkpure]: https://apkpure.com
[Fdroid]: https://www.f-droid.org/
[kuketz]: https://www.kuketz-blog.de/android-captive-portal-check-204-http-antwort-von-captiveportal-kuketz-de/
[GApps]: https://opengapps.org/
