# 📌 BACKUP



# ✅1.⁠ ⁠backup.sh Script
Create a new file named backup.sh inside your project folder:
<img width="739" height="321" alt="image" src="https://github.com/user-attachments/assets/e30007ad-f938-434a-9f47-a995f4491998" />



# ✅ 2. Make Script Executable
Run the following command once:

chmod 777 backup.sh

# ✅ 3. Testing the script
## 1. Create some samples .txt files:
<img width="750" height="49" alt="image" src="https://github.com/user-attachments/assets/99637ecb-8c87-4c17-a3e0-cc0bbb2a9b84" />

## 2. Run the script:

./backup.sh
<img width="753" height="82" alt="image" src="https://github.com/user-attachments/assets/13a716e7-e908-43d9-9194-dc2835c71ceb" />

## 3. Check the backup/folder:

ls backup/
<img width="754" height="63" alt="image" src="https://github.com/user-attachments/assets/794935ec-060e-4116-a2e0-0c2652b80b13" />


# 🔧 LAB4– File & Backup Automation

## Objective
Automate the backup of ⁠ .txt ⁠ files into a ⁠ backup/ ⁠ folder with timestamps in filenames.

---

## 🔧 Script Explanation

1.⁠ ⁠⁠ mkdir -p backup ⁠  
   Creates a folder n".

🔹 3. Using at (One-time Scheduling)
Run a script once at a specific time:

echo "/home/user/backup.sh" "
amed ⁠ backup ⁠ if it does not exist.

2.⁠ ⁠⁠ timestamp=$(date +"%Y%m%d_%H%M%S") ⁠  
   Generates a timestamp (format: YYYYMMDD_HHMMSS).

3.⁠ ⁠⁠ for file in *.txt; do ... done ⁠  
   Loops through all ⁠ .txt ⁠ files in the current directory.

4.⁠ ⁠⁠ basename "$file" .txt ⁠  
   Extracts the file name without extension.

5.⁠ ⁠⁠ cp "$file" "backup/${filename}_$timestamp.txt" ⁠  
   Copies the file into ⁠ backup/ ⁠ with the timestamp appended.

---

## 🔧 Example Run

### Input
Created two ⁠ .txt ⁠ files:

file1.txt
world.txt


### Command
./backup.sh


### Output
Files copied into ⁠ backup/ ⁠ with timestamps:

<img width="753" height="82" alt="image" src="https://github.com/user-attachments/assets/fcf7c6d6-b4b2-4dc7-a577-79cbd63f2be8" />

### 🛠️ Q1-What is the difference between cp,mv,and rsync?

     ans=cp-Copies files or directories
         rm-Moves or renames files or directories
         rsync-Synchronizes files/directories efficiently


### ✅ Q2-How can you schedule scripts to run automatically?
     
     ans=You can schedule scripts to run automatically using task schedulers built into your operating system.



### ✅ Q2-How can you schedule scripts to run automatically?
     
     ans=You can schedule scripts to run automatically using task schedulers built into your operating system.
