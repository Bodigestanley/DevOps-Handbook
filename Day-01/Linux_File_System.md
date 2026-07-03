# 📂 Linux File System

> **"Everything in Linux is treated as a file."**

---

# 📖 Introduction

Unlike Windows, Linux organizes everything under a single hierarchical directory structure that starts from the **root directory (`/`)**.

Whether it is a document, hard disk, USB drive, running process, or network device, Linux represents almost everything as a file.

Understanding the Linux file system helps you navigate servers, locate configuration files, troubleshoot issues, and manage applications efficiently.

---

# 🎯 Learning Objectives

After completing this chapter, you will be able to:

* Understand the Linux directory hierarchy.
* Navigate between directories.
* Identify the purpose of important system directories.
* Use navigation commands confidently.
* Understand absolute and relative paths.
* Explain why the Linux file system is important in DevOps.

---

# 🏗 Linux Directory Structure

Linux starts from a single top-level directory called the **root directory**.

```text
/
├── bin
├── boot
├── dev
├── etc
├── home
├── lib
├── media
├── mnt
├── opt
├── proc
├── root
├── run
├── sbin
├── srv
├── sys
├── tmp
├── usr
└── var
```

Everything in Linux exists somewhere inside this hierarchy.

---

# 📂 Important Directories

## `/`

The root directory.

It is the starting point of the entire Linux file system.

---

## `/home`

Stores personal files for normal users.

Example:

```text
/home/stanley
/home/alex
/home/john
```

This is where you created your `devops` folder.

---

## `/root`

The home directory of the **root** (administrator) user.

Normal users should not store files here.

---

## `/etc`

Contains system configuration files.

Examples:

* User configuration
* Network configuration
* SSH configuration
* Package configuration

Production servers rely heavily on files stored in `/etc`.

---

## `/bin`

Contains essential user commands.

Examples:

* `ls`
* `cp`
* `mv`
* `cat`

---

## `/sbin`

Contains system administration commands.

Examples:

* `reboot`
* `shutdown`
* `fsck`

Many commands here require administrator privileges.

---

## `/usr`

Stores installed software, libraries, documentation, and executable programs.

Think of it as one of the main locations for user applications.

---

## `/var`

Stores files that change frequently.

Examples:

* System logs
* Application logs
* Cache
* Mail queues

A DevOps engineer often checks `/var/log` while troubleshooting.

---

## `/tmp`

Stores temporary files.

Files here may be deleted automatically by the operating system.

---

## `/dev`

Contains device files.

Examples:

* Hard disks
* USB devices
* Terminals

Linux treats hardware devices as files.

---

## `/proc`

A virtual file system that provides information about the running system and processes.

Useful for monitoring and troubleshooting.

---

# 🧭 Navigation Commands

## Print Working Directory

```bash
pwd
```

Displays your current location.

Example:

```text
/home/stanley/devops
```

---

## List Files

```bash
ls
```

Lists files and directories.

---

## Detailed List

```bash
ls -la
```

Shows:

* Hidden files
* Permissions
* Owner
* Group
* Size
* Modification date

---

## Change Directory

```bash
cd
```

Examples:

```bash
cd /home
cd ~/devops
cd ..
cd -
```

---

# 📍 Absolute vs Relative Paths

## Absolute Path

Starts from the root directory (`/`).

Example:

```text
/home/stanley/devops/notes/day1.md
```

Absolute paths always point to the same location.

---

## Relative Path

Starts from your current directory.

Example:

```text
notes/day1.md
```

Relative paths depend on your current location.

---

# 🧪 Commands Practiced

During Day 1, you practiced:

```bash
pwd
ls
ls -la
cd
mkdir
touch
cp
mv
rm
cat
```

These commands form the foundation of Linux file management.

---

# 🌍 Real-World DevOps Scenario

Imagine an Nginx web server is not working.

A DevOps engineer might inspect:

```text
/etc/nginx/
```

to verify the configuration.

Then check:

```text
/var/log/nginx/
```

to review error logs.

Finally, they may deploy application files under:

```text
/var/www/
```

Understanding the Linux file system helps locate these files quickly.

---

# ⚠ Common Mistakes

* Confusing `/root` with `/`.
* Forgetting the difference between absolute and relative paths.
* Running commands from the wrong directory.
* Deleting files without checking the current location.

---

# ⭐ Best Practices

* Always confirm your location using `pwd`.
* Use `ls -la` before modifying files.
* Prefer absolute paths in automation scripts.
* Avoid working as the root user unless necessary.
* Keep personal projects inside your home directory.

---

# 🎤 Interview Questions

1. What is the Linux file system?
2. What is the root directory?
3. What is the difference between `/` and `/root`?
4. What is stored inside `/etc`?
5. Why is `/var/log` important?
6. Explain the purpose of `/home`.
7. What is the difference between absolute and relative paths?
8. Why is `/tmp` used?
9. What information does `pwd` display?
10. Why is understanding the Linux file system important for DevOps?

---

# 📝 Practice Questions

1. Draw the Linux directory hierarchy.
2. Explain the purpose of five important directories.
3. Compare absolute and relative paths with examples.
4. Demonstrate how to navigate between directories using `cd`.
5. Describe where application logs are typically stored.

---

# 📌 Chapter Summary

In this chapter, you learned:

* The Linux directory hierarchy.
* The purpose of major system directories.
* Navigation commands.
* Absolute and relative paths.
* Real-world DevOps use cases.
* Best practices for working in the Linux file system.

This knowledge will help you confidently navigate Linux systems and prepare you for managing applications, servers, and cloud environments.
