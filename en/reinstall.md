# Reinstall Windows on your Xiaomi Mi 9

## Files/Tools Needed

- [ADB & Fastboot](https://developer.android.com/studio/releases/platform-tools)

Modified Recovery:

| File Name                                       | Android version |
|-------------------------------------------------|-----------------|
| [ofox.img](https://github.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/releases/download/recoveries/ofox.img) | Android 12/12.1/13/14 |

### Boot into TWRP
>
> If MIUI has replaced your recovery, boot to fastboot and run

```cmd
fastboot flash recovery path\to\twrp.img reboot recovery
```

#### Formatting the Windows partition

```cmd
adb shell format
```

## [Next step: Reinstalling Windows](/en/3-install.md)
