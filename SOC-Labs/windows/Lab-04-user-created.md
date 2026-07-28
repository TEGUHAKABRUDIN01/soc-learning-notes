## LAB 04 USER ACCOUTN CREATED INVESTIGATION

## Objective

Learn how to investigate user account creation events using Windows Event Viewer.

## Scenario

SOC received an alert:

"A new local user account was created on a Windows computer."

## Tools

- Windows Event Viewer
- Command Line Administrator (CMD)

## Invetigation

Location:

Windows Logs -> Security

Filter:
Event ID 4720

## Evidence

Event ID: 4720
Time: 7/28/2025 09:16:03 AM
Computer: WINDOWS1

Subject
Security ID: WINDOWS1\vboxuser
Account Name: vboxuser

New Account
Security ID: WINDOWS1\soc_lab
Account Name: soc_lab

## Analysis

Event ID 4720 indicates that a new local user account was created.
The Subject Account Name was "vboxuser", indicating that this account initiated the account creation process.
The newly created account was "soc_lab".
Based on the lab scenario, the activity was expected because the account was intentionally created for training purposes.

## Conslusion

A new local user account named "soc_lab" was successfully created on the Windows system.
The account creation was performed by "vboxuser" at 09:16:03 AM.
Based on the available evidence and the lab scenario, this activity was legitimate and authorized.

## Learning

- Learned how to investigate Event ID 4720.
- Learned how to identify the account that created a new local user.
- Learned how to identify the newly created account.
- Understood that user account creation is not always malicious and should be verified against the activity context.
