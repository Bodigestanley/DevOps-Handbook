# 🚀 Day 2 – Linux Administration Fundamentals

> **"Linux administration is the backbone of DevOps. Before automating infrastructure, you must know how to manage the operating system that powers it."**

---

# 📖 Introduction

Welcome to **Day 2** of the **180-Day DevOps Engineer Roadmap**.

On Day 1, we learned the fundamentals of Linux, the file system, essential commands, and Git basics.

On Day 2, we move from using Linux as a user to **administering Linux like a DevOps engineer**.

This day focuses on understanding file permissions, user management, process management, software installation, environment variables, and job control. These are daily responsibilities for Linux administrators, DevOps engineers, cloud engineers, and site reliability engineers (SREs).

---

# 🎯 Learning Objectives

By the end of Day 2, you will be able to:

* Understand Linux file permissions.
* Change file and directory permissions using `chmod`.
* Understand file ownership and use `chown`.
* Create, inspect, and delete Linux users.
* Understand Linux groups and administrative privileges.
* Monitor running processes.
* Control and terminate processes safely.
* Run commands in the background and foreground.
* Install and update software packages.
* Understand and configure environment variables.

---

# 📚 Topics Covered

## 1. Linux Permissions

Learn:

* Read (r)
* Write (w)
* Execute (x)
* Owner
* Group
* Others
* Numeric permissions
* Symbolic permissions
* `chmod`
* `chown`

---

## 2. Users and Groups

Learn:

* User IDs (UID)
* Group IDs (GID)
* Root user
* Normal users
* Administrative access (`sudo`)
* User creation and deletion
* Group membership

---

## 3. Process Management

Learn:

* What is a process?
* Process lifecycle
* Viewing processes
* Process IDs (PID)
* Parent Process IDs (PPID)
* Monitoring CPU and memory usage

Commands:

```bash
ps
ps -e
ps -ef
top
htop
```

---

## 4. Process Control

Learn how to stop and manage running processes.

Commands:

```bash
kill
kill -9
pkill
killall
```

---

## 5. Background & Foreground Jobs

Learn how Linux manages interactive tasks.

Commands:

```bash
jobs
bg
fg
Ctrl + C
Ctrl + Z
```

---

## 6. Package Management

Ubuntu package management:

```bash
apt update
apt upgrade
apt install
apt remove
apt autoremove
```

Package installation using Snap:

```bash
snap install
snap list
```

---

## 7. Environment Variables

Learn:

* PATH
* HOME
* USER
* SHELL

Commands:

```bash
echo $PATH
echo $HOME
env
export
```

---

# 🛠 Hands-on Labs

Throughout Day 2, you performed practical labs including:

* Viewing Linux permissions.
* Changing permissions using `chmod`.
* Creating and deleting users.
* Exploring user information with `id`.
* Running and terminating processes.
* Using `top` and `htop`.
* Sending processes to the background.
* Bringing processes back to the foreground.
* Installing packages.
* Viewing and modifying environment variables.

---

# 🏢 Real-World DevOps Relevance

Every DevOps engineer performs these tasks regularly:

* Managing production Linux servers.
* Troubleshooting high CPU or memory usage.
* Controlling services and processes.
* Managing user access securely.
* Installing required software packages.
* Configuring environment variables for applications.
* Maintaining secure file permissions.

Without these skills, managing cloud servers, containers, and CI/CD systems becomes difficult.

---

# 📂 Files in this Chapter

```text
Day-02/
├── README.md
├── Linux_Permissions.md
├── Users_and_Groups.md
├── Process_Management.md
├── Process_Control.md
├── Background_Foreground.md
├── Package_Management.md
├── Environment_Variables.md
├── Labs.md
├── Practice_Questions.md
├── Interview_Questions.md
└── Cheat_Sheet.md
```

---

# 🎯 Skills Gained

By completing Day 2, you will be able to:

* Explain Linux permission models.
* Secure files using appropriate permissions.
* Manage users and groups.
* Monitor and troubleshoot running processes.
* Safely terminate unresponsive applications.
* Work efficiently with background and foreground jobs.
* Install and maintain software packages.
* Configure Linux environment variables.

---

# 📈 Industry Applications

These concepts are essential in:

* Linux System Administration
* DevOps Engineering
* Cloud Engineering
* Site Reliability Engineering (SRE)
* Platform Engineering
* Cybersecurity
* Infrastructure Automation

---

# 💡 Best Practices

* Follow the principle of least privilege.
* Avoid using the root account unless necessary.
* Grant only the permissions users need.
* Monitor system resources regularly.
* Stop processes gracefully before forcing termination.
* Keep software packages updated.
* Understand environment variables before modifying them.

---

# 🎯 Prerequisites

Before studying Day 2, you should be comfortable with:

* Linux terminal navigation.
* Basic Linux commands.
* File and directory management.
* Git basics.
* Creating and editing files.

If you're unsure about any of these topics, revisit **Day 1** before continuing.

---

# 📚 Daily Summary

On Day 2, you transition from basic Linux usage to Linux administration. You learn how Linux controls access to files, manages users, runs processes, installs software, and configures the operating environment.

These concepts form the operational foundation required for future topics such as Docker, Kubernetes, CI/CD pipelines, cloud platforms, and infrastructure automation.

---

# 🚀 Next Chapter

Continue with:

```text
Day-02/Linux_Permissions.md
```

This chapter introduces one of the most important Linux administration concepts—file permissions—and explains how Linux secures files and directories using owners, groups, permission bits, and administrative controls.
