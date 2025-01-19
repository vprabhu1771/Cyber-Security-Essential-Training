# 2 - File Operations
 
1. **Concatenate and display file contents**

```
cat file.txt
```

```
touch songs.txt
```

``` 
mousepad songs.txt
```

```    
cat songs.txt
```

```
one 
two
three
four
five
six
seven
eight
nine
ten
```


2. **Display the beginning or end of a file**

```
head -n 10 file.txt
```

```
head -n 3 songs.txt
```

```
one 
two
three
```

```       
tail -n 10 file.txt
```

```
tail -n 3 songs.txt
```

```
eight
nine
ten
```

3. **Search for text patterns in files**

```
grep "pattern" file.txt
```

The `grep` command is used to search for a specified pattern in a text file. Here's an example of how you might use it:

Suppose you have a text file called `file.txt` with the following content:


This is an example file.
It contains some text.
You can search for patterns using grep.
Let's try searching for the word "example."


To search for the pattern "example" in `file.txt`, you would run the following command in your terminal:

```
grep "example" file.txt
```

The output of this command will be:


This is an example file.
Let's try searching for the word "example."


In this example, `grep` searched for the pattern "example" in the `file.txt` and displayed the lines that contained the matching text.


4. **Search for files and directories**

```
find /path/to/search -name "filename"
```

5. **Compare two files**

```
diff file1.txt file2.txt
```

6. **grep**

```
hostnamectl
```

```
 Static hostname: kali
       Icon name: computer-vm
         Chassis: vm 🖴
      Machine ID: adae0cb13e174de4b9ed95eb5a24897e
         Boot ID: c49cfc5cb73847b99d1a973815b6a53f
  Virtualization: vmware
Operating System: Kali GNU/Linux Rolling          
          Kernel: Linux 6.3.0-kali1-amd64
    Architecture: x86-64
 Hardware Vendor: VMware, Inc.
  Hardware Model: VMware Virtual Platform
Firmware Version: 6.00
   Firmware Date: Thu 2020-11-12
    Firmware Age: 2y 10month 2w    

```

```
hostnamectl | grep Kernel
```

```
hostnamectl | grep Kernel
```

```
Kernel: Linux 6.3.0-kali1-amd64
```

```
hostnamectl | grep -i KERNEL
```

```
hostnamectl | grep -i KERNEL
```

```
Kernel: Linux 6.3.0-kali1-amd64
```


