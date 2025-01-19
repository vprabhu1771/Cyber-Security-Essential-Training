```
https://www.rubydoc.info/github/rapid7/metasploit-framework/Msf/Sessions/Meterpreter
```

Get a string representation of the current session platform.

```ruby
def getinfo(session)
   
   print_status("Getting Target system platform...")
   
   print_status("#{session.platform}")

end

getinfo(client)
```

```
meterpreter > run prabhu.rb
[*] Getting Target system platform...
[*] windows
```