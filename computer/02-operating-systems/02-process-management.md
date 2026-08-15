# Chapter OS-2 — Process Management

**Paper:** Paper-II Operating Systems  
**Time:** 60 minutes  
**Week:** 2, Day 11  

---

## Today's goal

1. Define process vs program  
2. Draw process state diagram  
3. Know PCB  
4. Know process vs thread  
5. Write 5 marks on process states  

---

## 1. Simple explanation

A **program** is a file on disk (like `chrome.exe`) — a recipe in a book.

A **process** is that program **while it is running** — the cook actually cooking.

One program can become many processes (two Chrome windows).  
The OS keeps a file for each process called the **PCB** (Process Control Block).

---

## 2. Definitions

> **Program:** a passive set of instructions stored on disk.  
> **Process:** an active instance of a program in execution.  
> **PCB:** a data structure the OS uses to store process ID, state, registers, memory info, open files, priority.  
> **Thread:** a lightweight unit of execution inside a process. Threads of one process share the same memory.

---

## 3. Process state diagram (must draw)

```
                 admit
  NEW ----------------------> READY
                               |  ^
                      dispatch |  | interrupt / timeout
                               v  |
                             RUNNING
                             /      \
                   I/O wait /        \ exit
                           v          v
                       WAITING      TERMINATED
                       (BLOCKED)
                           |
                           | I/O done
                           +-----> READY
```

| State | Meaning |
|-------|---------|
| **New** | Process is being created |
| **Ready** | Waiting for CPU; in RAM |
| **Running** | Using the CPU now |
| **Waiting / Blocked** | Waiting for I/O, key, or event |
| **Terminated / Exit** | Finished or killed |
| **Suspended** (extra) | Swapped to disk; not in main memory |

**Only one process runs on one CPU core at a given instant.** Others wait in Ready.

---

## 4. What is inside a process (memory image)

| Part | Content |
|------|---------|
| **Text / Code** | Instructions |
| **Data** | Global variables |
| **Heap** | Dynamic memory (`malloc`, objects) |
| **Stack** | Function calls, local variables |

---

## 5. Operations on processes

- **Create** (parent may fork a child)  
- **Schedule** (give CPU)  
- **Block / wake**  
- **Suspend / resume**  
- **Terminate** (normal exit or kill)  
- **IPC** — Inter-Process Communication: pipes, message queues, shared memory, sockets  

**Zombie process (Linux MCQ):** finished, but parent has not yet read its exit status.  
**Orphan:** parent died; `init`/`systemd` adopts it.

---

## 6. Process vs Thread

| Point | Process | Thread |
|-------|---------|--------|
| Weight | Heavy | Light |
| Memory | Own address space | Share process memory |
| Create time | Slower | Faster |
| Crash | One process usually isolated | A bad thread can hurt the whole process |
| Example | Word and Chrome | Chrome tab threads |

**Multithreading:** one process, many threads (browser: one thread download, one draw page).

---

## 7. Context switch

When CPU leaves process A and runs process B, OS saves A’s registers into A’s PCB and loads B’s. This is a **context switch**. It has a small time cost.

---

## 8. School teaching tip

Role-play: 5 students (processes), 1 chair (CPU). Only one sits. If a student “waits for water” (I/O), they leave the chair — another sits. This is process states + scheduling preview.

---

## 9. Practice MCQs

**1.** A program is ____; a process is ____.  
a) active, passive  b) passive, active  c) both hardware  d) both OS names  

**2.** PCB stores:  
a) Only wallpaper  b) Process information  c) Only toner  d) SMPS voltage  

**3.** A process waiting for a printer is in:  
a) Running  b) Ready  c) Waiting/Blocked  d) New  

**4.** Context switch means:  
a) Changing wall paint  b) Saving one process and loading another  c) Formatting disk  d) Compiling  

**5.** Threads of the same process share:  
a) Nothing  b) Address space  c) Different OS  d) Different CPUs always only  

**6.** How many processes run on one core at one instant?  
a) Unlimited  b) One  c) Exactly 10  d) Zero always  

**7.** Heap is used for:  
a) Boot firmware only  b) Dynamic memory  c) Only printing  d) CMOS  

**8.** Zombie process has:  
a) Finished but entry remains  b) Never started  c) Only GUI  d) No PID ever  

### Answers

1-b, 2-b, 3-c, 4-b, 5-b, 6-b, 7-b, 8-a

---

## 10. Descriptive 5-mark answer

**Question:** Explain process states with a neat diagram.

1. Define process.  
2. List New, Ready, Running, Waiting, Terminated with one line each.  
3. Explain Ready→Running (dispatch) and Running→Waiting (I/O).  
4. Draw the state diagram.  
5. Mention PCB stores the state.

---

## Quick revision box

- Program passive; process active  
- 5 states + diagram  
- PCB  
- Thread = light process  
- Context switch  
- Zombie / orphan  

---

## Homework

Draw the state diagram 3 times from memory. Write process vs thread table.

**Next:** [03 — CPU Scheduling](03-cpu-scheduling.md)
