# Nvidia Shield
For Nvidia Shield (2017 darcy) running Android **_9.1.0_**

If you are currently in bootloop, download the [developer or recovery image](https://developer.nvidia.com/gameworksdownload)

Extract/flash using official [instructions](https://developer.download.nvidia.com/assets/gameworks/downloads/regular/howtoflash/HowTO-Flash-Recovery-Image.txt)

Basically...
```
fastboot flash staging blob
fastboot flash boot boot.img
fastboot flash recovery recovery.img
fastboot flash system system.img
fastboot flash vendor vendor.img
fastboot reboot
```

**Make sure you are on Android version _9.1.0_**

Download [Magisk 25.2 apk](https://github.com/topjohnwu/Magisk/releases/download/v25.2/Magisk-v25.2.apk) from official repository:


On computer...
```
adb install Magisk-v25.2.apk
adb reboot bootloader
fastboot flash boot magisk_patched-25200_dY5W3.img
fastboot reboot
```
You should now be able to use Magisk.

_To restore_
```
adb reboot bootloader
fastboot flash boot boot.img
fastboot reboot
```
