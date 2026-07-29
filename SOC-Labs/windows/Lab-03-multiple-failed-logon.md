## LAB 03 MULTIPLE FAILED LOGON INVESTIGATION

## Objective

Learn how to investigate multiple failed logon events using Windows Event Viewer.

## Scenario

SOC received an alert:
"A user repeatedly failed to log on to a Windows computer."

## Tools

- Windows Event Viewer

## Investigation

- Location: Windows Logs -> Security

- Filter: Event ID 4625

## Evidence 1

- Event ID: 4625
- Account Name: vboxuser
- Account Domain: WINDOWS1
- Logon Type: 2 (Interactive)
- Time: 7/27/2026 07:44:02 PM
- Source Network Address: 127.0.0.1
- Workstation Name: WINDOWS1
- Failure Reason: Unknown user name or bad password
- Status: 0xC000006D
- Sub Status: 0xC000006A

## Evidence 2

- Event ID: 4625
- Account Name: vboxuser
- Account Domain: WINDOWS1
- Logon Type: 2 (Interactive)
- Time: 7/27/2026 07:44:10 PM
- Source Network Address: 127.0.0.1
- Workstation Name: WINDOWS1
- Failure Reason: Unknown user name or password bad
- Status: 0xC000006D
- Sub Status: 0xC000006A

## Analysis

Multiple Event ID 4625 entries were detected within a short period.

All events involved:

- The same account (vboxuser)
- Logon Type 2 (Interactive)
- The same source address (127.0.0.1)
- The same failure reason
- The same Status and Sub Status

This pattern indicates repeated failed authentication attempts against a single account.

The failed logon attempts occurred within a short period, making the activity suspicious and requiring further investigation.

## Conslusion

Multiple failed logon attempts were detected for the account "vboxuser" within a short period.

Based on the available evidence, the activity is consistent with indicators of a brute-force attack. Further investigation is recommended to determine whether the activity is malicious or caused by repeated user authentication failures.

## Learning

- Learned how to investigate multiple Event ID 4625 entries.
- Learned to compare multiple events instead of analyzing a single log.
- Understood how to identify indicators of a brute-force attempt.
- Learned the importance of Source Network Address and Workstation Name during authentication investigations.
- Learned that multiple failed logons do not automatically confirm an attack and require further investigation.
