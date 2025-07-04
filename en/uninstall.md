# Uninstall Windows and revert your Xiaomi Mi 9 to stock

## Why is this needed?

If you want to uninstall Windows, this is used instead of deleting partitions manually to avoid human error + writing a whole dedicated guide to just uninstalling.

If you want to relock your bootloader you'll need your partition table to be stock.

### Files/Tools Needed

- [ADB & Fastboot](https://developer.android.com/studio/releases/platform-tools)

Modified Recovery: (new method)

| File Name                                       | Android version |
|-------------------------------------------------|-----------------|
| [ofox.img](https://github.com/ivanvorvanin/Port-Windows-XiaoMI-9/releases/download/recovery/ofox.img) | Android 12/12.1/13/14 |

- [gpt_both0.bin](https://github.com/fbernkastel228/Port-Windows-XiaoMI-9/raw/refs/heads/main/Files/gpt_both0.bin) (old method)

## New method

### Switch to Android
> Or your device will not boot into Android after uninstalling Windows
- Run the **Switch to Android** or **Android** shortcut on your desktop, or flash a **boot.img** backup in fastboot/recovery.

### Boot the modded recovery
>
> Replace `path\to\ofox.img` with the actual path to the modded recovery image

```cmd
fastboot boot path\to\ofox.img
```

### Execute the restore script
```cmd
adb shell restore
```

##### Finished!

## Old method 
> In case the new one didn't work

### Switch to Android
> Or your device will not boot into Android after uninstalling Windows
- Run the **Switch to Android** or **Android** shortcut on your desktop, or flash a **boot.img** backup in fastboot/recovery.

### Boot into fastboot mode
> Hold the volume down + power button while the phone is turned off, or run the following command while it is booted
```cmd
adb reboot bootloader
```

### Restore GPT
> Replace ```path\to\gpt_both0.bin``` with the path to the gpt_both0.bin file.
```cmd
fastboot flash partition:0 path\to\gpt_both0.bin
```

#### Erase userdata
> To avoid a bootloop and restore FS size
```cmd
fastboot -w
```

##### Finished!
