# Installation
In this article we'll be going over the installation process of arch linux from top to bottom. We will use the 
archinstall script for an easy installation.

## Prequisites
- A USB-stick of at least 8GB
- An arch linux iso image (downloadable [here](https://archlinux.org/download/))
- A functioning computer or android device (where you can plug your usb drive in)

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
