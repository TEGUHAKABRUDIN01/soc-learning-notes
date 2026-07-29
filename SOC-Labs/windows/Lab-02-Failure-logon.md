## LAB 02 FAILURE LOGON INVESTIGATION

## Objective

Learn how to investigate failed logon events using Windows Event Viewer.

## Scenario

SOC received an alert:

"A user failed to log on to a Windows computer."

## Tools

- Windows Event Viewer

## Investigation

- Location: Windows Logs -> Security

- Filter: Event ID 4625

## Evidence

- Event ID: 4625
- Account Name: vboxuser
- Account Domain: WINDOWS1
- Logon Type: 2 (Interactive)
- Time: 7/25/2026 07:43:24 PM

- Failure Reason: Unknown user name or bad password
- Status: 0xC000006D
- Sub Status: 0xC000006A

## Analysis

Event ID 4625 indicates a failed logon attempt.

Logon Type 2 indicates that the user attempted to log on directly at the computer.

The Sub Status (0xC000006A) indicates that the logon failed because an incorrect password was entered.

## Conslusion

The user **vboxuser** failed to log on to the Windows computer at 07:43:24 PM using Interactive Logon (Logon Type 2).

The failed logon was caused by an incorrect password.

## Learning

- Learned how to investigate Event ID 4625.
- Understood the difference between successful and failed logon events.
- Learned that Status and Sub Status provide additional information about the cause of a failed logon.
- Learned that a single failed logon is not enough to conclude a brute-force attack.
- Learned how to interpret Failure Reason, Status, and Sub Status in Event ID 4625.
