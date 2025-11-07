## Experiment 7: Shell Programming, Process and Scheduling

### Name: Aditya Mishra  Roll No.: 590029219  Date: 2025-09-23

### Aim:

* To write shell scripts that demonstrate process management.
* To understand how to schedule processes using `cron` and `at`.
* To monitor running processes and practice job control commands.

### Requirements

* A Linux machine with bash shell.
* Access to process management commands (`ps`, `top`, `kill`, `jobs`, `fg`, `bg`).
* Access to scheduling utilities (`cron`, `at`).

## Theory

Every program running in Linux is a process identified by a unique process ID (PID). Shell programming allows automation of tasks including spawning and controlling processes. Process management commands like `ps`, `top`, `kill`, `jobs`, `bg`, and `fg` let users monitor and control execution. Scheduling utilities such as `cron` (repeated tasks) and `at` (one-time tasks) allow tasks to run automatically at defined times. Combining scripting with scheduling is a core system administration skill.

## Procedure & Observations

## Task 1 

### Task Statement:

Write a script that monitors the top 5 processes consuming the most CPU and logs them into a file every 10 seconds.

### Command(s):

```bash
for i in {0..5}; do
    echo "LOG on $(date)" >> output.txt
    ps -eo pid,comm,%cpu --sort=-%cpu | head -6 >> output.txt
    echo "------------------------------------------" >> output.txt
    sleep 10
done

```

### Output:
<img width="947" height="1018" alt="Screenshot 2025-11-07 141652" src="https://github.com/user-attachments/assets/36e8da9e-7c39-4603-9f9c-5577ded6fe04" />
<img width="950" height="961" alt="Screenshot 2025-11-07 141718" src="https://github.com/user-attachments/assets/40e82755-4d54-409d-a8b2-298e052f59ad" />
<img width="942" height="200" alt="Screenshot 2025-11-07 141737" src="https://github.com/user-attachments/assets/9f438f92-1908-4dac-b26f-119a348cda23" />


---

## Task 2

### Task Statement:

Write a script that accepts a PID from the user and displays its details (state, parent process, memory usage).

### Command(s):

```bash
#!/bin/bash

read -p "Enter the PID of the process: " pid

echo "Details for PID $pid:"
ps -p "$pid" -o pid,ppid,state,comm,%mem,%cpu

```

### Output:

<img width="948" height="363" alt="Screenshot 2025-11-07 142337" src="https://github.com/user-attachments/assets/0da81602-0435-42d9-875a-78d771880926" />


---

## Task 3

### Task Statement: 

Create a script that schedules a task to append the current date and time to a log file every minute using cron.



### Command(s):

```bash
#!/bin/bash
echo "$(date)" >> time_log.txt

```
```
crontab -e

* * * * * ~/log_time.sh
```


### Output:

<img width="948" height="632" alt="Screenshot 2025-11-07 142709" src="https://github.com/user-attachments/assets/ff736165-6a97-457a-9e26-35fb862b5f3c" />
<img width="931" height="621" alt="Screenshot 2025-11-07 142600" src="https://github.com/user-attachments/assets/17be519d-a83d-40d0-b3e6-f91432fb64af" />


---

## Task 4:

### Task Statement:
Modify the factorial function to check if input is negative. If yes, display an error message.

### Command(s):

```bash
#!/bin/bash

factorial() {
    local n=$1


    if [ $n -lt 0 ]; then
        echo "Error: Factorial is not defined for negative numbers."
        return 1
    fi

    local fact=1
    for (( i=1; i<=n; i++ )); do
        fact=$((fact * i))
    done
    echo "Factorial of $n is $fact"
}


read -p "Enter a number: " num
factorial $num

```

### Output:

<img width="944" height="299" alt="Screenshot 2025-11-07 143003" src="https://github.com/user-attachments/assets/29b6ad01-7508-4360-afa5-d04cb9e66150" />


---

## Task 5:

### Task Statement:

Schedule a script to run every day at 7:00 AM using `cron`.

### Command(s):

```bash
#!/bin/bash
echo "Script ran at $(date)" >> ~/daily_log.txt
```

```bash
crontab -e
0 7 * * * ~/my_script.sh
```

### Output:

<img width="952" height="635" alt="Screenshot 2025-11-07 143215" src="https://github.com/user-attachments/assets/39735d7f-8d43-42a9-b958-a7b84634b832" />


---



## Result

* Learned to create and run shell scripts.
* Managed processes using background, foreground, and kill commands.
* Monitored processes with `ps` and `top`.
* Scheduled recurring tasks with `cron` and one-time tasks with `at`.

## Challenges Faced & Learning Outcomes

* Challenge 1: Remembering the `crontab` time format. Solved by using online crontab generators and practice.
* Challenge 2: Ensuring `atd` service is running for `at` command. Fixed by starting the service with `systemctl start atd`.

### Learning:

* Gained hands-on knowledge of process creation and termination.
* Learned job control and scheduling using `cron` and `at`.

## Conclusion

This experiment provided practical experience with shell scripting, process management, and scheduling. These are critical skills for system administrators to automate and control Linux environments effectively.
