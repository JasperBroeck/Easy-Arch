# Connecting to WiFi
This article shows you how to connect to WiFi during the archlinux install using iwd.

## Starting the program
You start the program using the ```ìwctl``` command, this gives you another command line where you can give commands to the iwd tool.

## Connecting
1. First to see the devices (the different wireless cards) using ```device list```.
2. Turn this device on using these two commands: ```device name set-property Powered on``` & ```adapter adapter set-property Powered on```.
3. Scan for networks using ```station {device name} scan```.
4. List all the networks using ```station {device name} get-networks```.
5. Last but not least, connect to a network using ```station {device name} connect {network name}```, you'll need to put in the wifi password and you'll be connected.
6. Test your connection by pinging a site, for example: ```ping google.com```.

And...
...You're connected!
