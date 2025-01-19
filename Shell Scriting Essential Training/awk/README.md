# 1

```
cat data.txt
```

```
awk '{print}' data.txt
```

# 2

```
awk '{print $1}' data.txt
```

# 3

```
awk '{print $2}' data.txt
```

# 4

```
awk '{print $3}' data.txt
```

# 5

```
awk '{print $0}' data.txt
```

# 6

```
awk '{print $1,$3}' data.txt
```

# 7

```
ls -l
```

```
ls -l | awk '{print $1}' data.txt
```

```
ls -l | awk '{print $2}' data.txt
```

```
ls -l | awk '{print $5}' data.txt
```

# 8

```
echo "Hello from Prabhu"
```

```
echo "Hello from Prabhu" | awk '{print $1}'
```

```
echo "Hello from Prabhu" | awk '{print $1, $3}'
```

# 9

```
awk '{print $NF}' data.txt
```

```
cat data.txt
```

# 10

```
cat /etc/passwd
```

```
awk '{print $2}' /etc/passwd
```

# 11

```
cat /etc/passwd  | grep jay
```

# 12 - awk field separator

```
cat /etc/passwd

awk -F':' '{print $2}' /etc/passwd

awk -F':' '{print $3}' /etc/passwd

awk -F':' '{print $4}' /etc/passwd

awk -F':' '{print $5}' /etc/passwd


awk -F':' '{print $1,$7}' /etc/passwd
```