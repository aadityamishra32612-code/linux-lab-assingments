# 🔧understanding how existing scripts in repo work

# 🔧script 1

  ```
 #!/bin/bash      - shebang
 echo "hello world!"     - printing hello world
 name="aditya mishra"   - taking aditya mishravin variable name
 age=18    -  taking 19 in variable age 

 echo "My name is $name ansd I am $age year old."  - printing name and age
```
#### OUTPUT :
<img width="713" height="99" alt="image" src="https://github.com/user-attachments/assets/9e237fb7-221b-4dbc-9e23-be2dcf698497" />



# 🔧 script 2

```
#!/bin/bash        -shebang
a="Ashish Choudhary"           -taking Ashish choudhary in the variable a
b=40                 -taking 40 in the variable b

if [ $a="Ashish CHoudhary" ] && [ $b -gt 18 ]; then      -checking conditions and using an opreator and(&&)
    echo " you are adult "                     - printing you are adult
fi

if [ $a=" akshat" ] && [ $b -lt 18 ]; then       -checking conditions and using an opreator and(&&)
    echo "you are minor"                         - printing you are minor
fi

```
<img width="805" height="504" alt="image" src="https://github.com/user-attachments/assets/ced795cd-09f0-43ef-90b8-67883913352b" />

<img width="728" height="84" alt="image" src="https://github.com/user-attachments/assets/e84d3294-c3d5-4792-8711-27224c2e898a" />


### 🔧 Q1 what is the purpose of #!/bin/bash at the top of the script

ANS-- the shebang line at the top of a script specifies the interpreter that should be used to the run the script.

### 🔧 Q2 how do you make a script executable?
ANS-- 1. add the shebang at the top
          2. give permission using the chmod command
          3. run the code.
