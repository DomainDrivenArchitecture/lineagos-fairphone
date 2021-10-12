# FAQ

## If "5. Install LinegaeOS recovery image" does not work

You an try `fastboot flash boot_a <image_filename.img>` or `fastboot flash boot_b <image_filename.img>`. The `boot_a` is the name of our recovery boot partition. If your FP was rooted several times this my result in a non factory partition name ...