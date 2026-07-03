# 📦 Linux Package Management

> **"Package managers simplify software installation, updates, and maintenance. They are one of the most powerful tools available to Linux administrators."**

---

# 📖 Introduction

Linux applications are distributed as **packages**.

A package contains:

* Program files
* Libraries
* Configuration files
* Documentation
* Dependencies

Instead of downloading software manually, Linux uses **package managers** to install, update, and remove software safely.

---

# 🎯 Learning Objectives

By the end of this chapter, you will be able to:

* Understand what a package manager is.
* Install software using APT.
* Update package information.
* Upgrade installed software.
* Remove software safely.
* Understand Snap packages.
* Follow package management best practices.

---

# 📦 What is a Package?

A package is a bundled software application ready to be installed.

Examples:

* Git
* Docker
* Python
* Nginx
* Curl
* Vim

Each package includes everything required for the application to work correctly.

---

# 🛠 What is a Package Manager?

A package manager is a tool that:

* Installs software
* Updates software
* Removes software
* Resolves dependencies
* Keeps the system consistent

Ubuntu uses:

```text
APT (Advanced Package Tool)
```

---

# 🔄 Update Package Lists

Before installing new software, refresh the local package index.

Command:

```bash
sudo apt update
```

What it does:

* Contacts configured software repositories.
* Downloads the latest list of available packages.
* Does **not** install or upgrade software.

Think of it as refreshing the software catalog.

---

# ⬆️ Upgrade Installed Packages

Command:

```bash
sudo apt upgrade
```

What it does:

* Upgrades installed packages to newer versions.
* Uses the package information downloaded by `apt update`.

Recommended sequence:

```bash
sudo apt update
sudo apt upgrade
```

---

# 📥 Install Software

General syntax:

```bash
sudo apt install package-name
```

Example:

```bash
sudo apt install htop
```

After installation:

```bash
htop
```

launches the application.

---

# 🗑 Remove Software

Remove a package while keeping configuration files:

```bash
sudo apt remove htop
```

---

# 🧹 Remove Unused Dependencies

When software is removed, some libraries may no longer be needed.

Clean them up with:

```bash
sudo apt autoremove
```

This helps free disk space and keeps the system tidy.

---

# 📋 Search for Packages

Search the package database:

```bash
apt search nginx
```

This lists matching packages available in the configured repositories.

---

# ℹ️ View Package Information

Display detailed information about a package:

```bash
apt show git
```

Useful details include:

* Version
* Description
* Dependencies
* Maintainer
* Installed size

---

# 📦 Snap Packages

Snap is another package management system available on Ubuntu.

Advantages:

* Self-contained packages
* Automatic updates
* Sandboxed execution
* Easy installation

Install a Snap package:

```bash
sudo snap install tree
```

List installed Snap packages:

```bash
snap list
```

During our practice, you installed the `tree` command after the terminal suggested it.

---

# 🌳 The `tree` Command

The `tree` utility displays directories in a hierarchical format.

Example:

```bash
tree
```

Example output:

```text
.
├── Day-01
├── Day-02
├── README.md
└── Resources
```

Useful options:

```bash
tree -L 2
```

Show only two directory levels.

```bash
tree -a
```

Include hidden files and directories.

---

# 🏢 Real-World DevOps Examples

## Example 1: Install Git

```bash
sudo apt update
sudo apt install git
```

---

## Example 2: Install Docker Dependencies

```bash
sudo apt install \
ca-certificates \
curl \
gnupg
```

---

## Example 3: Install Monitoring Tools

```bash
sudo apt install htop
```

Use:

```bash
htop
```

to monitor CPU and memory usage interactively.

---

# ⚠️ Common Mistakes

* Running `apt upgrade` without first executing `apt update`.
* Forgetting `sudo` when administrative privileges are required.
* Removing packages without understanding dependencies.
* Installing software from untrusted repositories.

---

# 🔧 Troubleshooting

## Command Not Found

Example:

```text
tree: command not found
```

Solution:

```bash
sudo apt install tree
```

or

```bash
sudo snap install tree
```

depending on the package source.

---

## Package Not Found

If a package cannot be located:

1. Run:

```bash
sudo apt update
```

2. Verify the package name.

3. Check whether additional repositories are required.

---

# 💡 Best Practices

* Run `sudo apt update` before installing new software.
* Keep the operating system updated regularly.
* Remove unused packages with `apt autoremove`.
* Install software only from trusted repositories.
* Read package descriptions before installation.

---

# 🎯 What We Practiced

During Day 2, you successfully:

* Understood the purpose of APT.
* Learned the difference between `apt update` and `apt upgrade`.
* Installed the `tree` package.
* Used `tree`, `tree -a`, and `tree -L 2`.
* Organized your DevOps Handbook project structure.

---

# 📌 Chapter Summary

Package managers simplify software installation and maintenance by handling dependencies, updates, and removal automatically. Ubuntu primarily uses APT, while Snap provides an additional method for distributing self-contained applications.

Understanding package management is essential because nearly every DevOps tool is installed and maintained through a package manager.

---

# 🚀 Next Chapter

Continue with:

```text
Day-02/Environment_Variables.md
```

In the next chapter, you'll learn how Linux stores configuration information using environment variables such as `PATH`, `HOME`, `USER`, and `SHELL`, and how these variables influence command execution and application behavior.
