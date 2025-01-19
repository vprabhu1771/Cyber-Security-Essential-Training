# 1 - if

```bash
echo "enter your age"

read age

if [ $age -ge 18 ]
then
        echo "Congrats You are eligible for voting"
fi
```

OUTPUT

```
enter your age
20
Congrats You are eligible for voting
```

# 2 - if else

```bash
echo "enter your age"

read age

if [ $age -ge 18 ]
then 
        echo "Congrats You are eligible for voting"
else
        echo "Sorry You are not eligible for voting"
fi
```

OUTPUT

```
enter your age
20
Congrats You are eligible for voting


enter your age
10
Sorry You are not eligible for voting
```

# 3 - if else if

```bash
echo "enter any number"

read no


if [ $no -gt 0 ]
then 
	echo "$no is positive no"
elif [ $no -lt 0 ]
then
	echo "$no is negative no"
else
	echo "$no is zero"
fi
```

OUTPUT

```
enter any number
-5
-5 is negative no


enter any number
5
5 is positive no


enter any number
0
0 is zero
```

# 4 - if else with logical operator

```bash
echo "enter your age"

read age

if [ $age -ge 18 -a $age -lt 22 ]
then 
        echo "eligile for voting"
else
        echo "not eligible for voting"
fi
```

OUTPUT

```
enter your age
19

eligile for voting


enter your age
23

not eligible for voting
```

# 5 - nested if else ladder

```bash
echo "enter your age"

read age

if [ $age -ge 18 -a $age -le 22 ]
then 
        echo "you are eleigibe for house loan"

        if [ $age -ge 18 -a $age -le 20 ]
        then
                echo "Car loan also available"
        else
                echo "car loan not available"
        fi
else
        echo "you are not eligible for house loan"
fi
```

OUTPUT

```
enter your age
20
you are eleigibe for house loan
Car loan also available

enter your age
26
you are not eligible for house loan

enter your age
21
you are eleigibe for house loan
car loan not available
```

# 6 - case

```bash
echo "Enter any option"

read option

case $option in
1) 
    echo "Good Morning" ;;

2)
    echo "Good Afternoon" ;;

3)
    echo "Good Evening" ;;

4)
    echo "Good Night" ;;

*)      
    echo "Invaild Option" ;;

esac
```

OUTPUT

```
Enter any option
2
Good Afternoon

Enter any option
44
Invaild Option
```

# 7 - ternary operator

```bash
echo "enter your age"

read age

# full syntax

if [ $age -ge 18 ]; then  echo "eligible for voting"; else echo "not eligible f>

# short syntax

[ $age -ge 18 ] && echo "eligible for voting" || echo "not eligible for voting"
```

OUTPUT

```
enter your age
23
eligible for voting
eligible for voting


enter your age
11
not eligible for voting
not eligible for voting
```