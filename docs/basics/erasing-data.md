---
title: "Erasing Data"
icon: 'material/delete-forever'
---
**Erasing data** from your computer may seem like a simple task, but if you want to make sure it is unrecoverable, there are some things you need to consider.

##:material-harddisk-remove:Erasing Your Entire Drive

!!! note 

    If your drive is encrypted, you do not need to worry about leaving traces of files on your computer, as your files are already impossible to access without the encryption key. If your drive is not encrypted, you should choose one of these [full disk encryption](/encryption/#os-full-disk-encryption) options.

For an unencrypted drive, pressing ++del++ on a file isn't enough; this will tell the drive to allow this space to be overwritten, but the data will still be there. You don't know when the data will be overwritten, or even if it will at all. To ensure your files cannot be recovered, you will need to follow these steps:

!!! Warning

    The data on your drive will not be recoverable. You should make sure you have any files you need backed up before performing this action!

!!! note

    None of these methods are guaranteed to make your data completely unrecoverable. The best (and most fun) method is to grab a hammer or your favorite implement of destruction and smash it into pieces. Of course, make sure to be careful not injure yourself or anyone else.

###:material-harddisk:HDD

For an **HDD**, we recommend you use `nwipe`. Install [Balena Etcher](https://www.balena.io/etcher/) and make sure you have a usb flash drive (it will be wiped so make sure there aren't any important files on it). Download a [ShredOS](https://github.com/PartialVolume/shredos.x86_64#download-img-and-iso-files-for-burning-to-usb-flash-drives-and-cd-rdvd-r) .iso file and run Balena Etcher with your USB drive plugged in. Once you're done flashing the USB drive, restart your computer and enter your UEFI settings. There should be a "Boot Override" option somewhere. Select your USB device from the menu and it will boot into ShredOS. Follow the onscreen prompts to wipe your data.

###:material-run-fast:ATA SSD

Shut down your computer and enter your computer's UEFI settings. You may need to check your motherboard's manual for which key to press on startup. Usually it's ++f2++ at the top of your keyboard or the ++del++ key. Once in your UEFI settings, there should be an option called "SecureErase." Choosing this will let you safely wipe your drive.

###:material-run-fast:NVMe

##:material-file-remove:Erasing Specific Files

Erasing individual files is futile. You should copy your file over to a new (hopefully encrypted) drive and use the above methods to erase your current drive. SSD's implement wear leveling to help extend the life of the drive, which will cause data to be written in multiple places on the drive, making it impossible to know if the file was truly erased. Even if you attempt to overwrite all free space, the actual available storage on the drive is usually more than what is exposed to you, so there will still be leftover data. There's also the SLC cache which can be multiple gigabytes, meaning that the data data won't be erased for multiple minutes.



--8<-- "includes/abbreviations.en.md"
