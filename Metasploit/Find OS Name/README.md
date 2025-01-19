```ruby
def guess_target_platform(os)
    case os
    when /windows/i
      Msf::Module::Platform::Windows.realname.downcase
    when /darwin/i
      Msf::Module::Platform::OSX.realname.downcase
    when /mac os ?x/i
      # this happens with java on OSX (for real!)
      Msf::Module::Platform::OSX.realname.downcase
    when /freebsd/i
      Msf::Module::Platform::FreeBSD.realname.downcase
    when /openbsd/i, /netbsd/i
      Msf::Module::Platform::BSD.realname.downcase
    else
      Msf::Module::Platform::Linux.realname.downcase
    end
end

if client.sys.config.sysinfo && client.sys.config.sysinfo['OS']
  new_platform = guess_target_platform(client.sys.config.sysinfo['OS'])
  print_status(new_platform)
else
  print_error("Error: Unable to retrieve the operating system information.")
end
```

```
meterpreter > run prabhu.rb
[*] windows
```