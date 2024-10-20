# Partitioning your Xiaomi Mi 9

## Files/Tools Needed

- Unlocked bootloader

- [ADB & Fastboot](https://developer.android.com/studio/releases/platform-tools)

Modified Recovery:

| File Name                                       | Android version |
|-------------------------------------------------|-----------------|
| [ofox.img](https://github.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/releases/download/recoveries/ofox.img) | Android 12/12.1/13/14 |

### Notes
>
> [!WARNING]  
> All your data will be erased! Back up now if needed.
>
> Do not run the same command twice.
>
> DO NOT REBOOT YOUR PHONE if you think you made a mistake, ask for help in the [Telegram chat](https://t.me/woacepheus).
>
> Do not run all commands at once, execute them in order!

> [!IMPORTANT]
> Make sure you use the MODDED Recovery throughout this whole tutorial as we provide tools to help aid this installation process and make it as easy as possible for you.
>
> If you don't use it and you face any errors, consider it your fault and consider yourself alone if you try asking for support as you have deferred from the main guide.

### Opening CMD as an admin
>
> Download **platform-tools** and extract the folder somewhere, then open CMD as an **administrator**.
>
> It is recommended to keep this window open and use it throughout the entire guide.
>
> Replace `path\to\platform-tools` with the actual path to the platform-tools folder, for example **C:\platform-tools**.

```cmd
cd path\to\platform-tools
```

#### Flash the modded recovery
>
> Replace `path\to\moddedtwrp.img` with the actual path to the modded recovery image

```cmd
fastboot flash recovery path\to\moddedtwrp.img reboot recovery
```

#### Backing up your boot image
>
> This will back up your boot image in the current directory

```cmd
adb pull /dev/block/by-name/boot boot.img
```

### Run the partitioning script
>
> Replace **$** with the amount of storage you want Windows to have (do not add GB, just write the number)
>
> If it asks you to run it once again, do so

```cmd
adb shell partition $
```

### Check if Android still starts

- Just restart the phone, and see if Android still works

## [Next step: Rooting your phone](2-root.md)
