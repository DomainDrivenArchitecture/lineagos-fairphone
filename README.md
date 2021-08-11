# ungoogled-fairphone

[<img src="https://domaindrivenarchitecture.org/img/delta-chat.svg" width=20 alt="DeltaChat"> chat over e-mail](mailto:buero@meissa-gmbh.de?subject=community-chat) | [<img src="https://meissa-gmbh.de/img/community/Mastodon_Logotype.svg" width=20 alt="team@social.meissa-gmbh.de"> team@social.meissa-gmbh.de](https://social.meissa-gmbh.de/@team) | [Website & Blog](https://domaindrivenarchitecture.org)

## Rational

As it is widely known that Google tries to collect data from all possible sources, we offer a method where you can restrict many Google Services. We provide a manual for these restrictions for the Fairphone. There we install LineageOS instead of Android and furthermore we remove unnecessary functions like Google DNS or replacing the Play Store with the Open-Source based F-Droid Store. The goal is to prevent Google from tracking you.

For more details and more informations about specific google functions and dependencies we have removed, take a look at our [installation_guide](https://gitlab.com/domaindrivenarchitecture/ungoogled-fairphone/-/blob/main/installation_guide.md).


If you are interested how an arbitrary app is tracking you, we can recommend the [exodus][privacy] platform, another website which is highly recommendable for a safer smartphone usage is [mobilsicher][privacyII].

## How to bypass GooglePlay Store and use messenger of choice

Without a minimal google installation package (like GApps) it is no more possible to use the GooglePlay Store. This doesn't mean that you can't use its popular apps.
One of the most important apps for most of the users is the messenger of choice. We proposed the Open-Source based **F-Droid App Store**, but unfortunately there you can only directly download the **Telegram** messenger, although Signal is also FOSS it is not yet [available][signal] in the F-Droid store. 

But there are many workarounds, e.g. if you want to use **Signal** you can just download the apk [here][signalapk] (either install it directly on the smartphone or through your computer). Even if you still want to use WhatsApp you can go to the official WhatsApp [page][whatsapp] and the same will work there. 

Another easy way to install apps like WhatsApp, Signal and almost **any other app** from GooglePlay Store is to use the **Aurora App Store**. The Aurora Store is available in the F-Droid Store and you can easily download APKs from the PlayStore without a GooglePlay account. Furthermore Aurora gives you informations about in-app trackers and many more.



## See also
* https://github.com/JBNCK/fp3_debloater


## License
Copyright © 2021 meissa GmbH
Licensed under the [Apache License, Version 2.0](LICENSE) (the "License")


[privacy]: https://reports.exodus-privacy.eu.org/de/
[privacyII]: https://mobilsicher.de/
[signalapk]: https://signal.org/android/apk/
[whatsapp]: https://www.whatsapp.com/download/
[signal]: https://github.com/signalapp/Signal-Android/issues/281#issuecomment-21762482
