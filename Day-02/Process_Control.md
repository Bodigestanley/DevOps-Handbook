# 🛑 Linux Process Control

> **"Finding a process is only half the job. A Linux administrator must also know how to stop, restart, and control processes safely."**

---

# 📖 Introduction

Linux systems continuously run hundreds of processes. Some complete their work and exit automatically, while others run in the background for days or even months.

Sometimes a process:

* Stops responding
* Uses too much CPU
* Consumes excessive memory
* Becomes stuck
* Must be restarted during maintenance

Linux provides several commands to terminate or control processes.

---

# 🎯 Learning Objectives

By the end of this chapter, you will be able to:

* Understand Linux signals.
* Stop running processes.
* Use `kill`, `pkill`, and `killall`.
* Understand the difference between graceful and forceful termination.
* Identify when each command should be used.
* Troubleshoot unresponsive applications.

---

# 🧠 What Happens When You Run `kill`?

The command `kill` does not immediately destroy a process.

Instead, it sends a **signal** to the process.

The process then decides how to respond.

Some signals can be handled gracefully, while others cannot.

---

# 📡 Common Linux Signals

| Signal  | Number | Purpose                                |
| ------- | -----: | -------------------------------------- |
| SIGTERM |     15 | Gracefully request the process to stop |
| SIGKILL |      9 | Forcefully terminate the process       |
| SIGINT  |      2 | Interrupt a process (Ctrl + C)         |
| SIGSTOP |     19 | Pause a process                        |
| SIGCONT |     18 | Continue a paused process              |

---

# 🔹 Using `kill`

First, find the process:

```bash
ps -ef | grep sleep
```

Example:

```text
stanley   1175   ...   sleep 300
```

Terminate it:

```bash
kill 1175
```

This sends **SIGTERM (15)** by default.

A well-behaved application will clean up its work before exiting.

---

# 💥 Forcefully Killing a Process

If a process refuses to stop:

```bash
kill -9 1175
```

This sends **SIGKILL (9)**.

The operating system immediately removes the process.

⚠️ Use this only when necessary because the application cannot save data or perform cleanup.

---

# 🔎 Using `pkill`

Instead of specifying a PID, you can terminate processes by name.

Example:

```bash
pkill sleep
```

This stops every process named `sleep` owned by your user.

Useful when multiple instances of the same program are running.

---

# 🔎 Using `killall`

Another convenient option:

```bash
killall sleep
```

This terminates all processes with the specified name.

During our practice, after stopping the process, you saw:

```text
sleep: no process found
```

This confirmed that no `sleep` processes were left running.

---

# 📋 Comparing Process Control Commands

| Command   | Uses PID | Uses Process Name | Typical Use                           |
| --------- | :------: | :---------------: | ------------------------------------- |
| `kill`    |     ✅    |         ❌         | Stop one specific process             |
| `kill -9` |     ✅    |         ❌         | Force-stop an unresponsive process    |
| `pkill`   |     ❌    |         ✅         | Stop processes by name                |
| `killall` |     ❌    |         ✅         | Stop all processes with the same name |

---

# 🏢 Real-World DevOps Examples

## Example 1: Stuck Deployment Script

A deployment script hangs during execution.

Steps:

1. Find the process:

```bash
ps -ef | grep deploy.sh
```

2. Stop it:

```bash
kill <PID>
```

3. If it still doesn't exit:

```bash
kill -9 <PID>
```

---

## Example 2: Multiple Test Processes

Suppose several test processes are running:

```bash
sleep 300 &
sleep 300 &
sleep 300 &
```

Instead of killing each PID individually:

```bash
pkill sleep
```

or

```bash
killall sleep
```

---

# ⚠️ Common Mistakes

* Using `kill -9` before trying a normal `kill`.
* Killing the wrong PID.
* Forgetting to verify the process with `ps`.
* Accidentally terminating production services.
* Confusing `pkill` with `kill`.

---

# 🔧 Troubleshooting Tips

## Process Will Not Stop

Try:

```bash
kill PID
```

If it remains running:

```bash
kill -9 PID
```

---

## Verify That the Process Has Ended

```bash
ps -ef | grep process_name
```

If only the `grep` command appears in the output, the original process has already stopped.

---

# 💡 Best Practices

* Always verify the correct PID before terminating a process.
* Use `kill` (SIGTERM) first.
* Reserve `kill -9` (SIGKILL) for processes that ignore SIGTERM.
* Recheck with `ps` after terminating a process.
* Understand why a process became unresponsive before restarting it.

---

# 🎯 What We Practiced

During Day 2, you successfully:

* Started a `sleep 300` process.
* Found its PID using `ps -ef | grep sleep`.
* Terminated it with `kill`.
* Used `pkill sleep`.
* Used `killall sleep`.
* Observed the message `sleep: no process found`, confirming successful termination.

---

# 📌 Chapter Summary

Linux provides several ways to terminate processes. The `kill` command sends signals to a specific PID, while `pkill` and `killall` work with process names. Administrators should always attempt a graceful shutdown using SIGTERM before resorting to SIGKILL.

Knowing how to control processes safely is essential for maintaining stable Linux servers and production environments.

---

# 🚀 Next Chapter

Continue with:

```text
Day-02/Background_Foreground.md
```

In the next chapter, you'll learn how Linux manages foreground and background jobs using `jobs`, `bg`, `fg`, and keyboard shortcuts like **Ctrl + C** and **Ctrl + Z**.
