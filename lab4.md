## Experiment [4]: [Bash Scripting]
### Name:Aditya Mishra, Roll No.: 590029219, Date: 2025-09-04
### AIM: 
* [To Learn Basics of Bash Scripting.]

### Requirements:
* [Any Linux Distro, any kind of text editor (vs code, vim, notepad, nano, etc)]

### Theory: 
* [Learning the basics of bash scripting.]

## Procedure & Observations

## Exercise 1: [Hello World Script]

## Task Statement: 
* [Basic Usage of Shell Scripts]

## Explanation: 
* [Writing Begginer level Shell Scripts]

## Command(s):
```
#!/bin/bash
echo "Hello, World!"

```
### Output:
#<img width="949" height="693" alt="Screenshot 2025-11-17 122448" src="https://github.com/user-attachments/assets/cb83b747-71fa-4f14-9fd0-c57758e4926b" />


## Exercise 2: [Personalized Greeting Script]

## Task Statement: 
* [Basic Shell Script to callout user defined function.]

## Explanation: 
* [This Shell script will take input from user and store it in a variable and then call the variable which will output the stored value.]

## Command(s):
```
#!/bin/bash
echo "What is your name?"
read name
echo "Hello, $name! Welcome to Shell Scripting."

``` 

## Output:

<img width="959" height="691" alt="Screenshot 2025-11-17 122625" src="https://github.com/user-attachments/assets/f0876db1-fc03-42f1-af32-84687de41127" />

## Exercise 3: [Arithmetic Operations in Shell Scripting]

## Task Statement:
* [Using Basic Arithmetic Operations in Shell Scripts]

## Command(s):
```

#!/bin/bash
echo "Enter first number: "
read num1
echo "Enter second number: "
read num2

echo "Addition: $((num1 + num2))"
echo "Subtraction: $((num1 - num2))"
echo "Multiplication: $((num1 * num2))"
echo "Division: $((num1 / num2))"

```

## Output:

<img width="955" height="916" alt="Screenshot 2025-11-17 122726" src="https://github.com/user-attachments/assets/91b68b4e-9cbd-42c8-ab46-4a64c46dad11" />

## Exercise 4:
* [Voting Eligibility]

## Task Statement:
* [Using Conditionals in Shell script ]

## Command(s):
```
#!/bin/bash
echo "What is your age?"
read age
if [ $age -ge 18 ]; then
    
    echo "You are eligible to vote!"
    
else 
    echo "You are not eligible to vote!"

fi

```

## Output:

<img width="956" height="812" alt="Screenshot 2025-11-17 123052" src="https://github.com/user-attachments/assets/dde245f5-2be8-4f50-ad1b-07d6698c4004" />

## Result
* The Exercises were successfully completed for Basic Shell Scripting
