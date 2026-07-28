# Windows File Systems

## Overview

A file system is the method used by an operating system to organize, store, retrieve, and manage data on a storage device such as a hard disk, SSD, or USB flash drive.

Different file systems provide different capabilities, including maximum file size, partition size, security features, and compatibility.

---

## Types of Windows File Systems

### 1. FAT (File Allocation Table)

FAT is one of the earliest file systems developed by Microsoft. It is simple and widely compatible with many operating systems and devices.

**Characteristics:**

- Simple file system structure.
- High compatibility with Windows, Linux, macOS, cameras, and USB devices.
- Does not support advanced security features such as file permissions or encryption.
- Mostly replaced by FAT32 and NTFS.

---

### 2. FAT32 (File Allocation Table 32)

FAT32 is an improved version of FAT and remains popular for removable storage devices.

**Characteristics:**

- Maximum file size: **4 GB**
- Maximum partition size (Windows formatting): **32 GB**
- Compatible with almost all operating systems and devices.
- Does not support file permissions, compression, or encryption.

**Advantages:**

- Excellent compatibility across different operating systems.
- Commonly used for USB flash drives and memory cards.

**Limitations:**

- Cannot store a single file larger than **4 GB**.
- Not suitable for large files such as virtual machines or high-resolution videos.

> **SOC Analyst Note:** FAT32 is often encountered when analyzing USB flash drives because many removable storage devices are formatted using this file system.

---

### 3. exFAT (Extended File Allocation Table)

exFAT is a file system introduced by Microsoft as an improvement over FAT32. It is designed for flash storage devices and supports much larger files and storage capacities.

**Characteristics:**

- Supports files larger than **4 GB**.
- Supports very large storage devices.
- Better compatibility across Windows, macOS, Linux (with modern kernel support), cameras, and other devices.
- Does not support advanced security features such as file permissions, encryption, or journaling.

**Advantages:**

- Ideal for USB flash drives, SDXC cards, and external hard drives.
- No 4 GB file size limitation like FAT32.
- Better compatibility between different operating systems than NTFS.

**Limitations:**

- Does not provide the security and reliability features available in NTFS.
- Less suitable as a system drive for Windows.

> **SOC Analyst Note:** exFAT is commonly encountered on removable storage devices. During investigations, analysts may find evidence such as malware samples, stolen data, or transferred files on exFAT-formatted USB drives.

---

### 4. NTFS (New Technology File System)

NTFS is the default file system used by modern Windows operating systems.

**Characteristics:**

- Supports very large files and partitions.
- Supports file and folder permissions (Access Control Lists).
- Supports file compression.
- Supports Encrypting File System (EFS).
- Includes journaling to improve reliability after unexpected shutdowns.
- Supports disk quotas and auditing.

**Advantages:**

- Better security than FAT32 and exFAT.
- More reliable for enterprise and personal computers.
- Handles large files efficiently.

> **SOC Analyst Note:** NTFS is the most important file system for Windows investigations because it stores security information, file permissions, timestamps, and metadata that can be valuable during forensic analysis.

---

## Comparison

| Feature | FAT | FAT32 | exFAT | NTFS |
|---------|-----|--------|--------|------|
| Maximum File Size | Small | 4 GB | Very Large | Very Large |
| Maximum Partition Size | Limited | 32 GB (Windows formatting) | Very Large | Very Large |
| File Permissions | ❌ | ❌ | ❌ | ✅ |
| Encryption | ❌ | ❌ | ❌ | ✅ |
| Compression | ❌ | ❌ | ❌ | ✅ |
| Journaling | ❌ | ❌ | ❌ | ✅ |
| Cross-Platform Compatibility | High | High | Very High | Medium |
| Best Use Case | Legacy devices | USB flash drives, memory cards | External drives, SDXC cards, USB storage | Windows system drives |

---

## Key Takeaways for SOC Analysts

- **NTFS** is the default Windows file system and the primary focus during forensic investigations.
- **FAT32** is commonly found on USB flash drives and removable storage devices.
- **exFAT** is widely used on modern removable storage because it supports files larger than **4 GB** while maintaining excellent cross-platform compatibility.
- NTFS provides metadata, file permissions, and timestamps that are valuable when investigating security incidents.