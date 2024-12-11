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
### Disk Encryption
You can skip this one or complete all the options, it's self explanetory
### Swap
This is "virtual memory", you can enable this so when you run out of physical RAM, it uses a bit of your storage as memory but your real RAM is obviously faster.
### Bootloader
You have a couple of options in here, the systemd-boot one is the default and it's a great and pretty fast one. Your second real option is GRUB, it's a very popular option and the one many places take as the default.
### Hostname
This is the computer name.
### Root Password
The root password is the administrator password that has rights to cause big changes to your system.
### User Account
The user account is a simple one, you have a username, password and than the option to make your user a superuser or sudoer. In windows this would be called an administrator, a user that can execute root actions.
### Profile
In this step you'll install a desktop environment like GNOME or KDE Plasma, these are the two most used options and are both good options so go with either of them. If you really know what you're doing, you can also go for one of the other options but most of them are a lot harder so be careful.
### Audio
If you chose GNOME or KDE Plasma in the previous step, you can skip this but otherwise, choose pipewire since it's better supported and newer.
### Kernels
You can just use the linux kernel.
- The lts kernel is for extended support
- The zen kernel is for a faster experience but can be buggy
- The normal kernel is just the standard base kernel
### Network Configuration
If u chose GNOME OR KDE Plasam, choose the NetworkManager, otherwise you'll know what to choose I think.
### Additional Packages
Here you can specify apps you want to preinstall on your system and you can find a list of apps [here](https://archlinux.org/packages/)
### Optional Repositories
You don't need this unless you already know you do.
### Timezone
Choose your timezone for the clock to be correct in your system.
### Automatic Time Sync
This option automatically syncs your system time from the internet.

Now choose Install, follow the on-screen instructions and let it do it's thing.

## Chroot
after a while you'll be asked if you want to get into the newly installed chroot environment. It's basically a terminal environment from your newly installed system and you can do some stuff to your system but you can also say no, typ reboot and remove the usb drive to boot right into the fresh arch install!

## Post Install things
As far as post install goes, I think the most important thing is to check for updates although you probably don't have any because arch always downloads the newest packages!

Succes with your system and have fun!
