# Reinstall Windows on your Xiaomi Mi 9

## Files/Tools Needed

- [ADB & Fastboot](https://developer.android.com/studio/releases/platform-tools)

Modified Recovery:

| File Name                                       | Android version |
|-------------------------------------------------|-----------------|
| [ofox.img](https://github.com/ivanvorvanin/Port-Windows-XiaoMI-9/releases/download/recovery/ofox.img) | Android 12/12.1/13/14 |

#### Boot the modded recovery
>
> Replace `path\to\ofox.img` with the actual path to the modded recovery image

```cmd
fastboot boot path\to\ofox.img
```

#### Formatting the Windows partition

```cmd
adb shell format
```

## [Next step: Reinstalling Windows](/en/3-install.md)
