# Event ID 4724 - User Password Reset Investigation

## Objective

Learn how to investigate events where a user account password is reset using Windows Event Viewer.

## Scenario

SOC received an alert:

"A user account password was reset on a Windows computer."

## Tools

- Windows Event Viewer

## Evidence

- Event ID: 4724
- Level: Information
- Time: 7/31/2026 08:06:46 AM
- Computer: WINDOWS1

### Subject

- Security ID: WINDOWS1\GUH
- Account Name: GUH

### Target Account

- Security ID: WINDOWS1\GUH
- Account Name: GUH

## Analsysis

Event ID 4724 indicates that a password reset was attempted for a user account.

The Subject Account Name was **GUH**, indicating that this account initiated the password reset.

The target account was also **GUH**, meaning the password reset was performed on the same account.

Based on the lab scenario, the activity was expected because the password reset was intentionally performed for training purposes.

## Conclusion

The password for the account **GUH** was successfully reset.

The password reset was performed by **GUH** at **08:06:46 AM**.

Based on the available evidence and the lab scenario, this activity was legitimate and authorized.

## Learning

- Learned how to investigate Event ID 4724.
- Learned how to identify the account that initiated a password reset.
- Learned how to identify the target account whose password was reset.
- Understood the difference between a password change (Event ID 4723) and a password reset (Event ID 4724).
