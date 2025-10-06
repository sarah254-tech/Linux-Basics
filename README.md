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


Tips: 
#Practice Commands
List directories under root
ls /

 View contents of /etc
ls -l /etc

Check your current directory
pwd

Move into a directory
cd /home

Move one level up
cd ..

## 📝 Linux Text Editors — Study Summary

Text editors are essential tools in Linux for **creating and modifying text files**, such as configuration files, scripts, and code.  
They can be **command-line based** (terminal editors) or **graphical** (GUI editors).



### 🧭 Categories of Text Editors

| Type | Description | Examples |
|------|--------------|-----------|
| **Command-Line Editors** | Run inside the terminal. Ideal for servers and system admins. | `vi`, `vim`, `nano`, `emacs` |
| **Graphical Editors** | Run in desktop environments with menus and mouse support. | `gedit`, `kate`, `sublime-text`, `visual-studio-code` |



### 💻 Common Linux Command-Line Editors

#### 🟢 1. `nano`
A beginner-friendly editor available by default in most Linux distributions.

**Usage:**

nano filename.txt

| Key        | Function    |
| ---------- | ----------- |
| `Ctrl + O` | Save file   |
| `Ctrl + X` | Exit editor |
| `Ctrl + K` | Cut text    |
| `Ctrl + U` | Paste text  |
| `Ctrl + W` | Search text |

🔵 2. vi (or vim)

A powerful and popular editor among developers and system admins.

vi filename.txt

Modes in vi/vim:
| Mode               | Description                                                          |
| ------------------ | -------------------------------------------------------------------- |
| **Command Mode**   | Default mode for navigation and issuing commands.                    |
| **Insert Mode**    | Allows typing and editing text. Enter using `i`.                     |
| **Last-Line Mode** | Used for saving, quitting, or executing commands (triggered by `:`). |

Common Commands:
| Command | Function               |
| ------- | ---------------------- |
| `i`     | Enter insert mode      |
| `Esc`   | Return to command mode |
| `:w`    | Save changes           |
| `:q`    | Quit editor            |
| `:wq`   | Save and quit          |
| `:q!`   | Quit without saving    |
| `/text` | Search for “text”      |

🟣 3. emacs

A highly customizable and extensible editor with both command-line and GUI modes.

emacs filename.txt

Basic Shortcuts:
| Key                  | Function       |
| -------------------- | -------------- |
| `Ctrl + X, Ctrl + S` | Save file      |
| `Ctrl + X, Ctrl + C` | Exit editor    |
| `Ctrl + K`           | Cut line       |
| `Ctrl + Y`           | Paste line     |
| `Ctrl + S`           | Search forward |

🖥️ Graphical Editors (GUI)

GUI text editors are user-friendly and ideal for coding or editing multiple files visually.

| Editor           | Description                                   | Command to Install (Ubuntu/Debian)         |
| ---------------- | --------------------------------------------- | ------------------------------------------ |
| **gedit**        | Default GNOME editor; simple and easy to use. | `sudo apt install gedit`                   |
| **kate**         | KDE advanced text editor.                     | `sudo apt install kate`                    |
| **Sublime Text** | Fast, modern editor with rich plugins.        | `sudo snap install sublime-text --classic` |
| **VS Code**      | Popular cross-platform editor by Microsoft.   | `sudo snap install code --classic`         |



# 🔐 Linux File Permissions and Ownership

In Linux, **file permissions and ownership** control **who can read, write, or execute** a file or directory.  
This security model ensures that users and processes can only access what they are allowed to.

---

### 🧭 The Three Permission Types

| Permission | Symbol | Description | Example |
|-------------|----------|-------------|----------|
| **Read** | `r` | View file contents or list directory contents. | `cat file.txt` |
| **Write** | `w` | Modify file contents or add/delete files in a directory. | `nano file.txt` |
| **Execute** | `x` | Run files (programs/scripts) or enter directories. | `./script.sh` |

---

### 👥 File Ownership in Linux

Each file or directory in Linux has **three types of owners:**

| Owner Type | Description |
|-------------|--------------|
| **User (u)** | The person who created the file. |
| **Group (g)** | A set of users with shared access. |
| **Others (o)** | Everyone else on the system. |

You can view ownership and permissions using:

ls -l

Example Output:

-rwxr-xr--  1 sarah devops  2450 Oct 6 10:20 script.sh

Breakdown:
| Section  | Meaning                                         |
| -------- | ----------------------------------------------- |
| `-`      | File type (`-` = file, `d` = directory)         |
| `rwx`    | Permissions for **user** (read, write, execute) |
| `r-x`    | Permissions for **group** (read, execute)       |
| `r--`    | Permissions for **others** (read only)          |
| `sarah`  | File owner                                      |
| `devops` | Group owner                                     |

🔢 Numeric (Octal) Representation
Permissions can also be expressed as numbers (0–7), known as octal notation.

| Number | Permission | Binary | Meaning                |
| ------ | ---------- | ------ | ---------------------- |
| `0`    | ---        | 000    | No permissions         |
| `1`    | --x        | 001    | Execute only           |
| `2`    | -w-        | 010    | Write only             |
| `3`    | -wx        | 011    | Write + Execute        |
| `4`    | r--        | 100    | Read only              |
| `5`    | r-x        | 101    | Read + Execute         |
| `6`    | rw-        | 110    | Read + Write           |
| `7`    | rwx        | 111    | Read + Write + Execute |

so:
`chmod 755 file.sh` → User: `rwx`, Group: `r-x`, Others: `r-x`

`chmod 644 file.txt` → User: `rw`-, Group: `r--`, Others: `r--`

# ⚙️ Managing Permissions

## 1. Change permissions with chmod
### Add execute permission for user
`chmod u+x script.sh`

### Remove write permission for group
`chmod g-w notes.txt`

### Give read permission to everyone
`chmod a+r data.log`

### Set numeric permissions (User=7, Group=5, Others=5)
`chmod 755 script.sh`

## 2. Change ownership with chown
### Change owner of a file
`sudo chown sarah file.txt`

### Change owner and group
`sudo chown sarah:devops file.`txt`

### Change ownership recursively in a directory
`sudo chown -R sarah:devops /project`

## 3. Change group with 

`sudo chgrp developers report.txt`

### 📂 File Type Indicators (from ls -l)

| Symbol | Type             | Example      |
| ------ | ---------------- | ------------ |
| `-`    | Regular file     | `-rw-r--r--` |
| `d`    | Directory        | `drwxr-xr-x` |
| `l`    | Symbolic link    | `lrwxrwxrwx` |
| `b`    | Block device     | `brw-rw----` |
| `c`    | Character device | `crw-rw----` |
| `p`    | Named pipe       | `prw-r--r--` |
| `s`    | Socket           | `srwxr-xr-x` |

🧩 Practical Examples

### View permissions and ownership
ls -l

### Make a script executable
chmod +x deploy.sh

### Give group write permission
chmod g+w report.txt

### Change file ownership to 'sarah'
sudo chown sarah script.sh

Quick Recap
| Concept                                             | Description |
| --------------------------------------------------- | ----------- |
| **Read (r)** → View files or directories.           |             |
| **Write (w)** → Modify files or directory contents. |             |
| **Execute (x)** → Run scripts or enter directories. |             |
| **chmod** → Change permissions.                     |             |
| **chown / chgrp** → Change ownership and groups.    |             |
| **ls -l** → View permission and ownership details.  |             |

###  Practice Commands
Create a sample file
touch test.sh

### Check permissions
ls -l test.sh

### Give user full rights, others read-only
chmod 744 test.sh

### Assign to a group
sudo chown $USER:devops test.sh


# Tip
When setting permissions, always follow the principle of least privilege 
give users only the access they truly need to keep your system secure.


##### Always check if an editor is installed

`which vim`
`which nano`

##### To install any missing editor

`sudo apt install vim `  # or nano, gedit, emacs, kate

#### You can set yur preferred editor using

`export EDITOR=vim`


# 🔐 Access Control Lists (ACL) in Linux

In Linux, **Access Control Lists (ACLs)** give you *superpowers* over file permissions!  
They allow you to go **beyond the basic `rwx` permissions** (read, write, execute) and assign **specific access rights** to multiple users or groups — not just the file owner or group.

Think of ACLs as giving out **special VIP passes** to certain users for your files or folders. 🎟️



## 🎯 Why Use ACLs?

The regular Linux permissions system (owner, group, others) looks like this: 

` -rw-r--r--`

That means:
- Owner can **read/write**
- Group can **read**
- Others can **read**

But what if you want **one extra user** (not the owner or in the group) to also write to the file?

That’s where **ACLs** come in — they give you that extra control. 💪



## ⚙️ Enabling ACLs (if not already enabled)

Most modern Linux systems have ACLs enabled by default.  
To check if a filesystem supports it, run:

`mount | grep acl`
If it's not enabled, you can remount with:

`sudo mount -o remount,acl / `

## 🧩 Viewing ACLs
To see which ACLs are set on a file or directory:

` getfacl filename `

Example output:

 file: report.txt
 owner: sarah
 group: staff

user::rw-
user:alex:rw-
group::r--
mask::rw-
other::r--

Explanation:

user::rw- → file owner (Sarah)

user:alex:rw- → special ACL entry for Alex

group::r-- → group permissions

mask::rw- → maximum allowed permissions for users/groups

other::r-- → everyone else

## 🛠️ Setting ACLs
### ✅ Give a user permission to a file:

`setfacl -m u:alex:rw filename`
This gives Alex read and write access to `filename`

### ✅ Give a group permission to a directory:

`setfacl -m g:developers:rwx /project`
Now, all users in developers group can read, write and execute inside `/project`

### ✅ Apply ACLs recursively (to all files and folders inside a directory):

`setfacl -R -m u:alex:rw /project`

### ✅ Remove an ACL entry:

`setfacl -x u:alex filename`

### ✅ Remove all ACLs from a file:

`setfacl -b filename`

## Default ACLs for New Files

### You can set default ACLs so that any new files created inside a directory automatically inherit specific permissions.

`setfacl -m d:u:alex:rwx /shared`
Here, any file created inside `/shared` automatically gives Alex full access.

## 🧠 Quick Summary

| Command                        | Meaning                        |
| ------------------------------ | ------------------------------ |
| `getfacl file`                 | View ACLs for a file           |
| `setfacl -m u:user:perm file`  | Add or modify ACL for a user   |
| `setfacl -m g:group:perm dir`  | Add or modify ACL for a group  |
| `setfacl -x u:user file`       | Remove a specific user’s ACL   |
| `setfacl -b file`              | Remove all ACLs                |
| `setfacl -R`                   | Apply changes recursively      |
| `setfacl -m d:u:user:perm dir` | Set default ACLs for new files |


## 🧩 Pro Tip:
### To make sure ACLs are active on your system:

`sudo tune2fs -l /dev/sda1 | grep "Default mount options"`

If `acl` isn't listed, enable it in `/etc/fstab` by adding `acl` to your filesystem options.


## 💡 Real-Life Example

Imagine you’re working on a shared project folder `/project` with two colleagues:

You own the folder.

You want Alex to edit files.

You want Kim to only read files.

Here’s how you do it:
`setfacl -m u:alex:rw /project`
`setfacl -m u:kim:r /project`

Now both Alex and Kim have exactly the permissions they need — and you didn’t have to change the main ownership or group structure!


# 👥 User and Group Management in Linux

Linux is a **multi-user operating system**, meaning multiple people (or processes) can use the same system without interfering with one another.  
To keep everything organized and secure, Linux uses **users** and **groups** to control *who* can access *what*.

Let’s break it down in a fun and simple way! 



## 🧑‍💻 What is a User?

A **user** is anyone (or anything) that can log in to a Linux system.  
Every user has:
- A **username**
- A **password**
- A **home directory** (e.g., `/home/sarah`)
- A **unique user ID (UID)**

🧩 You can view your current user:

`whoami`
👀 Or view all system users:

`cat /etc/passwd`

Each Line in /etc/password looks like this:

`sarah:x:1000:1000:Sarah:/home/sarah:/bin/bash`

Explanation:

sarah → Username

`x` → Password (stored encrypted in /etc/shadow)

`1000` → User ID (UID)

`1000` → Group ID (GID)

`Sarah` → User info/comment

`/home/sarah` → Home directory

`/bin/bash` → Default shell

## 👨‍👩‍👧 What is a Group?

A group is a collection of users.
Groups make it easy to assign the same permissions to multiple people.

👀 See all groups:

`cat /etc/group`

Example line:

`developers:x:1001:alex,kim`

This means:

Group name: `developers`

Members: `alex` and `kim`

## 🧩 Managing Users
### ✅ Create a New User

`sudo adduser john`

This creates:

`/home/john` directory

Default shell `/bin/bash`

Entry in `/etc/passwd` and `/etc/shadow`

### ✅ Set or Change a User Password

`sudo passwd john`

### ✅ Delete a User

`sudo deluser john`

#### To delete the user and their home directory:

`sudo deluser --remove-home john`

### ✅ Modify a User
#### Change user info or settings:

`sudo usermod -l newname oldname`

Example: rename user from `john` to `johnny`

#### To change a user's home directory:

`sudo usermod -d /new/home john`

## 🧩 Managing Groups
### ✅ Create a Group

`sudo addgroup developers`

### ✅ Add a User to a Group

`sudo usermod -aG developers john`

(The -aG means “append to group” — don’t forget it!)

### ✅ Remove a User from a Group

`sudo gpasswd -d john developers`

### ✅ Delete a Group

`sudo delgroup developers`

## 👀 Viewing User & Group Info

| Command           | Description                               |
| ----------------- | ----------------------------------------- |
| `id`              | Show your UID, GID, and group memberships |
| `groups`          | List groups you belong to                 |
| `finger username` | Display user details                      |
| `getent passwd`   | View all user entries                     |
| `getent group`    | View all group entries                    |

## 🔐 Special Files

| File           | Description         |
| -------------- | ------------------- |
| `/etc/passwd`  | List of all users   |
| `/etc/shadow`  | Encrypted passwords |
| `/etc/group`   | List of all groups  |
| `/etc/gshadow` | Secure group info   |

## ⚙️ Default Users

Linux systems often come with special built-in users:
| User     | Purpose                         |
| -------- | ------------------------------- |
| `root`   | Superuser (has all permissions) |
| `daemon` | Runs background services        |
| `nobody` | Used for limited-access tasks   |

## 🌈 Practical Example

##### You’re managing a small DevOps team:

Sarah → admin

Alex → developer

Kim → tester

##### You can set it up like this:

`sudo addgroup devops`
`sudo adduser alex`
`sudo adduser kim`
`sudo usermod -aG devops alex`
`sudo usermod -aG devops kim`

Now both Alex and Kim belong to the devops group, and you can give the group permission to access project files easily.

Example:

`sudo chown :devops /project`
`sudo chmod 770 /project`

### ✅ Result: Only users in devops (Alex and Kim) can access /project.

# 🧠 Quick Summary

| Task              | Command Example                 |
| ----------------- | ------------------------------- |
| Create a user     | `sudo adduser sarah`            |
| Delete a user     | `sudo deluser sarah`            |
| Create a group    | `sudo addgroup admins`          |
| Add user to group | `sudo usermod -aG admins sarah` |
| View all users    | `cat /etc/passwd`               |
| View all groups   | `cat /etc/group`                |
| View user info    | `id sarah`                      |
| Change password   | `sudo passwd sarah`             |





































