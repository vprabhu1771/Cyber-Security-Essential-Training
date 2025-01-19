# 1 - Less Than

```bash
echo "Enter x value"

read x

echo "Enter y value"

read y

echo "$x < $y = $((x<y))"

#using expr
echo "$x < $y = $(expr $x \< $y)"

# using expr with bracket
echo "$x < $y = $[$x < $y]"
```

OUTPUT

```
Enter x value
1

Enter y value
10

1 < 10 = 1

1 < 10 = 1

1 < 10 = 1
```

# 2 - Less Than or Equal To

```bash
echo "Enter x value"

read x

echo "Enter y value"

read y

echo "$x <= $y = $((x<=y))"

#using expr
echo "$x <= $y = $(expr $x \<= $y)"

# using expr with bracket
echo "$x <= $y = $[$x <= $y]"
```

OUTPUT

```
Enter x value
10

Enter y value
10

10 <= 10 = 1

10 <= 10 = 1

10 <= 10 = 1
```

# 3 - Greater Than

```bash
echo "Enter x value"

read x

echo "Enter y value"

read y

echo "$x > $y = $((x>y))"

#using expr
echo "$x > $y = $(expr $x \> $y)"

# using expr with bracket
echo "$x > $y = $[$x > $y]"
```

OUTPUT

```
Enter x value
10

Enter y value
2

10 > 2 = 1

10 > 2 = 1

10 > 2 = 1
```

# 4 - Greater Than or Equal To

```bash
echo "Enter x value"

read x

echo "Enter y value"

read y

echo "$x >= $y = $((x>=y))"

#using expr
echo "$x >= $y = $(expr $x \>= $y)"

# using expr with bracket
echo "$x >= $y = $[$x >= $y]"
```

OUTPUT

```
Enter x value
10

Enter y value
10

10 >= 10 = 1

10 >= 10 = 1

10 >= 10 = 1
```

# 5 - Equal To

```bash
echo "Enter x value"

read x

echo "Enter y value"

read y

echo "$x == $y = $((x==y))"

#using expr
echo "$x == $y = $(expr $x \== $y)"

# using expr with bracket
echo "$x == $y = $[$x == $y]"
```

OUTPUT

```
Enter x value
10

Enter y value
10

10 == 10 = 1

10 == 10 = 1

10 == 10 = 1
```

# 6 - Not Equal To

```bash
echo "Enter x value"

read x

echo "Enter y value"

read y

echo "$x != $y = $((x!=y))"

#using expr
echo "$x != $y = $(expr $x \!= $y)"

# using expr with bracket
echo "$x != $y = $[$x != $y]"
```

OUTPUT

```
Enter x value
1

Enter y value
10

1 != 10 = 1

1 != 10 = 1

1 != 10 = 1
```