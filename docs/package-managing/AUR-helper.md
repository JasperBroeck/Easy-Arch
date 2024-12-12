# AUR Helper
In Arch you have something called the AUR or the Arch User Repository, here you can find a lot of extra apps that you won't find in the official arch repository.
In this article, I'll show you how to install an AUR helper so you can install packages from the AUR.

You have 2 options:
- Paru, a newer and easier AUR helper written in rust.
- Yay, a well known and widely spread AUR helper.

## Paru
Installing Paru isn't difficult, you just need to run a couple of commands and then you'll be able to use it!
The commands needed for this are the following:

```bash
sudo pacman -S --needed base-devel
git clone https://aur.archlinux.org/paru.git
cd paru
makepkg -si
```

Using Paru is like using pacman, you install a package by running the following command: ```paru -S <package>```. Notice you don't use sudo because AUR helpers won't even run with sudo.

## Yay
Installing Yay is almost the same as installing Paru, just run these commands:

```bash
sudo pacman -S --needed base-devel
git clone https://aur.archlinux.org/yay.git
cd yay
makepkg -si
```

Using Yay is like using pacman, you install a package by running the following command: ```yay -S <package>``. Notice you don't use sudo because AUR helpers won't even run with sudo.

## Finding packages
Finding packages from the AUR can be easily done by taking a look on [this](https://aur.archlinux.org/packages) page.