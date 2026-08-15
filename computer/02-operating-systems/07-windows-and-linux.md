# Chapter OS-7 — Windows and Linux Basics

**Paper:** Paper-I (high weight in the 10 computer marks) + Paper-II  
**Time:** 70 minutes  
**Week:** 2, Day 14  

---

## Today's goal

1. Windows desktop objects and Control Panel ideas  
2. Important Windows shortcuts  
3. Linux distros named in syllabus: Ubuntu, Mint, Red Hat  
4. 15 Linux commands on paper  
5. Compare Windows vs Linux for 5 marks  

---

## 1. Windows — what Paper-I actually asks

### Desktop objects

| Item | Job |
|------|-----|
| **Desktop** | Background work area |
| **Icon** | Small picture for a program/file |
| **Shortcut** | Arrow icon; pointer to the real file |
| **Taskbar** | Running apps; Start button |
| **System tray / notification** | Clock, volume, network |
| **Wallpaper** | Background image |
| **Screen saver** | Moving image after idle time |
| **Recycle Bin** | Deleted files |
| **This PC / My Computer** | Drives |
| **Control Panel / Settings** | Date, time, sound, devices, programs |

### Mouse

- Left click: select  
- Double click: open  
- Right click: **context menu**  
- Drag and drop  

### Window parts

Title bar, minimise, maximise/restore, close, menu bar, tool bar, status bar, scroll bar.

### Control Panel classics

Date and time, display, sound, mouse, keyboard, programs and features, user accounts, device manager, network.

---

## 2. Windows shortcuts (memorise 20)

| Shortcut | Action |
|----------|--------|
| Ctrl+C / X / V | Copy / Cut / Paste |
| Ctrl+Z / Y | Undo / Redo |
| Ctrl+S | Save |
| Ctrl+P | Print |
| Ctrl+A | Select all |
| Ctrl+F | Find |
| Alt+Tab | Switch apps |
| Alt+F4 | Close window |
| Windows+D | Show desktop |
| Windows+E | File Explorer |
| Windows+L | Lock PC |
| Windows+I | Settings |
| Ctrl+Shift+Esc | Task Manager |
| Ctrl+Alt+Del | Security screen |
| F2 | Rename |
| F5 | Refresh |
| PrtScn | Screenshot |

---

## 3. Linux — names and ideas

**Linux** is an open-source OS kernel (Linus Torvalds, 1991). A **distribution (distro)** packages kernel + tools + GUI.

Syllabus names:

| Distro | Note |
|--------|------|
| **Ubuntu** | Popular, beginner, Debian-based, school-friendly |
| **Linux Mint** | Easy desktop, also Ubuntu/Debian family |
| **Red Hat (RHEL)** | Enterprise; related: Fedora, CentOS |
| **Others** | Debian, Kali (security), Android (Linux kernel) |

**macOS:** Apple’s OS for Macintosh (also asked as a type of OS).

### Linux features (5-mark points)

- Open source, mostly free  
- Multi-user, multitasking  
- Strong security and permissions  
- Stable servers  
- CLI + GUI (GNOME, KDE, Cinnamon)  
- Case-sensitive file names (`Note` ≠ `note`)

---

## 4. Linux commands (write and say aloud)

Assume you are in a terminal.

| Command | Meaning | Example |
|---------|---------|---------|
| `pwd` | Print working directory | where am I? |
| `ls` | List files | `ls -l` long list |
| `cd` | Change directory | `cd /home` `cd ..` |
| `mkdir` | Make folder | `mkdir lab` |
| `rmdir` | Remove empty folder | |
| `touch` | Create empty file | `touch a.txt` |
| `cp` | Copy | `cp a.txt b.txt` |
| `mv` | Move or rename | `mv a.txt notes.txt` |
| `rm` | Delete file | `rm a.txt` (**dangerous**) |
| `cat` | Show file | `cat a.txt` |
| `nano` or `vi` | Edit | |
| `man` | Manual | `man ls` |
| `clear` | Clear screen | |
| `whoami` | Current user | |
| `date` | Date and time | |
| `cal` | Calendar | |
| `df -h` | Disk free | |
| `free -h` | RAM | |
| `uname -a` | Kernel info | |
| `chmod` | Change permissions | `chmod 755 script.sh` |
| `sudo` | Run as admin | `sudo apt update` |
| `apt` / `yum` / `dnf` | Install software | Ubuntu uses `apt` |

**Permission number (MCQ):** `rwx` = 4+2+1 = 7.  
`755` = owner rwx, group rx, others rx.

---

## 5. Windows vs Linux (table for exam)

| Point | Windows | Linux |
|-------|---------|-------|
| Cost | Paid (licence) | Mostly free |
| Source | Closed | Open |
| User | Very popular on school PCs | Servers + some labs |
| Viruses | More targeted | Fewer common viruses |
| CLI | CMD / PowerShell | Bash terminal |
| File system | NTFS, drive letters | ext4, single `/` tree |
| Case | Usually not case-sensitive | Case-sensitive |
| Software install | Setup.exe, Microsoft Store | apt/yum, packages |

---

## 6. School lab habit

- Students log in with their own IDs if possible  
- Teach **Lock (Win+L)** when leaving the seat  
- On Linux labs, teach `ls` and `cd` before any `rm`  
- Keep a printed command chart near terminals  

---

## 7. Practice MCQs

**1.** Ubuntu is a:  
a) Printer  b) Linux distribution  c) CPU  d) Port  

**2.** Windows+L:  
a) Log of Excel  b) Lock computer  c) Linux install  d) Low RAM  

**3.** `ls` in Linux:  
a) List files  b) Load SMPS  c) Lock screen  d) Laser print  

**4.** Linux file names are:  
a) Never letters  b) Case-sensitive  c) Only 8 characters  d) Always .exe  

**5.** Recycle Bin is in:  
a) ALU  b) Windows  c) Only MICR  d) Hex gate  

**6.** `pwd` shows:  
a) Password always  b) Current directory  c) Printer  d) IP  

**7.** Red Hat is:  
a) A topology  b) A Linux family / distro  c) A mouse brand only  d) ROM type  

**8.** Right-click opens:  
a) BIOS chip  b) Context menu  c) SMPS  d) XOR  

**9.** `chmod` changes:  
a) Wallpaper only  b) File permissions  c) Clock speed  d) Screen size only  

**10.** Founder of Linux kernel:  
a) Bill Gates  b) Linus Torvalds  c) Charles Babbage  d) Steve Jobs  

### Answers

1-b, 2-b, 3-a, 4-b, 5-b, 6-b, 7-b, 8-b, 9-b, 10-b

---

## 8. Descriptive 5-mark answer

**Question:** Compare Windows and Linux. Write any five Linux commands with use.

Use the table (5 points). Then 5 commands: `ls`, `cd`, `pwd`, `mkdir`, `rm` with one line each.

---

## Quick revision box

- Desktop, icon, taskbar, Control Panel  
- Win+E, Win+L, Ctrl+C/V, Alt+Tab  
- Ubuntu, Mint, Red Hat  
- `ls cd pwd mkdir cp mv rm cat chmod sudo`  
- NTFS + C:\  vs  ext4 + /  
- Torvalds 1991  

---

## Homework

1. Write 20 Windows shortcuts.  
2. Write 15 Linux commands + meaning.  
3. If you have a PC, open CMD and also try [https://bellard.org/jslinux/](https://bellard.org/jslinux/) or any online Linux terminal for 10 minutes.

**Next:** [08 — OS Chapter Practice](08-chapter-practice.md)
