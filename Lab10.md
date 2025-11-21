### EXPERIMENT 10
*************************************************************************
### SHELL PROGRAMMING CONTINUED MODULAR AND REUSABLE CODE 
### ADITYA MISHRA, BATCH-78, 590029219
#### 1.Modular and Reusable code
Modular Programming means breaking down a program into smaller, independent and reusable components. In shell scripting, this is achieved through:
##### Functions
* Named blocks of code that can be called multiple times 
* Improve code readability and maintainability
* Reduce code duplication
##### Sourcing Scripts
* Using `script.sh` or `source script.sh` to include external scripts
* Makes functions and variables from the source file available in current script
* Unlike executing a script ,sourcing runs in current shell 

#### 2.Script Optimization Techniques
* AVOID UNNECESSARY SUBSHELLS: Each `$command` creates a new process, which is resource intensive.
* USE BUILT-IN STRING OPERATIONS: Bash has built in string manipulation that'faster than external commands like `expr` , `sed` or `awk` .
* MINIMIZE LOOPS: Use shell expansions and built-in instead of loops when possible

### LAB EXERSISES EXPLAINED:
#### 1.STRING LENGTH
##### EXPLANATION:
* `${#str}`is a bash parameter expansion that returns the length of the variable 
* Much faster than `echo $str | wc -c` (which creates subshells and pipes)
#### Output:
![alt text](<Screenshot from 2025-11-21 11-52-28.png>)
#### 2.REVERSE STRING
##### EXPLANATION:
Explanation:
* `${str:$i:1}` extracts 1 character from position `$i` (string slicing)
* Loop runs from last character to first
* Alternative: `echo $str | rev` (if `rev` command is available).
#### Output:
![alt text](<Screenshot from 2025-11-21 12-03-04.png>)