# Create Local User (PowerShell)

## Overview

Windows PowerShell provides the `New-LocalUser` cmdlet to create a new local user account on a Windows computer.

Before creating the account, a password should be securely entered using `Read-Host -AsSecureString`. This method prevents the password from being displayed in plain text.

---

## Step 1: Create a Secure Password

Use the following command to securely enter a password.

### Syntax

```powershell
$password = Read-Host -AsSecureString
```

### Parameters

| Parameter | Description |
|-----------|-------------|
| `Read-Host` | Prompts the user to enter input from the keyboard. |
| `-AsSecureString` | Hides the entered characters and stores the password as a SecureString object. |

**Example**

```powershell
$password = Read-Host -AsSecureString
```

PowerShell will prompt:

```text
Enter password:
```

The password will not be displayed while typing.

---

## Step 2: Create a Local User

Use the stored password to create a new local user.

### Syntax

```powershell
New-LocalUser `
    -Name "username" `
    -FullName "Full Name" `
    -Description "description" `
    -Password $password
```

### Parameters

| Parameter | Description |
|-----------|-------------|
| `-Name` | Specifies the username for the local account. |
| `-FullName` | Specifies the user's full display name. |
| `-Description` | Adds a description to the user account. |
| `-Password` | Specifies the password stored in a `SecureString` object. |

**Example**

```powershell
$password = Read-Host -AsSecureString

New-LocalUser `
    -Name "john" `
    -FullName "John Smith" `
    -Description "IT Support" `
    -Password $password
```

---

## Verify the User

Display all local user accounts.

```powershell
Get-LocalUser
```

Display a specific local user.

```powershell
Get-LocalUser -Name "john"
```

---

## Delete a Local User

Delete a local user account.

```powershell
Remove-LocalUser -Name "john"
```

---

## SOC Analyst Note

Creating a local user is a normal administrative task, but attackers may also create unauthorized accounts to maintain persistence on a compromised system.

During an investigation, a SOC Analyst should verify:

- Who created the account.
- When the account was created.
- Whether the account creation was authorized.
- Whether the account was added to privileged groups such as **Administrators**.

A successful local user creation generates **Event ID 4720** in the Windows Security log, making it an important event for security monitoring and incident response.