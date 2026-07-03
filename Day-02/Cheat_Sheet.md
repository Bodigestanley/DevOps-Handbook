# ⚡ Day 02 Cheat Sheet – Linux Essentials

> **"Quick reference for all Day 2 Linux commands and concepts."**

---

# 📁 File Permissions

## View permissions

```bash id="cs1"
ls -l
```

## Change permissions

```bash id="cs2"
chmod +x file.sh
chmod 644 file.txt
chmod 600 file.txt
```

### Permission meanings

* `r` → read
* `w` → write
* `x` → execute

---

# 👥 Users & Groups

## Check user details

```bash id="cs3"
id
id username
```

## Switch user

```bash id="cs4"
su - username
```

## Create user

```bash id="cs5"
sudo adduser username
```

## Delete user

```bash id="cs6"
sudo userdel -r username
```

---

# ⚙️ Process Management

## View processes

```bash id="cs7"
ps
ps -e
ps -ef
```

## Search process

```bash id="cs8"
ps -ef | grep process_name
```

## Live monitoring

```bash id="cs9"
top
htop
```

---

# 🛑 Process Control

## Kill process by PID

```bash id="cs10"
kill PID
kill -9 PID
```

## Kill by name

```bash id="cs11"
pkill process_name
killall process_name
```

---

# 🔄 Background & Foreground

## Run in background

```bash id="cs12"
command &
```

## Jobs list

```bash id="cs13"
jobs
```

## Move to background

```bash id="cs14"
bg
```

## Bring to foreground

```bash id="cs15"
fg
```

## Keyboard shortcuts

```text id="cs16"
Ctrl + C → Kill process
Ctrl + Z → Pause process
```

---

# 📦 Package Management

## Update & upgrade

```bash id="cs17"
sudo apt update
sudo apt upgrade
```

## Install package

```bash id="cs18"
sudo apt install package_name
```

## Remove package

```bash id="cs19"
sudo apt remove package_name
sudo apt autoremove
```

---

# 🌍 Environment Variables

## View variables

```bash id="cs20"
env
printenv
```

## Show specific variable

```bash id="cs21"
echo $USER
echo $HOME
echo $PATH
```

## Create variable

```bash id="cs22"
VAR=value
export VAR=value
```

## Remove variable

```bash id="cs23"
unset VAR
```

---

# 📊 System Monitoring

## Process stats

```bash id="cs24"
top
htop
```

## CPU & memory

```bash id="cs25"
free -h
```

---

# 🧠 Key Concepts

## PID

Unique process ID.

## PPID

Parent process ID.

## Process Types

* Foreground → occupies terminal
* Background → runs independently

## Program vs Process

* Program → stored file
* Process → running instance

---

# 🏢 Troubleshooting Flow (VERY IMPORTANT)

## Website down?

```bash id="cs26"
ps -ef | grep nginx
```

Then:

* Check logs
* Restart service if needed

---

## System slow?

```bash id="cs27"
top
htop
ps -ef
```

Check:

* CPU usage
* Memory usage

---

# ⚡ Emergency Commands

```bash id="cs28"
kill -9 PID
pkill process
killall process
```

Use only when necessary.

---

# 🧩 Quick Memory Tricks

* `ps` → snapshot
* `top` → live view
* `kill` → stop process
* `&` → background
* `fg` → foreground
* `bg` → resume background
* `id` → user identity
* `chmod` → permissions

---

# 🎯 One-Line Summary

Linux administration =

> **Manage users + processes + permissions + packages + environment variables**

---

# 🚀 End of Day 2

You now have a complete Linux foundation:

* Permissions
* Users & Groups
* Processes
* Process Control
* Job Management
* Package Management
* Environment Variables

---


# 💡 Final Mentor Note

If you truly understand this cheat sheet, you already have the foundation of a **Linux System Administrator / DevOps Engineer**.

Next step: **Day 3 → Shell Scripting Basics** 🚀
