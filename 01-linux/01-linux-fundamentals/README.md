# Linux for DevOps 🐧

Welcome to **Linux for DevOps**!  
This repository is your go-to resource to understand **Linux fundamentals** from scratch and use them effectively as a DevOps Engineer.  

Whether you're completely new to Linux or just brushing up, this guide will help you build a solid foundation with hands-on practice.



## 📌 What is an Operating System (OS)?
An **Operating System** is the software that acts as a bridge between **hardware** and **users**.  
It manages:
- **Hardware resources** (CPU, Memory, Storage, Network)
- **Processes & Tasks**
- **Files & Security**
- **User Interaction** (through CLI or GUI)

Without an OS, your computer is just a bunch of components - it won’t do anything meaningful.



## 🐧 What is Linux?
Linux is a **free and open-source operating system** based on **Unix**.  
It is:
- **Secure** 🔒 (permissions & user management)
- **Stable** 🛠 (used in servers worldwide)
- **Free & Open-Source** 🌍 (anyone can contribute)
- **Customizable** ⚙️ (choose what you need)

Linux powers **over 90% of servers** on the internet - so if you’re learning DevOps, Linux is your best friend!



## 🏛 A Little History
- **1969:** Unix was created at Bell Labs.
- **1991:** Linus Torvalds (a student) wrote the first Linux kernel.
- **Today:** Linux is everywhere - servers, cloud, supercomputers, Android phones, IoT devices.



## 🖥 Setting Up Linux (Choose Your Way)


### 1️⃣ VMware / VirtualBox (Recommended for Beginners)
- Download **VMware Workstation Player** or **VirtualBox** (free).
- Download an **Ubuntu ISO** (Ubuntu is a beginner-friendly Linux distribution).
- Create a new Virtual Machine → Mount ISO → Install Ubuntu → Done!


### 2️⃣ WSL (Windows Subsystem for Linux)
If you use Windows 10/11:
```bash
wsl --install
````

Choose a distro like Ubuntu and start using Linux inside Windows terminal.

### 3️⃣ Docker Container (Quick Setup for Practice)

If you already have Docker installed:

```bash
docker run -it ubuntu bash
```

This will open a **Linux shell** inside a container - lightweight and perfect for experimenting.



## 🧩 Structure of Linux

Linux follows a **hierarchical file system** (like a tree):

```
/
├── bin   (essential binaries)
├── etc   (configuration files)
├── home  (user directories)
├── var   (variable data - logs, cache)
├── tmp   (temporary files)
└── root  (root user home)
```

Think of `/` as the "root folder" where everything starts.



## ⚙️ Core Components of Linux

1. **Kernel** - Heart of Linux (manages hardware)
2. **Shell** - Interface to interact (e.g., Bash)
3. **File System** - Organizes data
4. **System Utilities** - Tools to manage processes, users, packages
5. **Applications** - Anything you install (editors, servers, etc.)



## 🐧 Popular Linux Distributions (Distros)

* **Ubuntu** - Beginner-friendly, great for learning
* **CentOS / Rocky Linux** - Popular for servers
* **Debian** - Stable, used for production
* **Arch Linux** - Minimal, for advanced users



## ⌨️ Basic Linux Commands You Must Know

| Command          | Description            |
| ---------------- | ---------------------- |
| `pwd`            | Show current directory |
| `ls`             | List files & folders   |
| `cd`             | Change directory       |
| `mkdir`          | Create folder          |
| `touch file.txt` | Create a file          |
| `cat file.txt`   | View file content      |
| `cp src dest`    | Copy file              |
| `mv src dest`    | Move/Rename file       |
| `rm file.txt`    | Remove file            |
| `whoami`         | Show current user      |
| `sudo`           | Run command as admin   |

Practice these every day - they are the foundation of working with Linux.



## 📝 Summary

* Linux is the **backbone of DevOps**.
* Learn to **install it**, **navigate the file system**, and **use the terminal**.
* Mastering basics like `ls`, `cd`, `chmod`, `ps`, `kill` will make your DevOps journey smooth.
* This repo will guide you step by step - keep practicing!


🔥 **Pro Tip:** Don’t just read, **type commands yourself**. Break things, fix them, and explore. That’s how you truly learn Linux.



