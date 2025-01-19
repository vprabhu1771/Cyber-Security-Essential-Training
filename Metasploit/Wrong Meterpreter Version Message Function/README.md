```ruby
meter_type = client.platform

# Wrong Meterpreter Version Message Function

def wrong_meter_version(meter = meter_type)

   print_error("#{meter} version of Meterpreter is not supported with this Script!")
   raise Rex::Script::Completed

end

# Call Wrong Meterpreter Version Message Function

wrong_meter_version(meter_type)
```

```
meterpreter > run prabhu.rb
[-] windows version of Meterpreter is not supported with this Script!
```