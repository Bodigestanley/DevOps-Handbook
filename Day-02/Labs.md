# 🧪 Day 02 Labs

> **Objective:** Reinforce all Day 2 concepts through hands-on practice.

---

# 📋 Lab 1 – Linux Permissions

## Objective

Learn how to inspect and modify file permissions.

### Steps

```bash
pwd
mkdir permissions_lab
cd permissions_lab
touch script.sh
touch config.conf
touch private.key
ls -l
```

### Change Permissions

```bash
chmod +x script.sh
chmod 644 config.conf
chmod 600 private.key
ls -l
```

### Verify

Identify:

* File type
* Owner permissions
* Group permissions
* Others permissions

---

# 👥 Lab 2 – Users and Groups

## Objective

Create and manage Linux users.

### Create a User

```bash
sudo adduser devuser
```

### View User Information

```bash
id devuser
```

### Switch User

```bash
su - devuser
```

### Verify

```bash
whoami
pwd
id
```

### Attempt Administrative Command

```bash
sudo apt update
```

Observe:

```text
devuser is not in the sudoers file.
```

### Return to Original User

```bash
exit
```

### Delete User

```bash
sudo userdel -r devuser
```

Verify:

```bash
id devuser
```

Expected:

```text
id: ‘devuser’: no such user
```

---

# ⚙️ Lab 3 – Process Management

## Objective

Monitor running processes.

### View Current Processes

```bash
ps
```

### View All Processes

```bash
ps -e
```

### Detailed Process List

```bash
ps -ef
```

### Search Processes

```bash
ps -ef | grep bash
```

```bash
ps -ef | grep python
```

### Monitor Live Processes

```bash
top
```

Exit:

```text
q
```

### Install htop

```bash
sudo apt update
sudo apt install htop
```

Run:

```bash
htop
```

Exit:

```text
F10
```

---

# 🛑 Lab 4 – Process Control

## Objective

Terminate processes safely.

### Start a Process

```bash
sleep 300
```

Open another terminal.

Locate the process:

```bash
ps -ef | grep sleep
```

Terminate it:

```bash
kill <PID>
```

Verify:

```bash
ps -ef | grep sleep
```

---

### Start Again

```bash
sleep 300 &
```

Terminate by Name

```bash
pkill sleep
```

Repeat:

```bash
sleep 300 &
```

Terminate:

```bash
killall sleep
```

Expected:

```text
sleep: no process found
```

after all sleep processes are removed.

---

# 🔄 Lab 5 – Background & Foreground Jobs

## Objective

Manage jobs efficiently.

### Foreground Process

```bash
sleep 300
```

Stop:

```text
Ctrl + C
```

---

### Suspend a Process

```bash
sleep 300
```

Pause:

```text
Ctrl + Z
```

---

### View Jobs

```bash
jobs
```

---

### Resume in Background

```bash
bg
```

---

### Bring Back to Foreground

```bash
fg
```

Terminate:

```text
Ctrl + C
```

---

# 📦 Lab 6 – Package Management

## Objective

Install and manage software.

Refresh package lists:

```bash
sudo apt update
```

Upgrade packages:

```bash
sudo apt upgrade
```

Install:

```bash
sudo apt install tree
```

Verify:

```bash
tree
```

Display hidden files:

```bash
tree -a
```

Display two directory levels:

```bash
tree -L 2
```

Remove package (optional):

```bash
sudo apt remove tree
```

Clean unused dependencies:

```bash
sudo apt autoremove
```

---

# 🌍 Lab 7 – Environment Variables

## Objective

View and create environment variables.

View all:

```bash
env
```

or

```bash
printenv
```

View individual variables:

```bash
echo $USER
echo $HOME
echo $SHELL
echo $PATH
```

Create a temporary variable:

```bash
MY_NAME=Stanley
echo $MY_NAME
```

Export it:

```bash
export MY_NAME=Stanley
echo $MY_NAME
```

Remove it:

```bash
unset MY_NAME
echo $MY_NAME
```

Reload shell configuration (after editing `.bashrc` in the future):

```bash
source ~/.bashrc
```

---

# 🎯 Mini Challenge

Without looking at your notes:

1. Create a file and assign it permission `600`.
2. Create a temporary user and display its UID and GID.
3. Delete the temporary user.
4. Start a `sleep 300` process.
5. Find its PID.
6. Terminate it using `kill`.
7. Start another `sleep 300` process in the background.
8. Bring it to the foreground.
9. Install the `tree` package.
10. Display your current `PATH`.

If you can complete all ten tasks confidently, you've mastered the practical objectives for Day 2.

---

# 🏆 Day 2 Lab Checklist

| Lab                     | Status |
| ----------------------- | :----: |
| Linux Permissions       |    ☐   |
| Users and Groups        |    ☐   |
| Process Management      |    ☐   |
| Process Control         |    ☐   |
| Background & Foreground |    ☐   |
| Package Management      |    ☐   |
| Environment Variables   |    ☐   |

Mark each item after completing it independently.

---

# 🚀 Next File

Continue with:

```text
Day-02/Practice_Questions.md
```

This file contains scenario-based questions to help you think like a Linux administrator instead of simply memorizing commands.
