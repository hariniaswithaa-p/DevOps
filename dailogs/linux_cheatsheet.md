# 30 Basic Linux Commands

A quick-reference guide to essential Linux commands. Each entry has the command, a one-line explanation, and an example.

## Navigation

### 1. `pwd`
Prints the full path of the directory you are currently in.
```bash
pwd
```

### 2. `ls`
Lists files and folders in a directory (`-l` for details, `-a` to show hidden files).
```bash
ls -la
```

### 3. `cd`
Changes your current directory to another one.
```bash
cd /var/log
```

## Files and Directories

### 4. `mkdir`
Creates a new directory (`-p` creates parent folders too).
```bash
mkdir -p projects/devops/demo
```

### 5. `touch`
Creates an empty file or updates the timestamp of an existing one.
```bash
touch notes.txt
```

### 6. `cp`
Copies files or directories (`-r` for directories).
```bash
cp notes.txt backup_notes.txt
```

### 7. `mv`
Moves or renames a file or directory.
```bash
mv notes.txt documents/notes_old.txt
```

### 8. `rm`
Deletes files or directories (`-r` for directories; be careful, there is no recycle bin).
```bash
rm -r old_folder
```

### 9. `rmdir`
Removes an empty directory only.
```bash
rmdir empty_folder
```

### 10. `ln`
Creates a link to a file (`-s` creates a symbolic/shortcut link).
```bash
ln -s /var/log/syslog mylog
```

## Viewing File Content

### 11. `cat`
Displays the entire content of a file in the terminal.
```bash
cat notes.txt
```

### 12. `less`
Opens a file page by page so you can scroll through large files (press `q` to quit).
```bash
less /var/log/syslog
```

### 13. `head`
Shows the first 10 lines of a file (use `-n` to change the count).
```bash
head -n 5 notes.txt
```

### 14. `tail`
Shows the last lines of a file (`-f` follows new lines live, great for logs).
```bash
tail -f /var/log/syslog
```

### 15. `echo`
Prints text to the terminal or writes it into a file using `>`.
```bash
echo "Hello Linux" > hello.txt
```

## Searching

### 16. `grep`
Searches for a word or pattern inside files.
```bash
grep -i "error" /var/log/syslog
```

### 17. `find`
Searches for files and directories by name, type, or size.
```bash
find /home -name "*.txt"
```

### 18. `wc`
Counts lines, words, and characters in a file.
```bash
wc -l notes.txt
```

## Permissions and Ownership

### 19. `chmod`
Changes who can read, write, or execute a file.
```bash
chmod 755 script.sh
```

### 20. `chown`
Changes the owner and group of a file or directory.
```bash
sudo chown ubuntu:ubuntu notes.txt
```

### 21. `sudo`
Runs a command with administrator (root) privileges.
```bash
sudo apt update
```

### 22. `whoami`
Shows the username of the user you are logged in as.
```bash
whoami
```

## System Information and Processes

### 23. `uname`
Displays system information such as the kernel name and version (`-a` for all).
```bash
uname -a
```

### 24. `df`
Shows disk space usage of mounted file systems (`-h` for human-readable sizes).
```bash
df -h
```

### 25. `free`
Shows how much RAM is used and available.
```bash
free -h
```

### 26. `ps`
Lists the processes currently running on the system.
```bash
ps aux
```

### 27. `top`
Shows live, continuously updating CPU and memory usage of processes (press `q` to quit).
```bash
top
```

### 28. `kill`
Stops a running process using its process ID (PID).
```bash
kill 1234
```

## Software and Networking

### 29. `apt`
Installs, updates, and removes software on Ubuntu/Debian systems.
```bash
sudo apt install git
```

### 30. `ping`
Checks if another machine or website is reachable over the network (`-c` limits the packet count).
```bash
ping -c 4 google.com
```

---

## Bonus Tip

Use `man <command>` to open the manual page of any command, for example:
```bash
man ls
```
