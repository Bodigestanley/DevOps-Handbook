# 🌿 Git Basics

> **"Git is the industry-standard version control system that helps developers and DevOps engineers track, manage, and collaborate on code changes."**

---

# 📖 Introduction

Git is a distributed version control system (VCS) developed by **Linus Torvalds** in 2005. It allows developers to track changes in files, collaborate with teams, and maintain a complete history of a project.

Every modern software project uses Git, making it one of the most essential tools for DevOps engineers.

---

# 🎯 Learning Objectives

After completing this chapter, you should be able to:

* Understand what Git is.
* Explain why version control is important.
* Configure Git.
* Initialize a Git repository.
* Stage and commit changes.
* View commit history.
* Push a local repository to GitHub.

---

# 🤔 Why Do We Need Git?

Imagine working on a project without Git.

Problems include:

* No history of changes.
* Difficult collaboration.
* Accidental deletion of code.
* No easy way to revert mistakes.
* Multiple conflicting file versions.

Git solves these problems by maintaining a complete history of every change.

---

# 🌍 Real-World DevOps Example

A DevOps engineer updates a Kubernetes deployment file.

Without Git:

* If the deployment fails, recovering the previous version is difficult.

With Git:

* Every change is recorded.
* The previous version can be restored.
* Team members can review changes before deployment.

---

# 🔄 Git Workflow

```text
Working Directory
        │
        ▼
   git add
        │
        ▼
 Staging Area
        │
        ▼
 git commit
        │
        ▼
 Local Repository
        │
        ▼
   git push
        │
        ▼
GitHub Repository
```

---

# ⚙️ Git Configuration

Before using Git, configure your identity.

```bash
git config --global user.name "Stanley"
git config --global user.email "stanleybodige@gmail.com"
```

To verify:

```bash
git config --list
```

Example Output:

```text
user.name=Stanley
user.email=stanleybodige@gmail.com
```

---

# 🏁 Initialize a Repository

```bash
git init
```

This creates a hidden `.git` directory that stores the repository history and configuration.

---

# 🌱 Rename the Default Branch

```bash
git branch -m main
```

Most modern projects use `main` as the default branch.

---

# 📊 Check Repository Status

```bash
git status
```

Example:

```text
On branch main

No commits yet

Untracked files:
    linux_commands.txt
    notes/
```

This command shows:

* Current branch
* Staged files
* Untracked files
* Modified files

---

# ➕ Stage Changes

Stage all files:

```bash
git add .
```

Stage a single file:

```bash
git add README.md
```

The staging area lets you review exactly what will be included in the next commit.

---

# 💾 Create a Commit

```bash
git commit -m "Day 1: Linux basics and Git setup"
```

A commit acts as a snapshot of your project at a specific point in time.

---

# 📜 View Commit History

```bash
git log
```

Example:

```text
commit d8304ae...
Author: Stanley
Date: ...

Day 1: Linux basics and Git setup
```

---

# ☁️ Connect to GitHub

Add the remote repository:

```bash
git remote add origin https://github.com/your-username/your-repository.git
```

Verify:

```bash
git remote -v
```

---

# 🚀 Push to GitHub

First push:

```bash
git push -u origin main
```

Future pushes:

```bash
git push
```

The `-u` flag links your local `main` branch with the remote `main` branch.

---

# 📸 Lab Performed

During Day 1, you successfully:

* Configured Git.
* Initialized a repository.
* Renamed the default branch to `main`.
* Added files to the staging area.
* Created your first commit.
* Connected the repository to GitHub.
* Pushed the project successfully.

---

# 💡 Pro Tips

* Commit small, meaningful changes.
* Write clear commit messages.
* Check `git status` frequently.
* Never commit passwords or API keys.
* Push your work regularly to GitHub.

---

# ⚠️ Common Beginner Mistakes

* Forgetting to run `git add` before committing.
* Using vague commit messages like `"update"` or `"changes"`.
* Working directly on the wrong branch.
* Ignoring `git status`.
* Accidentally committing sensitive information.

---

# 🏢 Industry Best Practices

* One feature or fix per commit.
* Use meaningful commit messages.
* Review changes before committing.
* Keep repositories organized.
* Use GitHub as a backup and collaboration platform.

---

# 📋 Quick Command Reference

| Command                   | Purpose                          |
| ------------------------- | -------------------------------- |
| `git config --list`       | View Git configuration           |
| `git init`                | Initialize a repository          |
| `git status`              | Check repository status          |
| `git add .`               | Stage all changes                |
| `git add <file>`          | Stage a specific file            |
| `git commit -m "message"` | Save a snapshot                  |
| `git branch -m main`      | Rename current branch            |
| `git log`                 | View commit history              |
| `git remote -v`           | View configured remotes          |
| `git push -u origin main` | Push and track the remote branch |
| `git push`                | Push new commits                 |

---

# 🎤 Interview Questions

1. What is Git?
2. What is version control?
3. What is the difference between Git and GitHub?
4. Explain the Git workflow.
5. What is the staging area?
6. What does `git status` show?
7. Why do we use commits?
8. What is the purpose of `git log`?
9. Why do we use `git push -u origin main` only once?
10. What are some Git best practices?

---

# 📝 Practice Exercises

1. Create a new Git repository.
2. Create three text files.
3. Stage one file.
4. Check the repository status.
5. Stage all files.
6. Create a commit with a meaningful message.
7. View the commit history.
8. Rename the branch to `main`.
9. Connect the repository to GitHub.
10. Push the repository to GitHub.

---

# 📌 Chapter Summary

In this chapter, you learned:

* What Git is and why it is important.
* The Git workflow.
* How to configure Git.
* How to initialize a repository.
* How to stage and commit changes.
* How to view commit history.
* How to connect and push a repository to GitHub.

Git is a core skill for every DevOps engineer and will be used throughout this 180-day roadmap for tracking code, documentation, infrastructure, and automation projects.
