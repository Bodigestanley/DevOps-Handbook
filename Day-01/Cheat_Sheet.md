# 📋 Day 1 Cheat Sheet

> **Quick Revision Guide – Linux Basics & Git Fundamentals**

---

# 🎯 Linux Basics

## What is Linux?

* Free and open-source operating system.
* Based on Unix principles.
* Widely used in servers, cloud computing, DevOps, and containers.

---

## Why Linux?

* Stable
* Secure
* Fast
* Highly customizable
* Excellent for automation
* Preferred for cloud infrastructure

---

## Linux Architecture

```text
User
  │
Shell
  │
Kernel
  │
Hardware
```

### Kernel

* Process Management
* Memory Management
* Device Management
* File System Management
* Networking

### Shell

* Accepts user commands
* Passes commands to the Kernel
* Displays command output

---

# 📁 Important Directories

| Directory | Purpose                              |
| --------- | ------------------------------------ |
| `/`       | Root directory                       |
| `/home`   | Home directories of normal users     |
| `/root`   | Home directory of the root user      |
| `/etc`    | Configuration files                  |
| `/bin`    | Essential user commands              |
| `/sbin`   | System administration commands       |
| `/usr`    | Installed applications and libraries |
| `/var`    | Logs and variable data               |
| `/tmp`    | Temporary files                      |
| `/dev`    | Device files                         |
| `/proc`   | Process and kernel information       |

---

# 💻 Essential Linux Commands

## Navigation

```bash
pwd
ls
ls -la
cd
```

## File Management

```bash
mkdir
touch
cp
mv
rm
cat
```

## Terminal

```bash
clear
history
```

## System Monitoring

```bash
uptime
free -h
df -h
du -sh
```

---

# 📊 Command Summary

| Command   | Purpose                |
| --------- | ---------------------- |
| `pwd`     | Show current directory |
| `ls`      | List files             |
| `ls -la`  | Detailed file listing  |
| `cd`      | Change directory       |
| `mkdir`   | Create directory       |
| `touch`   | Create file            |
| `cp`      | Copy file              |
| `mv`      | Move or rename file    |
| `rm`      | Delete file            |
| `cat`     | Display file contents  |
| `clear`   | Clear terminal         |
| `history` | Show command history   |
| `uptime`  | Show uptime and load   |
| `free -h` | Display memory usage   |
| `df -h`   | Display disk usage     |
| `du -sh`  | Display directory size |

---

# 🌿 Git Workflow

```text
Working Directory
       │
       ▼
git add
       │
       ▼
Staging Area
       │
       ▼
git commit
       │
       ▼
Local Repository
       │
       ▼
git push
       │
       ▼
GitHub Repository
```

---

# 🌱 Git Commands

## Configure Git

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
git config --list
```

---

## Repository

```bash
git init
git status
git branch -m main
```

---

## Staging

```bash
git add .
git add filename
```

---

## Commit

```bash
git commit -m "Meaningful commit message"
```

---

## History

```bash
git log
```

---

## Remote Repository

```bash
git remote add origin <repository-url>
git remote -v
```

---

## Push

```bash
git push -u origin main
```

Future pushes:

```bash
git push
```

---

# 🚀 Real-World DevOps Commands

Check server health:

```bash
uptime
free -h
df -h
```

Check current directory:

```bash
pwd
```

Inspect files:

```bash
ls -la
```

Read logs:

```bash
cat filename
```

---

# ⚠️ Common Mistakes

* Running `rm` in the wrong directory.
* Forgetting `git add` before `git commit`.
* Ignoring `git status`.
* Using unclear commit messages.
* Confusing `/` with `/root`.
* Confusing `df` with `du`.

---

# 💡 Best Practices

* Check your location with `pwd`.
* Inspect files using `ls -la`.
* Commit frequently with meaningful messages.
* Push your work regularly to GitHub.
* Avoid working as the root user unless necessary.
* Practice Linux commands daily.

---

# 🎤 Interview Quick Review

### Linux

* What is Linux?
* What is the Kernel?
* What is the Shell?
* Explain the Linux file system.
* Difference between `/` and `/root`.

### Commands

* `pwd`
* `ls -la`
* `cp`
* `mv`
* `rm`
* `cat`
* `uptime`
* `free -h`
* `df -h`
* `du -sh`

### Git

* What is Git?
* What is GitHub?
* Explain the Git workflow.
* What is the staging area?
* What does `git status` show?
* Why do we use commits?

---

# 🏆 Day 1 Achievements

By completing Day 1, you can:

* ✅ Navigate the Linux terminal.
* ✅ Understand the Linux file system.
* ✅ Use essential Linux commands.
* ✅ Monitor system resources.
* ✅ Configure Git.
* ✅ Create a Git repository.
* ✅ Stage and commit changes.
* ✅ Push projects to GitHub.

---

# 📚 Revision Plan

## Daily (10 Minutes)

* Revise the Linux directory structure.
* Practice 10 Linux commands.
* Review the Git workflow.

## Weekly (30 Minutes)

* Recreate the Day 1 labs from scratch.
* Answer all interview questions.
* Complete the practice exercises without referring to notes.

---

# 🎯 Next Step

Day 2 focuses on Linux administration, including:

* File permissions
* Users and groups
* Process management
* Background and foreground jobs
* Package management
* Environment variables

These topics build directly on the Linux and Git fundamentals established in Day 1.
