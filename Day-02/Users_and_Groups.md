# 👥 Linux Users and Groups

> **"Linux is a multi-user operating system. Users and groups ensure that every person gets the right level of access—no more, no less."**

---

# 📖 Introduction

One of Linux's greatest strengths is its ability to securely support multiple users on the same system.

Every file, directory, process, and service is associated with a user and one or more groups. By assigning permissions through users and groups, Linux ensures that only authorized people can access or modify resources.

Understanding users and groups is essential for Linux administrators, DevOps engineers, cloud engineers, and system administrators.

---

# 🎯 Learning Objectives

By the end of this chapter, you will be able to:

* Understand what a Linux user is.
* Understand Linux groups.
* Explain UID and GID.
* Identify the root user.
* Understand `sudo` privileges.
* Create and delete users.
* View user information.
* Understand how Linux controls access using groups.

---

# 👤 What is a User?

A **user** is an identity created within Linux. Every person or service that interacts with the operating system does so as a user.

Examples:

* `stanley`
* `root`
* `ubuntu`
* `www-data`
* `mysql`

Each user has a unique **User ID (UID)**.

---

# 👥 What is a Group?

A **group** is a collection of users who share common permissions.

Instead of assigning permissions individually to every user, Linux administrators assign permissions to a group, and users inherit those permissions through group membership.

### Example

Imagine a development team with 50 engineers.

Instead of giving permissions to each engineer one by one, create a group named `developers` and add all engineers to it.

This simplifies administration and improves consistency.

---

# 🆔 UID (User ID)

Every Linux user has a unique numeric identifier.

Example:

```bash
id
```

Output:

```text
uid=1000(stanley)
```

### Common UID Ranges

| UID Range | Purpose                   |
| --------- | ------------------------- |
| 0         | Root user                 |
| 1–999     | System users and services |
| 1000+     | Regular users             |

---

# 🆔 GID (Group ID)

Every group also has a unique identifier.

Example:

```bash
id
```

Output:

```text
gid=1000(stanley)
```

---

# 🔍 Understanding the `id` Command

During our lab, you executed:

```bash
id
```

Example:

```text
uid=1000(stanley)
gid=1000(stanley)
groups=1000(stanley),27(sudo),4(adm),24(cdrom),30(dip)
```

### Breakdown

| Field  | Meaning                               |
| ------ | ------------------------------------- |
| UID    | User ID                               |
| GID    | Primary Group ID                      |
| Groups | Additional groups the user belongs to |

---

# 👑 The Root User

The **root** user is the Linux administrator.

Characteristics:

* UID = 0
* Full access to the system
* Can modify any file
* Can install software
* Can create and delete users
* Can manage services

### Warning

Avoid logging in as `root` for daily work. Instead, use `sudo` when administrative privileges are required.

---

# 🛡️ Understanding `sudo`

`sudo` stands for **Superuser Do**.

It allows authorized users to execute commands with administrative privileges without logging in as the root user.

Example:

```bash
sudo apt update
```

During our lab, you noticed that a normal user without `sudo` privileges received:

```text
devuser is not in the sudoers file.
```

This happened because `devuser` was not a member of the `sudo` group.

---

# 👤 Useful User Commands

### Display Current User

```bash
whoami
```

Example Output:

```text
stanley
```

---

### Display User Information

```bash
id
```

---

### Display Group Membership

```bash
groups
```

---

### Switch User

```bash
su username
```

---

# 👨‍💻 Creating a User

Create a new user:

```bash
sudo useradd -m devuser
```

Set a password:

```bash
sudo passwd devuser
```

The `-m` option creates a home directory automatically.

---

# 🗑️ Deleting a User

Delete a user:

```bash
sudo userdel devuser
```

Delete the user and their home directory:

```bash
sudo userdel -r devuser
```

During our practice, after deleting the user, running:

```bash
id devuser
```

returned:

```text
id: ‘devuser’: no such user
```

confirming that the account had been removed.

---

# 📂 Home Directories

Each normal user receives a home directory.

Examples:

```text
/home/stanley
/home/devuser
```

The root user's home directory is:

```text
/root
```

---

# 🔒 Home Directory Permissions

During the lab, you checked:

```bash
ls -ld /home/stanley
```

Example:

```text
drwxr-x--- 8 stanley stanley ...
```

This means:

* Owner: read, write, execute
* Group: read and execute
* Others: no access

This protects personal files from unauthorized users.

---

# 🏢 Real-World DevOps Example

Imagine a company with:

* Developers
* QA Engineers
* DevOps Engineers
* Security Team

Instead of assigning permissions individually:

* Create a `developers` group.
* Add all developers to that group.
* Grant project access to the group.

This approach is scalable and easier to maintain.

---

# ⚠️ Common Mistakes

* Working directly as the `root` user.
* Giving every user `sudo` access.
* Forgetting to remove unused accounts.
* Sharing user accounts between multiple people.
* Assigning incorrect permissions to groups.

---

# 💡 Best Practices

* Follow the Principle of Least Privilege.
* Use `sudo` instead of logging in as `root`.
* Create separate accounts for each user.
* Remove inactive accounts.
* Manage permissions through groups whenever possible.
* Review group memberships regularly.

---

# 🎯 What We Practiced

During Day 2, you successfully:

* Used `id` to inspect UID, GID, and group membership.
* Used `whoami` to verify the current user.
* Created the `devuser` account.
* Logged in as `devuser`.
* Observed the `sudoers` error.
* Inspected home directory permissions.
* Deleted the `devuser` account.
* Verified deletion using `id devuser`.

---

# 📌 Chapter Summary

Linux identifies every user with a unique UID and every group with a unique GID. Users can belong to multiple groups, allowing administrators to manage permissions efficiently. Administrative tasks are typically performed using `sudo`, while the root account is reserved for critical system administration.

Understanding users and groups is fundamental to Linux security and is an essential skill for every DevOps engineer.

---

# 🚀 Next Chapter

Continue with:

```text
Day-02/Process_Management.md
```

In the next chapter, you'll learn how Linux runs programs as processes, how to inspect them using commands like `ps`, `top`, and `htop`, and how to monitor CPU and memory usage in real time.
