# ungoogled-fairphone

[<img src="https://domaindrivenarchitecture.org/img/delta-chat.svg" width=20 alt="DeltaChat"> chat over e-mail](mailto:buero@meissa-gmbh.de?subject=community-chat) | [<img src="https://meissa-gmbh.de/img/community/Mastodon_Logotype.svg" width=20 alt="team@social.meissa-gmbh.de"> team@social.meissa-gmbh.de](https://social.meissa-gmbh.de/@team) | [Website & Blog](https://domaindrivenarchitecture.org)

## Übersicht

Da es bekannt ist, dass Google in allen möglichen Bereichen versucht Daten zu sammeln, zeigen wir hier eine Möglichkeit, wie man Google Services auf einem Smartphones entfernt und einschränkt. Wir stellen eine Anleitung für das Fairphone bereit. Auf diesem installieren wir LineageOS anstelle von Android und entfernen überflüssige Google Funktionen wie Google DNS oder ersetzen den PlayStore durch den Open-Source basierten F-Droid Store. Das Ziel dabei ist Google vom tracken abzuhalten.

Für mehr Details und Informationen über spezifische Google Funktionen und Abhängigkeiten die wir entfernt haben, werfen Sie einen Blick auf unsere [installations Anleitung][guide].

When Sie daran interessiert sind wie eine beliebige App sie tracken kann, können wir die [exodus][privacy] Platform empfehlen. Eine weitere empfehlenswerte Webseite für eine sicherere Smartphone Benutzung ist [mobilsicher][privacyII].


## Wie man den GooglePlay Store umgehen kann und trotzdem den Messenger der Wahl nutzen kann

Ohne das minimale Google Installationspaket (GApps) ist es nicht mehr Möglich den GooglePlay Store zu nutzen. Das bedeutet jedoch nicht, dass man die populären Apps nicht mehr benutzen kann.\
Eine der wichtigsten Apps für die meisten Nutzer ist der Messenger. Wir haben den **F-Droid App Store** empfohlen, leider steht dort nur der **Telegram** Messenger zum direkten Download zur Verfügung. Obwohl Signal ebenfalls FOSS (Free and open-source software) ist, ist Signal im F-Droid Store noch nicht verfügbar ([mehr Informationen][signal]).

Es existieren jedoch einige Möglichkeiten trotzdem an die gewollten Apps zu gelangen. Für den Download von **Signal** kann [hier][signalapk] die apk gedownloaded werden (und entweder direkt auf dem Smartphone installiert werden oder über den Computer). Auch falls weiterhin WhatsApp genutz werden soll, kann auf der offiziellen WhatsApp Seite die [apk][whatsapp] gedownloaded und installiert werden. Der einzige Nachteil ist, dass die Backup Funktionalität nicht funktioniert, da diese auf GoogleDrive basiert.

Eine andere einfache Möglichkeit Apps wie Signal, Threema, DeltaChat und fast **jede andere App** aus dem PlayStore zu installieren ist, den **Aurora App Store** zu benutzen. Der Aurora Store ist im F-Droid Store verfügbar und über diesen kann man einfach die apks aus dem PlayStore herunterladen und installieren ohne einen GooglePlay Account nutzen zu müssen, trotzdem werden weiterhin wichtige Sicherheitsupdates unterstützt. Außerdem gibt Aurora weitere Informationen über in-App Tracker und vieles mehr.



## Siehe auch
* https://github.com/JBNCK/fp3_debloater


## License
Copyright © 2021 meissa GmbH
Licensed under the [Apache License, Version 2.0](LICENSE) (the "License")

[guide]: https://gitlab.com/domaindrivenarchitecture/ungoogled-fairphone/-/blob/German/installation_guide.md
[privacy]: https://reports.exodus-privacy.eu.org/de/
[privacyII]: https://mobilsicher.de/
[signalapk]: https://signal.org/android/apk/
[whatsapp]: https://www.whatsapp.com/download/
[signal]: https://github.com/signalapp/Signal-Android/issues/281#issuecomment-21762482
