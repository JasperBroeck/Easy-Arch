# Troubleshooting Guide 🔧

Arch Linux is a powerful operating system, but even experienced users encounter issues from time to time. This guide will help you troubleshoot common problems effectively. Follow each step carefully, and don’t hesitate to reach out for help if needed.

## General Troubleshooting Tips
1. **Stay Calm and Read the Error Message**  
   - Most issues provide a helpful error message. Look for keywords to search online or in this wiki.

2. **Check Recent Changes**  
   - Did you recently update a package, edit a configuration file, or install new software? Undoing that change can help.

3. **Refer to the Logs**  
   - Use system logs to investigate issues:
     ```bash
     journalctl -xe
     ```
   - Check logs for specific services:
     ```bash
     systemctl status <service-name>
     ```

## Common Issues and Fixes

### 0. Needs elevated, sudo or admin privileges
- **Forgot Sudo**
  - Run ```sudo <command>``` instead of just ```<command>```, fill in your root password, press enter and it should be fixed!

### 1. System Fails to Boot
- **GRUB Error:**
  - Boot into a live USB and chroot into your system:
    ```bash
    arch-chroot /mnt
    ```
  - Reinstall GRUB and regenerate the configuration:
    ```bash
    grub-install --target=x86_64-efi --efi-directory=/boot --bootloader-id=GRUB
    grub-mkconfig -o /boot/grub/grub.cfg
    ```

- **Kernel Panic:**
  - Check for missing kernel files or reinstall the kernel:
    ```bash
    pacman -S linux linux-headers
    ```

### 2. Network Issues
- **No Internet Connection:**
  - Ensure your network manager is running:
    ```bash
    systemctl status NetworkManager
    systemctl enable NetworkManager
    systemctl start NetworkManager
    ```
  - For Wi-Fi, use:
    ```bash
    nmcli device wifi connect <SSID> password <password>
    ```

- **Bluetooth Not Working:**
  - Install necessary tools:
    ```bash
    pacman -S bluez bluez-utils
    systemctl enable bluetooth
    systemctl start bluetooth
    ```

### 3. Sound Issues
- **No Audio Output:**
  - Check if `pulseaudio` or `pipewire` is installed and running:
    ```bash
    pulseaudio --start
    ```
  - Install missing tools:
    ```bash
    pacman -S alsa-utils pulseaudio
    ```
  - Use `alsamixer` to adjust volume levels.

### 4. Pacman Errors
- **Failed to Synchronize Databases:**
  - Update the mirrorlist:
    ```bash
    reflector --latest 10 --sort rate --save /etc/pacman.d/mirrorlist
    ```
  - Sync and update:
    ```bash
    pacman -Syyu
    ```

- **Package is Broken or Missing Dependencies:**
  - Force reinstall the package:
    ```bash
    pacman -S <package-name> --needed
    ```

### 5. Desktop Environment Issues
- **Black Screen After Login:**
  - Check if your display manager is running:
    ```bash
    systemctl status gdm
    ```
  - Reinstall GPU drivers:
    ```bash
    pacman -S nvidia nvidia-utils
    ```

- **Desktop Environment Not Loading:**
  - Manually start it with:
    ```bash
    startx
    ```

## If All Else Fails
If you’ve carefully followed all steps but still encounter issues, don’t worry! There are two ways you can get help:
1. **Reach Out on Reddit:**  
   Post your problem on the Arch Linux subreddit or our dedicated Easy Arch Wiki thread.  
   Be sure to include detailed information, such as the error message, what you’ve tried, and your system specs.

2. **Open an Issue on GitHub:**  
   Visit our GitHub repository and open a new issue with a description of your problem. You can find the project here:  
   [Easy Arch Wiki on GitHub](https://github.com/JasperBroeck/Easy-ArchWiki)

---

Remember, troubleshooting takes patience and focus. Take it step by step, and you’ll get your system back on track in no time. Good luck, and happy Arching! 🎉
