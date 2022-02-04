# Installation issues

## If OEM-unlock code doesn't work

If you get the message "Password verification failed" on your phone after entering the unlock code.
It might be the problem, that you are using an old Android version. So update your Android and try it again.

For additional information see here: https://forum.fairphone.com/t/bootloader-unlocking-code-for-fairphone-3-not-working/66685/6


## If "5. Install LinegaeOS recovery image" does not work

You an try `fastboot flash boot_a <image_filename.img>` or `fastboot flash boot_b <image_filename.img>`. The `boot_a` is the name of our recovery boot partition. If your FP was rooted several times this my result in a non factory partition name ...

With `fastboot getvar current-slot` you can find out whether your suffix should be `_a` or `_b`. Find more possible names at https://forum.fairphone.com/t/find-out-boot-partitions-name/77171

