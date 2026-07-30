# Event ID 4732 - User Added to a Local Group Investigation

## Objective

Learn how to investigate events where a user account is added to a local security group using Windows Event Viewer.

## Scenarion

SOC received an alert:

"A user account was added to the local **Administrators** group on a Windows computer."

## Tools

- Windows Event Viewer
- Command Prompt (Run as Administrator)

## Investigation

- Location: Windows Logs -> Security
- Filter: Event ID 4732

## Evidence

### Subject

- Security ID: WINDOWS1\GUH
- Account Name: GUH

### Member

- Security ID: WINDOWS1\JOKO_WIDODO
- Account Name: -

### Group

- Security ID: BUILTIN\Administrator
- Group Name: Administrator

## Analysis

Event ID 4732 indicates that a user account was added to a local security group.

The Subject Account Name was **GUH**, indicating that this account initiated the group membership change.

The account added to the group was **JOKO_WIDODO**.

The target group was the local **Administrator** group.

Based on the lab scenario, this activity was expected because the group membership change was intentionally performed for training purposes.

## Conclusion

The account **JOKO_WIDODO** was successfully added to the local **Administrator** group.

The action was performed by **GUH** at **07:56:52 AM**.

Based on the available evidence and the lab scenario, this activity was legitimate and authorized.

## Learning

- Learned how to investigate Event ID 4732.
- Learned how to identify the account that modified a local security group.
- Learned how to identify which user account was added to the group.
- Understood that adding a user to the local Administrator group may indicate privilege escalation and should always be verified.
