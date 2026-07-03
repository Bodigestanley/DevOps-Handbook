# 💼 Day 02 Interview Questions

> **Objective:** Prepare for Linux, DevOps, and Cloud interviews by practicing conceptual, technical, and scenario-based questions.

---

# 📖 Basic Linux Questions

### 1. What is Linux?

**Expected Answer:**

Linux is an open-source, Unix-like operating system that manages hardware resources and provides services for running applications. It is widely used in servers, cloud computing, DevOps, and embedded systems because of its stability, security, and flexibility.

---

### 2. What is the difference between Linux and Windows?

**Expected Answer:**

* Linux is open-source; Windows is proprietary.
* Linux provides a powerful command-line interface.
* Linux is widely used for servers and cloud environments.
* Windows is commonly used for desktop applications.

---

### 3. What is a file permission?

**Expected Answer:**

File permissions determine who can read, write, or execute a file or directory. Permissions are assigned separately to the owner, group, and others.

---

### 4. Explain the permission:

```text
-rwxr-x---
```

**Expected Answer:**

* Regular file
* Owner: Read, Write, Execute
* Group: Read, Execute
* Others: No permissions

---

### 5. What does `chmod +x` do?

**Expected Answer:**

It adds execute permission to a file, allowing it to be run as a program or script (provided the file contains executable content).

---

# 👥 Users and Groups

### 6. What is the purpose of a Linux user?

**Expected Answer:**

A user represents an individual account that owns files, runs processes, and has specific permissions within the operating system.

---

### 7. Why are groups used?

**Expected Answer:**

Groups simplify permission management by allowing administrators to assign permissions to multiple users at once instead of configuring each user individually.

---

### 8. What is the root user?

**Expected Answer:**

The root user is the superuser with unrestricted administrative privileges over the Linux system.

---

### 9. Why shouldn't users log in as root for daily work?

**Expected Answer:**

Using the root account increases the risk of accidental system-wide changes or damage. Instead, users should perform administrative tasks through `sudo`, which provides controlled privilege escalation.

---

### 10. What information does the `id` command display?

**Expected Answer:**

It displays:

* UID (User ID)
* GID (Primary Group ID)
* Group memberships

---

# ⚙️ Process Management

### 11. What is the difference between a program and a process?

**Expected Answer:**

A program is a file stored on disk containing instructions. A process is a running instance of that program in memory.

---

### 12. What is a PID?

**Expected Answer:**

A PID (Process ID) is a unique number assigned to every running process.

---

### 13. What is a PPID?

**Expected Answer:**

A PPID (Parent Process ID) identifies the process that started another process.

---

### 14. Which command displays all running processes?

**Expected Answer:**

```bash
ps -ef
```

or

```bash
ps -e
```

---

### 15. What is the difference between `ps` and `top`?

**Expected Answer:**

* `ps` provides a snapshot of currently running processes.
* `top` provides a continuously updating, real-time view of system activity.

---

### 16. Why do many administrators prefer `htop`?

**Expected Answer:**

Because it is interactive, easier to navigate, colorized, and provides a more user-friendly interface than `top`.

---

# 🛑 Process Control

### 17. What does the `kill` command do?

**Expected Answer:**

It sends a signal to a process, typically requesting it to terminate gracefully.

---

### 18. What is the difference between `kill` and `kill -9`?

**Expected Answer:**

* `kill` sends SIGTERM (15), allowing the process to clean up before exiting.
* `kill -9` sends SIGKILL (9), immediately terminating the process without cleanup.

---

### 19. When would you use `pkill`?

**Expected Answer:**

When you want to terminate one or more processes by name instead of by PID.

---

### 20. How do you verify that a process has stopped?

**Expected Answer:**

Run:

```bash
ps -ef | grep process_name
```

If only the `grep` command appears, the target process is no longer running.

---

# 🔄 Background & Foreground Jobs

### 21. What is the difference between a foreground and background process?

**Expected Answer:**

A foreground process occupies the terminal until it finishes. A background process runs without blocking the terminal, allowing additional commands to be executed.

---

### 22. What does **Ctrl + C** do?

**Expected Answer:**

It sends the SIGINT signal, interrupting and usually terminating the foreground process.

---

### 23. What does **Ctrl + Z** do?

**Expected Answer:**

It pauses (suspends) the foreground process by sending the SIGSTOP signal.

---

### 24. Which command lists jobs?

**Expected Answer:**

```bash
jobs
```

---

### 25. Which command moves a suspended job to the background?

**Expected Answer:**

```bash
bg
```

---

### 26. Which command brings a background job to the foreground?

**Expected Answer:**

```bash
fg
```

---

# 📦 Package Management

### 27. What is APT?

**Expected Answer:**

APT (Advanced Package Tool) is Ubuntu's package management system used to install, update, upgrade, and remove software.

---

### 28. What is the difference between `apt update` and `apt upgrade`?

**Expected Answer:**

* `apt update` refreshes the local package index.
* `apt upgrade` installs available updates for installed packages.

---

### 29. How do you install a package?

**Expected Answer:**

```bash
sudo apt install package-name
```

---

### 30. What is `apt autoremove` used for?

**Expected Answer:**

It removes unused dependencies that are no longer required by installed packages.

---

# 🌍 Environment Variables

### 31. What is an environment variable?

**Expected Answer:**

A name-value pair used by the operating system and applications to store configuration information.

---

### 32. What is the purpose of the `PATH` variable?

**Expected Answer:**

It lists directories that Linux searches when you enter a command, allowing executables to be run without specifying their full path.

---

### 33. Which command displays all environment variables?

**Expected Answer:**

```bash
env
```

or

```bash
printenv
```

---

### 34. What does the `export` command do?

**Expected Answer:**

It makes a variable available to child processes started from the current shell.

---

# 🏢 Scenario-Based Questions

### 35. A website is down. What is your first troubleshooting step?

**Expected Answer:**

Check whether the web server process is running using a command such as:

```bash
ps -ef | grep nginx
```

Then review logs and verify the service status before restarting it.

---

### 36. A Linux server is very slow. What would you check first?

**Expected Answer:**

* CPU usage (`top` or `htop`)
* Memory usage (`top` or `free -h`)
* Running processes (`ps -ef`)
* Disk usage (later topics)

---

### 37. A process is consuming 100% CPU. What would you do?

**Expected Answer:**

* Identify the process.
* Investigate why it is consuming CPU.
* Attempt a graceful termination if appropriate.
* Use `kill -9` only if the process does not respond to SIGTERM.

---

### 38. A command returns:

```text
tree: command not found
```

How would you resolve it?

**Expected Answer:**

Install the package:

```bash
sudo apt install tree
```

---

### 39. A user reports:

```text
devuser is not in the sudoers file.
```

What does this mean?

**Expected Answer:**

The user is not a member of the `sudo` group and therefore does not have permission to execute commands with elevated privileges.

---

### 40. You accidentally started a long-running command in the foreground. How can you continue using the terminal?

**Expected Answer:**

Press **Ctrl + Z** to suspend the process, then run:

```bash
bg
```

to resume it in the background.

---

# 💡 Interview Tips

* Explain concepts before giving commands.
* Mention why a command is used, not just its syntax.
* Prefer safe actions (for example, `kill` before `kill -9`).
* Think aloud during troubleshooting questions.
* If you don't know an answer, explain how you would investigate it instead of guessing.

---

# 🎯 Self-Assessment

Rate yourself from **1 (Needs Practice)** to **5 (Confident)**.

| Topic                   | Rating |
| ----------------------- | :----: |
| Linux Permissions       |    ☐   |
| Users & Groups          |    ☐   |
| Process Management      |    ☐   |
| Process Control         |    ☐   |
| Background & Foreground |    ☐   |
| Package Management      |    ☐   |
| Environment Variables   |    ☐   |

---

# 🚀 Next File

Continue with:

```text
Day-02/Cheat_Sheet.md
```

This is the final file of Day 2 and contains a quick-reference summary of all commands and key concepts you'll want at your fingertips during labs, interviews, and daily Linux administration.
