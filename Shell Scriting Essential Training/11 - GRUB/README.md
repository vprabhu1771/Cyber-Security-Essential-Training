# 1 - Speed up the boot time

```
sudo nano /etc/default/grub
```

```
GRUB_TIMEOUT=5
```

Change To

```
GRUB_TIMEOUT=0
```

# 2 - Change Default OS

```
sudo nano /etc/default/grub
```

0 -> Debain

1 -> Windows

```
GRUB_DEFAULT=0
```

Change To

```
GRUB_DEFAULT=1
```

# 3 - Change Linux OS Name in GRUB

```
sudo nano /etc/default/grub
```

```
GRUB_DISTRIBUTOR=`lsb_release -i -s 2> /dev/null || echo Debian`
```

Change To

```
GRUB_DISTRIBUTOR=`lsb_release -i -s 2> /dev/null || echo OWN LINUX`
```