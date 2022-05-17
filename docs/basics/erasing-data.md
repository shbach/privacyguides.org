---
title: "Erasing Data"
icon: 'material/delete-forever'
---
**Erasing data** from your computer may seem like a simple task, but if you want to make sure they are unrecoverable, there are some things you need to consider.

##Erasing Your Entire Drive

If your drive is [encrypted](/encryption/#os-full-disk-encryption), then you don't usually need to worry about deleting files; all your data is already impossible to read without the encryption key. An unencryped drive is another story.

For this situation, pressing ++del++ on a file isn't enough; this will tell the drive to allow this space to be overwritten, but the data will still be there. You don't know when the data will be overwritten, or even if it will at all. To ensure your files cannot be recovered, you will need to follow these steps:

!!! Warning

    The data on your drive will not be recoverable. You should make sure you have any files you need backed up before performing this action!

###:material-harddisk:HDD

For an **HDD**, we recommend you use `nwipe`. Install [Balena Etcher](https://www.balena.io/etcher/) and make sure you have a usb flash drive (it will be wiped so make sure there aren't any important files on it). Download a [ShredOS](https://github.com/PartialVolume/shredos.x86_64#download-img-and-iso-files-for-burning-to-usb-flash-drives-and-cd-rdvd-r) .iso file and run Balena Etcher with your USB drive plugged in. Once you're done flashing the USB drive, restart your computer and enter your UEFI settings. There should be a "Boot Override" option somewhere. Select your USB device from the menu and it will boot into ShredOS. Follow the onscreen prompts to wipe your data.

###:material-run-fast:SSD

Shut down your computer and enter your computer's UEFI settings. You may need to check your motherboard's manual for which key to press on startup. Usually it's ++f2++ at the top of your keyboard or the ++del++ key. Once in your UEFI settings, there should be an option called "SecureErase." Choosing this will let you safely wipe your drive.

##Erasing Specific Files

--8<-- "includes/abbreviations.en.md"
