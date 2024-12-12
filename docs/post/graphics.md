# Graphics Drivers
GPU's on arch have pretty good support, but this mainly goes for AMD and Intel because NVIDIA isn't that supported, I'll show you how to install the drivers for your gpu.

## NVIDIA
NVIDIA Drivers are available for linux but they are generally less maintained or just worse than the drivers for an AMD or Intel system. If you want to install them I recommend going for the open source nouveau driver, to do so first install the mesa package using this command: ```sudo pacman -S mesa```, then remove all off the following packages if they're installed:
- nvidia, nvidia-open, nvidia-lts
- nvidia-settings, nvidia-utils
- egl-wayland

After these packages are removed, install the nouveau driver using ```sudo pacman -S vulkan-nouveau```

## AMD
If your system uses an AMD cpu with iGPU or dedicated AMD card, you can install the mesa package for the modern 3D acceleration driver.
If you want to install the mesa package, run ```sudo pacman -S mesa```

If you also need Vulkan, a cross-platform 3D graphics and compute API used by for example steam on linux, Install it running this command: ```sudo pacman -S vulkan-radeon```

## Intel
If your system uses an Intel CPU with iGPU or dedicated Intel GPU, you can install the mesa package for the modern 3D acceleration driver.
If you want to install the mesa package, run ```sudo pacman -S mesa```

If tou also need Vulkan, a cross-platform 3D graphics and compute API used by for example steam on linux, Install it running this command: ```sudo pacman -S vulkan-intel```