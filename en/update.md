# Updating drivers

## Files/Tools Needed

Modified Recovery:

| File Name                                       | Android version |
|-------------------------------------------------|-----------------|
| [ofox.img](https://github.com/ivanvorvanin/Port-Windows-XiaoMI-9/releases/download/recovery/ofox.img) | Android 12/12.1/13/14 |

- [Drivers](https://github.com/qaz6750/XiaoMi9-Drivers/releases/latest)

- [UEFI image](https://github.com/qaz6750/XiaoMi9-Drivers/releases/latest)  (Make sure to select **CepheusDisableSecureBoot.img**) 

### Boot the modded recovery
>
> Replace `path\to\ofox.img` with the actual path to the modded recovery image

```cmd
fastboot boot path\to\ofox.img
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
> Use `list volume` to find it, replace "$" with the actual number of **WINCEPHEUS**

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

> If it asks you to enter a letter, enter the drive letter of **WINCEPHEUS** (which should be **X**), then press enter

### Reboot your device
>
> Make sure to also change the UEFI image in Android, otherwise you may face a "blue screen of death" (BSoD) when booting Windows later.

```cmd
adb reboot
```

## Finished
