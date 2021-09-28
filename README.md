# Nvidia Shield
For Nvidia Shield (2017 darcy) running on version 8.2.3 developer image.

If you are currently in bootloop, download the developer image from here:
https://developer.nvidia.com/gameworksdownload

Extract/flash using these instructions: https://developer.download.nvidia.com/assets/gameworks/downloads/regular/howtoflash/HowTO-Flash-Recovery-Image.txt

Basically...
```
fastboot flash staging blob
fastboot flash boot boot.img
fastboot flash recovery recovery.img
fastboot flash system system.img
fastboot flash vendor vendor.img
fastboot reboot
```

`**!!!! Make sure you are on android version 8.2.3 !!!!**`

Download Magisk 23.0 apk from official repository:
https://github.com/topjohnwu/Magisk/releases/download/v23.0/Magisk-v23.0.apk

On computer...
```
adb install Magisk-v23.0.apk
adb reboot bootloader
fastboot flash boot boot_magisk23.0.img
fastboot reboot
```
You should now be able to use Magisk.

To restore:
```
adb reboot bootloader
fastboot flash boot boot.img
fastboot reboot
```
