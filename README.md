# ungoogled-fairphone

[<img src="https://domaindrivenarchitecture.org/img/delta-chat.svg" width=20 alt="DeltaChat"> chat over e-mail](mailto:buero@meissa-gmbh.de?subject=community-chat) | [<img src="https://meissa-gmbh.de/img/community/Mastodon_Logotype.svg" width=20 alt="team@social.meissa-gmbh.de"> team@social.meissa-gmbh.de](https://social.meissa-gmbh.de/@team) | [Website & Blog](https://domaindrivenarchitecture.org)

## Rational

As it is widely known that Google tries to collect data from all possible sources, we offer a method how you can remove and restrict many Google Services on your smartphone. We provide a manual for these restrictions for the Fairphone. There we install LineageOS instead of Android and furthermore we remove unnecessary functions like Google DNS or replacing the Play Store with the Open-Source based F-Droid Store. The goal is to prevent Google from tracking you.

For more details and more information about specific google functions and dependencies we have removed, take a look at our [installation_guide][guide].


If you are interested how an arbitrary app is tracking you, we can recommend the [exodus][privacy] platform, another website which is highly recommendable for a safer smartphone usage is [mobilsicher][privacyII].

## How to bypass GooglePlay Store and use your messenger of choice

Without a minimal google installation package (like GApps) it is no more possible to use the GooglePlay Store. This doesn't mean that you can't use its popular apps.\
One of the most important apps for most of the users is the messenger of choice. We proposed the Open-Source based **F-Droid App Store**, but unfortunately there you can only directly download the **Telegram** messenger, although Signal is also FOSS (Free and open-source software) it is not yet available ([more information][signal]) in the F-Droid store. 

But there are many workarounds, e.g. if you want to use **Signal** you can just download the apk [here][signalapk] (either install it directly on the smartphone or through your computer). Even if you still want to use WhatsApp you can go to the official WhatsApp [page][whatsapp] and the same will work there. The only disadvantage is that the backup functionality won't work because it's based on GoogleDrive.

Another easy way to install apps like Signal, Threema, DeltaChat and almost **any other app** from GooglePlay Store is to use the **Aurora App Store**. The Aurora Store is available in the F-Droid Store and you can easily download APKs from the PlayStore without a GooglePlay account, but nevertheless supports important security updates. Furthermore, Aurora gives you information about in-app trackers and many more.

Before you ungoogle your smartphone, it might be a good idea to backup your chats from your phone. Therefore you just have to store a backup file on your computer and after the installation you can copy this backup file back to your phone and restore your chats.


## How to synchronize the calendar of your computer with your smartphone without Google

A very popular and favoured feature of Google is the possibility to synchronize all your devices very easy. The downside is that for all those "free features" you don't have to pay with cash, but you pay with your data.\
Here we suggest a possibility how to bypass Google and still synchronize all your devices very easy.

One way is to use the Nextcloud, [here][nextcloud] you can sign up and get a cloud hostet e.g. in Germany with up to 5GB for free. There you can store all your data without concern. If you want even more security, you can even host your [own cloud-server][owncloud] with Nextcloud.\
If you want to synchronize your calendar through your devices, first download the Nextcloud app. Now you only have to install DAVx⁵ from the F-Droid Store which helps you to sync your calendar and contacts (for further informations see [here][davx5]).

If you don't want to use Nextcloud, you can use FOSS (Free and open-source) apps like [Simple Mobile Tools][smt] or [Etar][etar]. Both apps are available in the F-Droid Store and can also be synchronized with the help of [DAVx⁵][davx5].



## See also
* https://github.com/JBNCK/fp3_debloater


## License
Copyright © 2021 meissa GmbH
Licensed under the [Apache License, Version 2.0](LICENSE) (the "License")

[guide]: https://gitlab.com/domaindrivenarchitecture/ungoogled-fairphone/-/blob/main/installation_guide.md
[privacy]: https://reports.exodus-privacy.eu.org/de/
[privacyII]: https://mobilsicher.de/
[signalapk]: https://signal.org/android/apk/
[whatsapp]: https://www.whatsapp.com/download/
[signal]: https://github.com/signalapp/Signal-Android/issues/281#issuecomment-21762482
[nextcloud]: https://nextcloud.com/signup/
[owncloud]: https://nextcloud.com/devices/
[davx5]: https://docs.nextcloud.com/server/latest/user_manual/de/pim/sync_android.html
[smt]: https://www.simplemobiletools.com/
[etar]: https://github.com/Etar-Group/Etar-Calendar
