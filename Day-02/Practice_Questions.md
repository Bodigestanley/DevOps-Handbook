# 📝 Day 02 Practice Questions

> **Objective:** Strengthen your Linux administration skills by solving practical and scenario-based questions.

---

# 📖 Section 1 – Linux Permissions

## Basic Questions

### 1.

What does the following permission mean?

```text
-rwxr-x---
```

---

### 2.

What is the difference between:

```bash
chmod +x script.sh
```

and

```bash
chmod 644 script.sh
```

---

### 3.

Which permission allows a user to:

* Read a file
* Modify a file
* Execute a file

---

### 4.

What does permission `600` mean?

---

### 5.

Can a user enter a directory if the execute (`x`) permission is missing?

Explain why.

---

# 👥 Section 2 – Users and Groups

### 6.

What is the difference between a user and a group?

---

### 7.

Why do companies use groups instead of assigning permissions to every employee individually?

---

### 8.

What is the purpose of the root user?

---

### 9.

Why are most employees given `sudo` access instead of logging in directly as the root user?

---

### 10.

What information does the following command display?

```bash
id
```

---

### 11.

Explain the difference between:

* UID
* GID

---

### 12.

What happens when a user who is not in the `sudo` group runs:

```bash
sudo apt update
```

---

# ⚙️ Section 3 – Process Management

### 13.

What is the difference between a **program** and a **process**?

---

### 14.

What is a PID?

---

### 15.

What is a PPID?

---

### 16.

Which command displays all running processes?

---

### 17.

Which command shows only processes for the current terminal session?

---

### 18.

How do you search for all running Python processes?

---

### 19.

What is the difference between `ps` and `top`?

---

### 20.

Why do many Linux administrators prefer `htop` over `top`?

---

# 🛑 Section 4 – Process Control

### 21.

What is the purpose of the `kill` command?

---

### 22.

What is the difference between:

```bash
kill PID
```

and

```bash
kill -9 PID
```

---

### 23.

When should you use `pkill`?

---

### 24.

When should you use `killall`?

---

### 25.

How can you verify that a process has been terminated successfully?

---

# 🔄 Section 5 – Background & Foreground Jobs

### 26.

What is the difference between a foreground process and a background process?

---

### 27.

What happens when you press:

```text
Ctrl + C
```

---

### 28.

What happens when you press:

```text
Ctrl + Z
```

---

### 29.

Which command lists background and suspended jobs?

---

### 30.

Which command resumes a suspended job in the background?

---

### 31.

Which command brings a background job back to the foreground?

---

# 📦 Section 6 – Package Management

### 32.

What is a package manager?

---

### 33.

What is the difference between:

```bash
sudo apt update
```

and

```bash
sudo apt upgrade
```

---

### 34.

Which command installs a package?

---

### 35.

Which command removes a package?

---

### 36.

Why is `apt autoremove` useful?

---

### 37.

What is the purpose of the `tree` command?

---

# 🌍 Section 7 – Environment Variables

### 38.

What is an environment variable?

---

### 39.

How do you display all environment variables?

---

### 40.

What does the following command display?

```bash
echo $HOME
```

---

### 41.

Why is the `PATH` environment variable important?

---

### 42.

How do you create a temporary environment variable?

---

### 43.

How do you remove an environment variable?

---

### 44.

What is the purpose of the `export` command?

---

# 🏢 Real-World Scenarios

### Scenario 1

A website is down.

What commands would you execute first to determine whether the web server process is running?

Explain your approach.

---

### Scenario 2

A server is responding very slowly.

Which Linux commands would you use to identify whether CPU or memory usage is the cause?

---

### Scenario 3

A deployment script has become unresponsive.

Describe the steps you would take before forcefully terminating it.

---

### Scenario 4

You accidentally started a long-running command in the foreground.

How can you move it to the background without restarting it?

---

### Scenario 5

You receive the following message:

```text
tree: command not found
```

How would you resolve the issue?

---

### Scenario 6

A new developer joins your team.

What steps would you take to:

* Create the user
* Verify the account
* Confirm the UID and GID
* Remove the account after testing

---

# 🎯 Self-Evaluation Checklist

Rate yourself from **1 (Needs Practice)** to **5 (Confident)**.

| Topic                        | Rating |
| ---------------------------- | :----: |
| Linux Permissions            |    ☐   |
| Users & Groups               |    ☐   |
| Process Management           |    ☐   |
| Process Control              |    ☐   |
| Background & Foreground Jobs |    ☐   |
| Package Management           |    ☐   |
| Environment Variables        |    ☐   |

---

# 🏆 Challenge

Without referring to your notes, try to:

* Explain every command aloud.
* Predict the output before executing it.
* Complete all Day 2 labs from memory.
* Teach one topic to someone else (or explain it to yourself).

If you can do that confidently, you've truly understood the material rather than memorized it.

---

# 🚀 Next File

Continue with:

```text
Day-02/Interview_Questions.md
```

This file contains HR, technical, and scenario-based Linux interview questions similar to those asked in DevOps and Cloud Engineer interviews.
