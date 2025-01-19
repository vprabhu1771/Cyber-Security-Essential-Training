# 4 - System Information
 
1. **Display system information**

```
uname   
```

``` 
Linux
```

```
uname -a
```

```
Linux kali 6.3.0-kali1-amd64 #1 SMP PREEMPT_DYNAMIC Debian 6.3.7-1kali1 (2023-06-29) x86_64 GNU/Linux
```

2. **Display disk space usage**

```
df -h
```

```
Filesystem      Size  Used Avail Use% Mounted on
udev            940M     0  940M   0% /dev
tmpfs           196M  1.2M  195M   1% /run
/dev/sda1        79G   19G   56G  26% /
tmpfs           980M     0  980M   0% /dev/shm
tmpfs           5.0M     0  5.0M   0% /run/lock
/dev/loop0       84M   84M     0 100% /snap/scrcpy/399
/dev/loop2      128K  128K     0 100% /snap/bare/5
/dev/loop8       13M   13M     0 100% /snap/snap-store/959
/dev/loop1       92M   92M     0 100% /snap/gtk-common-themes/1535
/dev/loop4       74M   74M     0 100% /snap/core22/864
/dev/loop5      486M  486M     0 100% /snap/gnome-42-2204/126
/dev/loop7      497M  497M     0 100% /snap/gnome-42-2204/132
/dev/loop3       56M   56M     0 100% /snap/core18/2790
/dev/loop6       41M   41M     0 100% /snap/snapd/20092
tmpfs           196M  116K  196M   1% /run/user/1000
```

3. **Display memory usage**

```
free -m
```

```
               total        used        free      shared  buff/cache   available
Mem:            1958         904         261           7         962        1054
Swap:           1023           0        1023
```

4. **Monitor system processes**

```
top
```

```
top - 09:00:45 up 7 min,  1 user,  load average: 0.01, 0.08, 0.05
Tasks: 200 total,   1 running, 199 sleeping,   0 stopped,   0 zombie
%Cpu(s):  0.8 us,  1.1 sy,  0.0 ni, 97.7 id,  0.1 wa,  0.0 hi,  0.3 si,  0.0 st 
MiB Mem :   1958.3 total,    262.7 free,    903.2 used,    962.4 buff/cache     
MiB Swap:   1024.0 total,   1024.0 free,      0.0 used.   1055.1 avail Mem 

    PID USER      PR  NI    VIRT    RES    SHR S  %CPU  %MEM     TIME+ COMMAND                                                                                      
   2040 kali      20   0  448108 104604  85408 S   3.7   5.2   0:04.07 qterminal                                                                                    
    966 root      20   0  403072 130884  55984 S   3.3   6.5   0:07.54 Xorg                                                                                         
   1439 kali      20   0 1323272 107624  79516 S   1.0   5.4   0:02.67 xfwm4                                                                                        
   1503 kali      20   0  283736  26944  18560 S   0.3   1.3   0:01.64 panel-13-cpugra                                                                              
   1505 kali      20   0  358136  29784  20692 S   0.3   1.5   0:01.38 panel-15-genmon                                                                              
   6538 kali      20   0   11704   5248   3200 R   0.3   0.3   0:00.03 top                                                                                          
      1 root      20   0   21144  12652   9324 S   0.0   0.6   0:00.86 systemd      
```

The top command provides a real-time, dynamic view of system processes. 

It displays a list of processes and their resource utilization, such as CPU and memory usage. 

To exit top, press `q`.

```
htop
```

Similar to top, htop is an interactive process viewer that provides a more user-friendly and feature-rich interface.
 
It allows you to sort processes, send signals, and manage them easily.


5. **Neofetch**

```
sudo apt install neofetch
```

```
neofetch
```

```
kali@kali 
--------- 
OS: Kali GNU/Linux Rolling x86_64 
Host: VMware Virtual Platform None 
Kernel: 6.3.0-kali1-amd64 
Uptime: 4 mins 
Packages: 2821 (dpkg), 9 (snap) 
Shell: zsh 5.9 
Resolution: 1920x984 
DE: Xfce 4.18 
WM: Xfwm4 
WM Theme: Kali-Dark 
Theme: Kali-Dark [GTK2], adw-gtk3-dark [GTK3] 
Icons: Flat-Remix-Blue-Dark [GTK2/3] 
Terminal: qterminal 
Terminal Font: FiraCode 10 
CPU: 11th Gen Intel i7-11700K (4) @ 3.600GHz 
GPU: 00:0f.0 VMware SVGA II Adapter 
Memory: 756MiB / 1958MiB 
```