# Installation issues (Fairphone)

## If OEM-unlock code doesn't work on your Fairphone

If you get the message "Password verification failed" on your phone after entering the correct unlock code:
Your current Android version might be out of date, please update.

For additional information see the [Fairphone Forum](https://forum.fairphone.com/t/bootloader-unlocking-code-for-fairphone-3-not-working/66685/6)

## If "5. Install LinegaeOS recovery image" does not work

You can try `fastboot flash boot_a <image_filename.img>` or `fastboot flash boot_b <image_filename.img>`. The `boot_a` is the name of our recovery boot partition. 
If your FP was rooted several times this my result in a non factory partition name.

With `fastboot getvar current-slot` you can find out whether your suffix should be `_a` or `_b`. Find more possible names in this [thread](https://forum.fairphone.com/t/find-out-boot-partitions-name/)77171
