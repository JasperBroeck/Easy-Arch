# Installing a Desktop Environment
If you used our install guide, you normally already have a desktop but if not, you can follow this quick guide to install your desktop of choice! Here we'll go over GNOME, KDE Plasma and XFCE.

## GNOME
In GNOME there are two package groups available:
- gnome: contains only the base GNOME desktop and the well-integrated core apps.
- gnome-extra: this builds contains all the same as gnome and some more apps on top, for example a mail client or IRC client, a set of games and the gnome tweaks app that allows you to tune some small settings in gnome and apply custom themes.

```bash
# Install gnome using:
sudo pacman -S gnome

# Install gnome-extra using:
sudo pacman -S gnome-extra
```

Gnome also installs a desplay manager (Login screen), the Gnome Display Manager or GDM, before you can use your desktop you need to enable this display manager using: 

```bash
sudo systemctl start gdm
sudo systemctl enable gdm
```

## KDE Plasma
For KDE Plasma the recommendation is to install the plasma package group, this installs the desktop environment and their default applications. The Plasma package can be installed using ```sudo pacman -S plasma``` while you can also only install the desktop itself without of any extra apps by installing the plasma-desktop package using ```sudo pacman -S plasma-desktop```.

You can always install the KDE apps later with the kde-applications group, do so by running the following command: ```sudo pacman -S kde-applications```.