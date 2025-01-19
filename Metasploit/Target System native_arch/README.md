```
https://www.rubydoc.info/github/rapid7/metasploit-framework/Msf/Sessions/Meterpreter
```

Get a string representation of the architecture of the process in which the current session is running. This defaults to the same value of arch but can be overridden by specific meterpreter implementations to add support.

```ruby
def getinfo(session)
   
   print_status("Getting Target system native_arch ...")
   
   print_status("#{session.native_arch}")

end

getinfo(client)
```

```
meterpreter > run prabhu.rb
[*] Getting Target system native_arch ...
[*] x86
```