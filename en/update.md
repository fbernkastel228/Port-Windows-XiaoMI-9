# Updating drivers

## Files/Tools Needed

Modified Recovery:

| File Name                                       | Android version |
|-------------------------------------------------|-----------------|
| [ofox.img](https://github.com/woacepheus/Port-Windows-11-Xiaomi-Mi-9/releases/download/recoveries/ofox.img) | Android 12/12.1/13/14 |

- [Drivers](https://github.com/woa-vayu/POCOX3Pro-Releases/releases/latest)

- [UEFI image](https://github.com/woa-vayu/POCOX3Pro-Releases/releases/latest)

### Boot into TWRP
>
> If your recovery has been replaced by the stock recovery, flash it again using

```cmd
fastboot flash recovery path\to\moddedtwrp.img reboot recovery
```

#### Execute the msc script
>
> If it asks you to run it once again, do so

```cmd
adb shell msc
```

### Diskpart

```cmd
diskpart
```

#### Select the Windows volume of the phone
>
> Use `list volume` to find it, replace "$" with the actual number of **WINVAYU**

```diskpart
select volume $
```

#### Assign the letter X

```diskpart
assign letter x
```

#### Exit diskpart

```diskpart
exit
```

### Installing drivers
>
> [!Note]
> This process will take +- 20 minutes. Do not worry, this is normal.

- Unpack the driver archive, then open the `OfflineUpdater.cmd` file

> If it asks you to enter a letter, enter the drive letter of **WINVAYU** (which should be **X**), then press enter

### Reboot your device
>
> Make sure to also change the UEFI image in Android, otherwise you may face a "blue screen of death" (BSoD) when booting Windows later.

```cmd
adb reboot
```

## Finished
