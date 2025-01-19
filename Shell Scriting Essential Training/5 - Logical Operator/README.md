# 1 - And

```bash
x=1

y=10

echo "$x < $y && $x != $y"

echo $(($x<$y && $x!=$y))
```

OUTPUT

```
1 < 10 && 1 != 10
1
```

# 2 - Or

```bash
x=1

y=10

echo "$x < $y || $x != $y"

echo $(($x<$y || $x!=$y))
```

OUTPUT

```
1 < 10 || 1 != 10
1
```