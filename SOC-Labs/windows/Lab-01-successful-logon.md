## LAB 01 SUCCSSESSFULL LOGON INVESTIGATION

## Objective

Learn how to investigate successful logon events using Windows Event Viewer.

## Scenario

SOC received an alert:
"A user is suspected of successfully logging on to a Windows computer."

## Tools:

- Windows Event Viewer

## Investigation

Location:
Windows Logs -> Security

Filter:
Event ID 4624

## Evidenace 1

Event ID : 4624
Account Name : lenovo
Account Domain: GUH
Logon Type : 2 (Interactive)
Time : 24 July 2026 08:21:23

## Analysis

Logon Type 2 indicates an Interactive Logon, meaning the user logged on directly at the computer using the keyboard, mouse, password, or PIN.

## Conclusion

The user lenovo successfully logged on to the Windows computer at 08:21:23 using Interactive Logon (Logon Type 2).

## Evidenace 2

Event ID : 4624
Account Name : SYSTEM
Acoount Domain: NT AUTHORITY
Logon Type : 5 (Service Windows Login)
Time : 24 July 2026 08:21:23

## Analysis

Logon Type 5 indicates a Service Logon.This event shows that a Windows service started successfully using the SYSTEM account.

## Conclusion

The SYSTEM account successfully performed a Service Logon (Logon Type 5).

This event indicates that a Windows service started successfully and does not represent a human user logging into the computer.

## Learning

- Learned how to investigate Event ID 4624.
- Understood the difference between Interactive Logon (Type 2) and Service Logon (Type 5).
- Learned how to filter Security logs using Event Viewer.
- Learned that not every successful logon represents a human user.
