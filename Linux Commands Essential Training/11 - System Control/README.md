# 11 - System Control
 
1. **Reboot the system**

```
sudo reboot
```

2. **Shutdown the system**

```
sudo shutdown
```

OR

```
sudo shutdown -h now
```

3. **hostname**

DISPLAY HOSTNAME

```
hostname
```

CHANGE HOSTNAME 

```
hostnamectl set-hostname prabhu
```

4. **Control systemd services**

systemctl is a command-line tool used in Linux distributions that support systemd, which is a system and service manager. systemctl allows you to control various aspects of the system, such as managing services, examining the system state, and handling system processes.

Here are some commonly used systemctl commands:

1. systemctl start <service>: Start a specific service.

2. systemctl stop <service>: Stop a specific service.

3. systemctl restart <service>: Restart a specific service.

4. systemctl enable <service>: Enable a service to start automatically at boot time.

5. systemctl disable <service>: Disable a service from starting automatically at boot time.

6. systemctl status <service>: Check the status of a specific service.

7. systemctl list-units: List all active units (services, sockets, devices, etc.) on the system.

8. systemctl list-unit-files: List all available unit files on the system.

9. systemctl reload <service>: Reload the configuration of a specific service without restarting it.

10. systemctl is-active <service>: Check if a specific service is currently active.

11. systemctl is-enabled <service>: Check if a specific service is enabled to start at boot time.

Please note that some of the commands above require administrative privileges, so you may need to use sudo before running them.

Here are examples of each of the systemctl commands you mentioned:

1. Start a Service:

   sudo systemctl start apache2  

   This command starts the Apache web server service.

2. Stop a Service:
   
   sudo systemctl stop apache2  

   This command stops the Apache web server service.

3. Restart a Service:
   
   sudo systemctl restart apache2

   This command restarts the Apache web server service.

4. Enable a Service:
   
   sudo systemctl enable apache2

   This command enables the Apache web server service to start automatically at boot.

5. Disable a Service:
   
   sudo systemctl disable apache2   

   This command disables the automatic startup of the Apache web server service at boot.

6. Check the Status of a Service:
   
   systemctl status apache2 

   This command shows detailed information about the status of the Apache web server service, including whether it's active and recent log entries.

7. List All Active Units:
   
   systemctl list-units
   
   This command lists all active units on the system, which includes services, sockets, devices, and more.

8. List All Available Unit Files:
   
   systemctl list-unit-files   

   This command lists all available unit files on the system, which includes information about enabled/disabled services.

9. Reload a Service Configuration:
   
   sudo systemctl reload apache2   

   This command reloads the configuration of the Apache web server service without stopping or restarting it. This is useful when you've made changes to the configuration files.

10. Check if a Service is Active:
    
    systemctl is-active apache2    

    This command checks if the Apache web server service is currently active and returns "active" if it is.

11. Check if a Service is Enabled:
    
    systemctl is-enabled apache2    

    This command checks if the Apache web server service is enabled to start at boot and returns "enabled" if it is.

Remember to replace apache2 with the actual name of the service you want to manage in these examples. The service name and specific commands may vary depending on your Linux distribution and the services installed on your system.