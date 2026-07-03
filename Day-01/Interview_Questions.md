# 🎤 Day 1 Interview Questions

> **"If you can explain a concept clearly, you truly understand it."**

---

# 📖 Introduction

This chapter contains interview questions covering the Linux and Git concepts learned during Day 1.

The questions progress from beginner to intermediate level and reflect the type of discussions commonly seen in DevOps interviews.

---

# 🟢 Section 1 – Linux Fundamentals

### 1. What is Linux?

**Expected Answer:**

Linux is a free and open-source operating system based on Unix principles. It manages computer hardware and software resources while providing a secure and stable environment for running applications.

---

### 2. Why is Linux widely used in DevOps?

**Expected Answer:**

Because Linux is:

* Stable
* Secure
* Open source
* Highly customizable
* Automation-friendly
* Supported by most cloud platforms

---

### 3. What is an Operating System?

**Expected Answer:**

An operating system is software that acts as an interface between users, applications, and computer hardware.

---

### 4. Explain the difference between the Kernel and the Shell.

**Expected Answer:**

| Kernel                         | Shell                 |
| ------------------------------ | --------------------- |
| Core of the operating system   | Command interpreter   |
| Manages hardware and resources | Accepts user commands |
| Runs in kernel space           | Runs in user space    |

---

### 5. Name five Linux distributions.

**Expected Answer:**

* Ubuntu
* Debian
* Rocky Linux
* AlmaLinux
* Fedora

---

# 🟡 Section 2 – Linux File System

### 6. What is the root directory?

**Expected Answer:**

The root directory (`/`) is the top-level directory from which all other files and directories originate.

---

### 7. What is the difference between `/` and `/root`?

**Expected Answer:**

* `/` → Root of the file system.
* `/root` → Home directory of the root (administrator) user.

---

### 8. What is stored in `/etc`?

**Expected Answer:**

System configuration files such as network settings, user accounts, and service configurations.

---

### 9. What is `/var/log` used for?

**Expected Answer:**

It stores system and application log files used for monitoring and troubleshooting.

---

### 10. Explain absolute and relative paths.

**Expected Answer:**

* **Absolute path:** Starts from `/` and always points to the same location.
* **Relative path:** Starts from the current working directory and depends on your current location.

---

# 🟠 Section 3 – Linux Commands

### 11. What does the `pwd` command do?

Displays the current working directory.

---

### 12. Explain the difference between `ls` and `ls -la`.

* `ls` → Lists visible files and directories.
* `ls -la` → Displays all files, including hidden files, with detailed information.

---

### 13. What is the difference between `cp` and `mv`?

* `cp` copies files.
* `mv` moves or renames files.

---

### 14. What does `cat` do?

Displays the contents of a file.

---

### 15. Explain the difference between `du -sh` and `df -h`.

* `du -sh` → Shows the size of a directory.
* `df -h` → Shows disk usage for mounted file systems.

---

# 🔵 Section 4 – System Monitoring

### 16. What does `uptime` display?

* Current time
* System uptime
* Number of logged-in users
* Load average

---

### 17. What information does `free -h` provide?

Displays RAM and swap memory usage in a human-readable format.

---

### 18. Why is `df -h` important?

It helps monitor available disk space and prevents storage-related issues.

---

# 🟣 Section 5 – Git

### 19. What is Git?

Git is a distributed version control system used to track changes in files and collaborate on projects.

---

### 20. What is GitHub?

GitHub is a cloud-based platform for hosting Git repositories and enabling collaboration.

---

### 21. What is the purpose of `git init`?

Initializes a new Git repository by creating the hidden `.git` directory.

---

### 22. Explain the Git workflow.

Working Directory → Staging Area → Commit → Remote Repository

---

### 23. What is the staging area?

The staging area is where changes are prepared before creating a commit.

---

### 24. What does `git status` display?

* Current branch
* Staged files
* Modified files
* Untracked files

---

### 25. What is a commit?

A commit is a snapshot of your project at a specific point in time.

---

### 26. What does `git log` display?

The complete commit history of the repository.

---

### 27. Why do we use `git push -u origin main` only once?

The `-u` flag establishes the tracking relationship between the local and remote branches. Future pushes can simply use `git push`.

---

# 🔴 Scenario-Based Questions

### 28. A server is running slowly. Which commands would you use first?

Suggested answer:

```bash
uptime
free -h
df -h
du -sh /var/log
```

---

### 29. You accidentally committed the wrong files. What should you do first?

Suggested answer:

Check the repository status using:

```bash
git status
```

Then decide on the appropriate corrective action based on the situation.

---

### 30. Why is Git essential for DevOps?

Suggested answer:

Git enables version control, collaboration, rollback capabilities, auditing of changes, and seamless integration with CI/CD pipelines.

---

# 💡 Interview Tips

* Understand concepts instead of memorizing definitions.
* Explain commands with practical examples.
* Think aloud during scenario-based questions.
* Use clear and concise language.
* Relate answers to real-world DevOps workflows whenever possible.

---

# ⭐ Self-Evaluation

Rate yourself for each topic:

| Topic              | Rating (1–5) |
| ------------------ | ------------ |
| Linux Fundamentals | ☐            |
| Linux File System  | ☐            |
| Linux Commands     | ☐            |
| System Monitoring  | ☐            |
| Git Basics         | ☐            |

A rating of **4 or 5** across all topics indicates strong Day 1 readiness.

---

# 📌 Chapter Summary

This interview guide covers the essential Linux and Git concepts expected in beginner DevOps interviews. Reviewing these questions regularly will strengthen your understanding and improve your confidence when explaining technical concepts.
