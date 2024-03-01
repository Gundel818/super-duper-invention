# Root for Xiaomi Mi 11 Lite 5G unlocked using Magisk

## Prequerities 
- Device and bootloader unlocked
- USB debug activated
- Magisk installed
- Platform-tools downloaded on PC

### Phone steps

- Settings > About the device > MIUI version > 3 dots button at the top right corner > Download the last update package 

- When is downloaded : 
    - Open Magisk app > `Install` button (in Magisk category) > `Select and Patch a File` choice > Click on `Let's go` button

    - Select the ZIP package downloaded (in `Downloads/downloaded_rom` directory)

- Patch done

### PC steps

- Move the patched image on your PC

- Open the `platform-tools` directory in a terminal

- Check with `adb devices` command if your phone is listed : 
    - If the device is shown as `unauthorized`, check your phone and accept the access request popup

    - If the device is shown as `device`, then continue
- Restart your device in fastboot mode with : `adb reboot bootloader`

- Flash the patched image with : `fastboot flash boot C:\to\your\magisk\patched\image\magisk-patched-******.img`

```
Sending 'boot_a' (196608 KB)                       OKAY [  4.272s]
Writing 'boot_a'                                   OKAY [  0.690s]
Finished. Total time: 4.978s
```
- Reboot your device
- Open again Magisk (If a popup told you to reboot again the device, reboot it)

- Device rooted ! (Can be verified with `Root Checker Basic` app for example)
