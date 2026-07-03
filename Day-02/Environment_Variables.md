# 🌍 Linux Environment Variables

> **"Environment variables allow Linux and applications to store configuration values without hardcoding them into programs."**

---

# 📖 Introduction

Environment variables are named values stored by the operating system.

They provide information about the current user, system configuration, executable locations, and application settings.

Whenever you open a terminal, Linux automatically loads a set of environment variables.

Many applications also create their own environment variables.

---

# 🎯 Learning Objectives

By the end of this chapter, you will be able to:

* Understand environment variables.
* View existing variables.
* Create temporary variables.
* Understand the `PATH` variable.
* Use `export`.
* Understand where environment variables are commonly used.

---

# 🌍 What is an Environment Variable?

An environment variable is a **name-value pair**.

Example:

```text
USER=stanley
```

Here:

* Variable Name → `USER`
* Value → `stanley`

Applications can read these values while they are running.

---

# 📋 View All Environment Variables

Display all variables:

```bash
env
```

or

```bash
printenv
```

This prints every environment variable available in the current shell.

---

# 🔍 Display a Specific Variable

Use:

```bash
echo $VARIABLE_NAME
```

Examples:

```bash
echo $USER
```

Example Output:

```text
stanley
```

---

```bash
echo $HOME
```

Example Output:

```text
/home/stanley
```

---

```bash
echo $SHELL
```

Example Output:

```text
/bin/bash
```

---

```bash
echo $PATH
```

This displays one of the most important environment variables.

---

# 🛣️ Understanding PATH

Example:

```bash
echo $PATH
```

Example Output:

```text
/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin
```

Linux searches these directories when you type a command.

For example:

```bash
git
```

Linux searches each directory in `PATH` until it finds the `git` executable.

Without `PATH`, you would have to type the full location every time.

Example:

```bash
/usr/bin/git
```

instead of simply:

```bash
git
```

---

# ➕ Creating a Temporary Variable

Example:

```bash
MY_NAME=Stanley
```

Display it:

```bash
echo $MY_NAME
```

Output:

```text
Stanley
```

This variable exists only for the current shell session.

---

# 📤 Exporting Variables

To make a variable available to child processes:

```bash
export MY_NAME=Stanley
```

Verify:

```bash
echo $MY_NAME
```

---

# ❌ Removing a Variable

Remove an environment variable:

```bash
unset MY_NAME
```

Verify:

```bash
echo $MY_NAME
```

No output means the variable has been removed.

---

# 📁 Permanent Environment Variables

Temporary variables disappear after closing the terminal.

To make them permanent, add them to shell configuration files such as:

```text
~/.bashrc
```

or

```text
~/.profile
```

After editing:

```bash
source ~/.bashrc
```

Reloads the configuration without restarting the terminal.

---

# 🏢 Real-World DevOps Examples

## Example 1: AWS Credentials

```text
AWS_ACCESS_KEY_ID
AWS_SECRET_ACCESS_KEY
AWS_REGION
```

Applications read these values automatically.

---

## Example 2: Java

```text
JAVA_HOME
```

Many Java applications require this variable.

---

## Example 3: Python

```text
PYTHONPATH
```

Used to define additional module search paths.

---

## Example 4: Docker

```text
DOCKER_HOST
```

Allows Docker CLI to communicate with a remote Docker daemon.

---

## Example 5: Kubernetes

```text
KUBECONFIG
```

Defines which Kubernetes configuration file should be used.

---

# 🔐 Security Best Practices

Never store:

* Passwords
* API Keys
* Database Credentials
* Tokens

directly inside application code.

Instead, use environment variables or a dedicated secrets management solution.

---

# ⚠️ Common Mistakes

* Forgetting `$` when displaying a variable.
* Expecting temporary variables to persist after closing the terminal.
* Accidentally overwriting important variables such as `PATH`.
* Storing sensitive credentials in source code.

---

# 💡 Best Practices

* Use descriptive variable names.
* Export variables only when needed.
* Keep sensitive information out of Git repositories.
* Use environment variables for application configuration.
* Document required variables for your projects.

---

# 🎯 What We Practiced

During Day 2, you learned:

* How to view environment variables.
* How to display individual variables using `echo`.
* Why `PATH` is important.
* How Linux finds executable commands.
* The difference between temporary and exported variables.
* How environment variables are used in real DevOps projects.

---

# 📌 Chapter Summary

Environment variables allow Linux and applications to store configuration information separately from the application code. Variables such as `PATH`, `HOME`, `USER`, and `SHELL` are fundamental to everyday Linux usage, while application-specific variables enable secure and flexible software configuration.

Understanding environment variables is essential for Linux administration, cloud computing, containers, CI/CD pipelines, and DevOps automation.

---

# 🚀 Next Chapter

Continue with:

```text
Day-02/Labs.md
```

The next chapter combines all the practical exercises from Day 2 into one structured lab manual, allowing you to repeat every task from scratch and strengthen your hands-on Linux administration skills.
