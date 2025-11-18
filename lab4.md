
## Experiment [5]: [Shell Programming]

### Name: Aditya Mishra  Roll.: 590029219 Date: 2025-10-05

### AIM:
* [To Learn Basic Conditional Statements in Bash Scripting]

### Requirements:
* [Any Linux Distro, any kind of text editor (vs code, vim, notepad, nano, etc)]

### Theory:
* [Basic usage of conditions and arrays in bash scripting.]

## Procedure & Observations

## Exercise 1: [Prime Number Check]

## Task Statement:
* [To check if the number given by the user is a prime number or not.]

## Explanation:
* [using if else loop wap to check if the number is a prime number or not.]

## Command(s):
```
#!/bin/bash
echo "Enter a number: "
read num
flag=0

for ((i=2; i<num; i++))
do
    if [ $((num % i)) -eq 0 ]
    then
        flag=1
        break
    fi
done

if [ $flag -eq 0 ]
then
    echo "$num is a prime number."
else
    echo "$num is not a prime number."
fi
```

### Output:
<img width="950" height="598" alt="Screenshot from 2025-11-18 10-22-36" src="https://github.com/user-attachments/assets/5750571d-1140-4778-a22b-f88b14070bba" />

## Exercise 2: [Sum of Digits]

## Task Statement:
* [Take input from user and give the sum of two digits.]

## Explanation:
* [This script will take input from user and will give the following output.]

## Command(s):
```
#!/bin/bash
echo "Enter a number: "
read num
sum=0

while [ $num -gt 0 ]
do
    digit=$((num % 10))
    sum=$((sum + digit))
    num=$((num / 10))
done

echo "Sum of digits: $sum"
```

### Output:

<img width="950" height="352" alt="Screenshot from 2025-11-18 10-25-17" src="https://github.com/user-attachments/assets/3796b655-99a6-4223-a8a9-9bcbabe3300a" />

## Exercise 3: [Armstrong Numbers]

## Task Statement:
* [Take input user and give the sum of Armstrong number of n digits is a number equal to the sum of its digits raised to the power n. Example: 153 = 1^3^ + 5^3^ + 3^3^ ]

## Explanation:
* [This script will tell if the number entered by the user is an armstrong number or not.]

## Command(s):
```
#!/bin/bash
echo "Enter a number: "
read num
temp=$num
n=${#num}   # number of digits
sum=0

while [ $temp -gt 0 ]
do
    digit=$((temp % 10))
    sum=$((sum + digit**n))
    temp=$((temp / 10))
done

if [ $sum -eq $num ]
then
    echo "$num is an Armstrong number."
else
    echo "$num is not an Armstrong number."
fi
```

### Output:
<img width="950" height="275" alt="Screenshot from 2025-11-18 10-27-30" src="https://github.com/user-attachments/assets/f24f9205-3281-4b37-8c97-ad00be486219" />

## Result:
* The Exercises were successfully completed for Basic Shell Scripting.
