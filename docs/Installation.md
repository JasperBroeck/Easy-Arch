# Installation
In this article we'll be going over the installation process of arch linux from top to bottom. We will use the 
archinstall script for an easy installation.

## Prequisites
- A USB-stick of at least 8GB
- An arch linux iso image (downloadable [here](https://archlinux.org/download/))
- A functioning computer or android device (that you can plug your usb drive in)

## Making the bootable USB
Now you got all the prequisites figured out, you can start making your bootable USB drive by following the steps below
### On a computer: 
1. Go to the [balena etcher download page](https://etcher.balena.io/#download-etcher) and install it.
2. Open the balena etcher application and choose your arch linux iso image as the file.
3. Plug in your usb disk (**MAKE SURE THERE IS NOTHING IMPORTANT ON THERE ANYMORE**) and select it as the target.
4. Hit the "flash" button to start making the bootable usb (you might need to give administrator privileges).
5. You're done!
### On an android phone:
1. Download the EtchDroid app on the playstore from [here](https://play.google.com/store/apps/details?id=eu.depau.etchdroid&pli=1).
2. Click the "Write an image" button and choose your iso file.
3. Select your flash drive, grant access and then click "Write image"
4. Wait for a couple minutes and **DON'T TOUCH YOUR PHONE OR THE USB DRIVE"**.
5. You're done!

## Installation Boot
To install arch linux on your PC, you'll need to boot your laptop from the flash drive, to do so you need to diable secure boot. You can do so in the BIOS but accessing the BIOS is different on every laptop or PC. On many laptops you can do so by shutting your laptop down and then holding the f2, f12; delete or f9 key while booting back up, then go look in the security tab if there is one, otherwise just look it up for your device or motherboard.

Once you disabled secure boot, you can boot from the usb drive. To do so, it again depends on the brand of your motherboard or laptop, you can sometimes configure to boot from the usb drive in the BIOS settings but you can also most of the time get your machine to boot into a device selector so to know how to boot into the device selector, just look it up on the internet.

Once you're booting into the usb drive, just let everything do it's job until you're greeted with this screen or something similar:

![ISO greeter](/docs/images/iso_greeter.png)

Now for your own ease and comfort, plug in an ethernet cable or setup wired ethernet tethering from your phone, connecting to wifi is possible and you can do so by following [this](/docs/wifi.md) article but, connecting via a cable is just easier for the installation and also gives you a faster connection.

To start the installation process type in ```archinstall```, you don't have a mouse cursor right now but you can just typ and it'll work. after a small moment, you should see something like this:

![archinstaller](/docs/images/archinstall.png)

This is the installer, and this is also where you can already configure a lot for your system. Let's go over the steps

### Archinstall Language
The archinstall language is just the language of this installer but since you're following this guide in english, I think that'll be perfectly fine for you.
### Locales
You can change the locales to get your language and keyboard layout but please keep the locale encoding set to the standard UTF-8.
### Mirrors
The mirrors are basically the servers from which you'll download packages or apps and to get the fastest servers, I suggest selecting the one from your country or a country near you and then I always also select the one from the US and the worldwide one, this is just so you have a backup when the other one fails.
### Disk Configuration
Select it and press enter until you see an option called back and then select that, this way your partitioning we'll be all set and you don't need to do it manualy.
The options you go through are:
- The question if you want to do the partitioning yourself or automatically, we'll go with the automated option.
- It'll ask you what drive you want to install arch on, select the right one because all data on that drive will be deleted.
- Choose a filesystem like btrfs or ext4, btrfs is the default so we'll go with it.
- Then you get the option to choose for compression. The default is to use compression so we'll go with it.
- Then you might get a couple of not-important options so just go over them.
- The last thing to do is to click back or start again.

