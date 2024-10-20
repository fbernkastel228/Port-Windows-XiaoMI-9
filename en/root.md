# Rooting your Xiaomi Mi 9

## Files/Tools Needed

- [Magisk](https://github.com/topjohnwu/Magisk/releases/latest)

- [ADB & Fastboot](https://developer.android.com/studio/releases/platform-tools)

Modified Recovery:

| File Name                                       | Android version |
|-------------------------------------------------|-----------------|
| [ofox.img](https://github.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/releases/download/recoveries/ofox.img) | Android 12/12.1/13/14 |

### Boot into TWRP
>
> If your recovery has been replaced by the stock recovery, flash it again using

```cmd
fastboot flash recovery path\to\moddedtwrp.img reboot recovery
```

#### Backing up your boot image
>
> Sometimes flashing Magisk can cause a bootloop. To fix this, you'll need to restore a boot.img backup.

Use the TWRP backup feature to make a backup of the boot partition.

### Flashing Magisk

- Flash the **magisk.apk** (you may have to rename it to magisk.zip) and reboot your phone.
- Once booted, locate the **Magisk** app and open it.
- Follow any instructions provided. Select the **direct install** method if you are provided with several methods.

Your phone will now reboot, and you have succesfully rooted it.

> [!IMPORTANT]
> After you've rooted your phone, create a new boot.img backup in Android and in Windows (using the WOA Helper app) and remove any remaining boot.img backups you have made previously. If you don't do this, switching to Android will unroot your phone.
>
> After updating or changing your rom (and rerooting) you will have to repeat all the steps on this page.

## Finished
