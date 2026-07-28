# Task Scheduler & System Information

## Overview

Windows provides built-in administrative tools that help users manage scheduled tasks and view detailed system information.

For SOC Analysts, these tools are useful for identifying persistence mechanisms, verifying system configurations, and collecting evidence during an investigation.

---

# 1. Task Scheduler

## Overview

Task Scheduler is a Windows feature that allows programs, scripts, or commands to run automatically based on a specified time, event, or condition.

Task Scheduler is commonly used by administrators for automation. However, attackers may also abuse it to establish persistence on a compromised system.

---

## Opening Task Scheduler

Open Task Scheduler using the Run dialog:

```text
taskschd.msc
```

---

## Main Components

### Task Scheduler Library

Displays all scheduled tasks created by Windows, installed applications, or users.

> **SOC Analyst Note:** Review this folder for suspicious or unknown scheduled tasks.

---

### Trigger

Defines **when** a task will run.

**Examples:**

- At system startup
- At user logon
- Daily
- Weekly
- On a specific event

---

### Action

Defines **what** the task will do when triggered.

Examples include:

- Start a program
- Run a PowerShell script
- Execute a batch file
- Send a command

---

### Conditions

Specifies additional requirements before the task runs.

Examples include:

- Only if the computer is idle
- Only if connected to AC power
- Only if network is available

---

### History

Records task execution events.

Typical information includes:

- Task started
- Task completed
- Task failed
- Trigger activated

> **SOC Analyst Note:** The History tab helps determine whether a scheduled task has executed successfully and when it was last run.

---

## SOC Analyst Note

Scheduled Tasks are a common Windows persistence technique.

Attackers may create malicious scheduled tasks to:

- Launch malware after reboot.
- Execute PowerShell scripts automatically.
- Download additional payloads.
- Maintain persistence after gaining access.

During an investigation, verify:

- Task Name
- Trigger
- Action
- Author
- Last Run Time
- Next Run Time
- History

---

# 2. System Information

## Overview

System Information provides detailed information about the Windows operating system, hardware, and system configuration.

This tool helps administrators and SOC Analysts quickly identify important information about a computer.

---

## Opening System Information

Open System Information using the Run dialog:

```text
msinfo32
```

---

## Common Information

### OS Name

Displays the installed Windows operating system.

**Example:**

```text
Microsoft Windows 11 Pro
```

---

### Version

Displays the Windows version and build number.

---

### System Type

Displays the operating system architecture.

Examples:

- x64-based PC
- x86-based PC

---

### Processor

Displays the installed CPU.

**Example:**

```text
Intel(R) Core(TM) i5-12400
```

---

### Installed RAM

Displays the amount of physical memory installed.

---

### Windows Directory

Displays the Windows installation directory.

**Example:**

```text
C:\Windows
```

---

### System Directory

Displays the location of core Windows system files.

**Example:**

```text
C:\Windows\System32
```

---

### User Name

Displays the currently logged-in user.

---

### Domain / Workgroup

Displays whether the computer belongs to a Windows Domain or a Workgroup.

---

## SOC Analyst Note

System Information is useful for collecting host information during an investigation.

Common information gathered includes:

- Operating system version
- Computer architecture (32-bit or 64-bit)
- Logged-in user
- Windows installation path
- System directory
- Hardware specifications

This information helps analysts understand the environment before beginning deeper forensic or incident response activities.