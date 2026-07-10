#### TASK SCHEDULER WINDOWS

### Objective

- Learn how Task Scheduler works and how this feature can be used by administrators, or misused by attackers for persistence.

### What is Task Scheduler

- Task Scheduler is a Windows feature that runs programs automatically based on specific triggers.

### Example of a Trigger

- When I log on
- At Startup
- Daily
- weekly

### Lab

- Name : SOC-Lab-Notepad
- Trigger : When I log on
- Action : Start a program
- Program : notepad.exe

### Result

-Initially, the task failed to run.

History :

- Event 119 -> Active Trigger
- Event 101 -> The action (program) is being initiated.
- Event 203 -> The action failed to execute.

Reason:
I made a typo notedpad.exe should notepad.exe After correcting the typo, the task ran succsessfully.

## What is being checked

- Task Name
- Trigger
- Action
- Last Run Time
- Last Run Result
- History

### Relastion with MITRE ATT&CK

Technique: Persistence
because attackers may create scheduled tasks that malware runs automatically every login

### Learning

Task Scheduler can be used normally by administrators, but it can also be exploited by attackers to maintain access to the system.

### NOTES SOC

- During this lab, I intentionally analyzed the task execution history instead of only verifying whether the task worked.

The history events helped me identify that:

- The trigger executed successfully.
- The scheduled task attempted to start the action.
- The action failed because the program name contained a typo.

This exercise demonstrates how Windows event logs can be used to troubleshoot scheduled task execution and identify the root cause of failures.
