# Managing System Services with systemd

## Starting the service manager
You start the service manager using the `systemctl` command, which gives you a new command-line interface where you can give commands to the systemd tool.

### Listing devices
First, you need to list all available devices (wireless cards) using the following command:
```bash
systemctl --type=socket-list
```
This will show you a list of sockets that represent the available wireless interfaces.

## Enabling services
To enable a service to start automatically on boot, use the following command:
```bash
systemctl enable <service_name>
```
Replace `<service_name>` with the actual name of the service you want to enable.

## Starting services
To start a specific service, use the following command:
```bash
systemctl start <service_name>
```
Again, replace `<service_name>` with the actual name of the service you want to start.

## Restarting services
To restart a specific service, use the following command:
```bash
systemctl restart <service_name>
```

## Reloading configurations
To reload the configuration of a specific service, use the following command:
```bash
systemctl reload <service_name>
```

## Checking status
You can check the current status of a service using the following command:
```bash
systemctl status <service_name>
```
Replace `<service_name>` with the actual name of the service you want to check.

Note that `systemctl` is a powerful tool, and it's recommended to use it instead of traditional system administration tools like `rc.d` or `init.d`.

Let me know if this meets your requirements!