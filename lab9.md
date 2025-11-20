### EXPERIMENT 9
*************************************************************************
### SHELL PROGRAMMING CONTINUED AND SYSTEM PERFORMANCE MONITORING.
### ADITYA MISHRA , BATCH-78  , 590029219
### Q1: Write a script to find largest file in given directory.
### Step-by-Step Process
#### 1. Define the directory
```
Decide which directory you want to scan.
You can pass it as a script argument (recommended) or hard-code it.
```
#### 2. Validate the directory
~~~
Check whether the provided directory exists.
If it doesn’t, exit with an error.
~~~
#### 3. Traverse the directory
````
List all files (ignore subdirectories unless you want recursive search).
You may use:

os.listdir() (non-recursive)

os.walk() (recursive — scans all subfolders)
````
#### 4. Compare file sizes
````
For each file:

Build full path

Use os.path.getsize(path) to get file size

Track the largest file encountered
````

#### 5. Print the result
````
After scanning all files, output:

Largest file name

Full pathTTT

Size in bytes (or human-readable format)

````
### Script:
````
#!/bin/bash

# Check if a directory was provided
if [ -z "$1" ]; then
    echo "Usage: $0 /path/to/directory"
    exit 1
fi

DIR="$1"

# Find the largest file
largest=$(find "$DIR" -type f -printf "%s %p\n" 2>/dev/null | sort -nr | head -1)

if [ -z "$largest" ]; then
    echo "No files found in the specified directory."
    exit 1
fi

# Print result
size=$(echo "$largest" | awk '{print $1}')
file=$(echo "$largest" | cut -d' ' -f2-)

echo "--------------------------------------"
echo " Largest File in: $DIR"
echo "--------------------------------------"
echo "File: $file"
echo "Size: $size bytes"
echo "--------------------------------------"
````
#### Output:
![alt text](<Screenshot from 2025-11-20 11-41-34.png>)

### Q2:Create a script that counts how many .sh files exist in /home/user.
### STEP-BY-STEP PROCESS
#### STEP 1: Open the Terminal

```Press:

Ctrl + Alt + T


or open it from your application menu.
```
#### STEP 2: Create a new script file
```
Type:

nano count_sh_files.sh


This opens the nano text editor.
```
#### STEP 3: Paste the script inside nano
```
Copy and paste the following script:

#!/bin/bash

DIRECTORY="/home/user"

# Count .sh files
count=$(find "$DIRECTORY" -type f -name "*.sh" | wc -l)

echo "Number of .sh files in $DIRECTORY: $count"
```
#### STEP 4: Save the file in nano
```
Inside nano:

Press CTRL + O → writes the file

Press Enter → confirms the filename

Press CTRL + X → exits nano

Your script is now created.
```
#### STEP 5: Make the script executable
```
Run:

chmod +x count_sh_files.sh


This allows Linux to execute the script like a program.
```
#### STEP 6: Run the script
```
Now run:

./count_sh_files.sh


You will see output like:

Number of .sh files in /home/user: 5
```