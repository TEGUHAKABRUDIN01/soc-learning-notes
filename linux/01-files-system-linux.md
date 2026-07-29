# Linux File System

## Overview

A Linux file system is the method used by the Linux operating system to organize, store, retrieve, and manage data on storage devices such as hard disks, SSDs, and removable media.

It provides a structured way to access files and directories while ensuring efficient data management.

---

## Linux File System Structure

The Linux file system consists of three main layers.

### 1. Logical File System

The Logical File System provides the interface between user applications and the Linux file system.

Its responsibilities include:

- Managing file permissions.
- Handling file names and directories.
- Providing file-related system calls to applications.

---

### 2. Virtual File System (VFS)

The Virtual File System (VFS) provides a common interface for different file system types.

It allows applications to access files without needing to know the specific file system being used.

**Supported file systems include:**

- ext4
- XFS
- FAT32
- NTFS
- exFAT

---

### 3. Physical File System

The Physical File System interacts directly with storage hardware.

Its responsibilities include:

- Reading data from storage devices.
- Writing data to storage devices.
- Managing physical disk blocks.

---

## Linux File System Architecture

```text
![ Linux File System Architecture Image ] (../assets/image-arsitektur-file-system.png)
```

---

## Linux File System Types

### 1. ext (Extended File System)

The first file system designed specifically for Linux.

- Introduced in 1992.
- Foundation for later Extended File Systems.
- Rarely used today.

---

### 2. ext2 (Second Extended File System)

An improved version of ext.

**Characteristics:**

- Better performance than ext.
- Does not support journaling.
- Commonly used for USB flash drives and memory cards.

---

### 3. ext3 (Third Extended File System)

Introduced journaling to improve reliability.

**Characteristics:**

- Supports journaling.
- Faster recovery after unexpected shutdowns.
- Backward compatible with ext2.

---

### 4. ext4 (Fourth Extended File System)

The default file system for many modern Linux distributions.

**Characteristics:**

- Supports very large files and partitions.
- Improved performance.
- Supports journaling.
- Better reliability than ext3.

---

### 5. XFS

A high-performance journaling file system developed by Silicon Graphics (SGI).

**Characteristics:**

- Excellent performance for large files.
- Supports very large storage volumes.
- Commonly used on enterprise Linux servers.

---

## Comparison

| File System | Journaling | Performance | Common Usage                                 |
| ----------- | ---------- | ----------- | -------------------------------------------- |
| **ext**     | ❌         | Low         | Legacy systems                               |
| **ext2**    | ❌         | Good        | USB drives, legacy Linux systems             |
| **ext3**    | ✅         | Good        | Older Linux distributions                    |
| **ext4**    | ✅         | Excellent   | Modern Linux distributions                   |
| **XFS**     | ✅         | Excellent   | Enterprise servers and large storage systems |

---

## Summary

| File System | Purpose                                               |
| ----------- | ----------------------------------------------------- |
| **ext**     | The original Linux file system.                       |
| **ext2**    | Improved version of ext without journaling.           |
| **ext3**    | Added journaling for better reliability.              |
| **ext4**    | Modern default Linux file system.                     |
| **XFS**     | High-performance file system for large-scale storage. |
