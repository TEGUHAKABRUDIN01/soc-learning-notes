# LAB 08 - Process Creation Investigation (Event ID 4688)

## Objective

Learn how to investigate process creation events using Windows Event Viewer.

## Scenario

SOC received an alert:

"A new process was created on a Windows computer."

## Tools

- Windows Event Viewer

## Investigation

- Location: Windows Logs -> Security
- Filter: Event ID 4688

## Evidence

### Event Information

- Event ID: 4688
- Time: 8/3/2026 6:36:36 PM
- Computer: WINDOWS1
- Level: Information

### Subject

- Security ID: SYSTEM
- Account Name: WINDOWS1$

### Process Information

- New Process ID: 0xe6c
- New Process Name: C:\Windows\System32\SearchProtocolHost.exe
- Creator Process Name: C:\Windows\System32\SearchIndexer.exe
- Process Command Line: Not Available

## Analysis

Event ID 4688 indicates that a new process was created.

The process **SearchProtocolHost.exe** was executed by the Windows **SYSTEM** account (**WINDOWS1$**).

The parent process was **SearchIndexer.exe**, which is a legitimate Windows Search component responsible for indexing files to improve search performance.

The executable is located in the trusted **C:\Windows\System32** directory.

No suspicious indicators such as an unusual executable path, unexpected parent process, or abnormal command line arguments were observed.

Based on the available evidence and the lab scenario, the activity appears to be legitimate Windows operating system behavior.

## Conclusion

A new Windows process (**SearchProtocolHost.exe**) was successfully created.

The process was executed by the **SYSTEM** account and launched by **SearchIndexer.exe**.

Based on the available evidence, the activity is legitimate and does not indicate suspicious behavior.

## Learning

- Learned how to investigate Event ID 4688.
- Learned how to identify the account that executed a process.
- Learned how to identify the parent (creator) process.
- Understood the relationship between parent and child processes.
- Learned that not every process creation event indicates malicious activity.
- Understood that the process location and parent process are important indicators during process investigations.
