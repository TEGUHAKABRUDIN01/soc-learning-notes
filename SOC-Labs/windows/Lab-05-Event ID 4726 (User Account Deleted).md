# Event ID 4726 (User Account Deleted)

## Objective

Learn how to investigate user account deletion events using Windows Event Viewer.

## Scenario

SOC received an alert:

"A local user account was deleted from a Windows computer."

## Tools

- Windows Event Viewer
- Command Line Administrator (CMD)

## Invetigation

- Location: Windows Logs -> Security
- Filter: Event ID 4726

## Evidence

- Event ID: 4726
- Level: Information
- Time: 7/29/2026 07:35:52 PM
- Computer: windows1

### Subject

- Security ID: WINDOWS1\GUH
- Account Name: GUH

### Target Account

- Security ID: S-1-5-21-2062562350-3499454480-1003
- Account Name: soc_lab

## Analysis

Event ID 4726 indicates that a local user account was deleted.

The Subject Account Name was **GUH**, indicating that this account initiated the account deletion process.

The deleted account was **soc_lab**.

Based on the lab scenario, the activity was expected because the account was intentionally deleted for training purposes.

## Conslusion

The local user account **soc_lab** was successfully deleted from the Windows system.

The account deletion was performed by **GUH** at **07:35:52 PM**.

Based on the available evidence and the lab scenario, the activity was legitimate and authorized.

## Learning

- Learned how to investigate Event ID 4726.
- Learned how to identify the account that deleted a local user.
- Learned how to identify the deleted user account.
- Understood that account deletion events should be verified to determine whether they are authorized or suspicious.
