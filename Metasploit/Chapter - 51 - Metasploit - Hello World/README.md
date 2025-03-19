# 1 - Create a new file for your custom module

Creating a custom module in the Metasploit Framework (MSF) to print "Hello, World!" is a simple task. Below is an example of a basic custom module that accomplishes this:

Create a new file for your custom module. Let's name it `hello_world.rb`.

# 2 - `hello_world.rb`

```ruby
# hello_world.rb
require 'msf/core'

class MetasploitModule < Msf::Auxiliary
  include Msf::Exploit::Remote::Tcp

  def initialize
    super(
      'Name'        => 'Hello World Module',
      'Description' => 'Prints Hello, World!',
      'Author'      => 'Your Name',
      'License'     => MSF_LICENSE
    )
  end

  def run
    print_good('Hello, World!')
  end
end
```

Save the file in the `~/.msf4/modules/auxiliary/` directory.

# 3 - Open msfconsole

Now, you can load the custom module in Metasploit:

```
msfconsole
```

OR

```
msfconsole -q
```

# 4 - load your custom module

Once in the Metasploit console, load your custom module:

```
use auxiliary/hello_world
```

# 5 - Run the module

```
run


You should see the output:

[+] Hello, World!
[*] Auxiliary module execution completed


This is a very basic example, and in a real-world scenario, you would replace the `print_good` line with the actual functionality you want your module to perform, such as interacting with a target system. Customize the module according to your specific requirements.

Keep in mind that this is just an auxiliary module for demonstration purposes. If you are creating an exploit module or post-exploitation module, you'll need to include additional code and functionalities based on the nature of your module.

set RHOSTS 192.168.1.73
set RPORT 5555

run
[*] Running module against 192.168.1.73

[+] 192.168.1.73:5555 - Hello, World!
[*] Auxiliary module execution completed
```