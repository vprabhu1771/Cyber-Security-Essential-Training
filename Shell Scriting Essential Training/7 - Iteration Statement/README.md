# 1 - while loop

```bash
count=1

while [ $count -le 5 ]
do
  echo "count $count"
  count=$(( $count + 1 ))
done
```

OUTPUT

```
count 1
count 2
count 3
count 4
count 5
```

# 2 - break statement

```bash
count=1

while [ $count -le 5 ]
do

  echo $count
  count=$(( $count + 1 ))

  if [ $count -eq 2 ]
  then
    break
  fi
done
```

OUTPUT

```
1
```

# 3 - continue statement

```bash
count=1

while [ $count -le 5 ]
do

  echo $count
  count=$(( $count + 1 ))

  if [ $count -eq 2 ]
  then
    continue
  fi
done
```

OUTPUT

```
1
2
3
4
5
```

# 4 - for c style

```bash
for (( count=1; count<=5; count++ ))
do 
   echo $count
done
```

OUTPUT

```
1
2
3
4
5
```

# 5 - for range loop

```bash
for element in 1 2 3 4 5
do
  echo $element
done
```

OUTPUT

```
1
2
3
4
5
```

# 6 - for range loop type 2

```bash
for element in {1..5} 
do
  echo $element
done
```

OUTPUT

```
1
2
3
4
5
```

# 7 - for range loop type 3

```bash
for element in {0..10..2}
do
  echo $element
done
```

OUTPUT

```
0
2
4
6
8
10
```

# 8 - multiplication table using while loop

```bash
count=1

table_no=2

while [ $count -le 5 ]
do
  echo "$count * $table_no = $(( count * table_no ))"
  count=$(( $count + 1 ))
done
```

OUTPUT

```
1 * 2 = 2
2 * 2 = 4
3 * 2 = 6
4 * 2 = 8
5 * 2 = 10
```

# 9 - multiplication table using for loop

```bash
table_no=2

for element in 1 2 3 4 5
do
  echo "$element * $table_no = $(( element * table_no ))"
done
```

OUTPUT

```
1 * 2 = 2
2 * 2 = 4
3 * 2 = 6
4 * 2 = 8
5 * 2 = 10
```