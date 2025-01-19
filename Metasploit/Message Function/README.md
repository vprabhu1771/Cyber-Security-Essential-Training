```ruby
@exec_opts = Rex::Parser::Arguments.new(

   "-h" => [ false, "Help menu." ],

   "-p" => [ true, "The port on the remote host where Metasploit is listening (default: 4444)"],

   "-m" => [ false, "Start Exploit multi/handler for return connection"],

   "-pt" => [ true, "Specify Reverse Connection Meterpreter Payload.Default windows/meterpreter/reverse_tcp"],

   "-mr" => [ true, "Provide Multiple IP Addresses for Connections separated by comma."],

   "-mp" => [ true, "Provide Multiple PID for connections separated by comma one per IP."]

)

# Usage Message Function

def usage

   print_line "Meterpreter Script for injecting a reverse tcp Meterpreter Payload"

   print_line "in to memory of multiple PID's, if none is provided a notepad process."

   print_line "will be created and a Meterpreter Payload will be injected in to each."

   print_line(@exec_opts.usage)

   raise Rex::Script::Completed

end

# Call Usage Message Function
usage()
```

```
meterpreter > run prabhu.rb
Meterpreter Script for injecting a reverse tcp Meterpreter Payload
in to memory of multiple PID's, if none is provided a notepad process.
will be created and a Meterpreter Payload will be injected in to each.

OPTIONS:

    -h    Help menu.
    -m    Start Exploit multi/handler for return connection
    -mp   Provide Multiple PID for connections separated by comma one per IP.
    -mr   Provide Multiple IP Addresses for Connections separated by comma.
    -p    The port on the remote host where Metasploit is listening (default: 4444)
    -pt   Specify Reverse Connection Meterpreter Payload.Default windows/meterpreter/reverse_tcp

meterpreter > 
```