# 🔐 Linux File Permissions

> **"Linux security starts with understanding file permissions. Before you deploy applications, you must know who can read, write, or execute your files."**

---

# 📖 Introduction

Linux is a multi-user operating system. Many users can work on the same machine simultaneously, so Linux needs a secure way to control who can access files and directories.

This is achieved through the **Linux permission model**.

Every file and directory has:

* An Owner (User)
* A Group
* Others (Everyone else)

Each of these can have different permissions.

---

# 🎯 Learning Objectives

By the end of this chapter, you will be able to:

* Understand Linux permissions.
* Interpret the output of `ls -l`.
* Differentiate between files and directories.
* Understand read, write, and execute permissions.
* Change permissions using `chmod`.
* Change ownership using `chown`.
* Understand symbolic and numeric permission notation.
* Apply secure permission practices.

---

# 🏗 Linux Permission Structure

Example:

```text
-rwxr-xr--
```

Breakdown:

```text
-rwxr-xr--
│││ │││ │││
│││ │││ │└── Others
│││ │││
│││ └────── Group
│││
└────────── Owner
```

---

# 📌 First Character Meaning

| Symbol | Meaning          |
| ------ | ---------------- |
| `-`    | Regular file     |
| `d`    | Directory        |
| `l`    | Symbolic link    |
| `c`    | Character device |
| `b`    | Block device     |

Example:

```text
-rwxr-xr-x
```

Regular file

Example:

```text
drwxr-x---
```

Directory

---

# 👤 Three Permission Categories

Every Linux object has permissions for:

1. Owner (User)
2. Group
3. Others

Example:

```text
-rwxr-xr--
```

| Category | Permissions |
| -------- | ----------- |
| Owner    | rwx         |
| Group    | r-x         |
| Others   | r--         |

---

# 🔑 Permission Types

## Read (r)

For a file:

* View contents.

For a directory:

* List files inside.

---

## Write (w)

For a file:

* Modify the contents.

For a directory:

* Create, rename, or delete files inside (subject to directory permissions).

---

## Execute (x)

For a file:

* Run the file as a program or script.

Example:

```bash
chmod +x deploy.sh
./deploy.sh
```

Without execute permission:

```text
Permission denied
```

For a directory:

* Enter (traverse) the directory using `cd`.

---

# 📋 Understanding `ls -l`

Example:

```text
-rwxr-xr-x 1 stanley stanley 0 Jul 2 17:34 script.sh
```

Breakdown:

| Field         | Meaning                   |
| ------------- | ------------------------- |
| `-rwxr-xr-x`  | File type and permissions |
| `1`           | Number of hard links      |
| `stanley`     | Owner                     |
| `stanley`     | Group                     |
| `0`           | File size (bytes)         |
| `Jul 2 17:34` | Last modified time        |
| `script.sh`   | File name                 |

---

# 🔢 Numeric (Octal) Permissions

Each permission has a numeric value:

| Permission  | Value |
| ----------- | ----: |
| Read (r)    |     4 |
| Write (w)   |     2 |
| Execute (x) |     1 |

Add them together:

| Permission | Value |
| ---------- | ----: |
| `rwx`      |     7 |
| `rw-`      |     6 |
| `r-x`      |     5 |
| `r--`      |     4 |
| `---`      |     0 |

Examples:

| Command                 | Meaning                                     |
| ----------------------- | ------------------------------------------- |
| `chmod 777 file`        | Everyone has full access (not recommended). |
| `chmod 755 script.sh`   | Owner: rwx, Group: r-x, Others: r-x         |
| `chmod 644 config.conf` | Owner: rw-, Group: r--, Others: r--         |
| `chmod 600 private.key` | Only owner can read and write.              |

---

# ✍ Symbolic Permissions

Examples:

Give execute permission:

```bash
chmod +x deploy.sh
```

Remove execute permission:

```bash
chmod -x deploy.sh
```

Add write permission for the owner:

```bash
chmod u+w file.txt
```

Remove write permission from the group:

```bash
chmod g-w file.txt
```

Give read permission to others:

```bash
chmod o+r file.txt
```

---

# 👑 Changing Ownership

Display ownership:

```bash
ls -l
```

Change owner:

```bash
sudo chown user file.txt
```

Change owner and group:

```bash
sudo chown user:group file.txt
```

---

# 🏢 Real-World DevOps Examples

### Deploying a Script

A deployment script will not run if it lacks execute permission.

```bash
chmod +x deploy.sh
./deploy.sh
```

---

### Protecting SSH Keys

Private SSH keys should not be accessible to everyone.

Recommended permission:

```bash
chmod 600 ~/.ssh/id_rsa
```

This allows only the owner to read and modify the key.

---

### Web Server Files

Web server content often uses permissions such as:

```text
644
```

Directories commonly use:

```text
755
```

These settings balance accessibility and security.

---

# ⚠ Common Mistakes

* Using `chmod 777` on important files.
* Forgetting `+x` before running a script.
* Giving write permission to everyone.
* Confusing file permissions with directory permissions.
* Modifying permissions without understanding their impact.

---

# 🔧 Troubleshooting

## Problem

```text
Permission denied
```

Possible causes:

* Missing execute permission.
* Incorrect ownership.
* Insufficient user privileges.

Check:

```bash
ls -l filename
```

Then update permissions or ownership if appropriate.

---

# 💡 Best Practices

* Follow the Principle of Least Privilege.
* Use `600` for private keys.
* Use `644` for regular files unless stricter permissions are required.
* Use `755` for executable scripts and most directories.
* Avoid `777` unless absolutely necessary and only after understanding the risks.

---

# 🎯 What We Practiced

During Day 2, you successfully:

* Identified regular files and directories.
* Read permission strings from `ls -l`.
* Explained owner, group, and others.
* Understood the purpose of `r`, `w`, and `x`.
* Learned why `chmod +x deploy.sh` is required before executing a script.
* Practiced interpreting real permission examples.

---

# 📌 Chapter Summary

Linux permissions are a core security mechanism. Every file and directory has permissions assigned to the owner, group, and others. Understanding how to read and modify these permissions with `chmod` and `chown` is essential for Linux administration and DevOps.

---

# 🚀 Next Chapter

Continue with:

```text
Day-02/Users_and_Groups.md
```

In the next chapter, you'll learn how Linux identifies users with UIDs, manages groups with GIDs, grants administrative access using `sudo`, and controls system access in multi-user environments.
