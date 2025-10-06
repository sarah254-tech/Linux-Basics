# Linux-Basics
This repository is my personal Linux learning log and cheat sheet. It contains simple notes, commands, and examples that I'm practicing while learning the Linux operating system.

The goal is to keep everything short, clear, and easy to reference, like a quick guide for students and beginners.

## Goals
- Learn basic terminal commands
- Write shell scripts
- Configure a web server
- Document progress and commands

## How I work
Each day I create a short log entry under `logs/` with the date and what I practiced.

## Quick commands used
- `sudo apt update && sudo apt upgrade`
- `git clone <repo>`
- `ssh user@host`
- `nano|vim|code .`

## Progress
- 2025-10-02: Created repo, set up VM, installed VS Code.


# Linux Learning Lab

## 🌍 What is Linux?
Linux is an open-source operating system that powers most of the world’s servers, cloud systems, and even Android phones. Unlike Windows or macOS, Linux is free, customizable, and heavily used in software engineering, DevOps, cybersecurity, and system administration.  

It’s built around the **Linux kernel**, which controls the hardware, and comes in many distributions (like Ubuntu, CentOS, Fedora, and Debian).  



## 🔧 Uses of Linux OS
Linux is widely used because of its stability, flexibility, and security. Some common uses are:
- **Servers & Cloud**: Powers websites, databases, and cloud platforms (AWS, Google Cloud, Azure).  
- **Software Development**: Programming, DevOps pipelines, and automation.  
- **Cybersecurity & Networking**: Used in penetration testing (Kali Linux) and firewalls.  
- **Embedded Systems**: Runs on devices like routers, smart TVs, and IoT gadgets.  
- **Everyday Computing**: Desktop distributions like Ubuntu for personal use.  
- **Mobile**: Android is built on the Linux kernel.  



## 🏗️ Components of Linux and Their Functions
1. **Kernel** → The core of Linux, manages hardware, processes, memory, and devices.  
2. **Shell** → Command-line interpreter (e.g., Bash, Zsh) that lets users communicate with the kernel.  
3. **File System** → Organizes data in directories and files (everything in Linux is treated as a file).  
4. **System Libraries** → Provide standard functions for programs (like `glibc`).  
5. **System Utilities** → Basic tools (like `ls`, `cp`, `mv`) to manage the system.  
6. **Applications** → Software installed on Linux (like VS Code, browsers, servers).  



# 📖 Linux Command Cheat Sheet (DevOps Focus)

Here are the most widely used Linux commands, grouped into 11 categories:


### ========================
### 1. SYSTEM INFORMATION
### ========================
`uname -a`        # Show system and kernel

`hostname`        # Show system hostname

`uptime`          # Show system uptime

`df -h`           # Disk usage

`free -m`         # Memory usage

`top`             # Running processes

### ========================
### 2. NAVIGATION
### ========================
`pwd`             # Print working directory

`ls`              # List files

`cd /path`        # Change directory

`cd ..`           # Go up one directory

`tree`            # Show directories as a tree

### ========================
### 3. FILE OPERATIONS
### ========================
`touch file.txt`             # Create a new file

`cat file.txt`                # Show file content

`cp file.txt backup.txt`      # Copy file

`mv file.txt /tmp/ `          # Move file

`rm file.txt`                 # Remove file

### ========================
### 4. FILE PERMISSIONS
### ========================
`ls -l`                       # List permissions

`chmod 755 file.txt`          # Change permissions

`chown user:group file.txt`   # Change owner

`umask`                       # Show default permissions

### ========================
### 5. USER & GROUP MANAGEMENT
### ========================
`whoami`                      # Current user

`id`                          # Show user/group IDs

`adduser newuser`            # Add a new user

`passwd newuser`              # Set user password

`groups`                     # Show groups

### ========================
### 6. TEXT PROCESSING
### ========================
`cat file.txt `               # View file content

`less file.txt `              # Scroll through file

`grep "word" file.txt`        # Search text in file

`sort file.txt `              # Sort file content

`wc -l file.txt `             # Count lines in file


#### ========================
### 7. PROCESS MANAGEMENT
### ========================
`ps aux`                      # Show running processes

`top`                         # Monitor processes

`kill -9 PID`                # Kill a process

`jobs`                        # Show background jobs

`fg `                         # Bring job to foreground

### ========================
### 8. PACKAGE MANAGEMENT (Ubuntu/Debian)
### ========================
`sudo apt update `            # Update package list

`sudo apt upgrade `           # Upgrade packages

`sudo apt install pkg`        # Install package

`sudo apt remove pkg`        # Remove package

`dpkg -l`                     # List installed packages

### ========================
### 9. NETWORKING
### ========================
`ping google.com `            # Test connectivity

`ifconfig `                   # Show network interfaces

`ip addr show `              # Show IP addresses

`netstat -tuln `              # Show open ports

`curl http://example.com `    # Fetch URL

### ========================
### 10. COMPRESSION & ARCHIVING
### ========================
`tar -cvf archive.tar files/` # Create tar archive

`tar -xvf archive.tar`        # Extract tar archive

`gzip file.txt `              # Compress file

`gunzip file.txt.gz `         # Decompress file

### ========================
### 11. SYSTEM CONTROL
### ========================
`shutdown -h now `            # Shutdown immediately

`reboot`                      # Reboot system

`systemctl status service`    # Show service status

`systemctl start service `    # Start service

`systemctl stop service `     # Stop service


## 🗂️ Linux File System Hierarchy — Study Summary

The **Linux File System Hierarchy** defines how files and directories are organized on a Linux system.  
Everything in Linux is treated as a **file** — even hardware devices and processes.

At the top of the structure is the **root directory `/`**, which contains all other files and folders in a tree-like structure.



###  Top-Level Directories

| Directory | Description |
|------------|-------------|
| `/` | The **root directory** — everything starts here. It’s the base of the Linux file system tree. |
| `/bin` | Essential **user binaries** (programs) needed for the system to boot and run, such as `ls`, `cp`, `mv`, `cat`. |
| `/boot` | Contains files required for **booting the system**, including the Linux kernel (`vmlinuz`) and bootloader configuration (`grub`). |
| `/dev` | Contains **device files** — these represent hardware devices like disks (`/dev/sda`), terminals, and USBs. |
| `/etc` | System-wide **configuration files** for software and services. Example: `/etc/passwd`, `/etc/hosts`. |
| `/home` | Each user’s **personal directory**. Example: `/home/sarah` stores personal files, downloads, and configs. |
| `/lib`, `/lib64` | Essential **shared libraries** needed by system programs and the kernel. Similar to DLL files in Windows. |
| `/media` | Used to **mount external drives** (USBs, CDs, DVDs) automatically. |
| `/mnt` | A **temporary mount point** for manually mounted devices or partitions. |
| `/opt` | Used for **optional or third-party software** (e.g., apps installed outside the package manager). |
| `/proc` | A **virtual directory** that provides information about system and process status in real-time. Example: `/proc/cpuinfo`. |
| `/root` | The **home directory for the root (admin) user** — different from `/`. |
| `/run` | Stores **runtime data** like system information since boot. |
| `/sbin` | System binaries used by the **root user** for administrative tasks (e.g., `ifconfig`, `reboot`). |
| `/srv` | Contains **service data** for servers like FTP, HTTP, and databases. |
| `/sys` | Provides system and device information — used by the kernel and hardware drivers. |
| `/tmp` | Temporary files created by users or processes. Cleared after reboot. |
| `/usr` | Stands for **Unix System Resources**. Contains user programs, libraries, documentation, and utilities. |
| `/var` | Holds **variable data** like logs, emails, databases, and caches. Example: `/var/log/syslog`. |



### 🧩 Simplified Analogy

Think of Linux like a **house**:

| Linux Directory | Analogy |
|------------------|---------|
| `/` | 🏠 The entire property (foundation) |
| `/home` | 🛏️ Your personal bedroom |
| `/etc` | ⚙️ The control panel (settings) |
| `/bin` | 🧰 Everyday tools |
| `/var/log` | 📹 CCTV recordings (system logs) |
| `/dev` | 🔌 Electrical wiring and plumbing (hardware) |



### 🌲 Linux Directory Structure Diagram

/  
├── **bin/** → Essential user binaries  
├── **boot/** → Bootloader and kernel files  
├── **dev/** → Device files  
├── **etc/** → System configuration files  
├── **home/** → User home directories  
│&nbsp;&nbsp;&nbsp;&nbsp;├── sarah/  
│&nbsp;&nbsp;&nbsp;&nbsp;└── guest/  
├── **lib/** → Shared libraries  
├── **media/** → Removable media  
├── **mnt/** → Temporary mount point  
├── **opt/** → Optional software  
├── **proc/** → Kernel and process info  
├── **root/** → Root user's home directory  
├── **run/** → Runtime data  
├── **sbin/** → System binaries for root  
├── **srv/** → Service data (web, FTP, etc.)  
├── **sys/** → Kernel and hardware information  
├── **tmp/** → Temporary files  
├── **usr/** → User programs, documentation, and libraries  
│&nbsp;&nbsp;&nbsp;&nbsp;├── bin/  
│&nbsp;&nbsp;&nbsp;&nbsp;├── lib/  
│&nbsp;&nbsp;&nbsp;&nbsp;└── share/  
└── **var/** → Logs, mail, cache, and databases




### 🔍 Key Notes

- The **root (`/`) directory** is not the same as `/root`.  
  - `/` is the entire system’s top level.  
  - `/root` is the root user’s personal directory.  
- Linux is **case-sensitive**: `/Home` ≠ `/home`.  
- Use **absolute paths** (`/etc/passwd`) for system operations.  
- Access rights are controlled by **permissions and ownership**.

---

### 🧠 Quick Recap

| Concept | Summary |
|----------|----------|
| Everything is a file | Devices, directories, and data are treated the same way. |
| Hierarchical structure | Starts from `/` and branches into subdirectories. |
| Organized by purpose | Each directory has a defined function. |
| Root privileges | Only the root user can modify system-level files. |

---

### 🧪 Practice Commands

```bash
# List directories under root
ls /

# View contents of /etc
ls -l /etc

# Check your current directory
pwd

# Move into a directory
cd /home

# Move one level up
cd ..



