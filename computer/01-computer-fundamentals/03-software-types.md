# Chapter 3 — Software Types

**Paper:** Paper-I Computer Literacy + Paper-II Fundamentals  
**Time:** 55 minutes  
**Week:** 1, Day 3  

---

## Today's goal

1. Define software, program, and package  
2. Split software into system / application / utility  
3. Know OS, compiler, interpreter, driver  
4. Know MS Office vs open source  
5. Answer “difference between compiler and interpreter” in 5 marks  

---

## 1. Simple explanation

Hardware is a silent box until software wakes it.

A **program** is a set of instructions written in a language (C, Python).  
**Software** is one program or a group of programs plus documents.  
A **package** is ready-made software sold or given for a job (MS Word, Tally).

---

## 2. Exam definitions

> **Software:** A collection of programs, procedures and documentation that perform tasks on a computer.

> **System software:** Software that controls hardware and provides a platform for application software.

> **Application software:** Software designed for a specific user task (typing, accounts, browsing).

> **Utility software:** Small programs that maintain and service the computer (antivirus, disk cleanup).

---

## 3. Big classification tree (draw this)

```
                         SOFTWARE
                              |
          +-------------------+-------------------+
          |                   |                   |
   SYSTEM SOFTWARE     APPLICATION SW        UTILITY SW
          |                   |                   |
     OS, Device          Word, Excel,         Antivirus,
     Drivers,            Browser, Tally,      Zip, Backup,
     Language            Nudi, Scratch        Disk defrag
     Translators
```

Some books put utilities **under** system software. In the exam, either grouping is accepted if you explain clearly. Safer line:

> Utilities are system-related tools that help manage the computer.

---

## 4. System software — three must-know families

### 4.1 Operating System (OS)

Master software. Examples: **Windows**, **Linux (Ubuntu, Mint, Red Hat)**, **macOS**, **Android**, **iOS**.

Functions (short list — full chapter in OS folder):

1. Process management  
2. Memory management  
3. File management  
4. Device management  
5. Security and user interface  

### 4.2 Device drivers

A **driver** is a translator between OS and a device (printer, graphics card).  
Without the correct driver, the printer may not print even if it is connected.

### 4.3 Language translators

Humans write **source code**. CPU needs **machine code** (0 and 1).

| Translator | How it works | Example languages |
|------------|--------------|-------------------|
| **Compiler** | Translates **whole program** first, then runs | C, C++ |
| **Interpreter** | Translates **line by line** and runs immediately | Python, BASIC (classic) |
| **Assembler** | Assembly language → machine code | NASM |
| **Linker** | Joins compiled object files into one executable | |
| **Loader** | Loads the executable into RAM to run | |

#### Compiler vs Interpreter (memorise)

| Point | Compiler | Interpreter |
|-------|----------|-------------|
| Translation | Entire program | One line at a time |
| Speed of running | Faster after compile | Slower |
| Error display | After full compile (list of errors) | Stops at first error |
| Object file | Creates `.exe` / object code | Usually no separate exe |
| Debugging | Slightly harder for beginners | Easier, immediate |
| Example | C | Python |

**Java special MCQ:** Java uses a **compiler** (to bytecode) **and** a **JVM interpreter/JIT**. So “both” can be correct if the option says so.

---

## 5. Application software

| Type | Examples | School use |
|------|----------|------------|
| Word processor | MS Word, Google Docs, LibreOffice Writer | Letters, notes |
| Spreadsheet | MS Excel, Calc | Marks, charts |
| Presentation | MS PowerPoint, Impress | Lessons |
| Browser | Chrome, Firefox, Edge | Internet |
| DBMS front-end | MS Access, MySQL tools | Records |
| DTP | PageMaker, InDesign, Publisher | School magazine |
| Accounting | Tally | Office |
| Education | Scratch, GeoGebra, DIKSHA apps | Teaching |
| Kannada | **Nudi**, Baraha | Official Kannada typing |
| Graphics | Paint, GIMP, Photoshop | Diagrams |
| Communication | Gmail, Outlook | Email |

**Freeware** = free to use, source not given (Adobe Reader).  
**Shareware** = try first, pay later.  
**Open source** = source code open (Linux, LibreOffice, Python).  
**Proprietary** = owned, licence needed (MS Windows, MS Office).  
**Public domain** = no copyright control.

---

## 6. Programming languages — levels

| Level | Meaning | Example |
|-------|---------|---------|
| **Machine** | 0 and 1 only | 10110000 |
| **Assembly** | Mnemonics | MOV, ADD |
| **High-level** | Near English | C, Python, Java |
| **4GL** | Very high, database-ish | SQL |
| **5GL** | Problem / AI oriented (rare term in papers) | Some AI tools |

**High-level advantages:** easy, portable, faster to write.  
**Disadvantage:** must be translated; a little slower than pure assembly.

---

## 7. Software related to starting the PC

| Name | Role |
|------|------|
| **BIOS / UEFI** | Firmware that tests hardware (POST) and starts boot |
| **Boot loader** | Loads the OS from disk |
| **POST** | Power On Self Test |

**Cold boot:** start from power off.  
**Warm boot:** restart (Ctrl+Alt+Del or Restart).

---

## 8. School teaching tip

Class 6 activity: show the same letter

1. handwritten  
2. typed in Word  
3. printed  

Ask: *Which part is hardware? Which is software?*

Never install unknown games on lab PCs. Teach **licensed / open-source / virus risk** from Day 1.

---

## 9. Practice MCQs

**1.** Windows is:  
a) Application  b) System software  c) Utility only  d) Firmware only  

**2.** MS Excel is:  
a) OS  b) Compiler  c) Application software  d) Driver  

**3.** A compiler translates:  
a) One line and stops always  b) The whole program  c) Only pictures  d) Only Kannada  

**4.** Nudi is mainly:  
a) Antivirus  b) Kannada software  c) A CPU brand  d) A topology  

**5.** Device driver is needed to:  
a) Cool the CPU  b) Help OS talk to a device  c) Increase voltage  d) Draw charts  

**6.** Linux is:  
a) Only a printer  b) Open-source OS  c) A spreadsheet  d) A port  

**7.** POST happens:  
a) When printing  b) When the computer is switched on  c) Only in Excel  d) In a browser  

**8.** Which is a utility?  
a) Antivirus  b) Keyboard  c) Monitor  d) CPU  

**9.** SQL is best called a:  
a) Machine language  b) 4GL / database language  c) Assembler  d) Device  

**10.** Shareware means:  
a) Always paid first  b) Try then pay  c) Only for government  d) Hardware share  

### Answers

1-b, 2-c, 3-b, 4-b, 5-b, 6-b, 7-b, 8-a, 9-b, 10-b

---

## 10. Descriptive 5-mark answer

**Question:** Explain types of software with examples.

1. **Definition** of software.  
2. **System software:** OS, drivers, compilers — example Windows, Ubuntu.  
3. **Application software:** Word, Excel, Chrome, Nudi.  
4. **Utility:** antivirus, backup, zip.  
5. **Conclusion:** hardware needs software; schools use both Office and open-source tools.

**Second common question:** Difference between compiler and interpreter — use the table in section 4.3.

---

## Quick revision box

- System = OS + drivers + translators  
- Application = user jobs  
- Utility = maintenance  
- Compiler = whole; Interpreter = line  
- Open source = Linux, LibreOffice  
- Nudi = Kannada  
- BIOS/UEFI + POST + boot  

---

## Homework

1. Draw the software tree.  
2. Write compiler vs interpreter table twice.  
3. List 5 system + 5 application + 3 utility names.

**Next:** [04 — CPU Organization](04-cpu-organization.md)
