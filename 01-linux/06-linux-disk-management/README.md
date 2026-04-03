
# 🖥️ Linux Monitoring & Disk Management

Welcome back!  
Today we focus on **monitoring system health** 🧠 and **managing disks** 💽 - two key skills for any DevOps engineer.  
Let’s keep this **practical** - less theory, more commands.  



## 📊 What is Monitoring?
Monitoring means checking the **health & performance** of your system - CPU, Memory, Processes, I/O.  
Here’s how to do it in Linux step by step.  



## 🏃‍♂️ Process & Resource Monitoring

### 🔝 `top` - Live Process Monitoring
```bash
top
````

Shows CPU, memory usage, running processes.
Press:

* `q` to quit
* `k` to kill a process
* `M` to sort by memory usage
* `P` to sort by CPU usage



### 🌈 `htop` - Better `top`

```bash
htop
```

A colorful, interactive version of `top`.

* Arrow keys to scroll
* F9 to kill process

Install if missing:

```bash
sudo apt install htop -y
```



### 📊 `vmstat` - Virtual Memory Statistics

```bash
vmstat
```

Gives a quick summary of processes, memory, swap, CPU.

Run every 2 seconds:

```bash
vmstat 2
```



### 💻 `mpstat` - CPU Usage Per Core

```bash
mpstat
```

Shows CPU utilization per processor/core.



### 🧠 `free` - Memory Usage

```bash
free -m   # Show in MB
free -h   # Show in human-readable format (MB/GB)
```



### 🧵 `nproc` - Number of CPU Cores

```bash
nproc
```



### 💽 `df` - Disk Usage

```bash
df -h
```

Shows available disk space for all mounted partitions.



### 📦 `du` - Folder Size

```bash
du -sh /var/log
```

Shows total size of a directory.



### ⚡ `iostat` - I/O Performance

```bash
iostat
```

Displays CPU and disk I/O statistics.

Install if missing:

```bash
sudo apt install sysstat -y
```



### 🧍 `pidstat` - Monitor Specific Process

```bash
pidstat
```

Shows CPU, memory usage per process.



## 💽 Disk Management

### 🔗 `lsblk` - List Block Devices

```bash
lsblk
```

Displays all disks, partitions, mount points.



### 🔧 `fdisk` - Manage Partitions

```bash
sudo fdisk -l
```

Lists all partitions, sizes, and types.
(Be careful: modifying partitions may wipe data!)



### 🆔 `blkid` - Show UUID of Disks

```bash
sudo blkid
```

Shows disk UUIDs - useful for mounting in `/etc/fstab`.



### 📌 Mounting & Unmounting

Mount a disk:

```bash
sudo mount /dev/sdb1 /mnt
```

Unmount a disk:

```bash
sudo umount /mnt
```



### 🩺 `fsck` - File System Check

```bash
sudo fsck /dev/sdb1
```

Checks and repairs file system issues.



## 📝 Summary Checklist

✅ Monitor CPU, Memory, I/O with `top`, `htop`, `vmstat`, `iostat`
✅ Check disk space with `df -h`, folder size with `du -sh`
✅ List disks with `lsblk`, partitions with `fdisk -l`
✅ Mount/Unmount partitions manually
✅ Run `fsck` to fix disk errors



⚡ **Pro Tip:** Run these commands daily while learning - you’ll naturally build muscle memory.
This will help you troubleshoot servers faster in real-world DevOps work.


