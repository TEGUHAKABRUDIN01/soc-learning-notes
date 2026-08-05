# LAB 09 - Explicit Credential Logon Investigation (Event ID 4648)

## Objective

Learn how to investigate explicit credential logon events using Windows Event Viewer.

## Scenario

SOC received an alert:

"A user attempted to log on using explicit credentials on a Windows computer."

The SOC analyst needs to determine who initiated the authentication request, which credentials were used, and whether the activity is legitimate or suspicious.

## Tools

- Windows Event Viewer
- Command Prompt (CMD)

## Investigation

- Location: Windows Logs -> Security
- Filter: Event ID 4648

## Evidence

### Event Information

- Event ID: 4648
- Time: 8/3/2026 6:42:22 PM
- Computer: WINDOWS1
- Level: Information

### Subject

- Security ID: WINDOWS1\vboxuser
- Account Name: vboxuser
- Account Domain: WORKGROUP
- Logon ID: 0x3E7

### Account Whose Credentials Were Used

- Account Name: JOKO_WIDODO
- Account Domain: WINDOWS1

### Process Information

- Process Name: C:\Windows\System32\svchost.exe

### Network Information

- Target Server Name: localhost

## Analysis

Event ID 4648 indicates that a logon attempt was made using explicit credentials.

The **Subject Account Name** was **vboxuser**, indicating that this account initiated the authentication request.

The credentials used belonged to the account **JOKO_WIDODO**.

The process involved in the authentication request was **svchost.exe**, and the target server was **localhost**.

Based on the lab scenario, the activity was expected because the explicit credentials were intentionally used for training purposes. No evidence of unauthorized credential use or suspicious behavior was observed.

## Conclusion

An explicit credential logon attempt was successfully performed using the credentials of **JOKO_WIDODO**.

The authentication request was initiated by **vboxuser** at **6:42:22 PM**.

Based on the available evidence and the lab scenario, the activity was legitimate and authorized.

## Learning

- Learned how to investigate Event ID 4648.
- Learned the difference between the **Subject Account** and the **Account Whose Credentials Were Used**.
- Learned how to identify the account that initiated an authentication request.
- Learned how to identify the credentials used during an authentication attempt.
- Understood that Event ID 4648 does not necessarily indicate malicious activity and should always be analyzed in context.
- Learned that explicit credential usage should be verified to determine whether the activity is legitimate or suspicious.
