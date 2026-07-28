# Windows Registry

## Overview

The Windows Registry is a hierarchical database that stores configuration settings for the Windows operating system, hardware, installed applications, and user preferences.

It acts as a central repository that determines how the operating system and applications behave.

---

## Functions of the Windows Registry

### 1. Central System Configuration

Stores configuration settings for the Windows operating system, including hardware, software, services, and device drivers.

### 2. Application Configuration Storage

Stores settings and preferences for installed applications, allowing programs to save and retrieve configuration data.

### 3. System Behavior Control

Controls how Windows operates by storing system policies, startup settings, security configurations, and other operating system parameters.

---

## Registry Root Keys (HKEY)

The Windows Registry is organized into several root keys, each serving a different purpose.

### 1. HKEY_CLASSES_ROOT (HKCR)

Stores information about file associations, COM objects, and the applications used to open different file types.

**Example:**

- `.txt` → Notepad
- `.pdf` → Adobe Acrobat Reader

---

### 2. HKEY_CURRENT_USER (HKCU)

Stores configuration settings for the user who is currently logged in.

Examples include:

- Desktop settings
- Control Panel preferences
- Environment variables
- Application preferences

---

### 3. HKEY_LOCAL_MACHINE (HKLM)

Stores configuration settings that apply to the entire computer, regardless of which user is logged in.

Examples include:

- Installed software
- Device drivers
- Hardware configuration
- Windows services

---

### 4. HKEY_USERS (HKU)

Contains user profiles and registry settings for all user accounts on the computer.

Each user has a unique Security Identifier (SID) containing their personal registry settings.

---

### 5. HKEY_CURRENT_CONFIG (HKCC)

Stores information about the current hardware profile used during system startup.

Examples include:

- Display configuration
- Printer configuration
- Hardware profile information

---

## Summary

| Registry Key | Purpose |
|--------------|---------|
| **HKCR** | Stores file associations and COM object information. |
| **HKCU** | Stores settings for the currently logged-in user. |
| **HKLM** | Stores system-wide configuration settings. |
| **HKU** | Stores registry settings for all user accounts. |
| **HKCC** | Stores the current hardware configuration used during startup. |