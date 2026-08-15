# Chapter OS-5 — File Systems

**Paper:** Paper-I Windows/Linux files + Paper-II  
**Time:** 50 minutes  
**Week:** 2, Day 13 (second half)  

---

## Today's goal

1. Define file and directory  
2. Know file types and attributes  
3. Know allocation methods  
4. Know FAT, NTFS, ext4  
5. Windows + Linux path basics  

---

## 1. Simple explanation

A **file** is a named collection of related data on secondary storage — a notebook with a title.

A **folder / directory** is a list of files and other folders — a rack in the almirah.

The **file system** is the method the OS uses to store and find them.

---

## 2. Definitions

> **File:** a named collection of data stored on secondary memory.  
> **File system:** OS structure that controls how files are named, stored, accessed, and protected.

---

## 3. File attributes

Name, type/extension, size, location, date/time, owner, permissions (read/write/execute), hidden, read-only.

Common extensions: `.txt .docx .xlsx .pptx .pdf .jpg .mp4 .exe .c .py .html`

---

## 4. Directory structures

| Structure | Idea |
|-----------|------|
| **Single level** | All files in one folder (old) |
| **Two level** | One folder per user |
| **Tree** | Folders inside folders (Windows, Linux) |
| **Acyclic graph** | Sharing via links |
| **General graph** | Links may form cycles; needs care |

**Absolute path:** from the root.  
Windows: `C:\Users\Teacher\Notes\os.md`  
Linux: `/home/teacher/notes/os.md`

**Relative path:** from the current folder (`..\chapter.md`).

---

## 5. Allocation methods (how file sits on disk)

| Method | Idea | Problem / plus |
|--------|------|----------------|
| **Contiguous** | File in consecutive blocks | Fast; external fragmentation |
| **Linked** | Each block points to next | No external frag; slow random access |
| **Indexed** | Index block holds all addresses | Good random access (Unix inode idea) |

**inode (Linux):** a number + metadata for a file; directory stores name → inode.

---

## 6. File systems you must name

| FS | Used on | Exam point |
|----|---------|------------|
| **FAT16 / FAT32** | Pendrives, old Windows | Simple; FAT32 max file 4 GB |
| **exFAT** | Large pen drives | Big files |
| **NTFS** | Modern Windows | Permissions, encryption, large disks |
| **ext3 / ext4** | Linux | Journaling |
| **HFS+ / APFS** | Mac | |
| **ISO 9660** | CDs | |

**Journaling:** keeps a log so the disk recovers better after a crash.

---

## 7. Windows file ideas (Paper-I)

- Drive letters C:, D:  
- **File Explorer**  
- Recycle Bin (not permanently deleted at once)  
- Cut / copy / paste / rename / delete  
- **Shortcut** (`.lnk`) — pointer, not the real file  
- Hidden files, extensions  

---

## 8. Linux file ideas

- Everything starts at `/`  
- Important dirs: `/home` `/etc` `/bin` `/usr` `/tmp` `/var` `/root`  
- Permissions: `rwx` for user, group, others  
- Commands (full list in Windows/Linux chapter): `ls`, `cd`, `pwd`, `cp`, `mv`, `rm`, `mkdir`

---

## 9. Practice MCQs

**1.** FAT32 single file limit is commonly:  
a) 4 GB  b) 4 KB  c) 1 bit  d) unlimited always  

**2.** NTFS is default in:  
a) Only Android phones  b) Modern Windows  c) Only CDs  d) Only BIOS  

**3.** ext4 is used by:  
a) Typical Linux  b) Only Windows 3.1  c) Only plotters  d) MICR  

**4.** A shortcut in Windows is:  
a) A full second copy always  b) A link/pointer  c) A CPU  d) RAM  

**5.** Absolute Linux path starts with:  
a) C:  b) /  c) ~ only  d) http  

**6.** Indexed allocation helps:  
a) Random access  b) Only printing  c) Cooling  d) Hex only  

**7.** Recycle Bin files are:  
a) Always gone forever at once  b) Usually recoverable until emptied  c) Stored in ALU  d) ROM  

**8.** inode is a concept of:  
a) Paint  b) Unix/Linux files  c) HDMI  d) OMR  

### Answers

1-a, 2-b, 3-a, 4-b, 5-b, 6-a, 7-b, 8-b

---

## 10. Descriptive 5-mark answer

**Question:** What is a file system? Explain directory structure and any two file systems.

Define file + file system. Tree directory + absolute path example. NTFS vs ext4 / FAT32. Mention permissions.

---

## Quick revision box

- File + directory + path  
- Contiguous / linked / indexed  
- FAT32 4 GB; NTFS Windows; ext4 Linux  
- C:\ vs /  
- Shortcut ≠ copy  
- inode, journaling  

---

**Next:** [06 — Deadlocks](06-deadlocks.md)
