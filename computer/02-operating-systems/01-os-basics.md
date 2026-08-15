# Chapter OS-1 — Operating System: Meaning and Functions

**Paper:** Paper-I OS basics + Paper-II OS  
**Time:** 55 minutes  
**Week:** 2, Day 10  

---

## Today's goal

1. Define OS  
2. List 6–8 functions  
3. Know types of OS  
4. Know booting  
5. Write a 5-mark “functions of OS” answer  

---

## 1. Simple explanation

Without an OS, you would have to talk to the CPU in 0s and 1s.

The **Operating System** is the **manager of the school**:

- allots rooms (memory)  
- allots periods (CPU time)  
- keeps files in almirahs (file system)  
- watches the gate (security)  
- talks to visitors (user interface)

Examples: **Windows 10/11**, **Ubuntu**, **Linux Mint**, **Red Hat**, **macOS**, **Android**.

---

## 2. Exam definition

> An **operating system** is system software that acts as an interface between the user and the computer hardware. It manages resources (CPU, memory, files, devices) and provides services to application programs.

**Kernel:** the core of the OS that talks to hardware.  
**Shell:** the interface that takes user commands (GUI or CLI).

```
  User
    |
 Application software (Word, Chrome)
    |
     OS  (shell + kernel)
    |
  Hardware
```

---

## 3. Functions of OS (write these 8)

| Function | One line |
|----------|----------|
| **1. Process / CPU management** | Decide which program runs on the CPU |
| **2. Memory management** | Allot and free RAM |
| **3. File management** | Create, delete, copy, protect files and folders |
| **4. Device / I/O management** | Control printer, disk, keyboard via drivers |
| **5. Security** | Passwords, permissions, antivirus hooks |
| **6. User interface** | GUI (icons) or CLI (commands) |
| **7. Job accounting / error handling** | Logs, error messages |
| **8. Networking (modern OS)** | Share files, TCP/IP stack |

---

## 4. Types of operating systems

| Type | Meaning | Example |
|------|---------|---------|
| **Batch** | Jobs collected, run without user sitting | Old mainframes |
| **Time sharing / Multi-user** | Many users share CPU in time slices | Linux servers, Unix |
| **Multiprogramming** | Many programs in RAM; CPU never idle | All modern OS |
| **Multitasking** | One user, many programs at once | Windows |
| **Multiprocessing** | More than one CPU/core | Modern PCs |
| **Real-time (RTOS)** | Strict time limits | Airbags, robots |
| **Distributed** | Many computers act as one | Clusters |
| **Network OS** | Designed to serve a network | Windows Server |
| **Embedded** | Inside appliances | TV, washing machine |
| **Mobile** | Phones | Android, iOS |

**Single user single task:** old MS-DOS.  
**Single user multitask:** Windows home PC.  
**Multi user multitask:** Linux server in a college.

---

## 5. User interfaces

| UI | Meaning | Exam examples |
|----|---------|----------------|
| **CLI** | Command Line Interface | `dir`, `ls`, CMD, Terminal |
| **GUI** | Graphical User Interface | Desktop, icons, windows, mouse |
| **Menu-driven** | Choose from a list | Old BIOS menus |
| **Touch / voice** | Mobile, assistants | Android |

**Windows parts (Paper-I loves this):** desktop, icons, taskbar, Start, notification area, wallpaper, screensaver, Control Panel / Settings, Recycle Bin, This PC.

---

## 6. Booting

> **Booting** is the process of starting the computer and loading the OS into RAM.

| Term | Meaning |
|------|---------|
| **Cold boot** | Power on from off |
| **Warm boot** | Restart |
| **POST** | Power On Self Test (BIOS/UEFI) |
| **Bootstrap** | Small ROM program that loads OS |
| **BIOS vs UEFI** | Old firmware vs modern firmware |
| **Safe mode** | Windows starts with minimal drivers |

Order (simplified): Power → POST → find boot disk → bootloader → kernel → login screen.

---

## 7. School teaching tip

Class 6: “Windows is the headmaster.” Open Task Manager and show many programs sharing one CPU.

Never let students format C: drive while teaching File Explorer.

---

## 8. Practice MCQs

**1.** OS is:  
a) Application  b) System software  c) Only a game  d) A printer  

**2.** Kernel is:  
a) A spreadsheet  b) Core of OS  c) A mouse  d) A port  

**3.** Android is:  
a) Batch OS only  b) Mobile OS  c) A CPU  d) A printer type  

**4.** CLI means:  
a) Computer Large Internet  b) Command Line Interface  c) Control Lock Icon  d) Cache Level Index  

**5.** Cold booting means:  
a) Restart only  b) Starting from power off  c) Sleep  d) Shutdown only  

**6.** RTOS is needed in:  
a) Writing a poem  b) Airbag system  c) Painting  d) Only Nudi  

**7.** Multiprogramming mainly keeps:  
a) CPU busy  b) Printer off  c) ROM empty  d) Mouse unplugged  

**8.** Recycle Bin is part of:  
a) ALU  b) Windows GUI  c) SMPS  d) BIOS chip only  

### Answers

1-b, 2-b, 3-b, 4-b, 5-b, 6-b, 7-a, 8-b

---

## 9. Descriptive 5-mark answer

**Question:** What is an operating system? Explain its functions.

1. Definition + interface between user and hardware.  
2. Examples: Windows, Linux.  
3. Six functions with one line each (process, memory, file, device, security, UI).  
4. Diagram: User → App → OS → Hardware.  
5. Conclusion: no OS, no easy use of school computers.

---

## Quick revision box

- OS = resource manager + interface  
- Kernel / shell  
- 8 functions  
- Batch, time-share, real-time, distributed, mobile  
- CLI vs GUI  
- Cold / warm boot, POST  

---

## Homework

Write 8 functions twice. List 6 OS names including 3 Linux flavours.

**Next:** [02 — Process Management](02-process-management.md)
