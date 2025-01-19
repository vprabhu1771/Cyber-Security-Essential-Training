```ruby
def getinfo(session)
   
   print_status("Getting system information ...")

   print_status("The target machine OS is #{session.sys.config.sysinfo}")

end

getinfo(client)
```

```
meterpreter > run prabhu.rb
[*] Getting system information ...
[*] The target machine OS is {"Computer"=>"MAIN3", "OS"=>"Windows 10 (10.0 Build 19045).", "Architecture"=>"x64", "BuildTuple"=>nil, "System Language"=>"en_US", "Domain"=>"WORKGROUP", "Logged On Users"=>2}

meterpreter > 
```

```ruby
def getinfo(session)
   
   print_status("Getting system information ...")

   print_status("The target machine OS is #{session}")
   
   print_status("The target machine OS is #{session.sys}")
          
   print_status("The target machine OS is #{session.sys.config}")
 
   print_status("The target machine OS is #{session.sys.config.sysinfo}")

end

getinfo(client)


meterpreter > run prabhu.rb
[*] Getting system information ...
[*] The target machine OS is #<Msf::Sessions::Meterpreter_x86_Win:0x00007f88753fd748>
[*] The target machine OS is #<Rex::Post::Meterpreter::ObjectAliases:0x00007f885f75bea0>
[*] The target machine OS is #<Rex::Post::Meterpreter::Extensions::Stdapi::Sys::Config:0x00007f885f760388>
[*] The target machine OS is {"Computer"=>"MAIN3", "OS"=>"Windows 10 (10.0 Build 19045).", "Architecture"=>"x64", "BuildTuple"=>nil, "System Language"=>"en_US", "Domain"=>"WORKGROUP", "Logged On Users"=>2}
```


```
https://docs.metasploit.com/api/Rex/Post/Meterpreter/Extensions/Stdapi/Net/Socket.html
```

```ruby
def getinfo(session)
   
   print_status("Getting system IP information ...")

   print_status("The local machine IP #{session.sock.localhost}")   

   print_status("The local machine Port #{session.sock.localport}")

   print_status("The target machine IP #{session.sock.peerhost}")   
   
   print_status("The target machine Port #{session.sock.peerport}")

end

getinfo(client)
```

```
meterpreter > run prabhu.rb
[*] Getting system IP information ...
[*] The local machine IP 192.168.1.112
[*] The local machine Port 4444
[*] The target machine IP 192.168.1.73
[*] The target machine Port 54076
meterpreter > 
```


```ruby
def getinfo(session)

    begin
       sysnfo = session.sys.config.sysinfo

       runpriv = session.sys.config.getuid

       print_status("Getting system information ...")

       print_status("The target machine OS is #{sysnfo['OS']}")

       print_status("The computer name is #{'Computer'} ")

       print_status("Script running as #{runpriv}")

    rescue ::Exception => e

       print_error("The following error was encountered #{e}")

    end

end

getinfo(client)
```

```
meterpreter > run prabhu.rb                                                                                                                                                                                                                 
[*] Getting system information ...                                                                                                                                                                                                          
[*] The target machine OS is Windows 10 (10.0 Build 19045).                                                                                                                                                                                 
[*] The computer name is Computer                                                                                                                                                                                                           
[*] Script running as MAIN3\windows_rig3  
```