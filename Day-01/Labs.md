# 🧪 Day 1 Labs

> **"Learning Linux is not about memorizing commands—it's about practicing them until they become second nature."**

---

# 📖 Objective

The purpose of these labs is to gain hands-on experience with:

* Linux terminal navigation
* File and directory management
* System monitoring
* Git initialization
* Version control
* GitHub integration

---

# 🧪 Lab 1 – Create the DevOps Workspace

## Objective

Create a workspace to store DevOps notes, projects, and practice files.

## Commands

```bash
mkdir ~/devops
cd ~/devops

mkdir day1
mkdir notes
mkdir projects
```

## Verify

```bash
pwd
```

Expected Output

```text
/home/stanley/devops
```

```bash
ls
```

Expected Output

```text
day1
notes
projects
```

---

# 🧪 Lab 2 – Create Practice Files

## Objective

Create files for practicing Linux commands.

## Commands

```bash
touch linux_commands.txt

touch notes/day1.md

touch notes/copy.txt
```

Verify

```bash
tree
```

Expected Output

```text
.
├── day1
├── linux_commands.txt
├── notes
│   ├── copy.txt
│   └── day1.md
└── projects
```

---

# 🧪 Lab 3 – Read File Contents

## Objective

Display the contents of a text file.

## Commands

```bash
cat linux_commands.txt
```

Example Output

```text
hello world stanley
```

---

# 🧪 Lab 4 – Monitor System Resources

## Objective

Check the health of the Linux system.

### Check Uptime

```bash
uptime
```

Purpose

Displays:

* Current time
* System uptime
* Logged-in users
* Load average

---

### Check Memory

```bash
free -h
```

Purpose

Shows:

* Total RAM
* Used RAM
* Free RAM
* Swap memory

---

### Check Disk Usage

```bash
df -h
```

Purpose

Displays storage utilization for mounted file systems.

---

### Check Directory Size

```bash
du -sh
```

Purpose

Shows the total size of the current directory.

---

# 🧪 Lab 5 – Configure Git

## Objective

Configure Git with your identity.

Commands

```bash
git config --global user.name "Stanley"

git config --global user.email "stanleybodige@gmail.com"
```

Verify

```bash
git config --list
```

Example Output

```text
user.name=Stanley
user.email=stanleybodige@gmail.com
```

---

# 🧪 Lab 6 – Initialize a Git Repository

## Objective

Create a Git repository inside the DevOps workspace.

Commands

```bash
git init
```

Verify

```bash
ls -la
```

You should see a hidden `.git` directory.

---

# 🧪 Lab 7 – Rename the Default Branch

## Objective

Rename the default branch to `main`.

Command

```bash
git branch -m main
```

Verify

```bash
git status
```

Expected Output

```text
On branch main
```

---

# 🧪 Lab 8 – Stage Files

## Objective

Add project files to the Git staging area.

Command

```bash
git add .
```

Verify

```bash
git status
```

Expected Output

```text
Changes to be committed:
```

followed by the list of staged files.

---

# 🧪 Lab 9 – Create the First Commit

## Objective

Save the project snapshot.

Command

```bash
git commit -m "Day 1: Linux basics and Git setup"
```

Verify

```bash
git log
```

You should see your first commit with the commit ID, author, date, and message.

---

# 🧪 Lab 10 – Push to GitHub

## Objective

Upload the local repository to GitHub.

### Add Remote

```bash
git remote add origin https://github.com/<username>/<repository>.git
```

### Push

```bash
git push -u origin main
```

Verify

Visit your GitHub repository in a web browser and confirm that the files are available.

---

# 📋 Lab Summary

| Lab    | Topic              | Status      |
| ------ | ------------------ | ----------- |
| Lab 1  | Workspace Setup    | ✅ Completed |
| Lab 2  | File Creation      | ✅ Completed |
| Lab 3  | Reading Files      | ✅ Completed |
| Lab 4  | System Monitoring  | ✅ Completed |
| Lab 5  | Git Configuration  | ✅ Completed |
| Lab 6  | Git Initialization | ✅ Completed |
| Lab 7  | Branch Rename      | ✅ Completed |
| Lab 8  | Staging Files      | ✅ Completed |
| Lab 9  | First Commit       | ✅ Completed |
| Lab 10 | GitHub Push        | ✅ Completed |

---

# 💡 Lessons Learned

After completing these labs, you should be able to:

* Work confidently in the Linux terminal.
* Organize files and directories.
* Check basic system health.
* Initialize and manage a Git repository.
* Track project changes using Git.
* Upload projects to GitHub.

These practical skills are the foundation for all upcoming DevOps tools and workflows.

---

# 🚀 Next Steps

Day 2 builds upon these fundamentals by introducing:

* Linux file permissions
* Users and groups
* Process management
* Background and foreground jobs
* Package management
* Environment variables

Mastering Day 1 ensures you're ready to manage Linux systems more effectively in the following chapters.
