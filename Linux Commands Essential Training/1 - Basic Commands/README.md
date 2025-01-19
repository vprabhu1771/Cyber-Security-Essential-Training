# 1 - Basic Commands
 
1. **List files and directories**

Syntax
```
ls
```

```
Desktop  Documents  Downloads  Music  Pictures  Public  snap  Templates  Videos
```

2. **Change the current directory**

Syntax

```
cd /path/to/directory
```

```
ls
```

```
Desktop  Documents  Downloads  Music  Pictures  Public  snap  Templates  Videos
```                                                                                                                                                                    
```
cd Desktop
```

```
┌──(kali㉿kali)-[~/Desktop]
└─$
```

3. **Print the working directory**

Syntax
```
pwd
```

```
┌──(kali㉿kali)-[~/Desktop]
└─$ pwd                      
/home/kali/Desktop
```


4. **Create a new directory**

```
mkdir new_directory
```

```
┌──(kali㉿kali)-[~]
└─$ cd Desktop
```

```
┌──(kali㉿kali)-[~/Desktop]
└─$ mkdir songs        
```

```
┌──(kali㉿kali)-[~/Desktop]
└─$ ls
songs
```

```
┌──(kali㉿kali)-[~/Desktop]
└─$ 
```


5. **Remove a directory - Empty Directory**

```
rmdir directory_to_remove
```

```
┌──(kali㉿kali)-[~/Desktop]
└─$ rmdir songs      
```

```
┌──(kali㉿kali)-[~/Desktop]
└─$ ls
```

6. **Create an empty file**

```
touch new_file.txt
```

```
┌──(kali㉿kali)-[~/Desktop]
└─$ touch songs.txt  
```

```
┌──(kali㉿kali)-[~/Desktop]
└─$ touch app.py
```

7. **Clear the Terminal Screen**

If you want to clear the contents of your terminal screen to get rid of previous commands and output, 
you can use the clear command. Simply open your terminal and type:

```
clear
```

This will clear the terminal and give you a clean slate.

8. **View History**

```
history
```

9. **Clear History**

```
rm /home/kali/.bash_history
```

```
rm /home/kali/.zsh_history
```

```
rm ~/.zsh_history 
```

OR

```
rm .zsh_history 
```

Make Sure Close and Open Terminal

10. **display the current user's username**

The whoami command in Linux is used to display the username of the currently logged-in user. When you run this command in a terminal, it will simply output your username. For example:

```
whoami
```

```
┌──(kali㉿kali)-[~]
└─$ whoami
kali
```

11. **Redirect Output to txt file**

Using > (redirect):

```
ifconfig > example.txt
```

```
┌──(kali㉿kali)-[~]
└─$ ifconfig
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet 192.168.1.112  netmask 255.255.255.0  broadcast 192.168.1.255
        inet6 fe80::60a9:bbdc:b61b:ef97  prefixlen 64  scopeid 0x20<link>
        ether 00:0c:29:45:0d:4f  txqueuelen 1000  (Ethernet)
        RX packets 22027  bytes 32747951 (31.2 MiB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 10793  bytes 841003 (821.2 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73<UP,LOOPBACK,RUNNING>  mtu 65536
        inet 127.0.0.1  netmask 255.0.0.0
        inet6 ::1  prefixlen 128  scopeid 0x10<host>
        loop  txqueuelen 1000  (Local Loopback)
        RX packets 4  bytes 240 (240.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 4  bytes 240 (240.0 B)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
```

```
┌──(kali㉿kali)-[~]
└─$ ifconfig > /home/kali/Desktop/result.txt
```

12. **Clear a File**

If you want to clear the contents of a text file, you can use the `>`, `cat /dev/null`, or `truncate` commands to achieve this. For example, if you have a file named `example.txt` and you want to clear it, you can do one of the following:

Using `>` (redirect):

```
> example.txt
```

Using `cat` and `/dev/null`:

```
cat /dev/null > example.txt
```

Using truncate:

```
truncate -s 0 example.txt
```

All of these commands will clear the content of `example.txt` and make it an empty file.

```
┌──(kali㉿kali)-[~]
└─$ cat /dev/null > /home/kali/Desktop/result.txt
```

13. **Open File via Mousepad**

```
mousepad new_file.txt
```

14. **Copy files**

```
cp file_to_copy.txt new_location/
```

```
┌──(kali㉿kali)-[~]
└─$ cd Desktop
```

```
┌──(kali㉿kali)-[~/Desktop]
└─$ touch songs.txt
```

```
┌──(kali㉿kali)-[~/Desktop]
└─$ ls
songs.txt
```

```
┌──(kali㉿kali)-[~/Desktop]
└─$ mousepad songs.txt
```

```
┌──(kali㉿kali)-[~/Desktop]
└─$ mkdir entertainment
```

```
┌──(kali㉿kali)-[~/Desktop]
└─$ ls
entertainment  songs.txt
```

```
┌──(kali㉿kali)-[~/Desktop]
└─$ cp songs.txt entertainment/ 
```

```
┌──(kali㉿kali)-[~/Desktop]
└─$ cd entertainment            
```

```
┌──(kali㉿kali)-[~/Desktop/entertainment]
└─$ ls
songs.txt
```

```
──(kali㉿kali)-[~/Desktop/entertainment]
└─$ cd ..           
```

```
┌──(kali㉿kali)-[~/Desktop]
└─$
```

15. **Copy directories**

```
cp -r directory_to_copy/ new_location/
```

```
┌──(kali㉿kali)-[~/Desktop]
└─$ mkdir personal     
```

```
┌──(kali㉿kali)-[~/Desktop]
└─$ cp -r entertainment personal 
```

```
┌──(kali㉿kali)-[~/Desktop]
└─$ cd personal                 
```

```
┌──(kali㉿kali)-[~/Desktop/personal]
└─$ ls
entertainment
```

```
┌──(kali㉿kali)-[~/Desktop/personal]
└─$ cd entertainment 
```

```
┌──(kali㉿kali)-[~/Desktop/personal/entertainment]
└─$ ls
songs.txt
```

```
┌──(kali㉿kali)-[~/Desktop/personal/entertainment]
└─$
```

16. **Rename files**

```
mv old_file.txt new_name.txt
```

```
┌──(kali㉿kali)-[~]
└─$ cd Desktop 
```

```
┌──(kali㉿kali)-[~/Desktop]
└─$ touch songs.txt
```

```
┌──(kali㉿kali)-[~/Desktop]
└─$ mousepad songs.txt
```

```
┌──(kali㉿kali)-[~/Desktop]
└─$ mv songs.txt movies.txt 
```

17. **Move files**

```
mv old_file.txt new_name.txt
```

```
┌──(kali㉿kali)-[~/Desktop]
└─$ mkdir personal         
```

```
┌──(kali㉿kali)-[~/Desktop]
└─$ mv movies.txt personal 
```

```
┌──(kali㉿kali)-[~/Desktop]
└─$ ls
```

```
┌──(kali㉿kali)-[~/Desktop]
└─$ cd personal 
```

```
┌──(kali㉿kali)-[~/Desktop/personal]
└─$ ls
movies.txt
```

18. **Move directories**

```
mv /old/location/ /new/location/
```

```
┌──(kali㉿kali)-[~/Desktop]
└─$ mkdir entertainment
```

```
┌──(kali㉿kali)-[~/Desktop]
└─$ touch songs.txt
``` 

```
┌──(kali㉿kali)-[~/Desktop]
└─$ mousepad songs.txt 
``` 

```
┌──(kali㉿kali)-[~/Desktop]
└─$ mv songs.txt entertainment 
```

```
┌──(kali㉿kali)-[~/Desktop]
└─$ mv entertainment/ personal/
```

```
┌──(kali㉿kali)-[~/Desktop]
└─$ cd personal     
```

```
┌──(kali㉿kali)-[~/Desktop/personal]
└─$ ls         
entertainment  movies.txt
```

```
┌──(kali㉿kali)-[~/Desktop/personal]
└─$ cd entertainment 
```

``` 
┌──(kali㉿kali)-[~/Desktop/personal/entertainment]
└─$ ls
songs.txt
```

19. **Remove files**

```
rm file_to_remove.txt
```

20. **Remove directories**

```
rm -r directory_to_remove
```

21. **Open The Current Directory.txt**

```
xdg-open .
```

The `xdg-open` command is used in Unix-like operating systems to open a file or URL using the default application associated with the file type or URL scheme. When you run `xdg-open .`, you are essentially asking the system to open the current directory (`.`) using the default file manager. Here are some topics related to this command:

1. **xdg-open Overview**: Understanding what `xdg-open` is and how it fits into the Linux/Unix ecosystem. It's a part of the freedesktop.org standards and aims to provide a consistent way to open files and URLs across different desktop environments.

2. **Default Applications**: Learn how to set and manage default applications for various file types and URL schemes. `xdg-open` relies on these settings to determine which program to use when opening a file or URL.

3. **File Managers**: Explore different file managers available on Linux, such as Nautilus (GNOME), Dolphin (KDE), Thunar (Xfce), and others. `xdg-open` typically opens the current directory using the default file manager.

4. **URL Handling**: Understand how `xdg-open` handles URLs, including web URLs (http:// and https://) and other custom URL schemes. You can configure which web browser is used to open URLs.

5. **Command Usage**: Learn the basic syntax and usage of the `xdg-open` command, including how to specify a file or URL as an argument.

6. **Troubleshooting**: Address common issues and error messages related to `xdg-open`. Sometimes, it might not behave as expected, and troubleshooting can help resolve these problems.

7. **Security Considerations**: Understand the security implications of using `xdg-open` to open files or URLs. It's important to be cautious when opening files from untrusted sources.

8. **Alternatives**: Explore alternative commands or methods to open files and URLs in a Unix-like environment, such as using specific programs like `xdg-mime`, `gio`, or directly invoking applications.

9. **Desktop Environment Differences**: Note that the behavior of `xdg-open` may vary slightly depending on the desktop environment you are using. Familiarize yourself with any specific behaviors or configuration options for your desktop environment.

10. **Customization**: Learn how to customize the behavior of `xdg-open` by modifying configuration files or environment variables.

By exploring these topics, you can gain a comprehensive understanding of how to use `xdg-open` effectively and troubleshoot any issues that may arise when opening files and URLs on your Linux system.