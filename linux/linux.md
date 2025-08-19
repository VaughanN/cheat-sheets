# Linux

## Keyboard shortcuts
### Search history
*command* + \<ctrl+r\>
E.g. `watch` + \<ctrl+r\>

*command* + \<PgUp\>
E.g. `watch` + \<PgUp\>
# Linux Command Cheat Sheet for Data Engineers and Analysts [source](https://dev.to/grayhat/the-ultimate-linux-command-cheat-sheet-for-data-engineers-and-analysts-570h)
### **1. Navigating the File System**

These are the basics you’ll use daily to move through directories and manage files:

- `pwd` – Print the current working directory.
- `ls` – List contents of a directory.
- `cd [dir]` – Change to a different directory.
- `mkdir [dir]` – Create a new directory.
- `rm [file/dir]` – Remove files or directories (`-r` for recursive).
- `cp [src] [dest]` – Copy files or directories.
- `mv [src] [dest]` – Move or rename files/directories.
- `touch [file]` – Create an empty file or update a timestamp.
- `cat [file]` – View file content.
- `head [file]` – View the first lines of a file.
- `tail [file]` – View the last lines of a file (use `-f` to monitor logs live).

---

### **2. Data Search & Manipulation**

Often you'll be digging through logs, config files, or large text files. These tools are essential:

- `grep 'pattern' [file]` – Search for patterns in files.
- `find [dir] -name 'filename'` – Search for files.
- `awk '{print $1}'` – Parse and process text line by line.
- `sed 's/old/new/g'` – Stream editor for replacing text.
- `cut -d',' -f2` – Cut specific fields from files (e.g., CSV).
- `sort` – Sort file content.
- `uniq` – Remove duplicates (use with `sort`).
- `wc -l [file]` – Count lines, words, characters.
- `diff [file1] [file2]` – Compare files line by line.
- `tee` – Redirect output to a file and the terminal.

---

### **3. System Monitoring & Performance**

Understanding system performance helps identify bottlenecks in pipelines and jobs:

- `top` – Real-time system resource usage.
- `ps aux` – List all running processes.
- `kill [PID]` – Terminate a process.
- `uptime` – Show system uptime and load.
- `df -h` – Disk space usage.
- `du -sh [dir]` – Directory size.
- `free -m` – Memory usage.
- `lsof` – List open files and related processes.
- `lscpu`, `lshw`, `lspci`, `lsusb` – Hardware inspection commands.

---

### **4. Networking Tools**

Crucial when pulling data from APIs or working with distributed systems:

- `ifconfig` / `ip a` – View and configure network interfaces.
- `ping [host]` – Test connectivity.
- `netstat -tulnp` – Network connections and listening ports.
- `nslookup [domain]` – DNS lookup.
- `ssh [user@host]` – Connect to remote servers.
- `scp [src] [user@host:dest]` – Secure file copy.
- `rsync -av [src] [dest]` – Efficient file synchronization.
- `curl [URL]` – Transfer data from/to a server.
- `wget [URL]` – Download files from the web.
- `iftop` – Monitor real-time bandwidth usage.
- `nc` – Lightweight networking tool (debugging, file transfers).

---

### **5. File Archiving & Compression**

Handling large datasets or transferring logs often requires compressing files:

- `tar -czf archive.tar.gz [files]` – Create a compressed tar archive.
- `tar -xzf archive.tar.gz` – Extract a tar.gz archive.
- `gzip [file]` / `gunzip [file.gz]` – Compress/decompress using gzip.
- `zip [archive.zip] [file]` / `unzip [archive.zip]` – Zip utilities.

---

### **6. Automation & Scheduling**

Data engineers automate tasks—these tools help manage that:

- `crontab -e` – Schedule scripts (e.g., ETL jobs).
- `nohup [command] &` – Run long processes immune to terminal closure.
- `alias ll='ls -alF'` – Create command shortcuts.
- `source script.sh` – Run a script in the current shell session.

---

### **7. Permissions & User Management**

Access control is critical when working in shared or production environments:

- `sudo [command]` – Run with admin privileges.
- `su [user]` – Switch user.
- `chmod 755 [file]` – Change file permissions.
- `chown user:group [file]` – Change ownership.
- `chgrp [group] [file]` – Change group ownership.
- `who` – Show logged-in users.

---

### **8. System Utilities**

Handy for general Linux system administration:

- `man [command]` – View command documentation.
- `which [command]` – Show command location.
- `history` – Show previously run commands.
- `date` – Display or set system time.
- `cal` – Calendar display.
- `shutdown now` / `reboot` / `halt` – Power control.
- `locate [file]` – Quickly find files.
- `updatedb` – Update database for `locate`.

#cheat-sheet