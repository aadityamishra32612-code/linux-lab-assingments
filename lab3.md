# modifying script

## original script

```
#!/bin/bash        ---shebang
a="Ashish Choudhary"           ---taking vansh in the variable a
b=40                 ---taking 40 in the variable b

if [ $a="Ashish Choudhary" ] && [ $b -gt 18 ]; then      ---checking conditions and using an opreator and(&&)
    echo " you are adult "                     ---printing you are adult
fi

if [ $a=" akshat" ] && [ $b -lt 18 ]; then       ---checking conditions and using an opreator and(&&)
    echo "you are minor"                         --- printing you are minor
fi

```
<img width="805" height="504" alt="image" src="https://github.com/user-attachments/assets/eaaa23d8-7f8f-455f-9f6d-11d756287003" />

<img width="728" height="84" alt="image" src="https://github.com/user-attachments/assets/99c7e4ee-0d4c-480a-876a-b409e36460bd" />


##  modified script

```
#!/bin/bash 
# prompt user for input

read -p "enter your name: " name      --- taking name from the user
read -p "enter your age: " age        --- taking age from the user

if [ $name="Ashish Choudhary" ] && [ $age -gt 18 ]; then    --- checking conditions with if and opreator and(&&)     
    echo " you are adult "                     --- printing (you are adult)
fi

if [ $name=" akshat" ] && [ $age -lt 18 ]; then  ----  checking conditions with if and opreator and(&&)      
    echo "you are minor"                         ---- printing (you are minor)
fi
```
## the difference between the original and modified script is that in the first one we check for fixed value and in the next case we check for all cases .

<img width="745" height="292" alt="image" src="https://github.com/user-attachments/assets/5f793cb2-caf2-42df-90b0-805f81e74011" />


## checking with differnt examples
#### output is :
<img width="727" height="230" alt="image" src="https://github.com/user-attachments/assets/57dbbd1a-c351-4362-a995-be985a3b71cb" />


### Q1=differnce between $1,$@ and $# in bash?

Ans-- 0 $1= this refers to positional parameters
         $@= represents all arguments passed to the script
         $#= returns the number of arguments passed

### Q2=what does exit 1 mean in the script
    
Ans-- general error (something went wrong) Or exit with error.
