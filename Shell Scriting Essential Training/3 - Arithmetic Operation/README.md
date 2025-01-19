# 1 - Addition

```bash
echo "Enter x value"

read x

echo "Enter y value"

read y

echo "x = $x"

echo "y = $y"

echo "$x + $y = $((x+y))"

#using expr
echo "$x + $y = $(expr $x + $y)"

# using expr with bracket
echo "$x + $y = $[$x + $y]"
```

OUTPUT

```
Enter x value
2

Enter y value
2

x = 2

y = 2

2 + 2 = 4

2 + 2 = 4

2 + 2 = 4
```

# 2 - Subtraction

```bash
echo "Enter x value"

read x

echo "Enter y value"

read y

echo "x = $x"

echo "y = $y"

echo "$x - $y = $((x-y))"

#using expr
echo "$x - $y = $(expr $x - $y)"

# using expr with bracket
echo "$x - $y = $[$x - $y]"
```

OUTPUT

```
Enter x value
10

Enter y value
2

x = 10
y = 2

10 - 2 = 8

10 - 2 = 8

10 - 2 = 8
```

# 3 - Multiplication

```bash
echo "Enter x value"

read x

echo "Enter y value"

read y

echo "x = $x"

echo "y = $y"

echo "$x * $y = $((x*y))"

#using expr
echo "$x * $y = $(expr $x \* $y)"

# using expr with bracket
echo "$x * $y = $[$x * $y]"
```

OUTPUT

```
Enter x value
10

Enter y value
2

x = 10
y = 2

10 * 2 = 20

10 * 2 = 20

10 * 2 = 20
```

# 4 - Division

```bash
echo "Enter x value"

read x

echo "Enter y value"

read y

echo "x = $x"

echo "y = $y"

echo "$x / $y = $((x/y))"

#using expr
echo "$x / $y = $(expr $x / $y)"

# using expr with bracket
echo "$x / $y = $[$x / $y]"
```

OUTPUT

```
Enter x value
7

Enter y value
3

x = 7
y = 3

7 / 3 = 2

7 / 3 = 2

7 / 3 = 2
```

# 5 - Modulus

```bash
echo "Enter x value"

read x

echo "Enter y value"

read y

echo "x = $x"

echo "y = $y"

echo "$x % $y = $((x%y))"

#using expr
echo "$x % $y = $(expr $x % $y)"

# using expr with bracket
echo "$x % $y = $[$x % $y]"
```

OUTPUT

```
Enter x value
7

Enter y value
3

x = 7
y = 3

7 % 3 = 1

7 % 3 = 1

7 % 3 = 1
```