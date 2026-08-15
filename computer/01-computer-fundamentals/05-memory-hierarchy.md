# Chapter 5 — Memory Hierarchy and Memory Types

**Paper:** Paper-I + Paper-II  
**Time:** 60 minutes  
**Week:** 1, Day 5  

---

## Today's goal

1. Draw the memory pyramid  
2. Differentiate RAM, ROM, cache, register, HDD/SSD  
3. Know RAM types (SRAM, DRAM) and ROM types  
4. Convert storage units  
5. Write 5 marks on memory hierarchy  

---

## 1. Simple explanation

The CPU is extremely fast. A hard disk is slow. If the CPU always waited for the disk, the computer would crawl.

So designers keep a **ladder of memories**:

- smallest and fastest next to the CPU  
- largest and cheapest far away  

This ladder is the **memory hierarchy**.

School picture:

| Place | Like | Speed | Size |
|-------|------|-------|------|
| Registers | Words in your mouth | Fastest | Tiny |
| Cache | Notes on the desk | Very fast | Small |
| RAM | Open textbooks on the table | Fast | Medium |
| SSD/HDD | Books in the almirah | Slow | Huge |
| Cloud / tape | Books in another building | Slowest | Enormous |

---

## 2. Exam definition

> **Memory hierarchy** is the arrangement of storage devices in levels from fastest/smallest (registers) to slowest/largest (secondary and tertiary storage) to give the CPU data as quickly as possible at a reasonable cost.

> **Primary memory:** memory the CPU can address directly (RAM, ROM, cache).  
> **Secondary memory:** online storage for files (HDD, SSD, pen drive).  
> **Tertiary / offline:** backup tapes, optical archives.

---

## 3. The pyramid (draw in exam)

```
                    /\
                   /  \          Registers
                  /----\         Cache (L1, L2, L3)
                 /      \        Main memory (RAM)
                /--------\       SSD / HDD
               /          \      Optical, tape, cloud
              /____________\
           FAST + COSTLY              SLOW + CHEAP
           SMALL                      LARGE
```

**Principle of locality:** programs reuse nearby data (spatial) and recent data (temporal). Cache works because of this.

---

## 4. Primary memory

### 4.1 RAM — Random Access Memory

- **Volatile:** data lost when power is off  
- Read and write  
- Holds running OS, programs, and data  

| Type | Full form | Note |
|------|-----------|------|
| **DRAM** | Dynamic RAM | Cheap, needs refresh; used as main RAM |
| **SRAM** | Static RAM | Faster, no refresh, costlier; used in **cache** |
| **SDRAM** | Synchronous DRAM | Synced to system clock |
| **DDR, DDR2, DDR3, DDR4, DDR5** | Double Data Rate | Each generation faster; school PCs often DDR3/DDR4 |
| **DIMM / SODIMM** | Module shapes | Desktop / laptop sticks |

**Virtual memory:** part of HDD/SSD used as extra RAM (page file / swap). Slower than real RAM.

### 4.2 ROM — Read Only Memory

- **Non-volatile:** keeps data without power  
- Stores **bootstrap / BIOS / firmware**  
- Traditionally read-only; some types can be updated  

| Type | Meaning |
|------|---------|
| **MROM** | Mask ROM — factory programmed |
| **PROM** | Programmable once |
| **EPROM** | Erasable with **UV light** |
| **EEPROM** | Electrically erasable |
| **Flash** | Modern EEPROM family; BIOS/UEFI, pendrives, SSDs |

### 4.3 Cache memory

- Very fast SRAM between CPU and RAM  
- **L1:** inside core, smallest, fastest  
- **L2:** larger, a bit slower  
- **L3:** shared among cores on many CPUs  

**Hit:** data found in cache (good).  
**Miss:** must go to RAM (slower).

### 4.4 Registers

Already in CPU chapter. Fastest. Measured in bits/words, not GB.

---

## 5. Secondary memory

| Device | Volatile? | Notes |
|--------|-----------|-------|
| **HDD** | No | Magnetic disks, tracks, sectors, cylinders |
| **SSD** | No | Flash; faster; limited write cycles but fine for school |
| **Pen drive / USB flash** | No | Portable |
| **Memory card** | No | SD, microSD |
| **CD / DVD / Blu-ray** | No | Optical; 700 MB / 4.7 GB / 25 GB (single layer typical) |
| **Floppy** | No | 1.44 MB — history MCQ only |

**HDD terms:**

- **Platter, track, sector, cylinder**  
- **RPM:** 5400 / 7200  
- **Access time** = seek + rotational delay + transfer  

**Formatting:** prepares disk with file system (NTFS, FAT32, ext4).

---

## 6. Units (write until automatic)

```
4 bits  = 1 nibble
8 bits  = 1 byte
1024 B  = 1 KB
1024 KB = 1 MB
1024 MB = 1 GB
1024 GB = 1 TB
1024 TB = 1 PB
```

**Word:** CPU-dependent (16/32/64 bits).  
**Character:** often 1 byte in ASCII; Unicode may use 2 or more.

---

## 7. RAM vs ROM (classic 5-mark table)

| Point | RAM | ROM |
|-------|-----|-----|
| Full form | Random Access Memory | Read Only Memory |
| Volatile | Yes | No |
| Read/Write | Both | Mostly read |
| Use | Running programs | Boot / firmware |
| Speed | Fast | Varies; not for main workspace |
| Size in PC | 4–32 GB typical | Few MB for BIOS |

---

## 8. Other exam words

| Word | Meaning |
|------|---------|
| **Volatile** | Needs power to keep data |
| **Non-volatile** | Keeps data without power |
| **Sequential access** | Magnetic tape — must wind |
| **Direct / random access** | RAM, disk — jump to location |
| **Buffer** | Temporary holding area |
| **PROM programmer** | Device to burn PROM |

---

## 9. School teaching tip

Use **school bags**:

- Register = one chit in hand  
- RAM = open bag on bench (emptied when “school over” / power off)  
- ROM = printed timetable stuck on wall (stays)  
- HDD = locked cupboard  

---

## 10. Practice MCQs

**1.** Which is volatile?  
a) ROM  b) HDD  c) RAM  d) CD  

**2.** Cache is usually made of:  
a) DRAM  b) SRAM  c) Magnetic tape  d) Paper  

**3.** BIOS is typically stored in:  
a) RAM  b) Cache  c) ROM / Flash  d) Register  

**4.** 1 GB =  
a) 1024 MB  b) 1000 KB  c) 1024 TB  d) 8 bits  

**5.** Virtual memory uses:  
a) Only registers  b) Disk space as extra RAM  c) Only ROM  d) Printer memory  

**6.** EPROM is erased by:  
a) Hammer  b) UV light  c) Only scissors  d) Cooling  

**7.** Fastest memory among these:  
a) HDD  b) RAM  c) Register  d) CD  

**8.** SSD has:  
a) Spinning platters  b) Flash memory chips  c) Only vacuum tubes  d) Only ROM mask  

**9.** L1 cache is:  
a) Largest and slowest  b) Smallest and fastest cache  c) A printer  d) A topology  

**10.** Floppy disk capacity (classic 3.5"):  
a) 4.7 GB  b) 700 MB  c) 1.44 MB  d) 1 TB  

### Answers

1-c, 2-b, 3-c, 4-a, 5-b, 6-b, 7-c, 8-b, 9-b, 10-c

---

## 11. Descriptive 5-mark answer

**Question:** Explain memory hierarchy with a diagram.

1. Definition.  
2. Levels: registers → cache → RAM → secondary → tertiary.  
3. As we go down: speed ↓, size ↑, cost per bit ↓.  
4. RAM volatile; ROM and disk non-volatile.  
5. Cache reduces the speed gap between CPU and RAM.  
6. Draw the pyramid.

---

## Quick revision box

- Hierarchy pyramid  
- RAM volatile; ROM not  
- DRAM = main; SRAM = cache  
- PROM / EPROM / EEPROM / Flash  
- L1 < L2 < L3 (size grows, speed drops)  
- 1024 chain  
- Virtual memory = disk as RAM  

---

## Homework

1. Draw pyramid from memory.  
2. RAM vs ROM table.  
3. Convert: 2 GB = ? MB; 4096 KB = ? MB.

**Next:** [06 — I/O Devices](06-io-devices.md)
