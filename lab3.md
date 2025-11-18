## Experiment 3: Linux File Manipulation and System Manipulation I

### Name: Aditya Mishra  Roll No.: 590029219  Date: 2025-09-23

### Aim:

* To practice Linux file manipulation commands like `touch`, `cp`, `mv`, `rm`, `cat`, `less`, `head`, `tail`.
* To explore file permissions and ownership with `ls -l`, `chmod`, `chown`, and `chgrp`.
* To search and filter files using `find` and `grep`.
* To understand archiving and compression with `tar`, `gzip`, and `gunzip`.
* To create and manage links (`ln`) for both hard and symbolic links.

### Requirements

* A Linux machine with bash shell (Ubuntu/Fedora/other).
* User privileges to create, modify, and delete files and directories.
* Access to system utilities like `tar`, `gzip`, `grep`, and `find`.

## Theory

Linux file management involves creating, copying, moving, removing, and viewing files. File permissions and ownership ensure secure access control. Searching and filtering tools like `grep` and `find` help locate information efficiently. Archiving with `tar` and compression with `gzip` reduce storage usage and simplify file transfer. Links (`ln`) allow multiple references to the same file data (hard links) or path references (symbolic links).

## Procedure & Observations

## Exercise 1: Creating and Managing Files

### Task Statement:

Create files and manage timestamps using `touch`.

### Command(s):

```bash
touch newfile.txt
touch file1.txt file2.txt file3.txt
touch -t 202401151430 dated_file.txt
```

### Output:
<img width="903" height="76" alt="Screenshot 2025-11-15 221249" src="https://github.com/user-attachments/assets/05c09d62-face-47c7-8f96-1f4bea6d7fb5" />
<img width="946" height="216" alt="Screenshot 2025-11-15 221445" src="https://github.com/user-attachments/assets/7884c8be-82d3-4c9a-8de8-6baaa346adb1" />

---

## Exercise 2: Copying, Moving, and Deleting Files

### Task Statement:

Use `cp`, `mv`, and `rm` to copy, rename, move, and delete files and directories.

### Command(s):

```bash
cp document.txt backup_document.txt
mv oldname.txt newname.txt
rm unwanted_file.txt
rm -r old_directory/
```

### Output:

<img width="947" height="634" alt="Screenshot 2025-11-15 222237" src="https://github.com/user-attachments/assets/e6ade08a-e8bd-4650-a89f-c294d4b610b4" />


---

## Exercise 3: Viewing File Contents

### Task Statement:

Display file contents using `cat`, `less`, `head`, and `tail`.

### Command(s):

```bash
cat filename.txt
head -n 5 filename.txt
tail -n 20 filename.txt
```


### Output:

<img width="958" height="410" alt="Screenshot 2025-11-15 223822" src="https://github.com/user-attachments/assets/f7754a1a-8ce6-497f-87f9-71c1257b9070" />


---

## Exercise 4: File Permissions and Ownership

### Task Statement:

Explore file permissions and ownership with `ls -l`, `chmod`, `chown`, and `chgrp`.

### Command(s):

```bash
ls -l
chmod 755 script.sh
chmod u+x script.sh
```

### Output:

<img width="949" height="558" alt="Screenshot 2025-11-15 224140" src="https://github.com/user-attachments/assets/5bb2ebe7-02ef-4fb2-939f-eb84e4dace28" />


---

## Exercise 5: File Searching with `find`

### Task Statement:

Search files by name, type, size, and permissions using `find`.

### Command(s):

```bash
find /home -name "*.txt"
find /home -type f -size +100M
find /etc -name "*conf*"
find /tmp -type f -empty -delete
```

### Output:

<img width="957" height="1005" alt="Screenshot 2025-11-15 224551" src="https://github.com/user-attachments/assets/9a589fa2-719b-4c3b-a50f-0fd7cb3e0e62" />


---

## Exercise 6: Pattern Searching with `grep`

### Task Statement:

Search for patterns in files using `grep`.

### Command(s):

```bash
grep "error" /var/log/syslog
grep -i "Error" logfile.txt
grep -r "function" ~/code/
grep -n "TODO" *.txt
```

### Output:
<img width="952" height="1008" alt="Screenshot 2025-11-15 224945" src="https://github.com/user-attachments/assets/7cc510cf-91c7-42c8-a9a9-0726b5be2204" />


---

## Exercise 7: Archiving and Compression

### Task Statement:

Create and extract archives using `tar`, compress and decompress with `gzip`/`gunzip`.

### Command(s):

```bash
tar -czf backup.tar.gz /home/user/documents
tar -xzf backup.tar.gz -C /restore/
gzip largefile.txt
gunzip largefile.txt.gz
```

### Output:

<img width="945" height="766" alt="Screenshot 2025-11-15 225521" src="https://github.com/user-attachments/assets/5e325321-cfe3-4cfb-90d4-4b7fae3b68e7" />


---

## Exercise 8: Creating Links

### Task Statement:

Create and test hard and symbolic links using `ln`.

### Command(s):

```bash
echo "Hello" > original.txt
ln original.txt hardlink.txt
ln -s original.txt symlink.txt
ls -li original.txt hardlink.txt symlink.txt
```

### Output:

<img width="940" height="1011" alt="Screenshot 2025-11-15 225853" src="https://github.com/user-attachments/assets/7d6c5e2e-1ec9-4ade-9242-6c028ce6ecac" />


---

## Result

* Successfully created, copied, moved, and deleted files.
* Practiced viewing file contents and monitoring logs.
* Explored file permissions and ownership management.
* Used `find` and `grep` to locate and filter data.
* Created archives and compressed files.
* Demonstrated both hard and symbolic links.

## Challenges Faced & Learning Outcomes

* Challenge 1: Accidentally deleted files with `rm` without `-i`. Learned to use `rm -i` for safety.
* Challenge 2: Remembering numeric vs symbolic permissions in `chmod`. Fixed through repeated practice.

### Learning:

* Gained practical skills with file manipulation and permission commands.
* Learned how to efficiently search files and patterns in Linux.
* Understood how to archive and compress files for better storage management.
* Understood differences between hard and symbolic links.

## Conclusion

This experiment provided hands-on experience with core Linux file management, permissions, searching, archiving, and linking. These are foundational skills for effective Linux system administration and daily usage.
