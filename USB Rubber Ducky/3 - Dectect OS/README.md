# 1 - Dectect OS and Write Output in Windows

To detect the operating system and write the output to a specific text editor on Windows or 
macOS using the USB Rubber Ducky, you can modify the Ducky Script as follows:

For Windows:

```
DELAY 1000
GUI r
DELAY 1000
STRING cmd
DELAY 1000
ENTER
DELAY 1000
STRING systeminfo | findstr /B /C:"OS Name" /C:"OS Version" > %userprofile%\Desktop\os_info.txt
ENTER
```

This script will first wait for 1 second (1000 milliseconds), 
then simulate pressing the "Windows" key and the "R" key together to open the "Run" dialog box. 

It will then type "notepad" and press Enter to open Notepad. 
Finally, it will run the "systeminfo" command and filter the output to display only the 
operating system name and version, and then save the output to a text file named "os_info.txt" on the user's desktop.

# 3 - Dectect OS and Write Output in macOS

To detect the operating system and write the output to a specific text editor on macOS using the USB Rubber Ducky, you can modify the Ducky Script as follows:

For macOS:

```
DELAY 1000
GUI SPACE
DELAY 500
STRING textedit
ENTER
DELAY 1000
STRING echo "Operating System Information: " > ~/Desktop/os_info.txt && system_profiler SPSoftwareDataType | grep 'System Version' >> ~/Desktop/os_info.txt
ENTER
```

This script will first wait for 1 second (1000 milliseconds), then simulate pressing the "Command" key and the "Space" key together to open Spotlight search. It will then type "textedit" and press Enter to open TextEdit. Finally, it will run a command that echoes a header message to the text file, and then retrieves the operating system information using the "system_profiler" command and saves the output to a text file named "os_info.txt" on the user's desktop.

Once the script has run, the output will be saved to the specified text editor on the respective operating system.

# 4 - Dectect OS and Write Output in Linux

To detect the operating system and write the output to a specific text editor on Linux using the USB Rubber Ducky, you can modify the Ducky Script as follows:

For Linux:

```
DELAY 1000
GUI r
DELAY 500
STRING gnome-terminal
ENTER
DELAY 1000
STRING uname -a > ~/Desktop/os_info.txt
ENTER
```

This script will first wait for 1 second (1000 milliseconds), then simulate pressing the "Windows" key and the "R" key together to open the "Run" dialog box. It will then type "gnome-terminal" and press Enter to open a Terminal window. Finally, it will run the "uname -a" command and redirect the output to a text file named "os_info.txt" on the user's desktop.

Note that this script assumes that the target Linux machine has a GNOME desktop environment installed, which is the default desktop environment for many popular Linux distributions. If the target machine uses a different desktop environment or terminal emulator, you'll need to modify the script accordingly.

Once the script has run, the output will be saved to the specified text file on the Linux machine.