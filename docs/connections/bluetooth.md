# Connecting to Bluetooth

This article shows you how to connect to Bluetooth devices during the archlinux install using bluez.

## Starting the program
You start the program using the `bluetoothctl` command, this gives you another command line where you can give commands to the bluez tool.

## Listing devices
1. First to list all available devices (the different bluetooth cards) using ```device list```.
2. List all the devices using ```devices``` command.
3. Get more info about a specific device using the following command: ```info <device_name>```.

You can confirm if you're connected using the `info` command like this, ```info```.

And... You're connected!

**Pairing with Bluetooth**

In this article, I'll show you how to pair with a bluetooth device.

## Enabling pairing
To enable pairing, use the following command:
```bash
devices
```
This will list all available devices and their status.

## Paired devices
To see which devices are already paired, use the following command:
```bash
paired-devices
```

And... You're paired!

**Checking connectivity**

In this article, I'll show you how to check the connectivity of a bluetooth device.

## Checking connectivity
To check if you're connected, run the following command:
```bash
info <device_name>
```
Replace `<device_name>` with the actual name of the paired device.

And... You're connected!
