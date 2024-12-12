# Installing, updating or deleting packages (Apps)
Arch uses pacman to install apps or how we call it in linux, packages.
Pacman is pretty simple if you just need the basics, We'll start of by installing...

## Installing
Installing packages can be done using the -S flag in the pacman command like this:

```bash
sudo pacman -S <package>
```

You'll need to run this as a superuser (sudo) and thus enter your password. This command normally also automatically installs the dependencies for the chosen package.
**INFORMATION:** finding packages can be hard but googling what you need with "archlinux" after it or looking [here](https://archlinux.org/packages/) can get you started.

## Updating
Updating your packages is very important so you always get the latest patches and don't stay behind.
Updating a single package can be done using the install command for that package, it will just update it to the newest version, updating all your packages at once can be done using the -Syu flag like this:

```bash
sudo pacman -Syu <package>
```

Update your packages every now and then so your always up to date!

## Removing
Removing packages isn't hard but to remove an app completely you need to run the pacman command with the -Rns flag like this:

```bash
sudo pacman -Rns <package>
```

Like this, your package doesn't leave anything behind and it also removes the dependencies this app used (only the ones that were only used by this package).