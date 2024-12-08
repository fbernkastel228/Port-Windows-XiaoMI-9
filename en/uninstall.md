# Uninstall Windows and revert your Xiaomi Mi 9 to stock

## Why is this needed?

If you want to uninstall Windows, this is used instead of deleting partitions manually to avoid human error + writing a whole dedicated guide to just uninstalling.

If you want to relock your bootloader you'll need your partition table to be stock.

### Files/Tools Needed

- [ADB & Fastboot](https://developer.android.com/studio/releases/platform-tools)

Modified Recovery:

| File Name                                       | Android version |
|-------------------------------------------------|-----------------|
| [ofox.img](https://github.com/ivanvorvanin/Port-Windows-XiaoMI-9/releases/download/recovery/ofox.img) | Android 12/12.1/13/14 |

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

#### Finished
