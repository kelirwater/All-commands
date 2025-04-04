# Common Linux Commands

## File and Directory Operations

- `ls` : List directory contents
- `cd [dir]` : Change directory
- `pwd` : Print working directory
- `mkdir [dir]` : Create a new directory
- `rmdir [dir]` : Remove empty directory
- `rm [file]` : Remove a file
- `rm -r [dir]` : Remove a directory and its contents
- `cp [source] [destination]` : Copy files or directories
- `mv [source] [destination]` : Move or rename files or directories
- `touch [file]` : Create an empty file or update timestamp
- `find [path] -name [name]` : Search for files by name

## File Permissions

- `chmod [permissions] [file]` : Change file permissions
- `chown [user]:[group] [file]` : Change file owner and group
- `ls -l` : List files with detailed information (including permissions)

## File Viewing and Editing

- `cat [file]` : View file content
- `less [file]` : View file content page by page
- `head [file]` : View the first 10 lines of a file
- `tail [file]` : View the last 10 lines of a file
- `nano [file]` : Open a file in the Nano text editor
- `vim [file]` : Open a file in the Vim text editor

## System Information

- `top` : Display system processes and resource usage
- `htop` : Interactive process viewer (requires installation)
- `df` : Show disk space usage
- `free` : Show memory usage
- `uname -r` : Show kernel version
- `hostname` : Display or set the system hostname
- `uptime` : Show system uptime and load averages
- `ps` : Display current processes
- `dmesg` : Print kernel ring buffer messages

## Package Management (Debian/Ubuntu)

- `sudo apt update` : Update package list
- `sudo apt upgrade` : Upgrade installed packages
- `sudo apt install [package]` : Install a package
- `sudo apt remove [package]` : Remove a package
- `sudo apt search [package]` : Search for a package

## Network Commands

- `ping [host]` : Test network connection to a host
- `ifconfig` : Display or configure network interfaces
- `ip a` : Display network interfaces (modern alternative to ifconfig)
- `netstat` : Display network connections, routing tables, etc.
- `ssh [user]@[host]` : Connect to a remote server via SSH
- `scp [source] [user]@[host]:[destination]` : Copy files between hosts over SSH

## Disk Operations

- `lsblk` : List block devices
- `fdisk -l` : List partitions on disks
- `mount [device] [mount-point]` : Mount a filesystem
- `umount [mount-point]` : Unmount a filesystem
- `fsck [device]` : Check and repair a filesystem

## Searching Files and Content

- `grep [pattern] [file]` : Search for a pattern in a file
- `grep -r [pattern] [dir]` : Search for a pattern recursively in a directory
- `find [dir] -name [filename]` : Find files by name

## Compression and Archiving

- `tar -cvf [archive.tar] [dir]` : Create a tar archive
- `tar -xvf [archive.tar]` : Extract a tar archive
- `gzip [file]` : Compress a file using gzip
- `gunzip [file.gz]` : Decompress a file using gzip
- `zip [archive.zip] [file]` : Create a zip archive
- `unzip [archive.zip]` : Extract a zip archive

## System Shutdown and Reboot

- `shutdown -h now` : Shutdown the system immediately
- `reboot` : Reboot the system
- `poweroff` : Turn off the system

## User Management

- `adduser [username]` : Add a new user
- `passwd [username]` : Change user password
- `userdel [username]` : Delete a user
- `usermod -aG [group] [user]` : Add a user to a group

# Common Linux Commands with Examples

## File and Directory Operations

# Linux Commands Cheat Sheet

## File Management

- `ls` - List files in a directory
  - Example: `ls -l` (detailed list with permissions)
- `cd <directory>` - Change directory
  - Example: `cd /home/user`
- `pwd` - Print working directory
  - Example: `pwd`
- `mkdir <directory>` - Create a new directory
  - Example: `mkdir new_folder`
- `rm <file>` - Remove a file
  - Example: `rm file.txt`
- `rm -r <directory>` - Remove a directory and its contents
  - Example: `rm -r old_folder`
- `cp -r <source> <destination>` - Copy files or directories
  - Example: `cp -r file1.txt backup/`
- `mv <source> <destination>` - Move or rename files
  - Example: `mv oldname.txt newname.txt`
- `touch <file>` - Create a new empty file
  - Example: `touch newfile.txt`

## Writing to Files

- `echo "text" > <file>` - Write text to a file (overwrites existing content)
  - Example: `echo "Hello, Linux!" > myfile.txt`
- `echo "text" >> <file>` - Append text to a file
  - Example: `echo "This is a new line" >> myfile.txt`
- `cat > <file>` - Create a new file and write content interactively (Ctrl+D to save)
  - Example: `cat > newfile.txt` (then type content and press Ctrl+D)
- `tee <file>` - Write to a file and display the output
  - Example: `echo "Hello" | tee output.txt`
- `nano <file>` - Open a file in a text editor
  - Example: `nano notes.txt`
- `vim <file>` - Open a file in Vim editor

  - Example: `vim script.sh`

  ## Vim Editor

  # How to Exit Vim

To exit Vim (the Vim editor), you have several options, depending on whether you want to save your changes or not. Here are the most common commands:

### Exit without saving changes:

1. Press `Esc` to make sure you're not in insert mode.
2. Type `:q!` and press `Enter`.

### Save and exit:

1. Press `Esc` to make sure you're not in insert mode.
2. Type `:wq` and press `Enter`.

### Exit (if no changes have been made):

1. Press `Esc` to make sure you're not in insert mode.
2. Type `:q` and press `Enter`.

### Save (but stay in Vim):

1. Press `Esc` to make sure you're not in insert mode.
2. Type `:w` and press `Enter`.

---

Let me know if you're trying to do something specific with Vim!

## File Permissions

- `chmod <mode> <file>` - Change file permissions
  - Example: `chmod 755 script.sh`
- `chown <owner>:<group> <file>` - Change file owner and group
  - Example: `chown user:group file.txt`
- `ls -l` - View file permissions
  - Example: `ls -l file.txt`
  - `ls -la` - list content of a directory
  - Example: `ls -la`

## Process Management

- `ps aux` - Display active processes
  - Example: `ps aux | grep apache`
- `top` - Show real-time process monitoring
  - Example: `top`
- `kill <PID>` - Terminate a process by PID
  - Example: `kill 1234`
- `pkill <name>` - Terminate a process by name
  - Example: `pkill firefox`
- `htop` - Interactive process viewer (if installed)
  - Example: `htop`

## Networking

- `ping <host>` - Check connectivity to a host
  - Example: `ping google.com`
- `curl <URL>` - Fetch a webpage or API data
  - Example: `curl https://example.com`
- `wget <URL>` - Download a file from the internet
  - Example: `wget https://example.com/file.zip`
- `netstat -tulnp` - Show active network connections
  - Example: `netstat -tulnp`
- `ip a` - Show network interfaces and IP addresses
  - Example: `ip a`

## System Monitoring

- `df -h` - Show disk space usage
  - Example: `df -h`
- `du -sh <directory>` - Show size of a directory
  - Example: `du -sh /var/log`
- `free -m` - Show memory usage
  - Example: `free -m`
- `uptime` - Show system uptime
  - Example: `uptime`
- `who` - Show who is logged in
  - Example: `who`
- `uname -a` - Show system information
  - Example: `uname -a`

## Package Management

### Debian-based (Ubuntu, Debian)

- `apt update` - Update package lists
  - Example: `sudo apt update`
- `apt upgrade` - Upgrade installed packages
  - Example: `sudo apt upgrade`
- `apt install <package>` - Install a package
  - Example: `sudo apt install vim`
- `apt remove <package>` - Remove a package
  - Example: `sudo apt remove vim`

### Red Hat-based (Fedora, CentOS)

- `dnf update` - Update system packages
  - Example: `sudo dnf update`
- `dnf install <package>` - Install a package
  - Example: `sudo dnf install nano`
- `dnf remove <package>` - Remove a package
  - Example: `sudo dnf remove nano`

## User Management

- `whoami` - Show current user
  - Example: `whoami`
- `id` - Show user ID (UID) and group ID (GID)
  - Example: `id`
- `adduser <username>` - Add a new user
  - Example: `sudo adduser newuser`
- `passwd <username>` - Change user password
  - Example: `sudo passwd newuser`
- `deluser <username>` - Delete a user
  - Example: `sudo deluser newuser`

## Miscellaneous

- `echo "Hello World"` - Print text to terminal
  - Example: `echo "Hello Linux"`
- `cat <file>` - Display file contents
  - Example: `cat notes.txt`
- `grep "pattern" <file>` - Search for a pattern in a file
  - Example: `grep "error" log.txt`
- `history` - Show command history
  - Example: `history`
- `clear` - Clear terminal screen
  - Example: `clear`
- `alias ll='ls -la'` - Create an alias
  - Example: `alias ll='ls -la'`

## Scripting

- `bash <script>.sh` - Execute a bash script
  - Example: `bash myscript.sh`
- `chmod +x <script>.sh` - Make script executable
  - Example: `chmod +x myscript.sh
