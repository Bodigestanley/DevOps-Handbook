# ⚙️ Linux Process Management

> **"Everything running on Linux is a process. Understanding processes is the first step toward troubleshooting servers, optimizing performance, and managing production systems."**

---

# 📖 Introduction

A **process** is a program that is currently running.

When you execute a command, open an application, or start a service, Linux creates a process.

Examples:

* Opening Google Chrome
* Running Visual Studio Code
* Starting Nginx
* Running a Python script
* Executing a Bash script

All of these create one or more processes.

---

# 🎯 Learning Objectives

By the end of this chapter, you will be able to:

* Understand what a process is.
* Differentiate between a program and a process.
* Understand PID and PPID.
* Monitor running processes.
* Read the output of `ps`.
* Use `top` and `htop`.
* Identify CPU and memory usage.
* Search for specific processes.

---

# 📚 Program vs Process

## Program

A **program** is a set of instructions stored on disk.

Examples:

* Google Chrome
* Visual Studio Code
* Python
* Nginx

A program is **not running** until it is executed.

---

## Process

A **process** is a running instance of a program.

Example:

```bash
python app.py
```

The `python` program becomes a running process.

---

# 🆔 Process ID (PID)

Every running process has a unique identifier called the **Process ID (PID)**.

Example:

```bash
ps
```

Output:

```text
PID TTY          TIME CMD
318 pts/0    00:00:00 bash
876 pts/0    00:00:00 ps
```

Here:

* `318` → PID of the Bash shell.
* `876` → PID of the `ps` command.

---

# 👨‍👦 Parent Process ID (PPID)

Every process is started by another process.

The process that starts another process is called the **Parent Process**.

Example:

```bash
ps -ef
```

Output:

```text
UID      PID   PPID  CMD
stanley  318   317   -bash
```

* PID = 318
* PPID = 317

This means the Bash shell was started by process `317`.

---

# 🔍 Viewing Processes

## Show Current Terminal Processes

```bash
ps
```

Displays only the processes associated with the current terminal session.

---

## Show All Processes

```bash
ps -e
```

Displays all running processes on the system.

---

## Detailed Process Information

```bash
ps -ef
```

Displays:

* User
* PID
* PPID
* CPU usage
* Start time
* Terminal
* Running command

---

# 🔎 Searching for a Process

Search for a specific process using `grep`.

Example:

```bash
ps -ef | grep python
```

During our practice, you ran:

```bash
ps -ef | grep bash
```

Output:

```text
stanley 318 317 -bash
stanley 388 319 -bash
```

This showed two active Bash shell processes.

---

# 📊 Understanding `top`

Run:

```bash
top
```

`top` updates continuously and displays:

* Running processes
* CPU usage
* Memory usage
* Load average
* Running users
* Process priorities

Unlike `ps`, `top` refreshes automatically.

---

# 🎨 Understanding `htop`

Install:

```bash
sudo apt install htop
```

Run:

```bash
htop
```

Advantages over `top`:

* Colorful interface
* Easier to navigate
* Interactive controls
* Better process filtering
* Simpler process management

During our discussion, you correctly identified `htop` as more user-friendly.

---

# 📈 Load Average

The load average represents the average system workload over time.

Example:

```text
Load average:
0.00 0.00 0.00
```

These values correspond to:

| Value  | Time Period     |
| ------ | --------------- |
| First  | Last 1 minute   |
| Second | Last 5 minutes  |
| Third  | Last 15 minutes |

Higher values indicate a busier system.

---

# 💻 CPU Usage

High CPU usage may indicate:

* Heavy applications
* Infinite loops
* Resource-intensive workloads
* High user traffic

Use:

```bash
top
```

to identify which process is consuming CPU resources.

---

# 🧠 Memory Usage

Monitor RAM usage with:

```bash
free -h
```

or within:

```bash
top
```

High memory usage may cause applications to slow down or trigger swapping.

---

# 🏢 Real-World DevOps Examples

## Example 1: Website is Slow

A monitoring system reports:

> CPU usage is 98%.

A DevOps engineer would:

1. Run `top`.
2. Identify the high-CPU process.
3. Investigate the application.
4. Optimize or restart the service if necessary.

---

## Example 2: Python Process is Hanging

Search for Python processes:

```bash
ps -ef | grep python
```

If a process is unresponsive, the next step is to investigate or terminate it safely.

---

# ⚠️ Common Mistakes

* Confusing a program with a process.
* Assuming every `grep` result is the target process (the `grep` command itself often appears in the output).
* Looking only at PID without checking PPID or the associated command.
* Ignoring high CPU or memory usage alerts.

---

# 💡 Best Practices

* Use `ps` for quick snapshots.
* Use `top` or `htop` for live monitoring.
* Check CPU and memory before restarting services.
* Understand the parent-child relationship between processes.
* Investigate the cause of resource usage instead of immediately killing a process.

---

# 🎯 What We Practiced

During Day 2, you successfully:

* Explained the difference between a program and a process.
* Identified PID and PPID.
* Used `ps`, `ps -e`, and `ps -ef`.
* Searched for processes using `grep`.
* Compared `top` and `htop`.
* Understood load average and CPU usage.
* Interpreted real command outputs from your own Linux environment.

---

# 📌 Chapter Summary

Linux executes every running application as a process. Each process has a unique PID and is typically created by another process (its parent). Commands such as `ps`, `top`, and `htop` allow administrators to monitor processes, identify resource usage, and troubleshoot system performance.

Process management is a fundamental skill for Linux administrators and DevOps engineers responsible for maintaining reliable production systems.

---

# 🚀 Next Chapter

Continue with:

```text
Day-02/Process_Control.md
```

In the next chapter, you'll learn how to stop, terminate, and manage processes using commands like `kill`, `pkill`, and `killall`, including the differences between graceful and forceful termination.
