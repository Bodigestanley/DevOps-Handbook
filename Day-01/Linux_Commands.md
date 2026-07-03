# 💻 Linux Commands

> **"The Linux terminal is the primary workspace of a DevOps Engineer."**

---

# 📖 Introduction

Linux commands allow users to interact with the operating system through the terminal. Almost every DevOps task—from deploying applications to troubleshooting servers—starts with using Linux commands.

This chapter documents the commands practiced during **Day 1** of the DevOps roadmap.

---

# 🎯 Learning Objectives

After completing this chapter, you should be able to:

* Navigate directories.
* Create and manage files.
* Copy, move, and delete files.
* Display file contents.
* Monitor system resources.
* Understand basic command syntax.

---

# 📚 Command Syntax

Most Linux commands follow this structure:

```text
command [options] [arguments]
```

Example:

```bash
ls -la
```

* `ls` → Command
* `-la` → Options

---

# 📂 Navigation Commands

## Print Working Directory

### Command

```bash
pwd
```

### Purpose

Displays the current working directory.

### Example Output

```text
/home/stanley/devops
```

### Real-World Use

Before editing or deleting files, verify your current location.

---

## List Directory Contents

### Command

```bash
ls
```

### Purpose

Lists files and directories.

### Example

```text
day1
notes
projects
linux_commands.txt
```

---

## Detailed Directory Listing

### Command

```bash
ls -la
```

### Purpose

Displays:

* Hidden files
* Permissions
* Owner
* Group
* Size
* Modification time

---

## Change Directory

### Command

```bash
cd
```

### Examples

```bash
cd /home
cd ~/devops
cd ..
cd -
```

### Purpose

Moves between directories.

---

# 📄 File Management Commands

## Create Directory

```bash
mkdir day1
```

Creates a new directory.

---

## Create Empty File

```bash
touch notes.txt
```

Creates an empty file.

---

## Copy Files

```bash
cp source.txt destination.txt
```

Copies files.

---

## Move or Rename Files

```bash
mv old.txt new.txt
```

Moves or renames files.

---

## Remove Files

```bash
rm file.txt
```

Deletes a file.

> ⚠️ Be careful. Deleted files are not moved to a recycle bin.

---

# 📖 Display File Contents

## Command

```bash
cat filename.txt
```

### Purpose

Displays the contents of a file.

### Example

```bash
cat linux_commands.txt
```

Output:

```text
hello world stanley
```

---

# 🧹 Clear Terminal

## Command

```bash
clear
```

Clears the terminal screen.

Shortcut:

```text
Ctrl + L
```

---

# 📜 Command History

## Command

```bash
history
```

Displays previously executed commands.

Useful for:

* Reviewing commands
* Repeating previous work
* Learning from past sessions

---

# 📊 System Monitoring Commands

## Check System Uptime

```bash
uptime
```

Displays:

* Current time
* System uptime
* Logged-in users
* Load average

### Why DevOps Engineers Use It

To quickly check server availability and system load.

---

## Memory Usage

```bash
free -h
```

Displays RAM and swap usage in a human-readable format.

### Why It Matters

Helps identify memory shortages or excessive RAM usage.

---

## Disk Usage

```bash
df -h
```

Displays disk usage for mounted file systems.

### Why It Matters

Prevents servers from running out of storage.

---

## Directory Size

```bash
du -sh
```

Displays the size of the current directory.

Example:

```bash
du -sh ~/devops
```

Useful for identifying large folders.

---

# 🏢 Real-World DevOps Scenario

A production server is reported to be running slowly.

A DevOps engineer may begin with:

```bash
uptime
free -h
df -h
du -sh /var/log
```

These commands provide a quick overview of system load, memory usage, disk utilization, and storage consumed by logs.

---

# ⚠️ Common Beginner Mistakes

* Running `rm` in the wrong directory.
* Forgetting to check the current path with `pwd`.
* Confusing `cp` and `mv`.
* Forgetting that Linux commands are case-sensitive.
* Using `du` and `df` interchangeably.

---

# ⭐ Best Practices

* Check your location with `pwd` before making changes.
* Use `ls -la` to inspect files before editing or deleting them.
* Use descriptive directory and file names.
* Avoid deleting files unless you are certain they are no longer needed.
* Monitor system resources regularly on production servers.

---

# 📋 Quick Command Reference

| Command   | Purpose                |
| --------- | ---------------------- |
| `pwd`     | Show current directory |
| `ls`      | List files             |
| `ls -la`  | Detailed file listing  |
| `cd`      | Change directory       |
| `mkdir`   | Create a directory     |
| `touch`   | Create an empty file   |
| `cp`      | Copy files             |
| `mv`      | Move or rename files   |
| `rm`      | Delete files           |
| `cat`     | Display file contents  |
| `clear`   | Clear terminal         |
| `history` | Show command history   |
| `uptime`  | Show uptime and load   |
| `free -h` | Display memory usage   |
| `df -h`   | Display disk usage     |
| `du -sh`  | Display directory size |

---

# 🎤 Interview Questions

1. What does `pwd` do?
2. What is the difference between `ls` and `ls -la`?
3. Explain the difference between `cp` and `mv`.
4. What does `cat` do?
5. Why is `df -h` important?
6. What information does `free -h` provide?
7. What is the purpose of `history`?
8. Explain the difference between `du` and `df`.
9. Why should you use `pwd` before deleting files?
10. Which commands are useful for checking server health?

---

# 📝 Practice Exercises

1. Create a directory named `practice`.
2. Create three empty files inside it.
3. Rename one file.
4. Copy another file.
5. Display the contents of a text file using `cat`.
6. Check your current directory.
7. Display memory usage.
8. Display disk usage.
9. View your command history.
10. Delete the practice directory after completing the exercises.

---

# 📌 Chapter Summary

In this chapter, you learned the essential Linux commands required for file management, directory navigation, and basic system monitoring.

These commands form the foundation of everyday Linux administration and are used extensively by DevOps engineers while managing servers, troubleshooting systems, and automating tasks.
