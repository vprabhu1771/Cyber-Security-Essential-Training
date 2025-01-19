# Displays the local date and time at the remote system location.

```ruby
def cmd_localtime(*args)
    print_line("Local Date/Time: " + client.sys.config.localtime);
    return true
end
```