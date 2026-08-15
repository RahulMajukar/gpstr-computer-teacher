# Chapter OS-4 — Memory Management

**Paper:** Paper-II OS  
**Time:** 60 minutes  
**Week:** 2, Day 13 (first half)  

---

## Today's goal

1. Why OS manages memory  
2. Fixed vs variable partitions  
3. Paging and virtual memory  
4. Fragmentation  
5. Page replacement names: FIFO, LRU, Optimal  

---

## 1. Simple explanation

RAM is a hostel with limited beds. Many processes want to sleep there.

The OS is the warden:

- gives beds (frames)  
- may send someone to a cheaper lodge (swap / virtual memory on disk)  
- must not give the same bed to two guests at once  

---

## 2. Definitions

> **Memory management** is the OS function of allocating, protecting, and freeing main memory for processes.

> **Virtual memory:** using disk as an extension of RAM so programs can be larger than physical memory.

> **Page:** fixed-size block of a process (e.g. 4 KB).  
> **Frame:** fixed-size block of physical RAM of the same size.  
> **Page table:** map from page number → frame number.

---

## 3. Techniques (exam list)

| Technique | Idea |
|-----------|------|
| **Single contiguous** | One user program in RAM (old) |
| **Fixed partition** | RAM cut into fixed rooms |
| **Variable partition** | Rooms sized to the process |
| **Paging** | Process cut into pages; RAM into frames; non-contiguous |
| **Segmentation** | Logical parts: code, data, stack |
| **Segmented paging** | Both |
| **Swapping** | Move a whole process to disk and back |

---

## 4. Fragmentation

| Type | Meaning | Typical where |
|------|---------|----------------|
| **Internal** | Wasted space **inside** an allocated block | Fixed partitions, last page of paging |
| **External** | Free holes **between** processes; total free is enough but not in one piece | Variable partitions |

**Compaction:** shift processes to join free holes (costly).  
**Paging** almost removes external fragmentation.

---

## 5. Allocation of free holes (variable partitions)

| Policy | Rule |
|--------|------|
| **First fit** | First hole that is big enough |
| **Best fit** | Smallest hole that fits (least leftover) |
| **Worst fit** | Largest hole |

---

## 6. Paging picture

```
Process pages          Physical frames
  Page 0  ------>        Frame 3
  Page 1  ------>        Frame 0
  Page 2  ------>        Frame 5
```

CPU generates a **logical address** = page number + offset.  
MMU (Memory Management Unit) converts to **physical address**.

**Page fault:** needed page is not in RAM; OS loads it from disk. Too many faults = **thrashing** (system spends all time paging).

---

## 7. Page replacement (when RAM is full)

| Algorithm | Rule | Note |
|-----------|------|------|
| **FIFO** | Remove oldest page | Simple; Belady’s anomaly possible |
| **LRU** | Remove Least Recently Used | Good; harder to implement perfectly |
| **Optimal** | Remove page used farthest in future | Best, theoretical |
| **Clock / Second chance** | Approximate LRU | |

**Belady’s anomaly:** more frames sometimes cause *more* page faults in FIFO (strange but asked).

---

## 8. Other words

- **Overlay:** old trick — load part of program, then another part  
- **Buddy system:** allocate sizes in powers of 2  
- **Protection:** one process cannot write another’s memory  

---

## 9. Practice MCQs

**1.** Virtual memory uses:  
a) Only ROM  b) Disk + RAM  c) Only cache  d) Printer  

**2.** External fragmentation is reduced by:  
a) Painting  b) Paging / compaction  c) More printers  d) BIOS only  

**3.** Page fault means:  
a) Page is in RAM  b) Page is not in RAM  c) OS crashed always  d) Keyboard error  

**4.** LRU removes:  
a) Newest page  b) Least recently used  c) Only OS pages  d) ROM  

**5.** Thrashing is:  
a) Too much paging  b) Too much printing  c) Fast cache  d) Cold boot  

**6.** Internal fragmentation happens:  
a) Between processes only  b) Inside allocated block  c) Only on CD  d) In ALU add  

**7.** Best fit chooses:  
a) Largest hole  b) Smallest sufficient hole  c) First hole always  d) No hole  

**8.** Belady’s anomaly is linked to:  
a) LRU  b) FIFO  c) Optimal  d) RR scheduling only  

### Answers

1-b, 2-b, 3-b, 4-b, 5-a, 6-b, 7-b, 8-b

---

## 10. Descriptive 5-mark answer

**Question:** Explain paging and virtual memory.

1. RAM limited; processes large.  
2. Process split into pages, RAM into frames.  
3. Page table maps pages to frames.  
4. Virtual memory keeps unused pages on disk.  
5. Page fault loads a page; too many faults = thrashing.  
6. Small diagram of pages → frames.

---

## Quick revision box

- Allocate / protect / free RAM  
- Internal vs external fragmentation  
- First / best / worst fit  
- Page + frame + page table  
- Virtual memory, page fault, thrashing  
- FIFO, LRU, Optimal  

---

**Next:** [05 — File Systems](05-file-systems.md)
