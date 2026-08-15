# Chapter OS-6 — Deadlocks

**Paper:** Paper-II OS  
**Time:** 55 minutes  
**Week:** 2, Day 14  

---

## Today's goal

1. Define deadlock with a school story  
2. Four Coffman conditions  
3. Prevention, avoidance, detection, ignore  
4. Banker’s algorithm idea  
5. Write a full 5-mark answer  

---

## 1. Simple explanation (never forget this story)

Two children. One has a **scale**, needs an **eraser**. The other has the **eraser**, needs the **scale**. Neither leaves the thing they hold. Both wait forever.

That is **deadlock**.

In OS: Process A holds a printer and wants the tape drive. Process B holds the tape drive and wants the printer.

---

## 2. Exam definition

> A **deadlock** is a situation in which a set of processes are blocked because each process is holding a resource and waiting for another resource held by some other process in the set.

---

## 3. Four necessary conditions (Coffman) — all four must be true

Remember **MHNC** or **“Can All People Circle?”** — better: **M-H-N-C**

| # | Condition | Meaning |
|---|-----------|---------|
| 1 | **Mutual exclusion** | Resource cannot be shared (one printer) |
| 2 | **Hold and wait** | Process holds one resource and waits for another |
| 3 | **No preemption** | You cannot forcibly snatch the resource |
| 4 | **Circular wait** | A waits for B, B waits for C, C waits for A |

If **any one** is broken, deadlock cannot occur.

---

## 4. Resource Allocation Graph (RAG)

Circles = processes. Squares = resources. Arrow P→R means “wants”. Arrow R→P means “holds”.

A **cycle** may mean deadlock (for single-instance resources, cycle ⇒ deadlock).

---

## 5. Handling deadlock (4 strategies)

### 5.1 Ignore (Ostrich)

Windows/Linux often **ignore** rare deadlocks and let the user restart. Cheap. Asked in MCQ.

### 5.2 Prevention — break a condition

| Break | How |
|-------|-----|
| Mutual exclusion | Share if possible (read-only files) |
| Hold and wait | Take **all** resources at start |
| No preemption | OS can take resources away |
| Circular wait | Number resources; request only in increasing order |

### 5.3 Avoidance — Banker’s algorithm (Dijkstra)

Do not give a resource if the system would go into an **unsafe** state.

Like a banker: lend only if you can still satisfy every customer’s remaining need in some order.

**Safe state:** there exists an order to finish all processes.  
**Unsafe:** not necessarily deadlock yet, but danger.

You need: total resources, allocated, remaining need, available.

(For GPSTR, **idea + terms** are enough; a 3-process numerical may appear — practise one from any OS book.)

### 5.4 Detection and recovery

Allow deadlock, **detect** cycle, then:

- Kill one or more processes  
- Preempt resources  
- Rollback  

---

## 6. Deadlock vs starvation vs livelock

| Term | Meaning |
|------|---------|
| **Deadlock** | Circular wait; nobody progresses |
| **Starvation** | One process waits too long (low priority) |
| **Livelock** | Processes change state but still get no work done (two people always stepping aside the same way) |

---

## 7. School teaching tip

Two students, one scale, one eraser. Freeze the class when both wait. Then ask: *Which Coffman condition shall we break?* (Teacher snatches scale = preemption.)

---

## 8. Practice MCQs

**1.** Deadlock needs how many Coffman conditions together?  
a) 1  b) 2  c) 3  d) 4  

**2.** Banker’s algorithm is for:  
a) Deadlock avoidance  b) Disk speed  c) Compiling  d) GUI themes  

**3.** Circular wait means:  
a) CPU fan circle  b) Cycle of processes waiting  c) Only RR  d) Hex loop  

**4.** Ostrich approach means:  
a) Detect always  b) Ignore deadlock  c) Banker always  d) Kill all at start  

**5.** Safe state means:  
a) Virus free only  b) There is a sequence to finish all  c) No RAM  d) Only one process ever  

**6.** Starvation is:  
a) Same as deadlock always  b) Indefinite waiting of one process  c) A file system  d) A port  

**7.** Hold and wait means:  
a) Hold nothing  b) Hold some, wait for more  c) Only GUI  d) Only ROM  

**8.** Who gave Banker’s algorithm?  
a) Dijkstra  b) Babbage  c) Boole  d) Turing only  

### Answers

1-d, 2-a, 3-b, 4-b, 5-b, 6-b, 7-b, 8-a

---

## 9. Descriptive 5-mark answer

**Question:** What is deadlock? Explain the necessary conditions and any two methods to handle it.

1. Definition + two-process printer story.  
2. Four conditions named and one line each.  
3. Prevention (break a condition) + Avoidance (Banker) **or** Detection.  
4. Mention ignore method in desktop OS.  
5. Optional RAG cycle.

---

## Quick revision box

- Forever wait + cycle  
- 4 conditions: ME, Hold-wait, No preemption, Circular wait  
- Prevent / Avoid (Banker) / Detect / Ignore  
- Safe vs unsafe  
- Deadlock ≠ starvation  

---

**Next:** [07 — Windows and Linux Basics](07-windows-and-linux.md)
