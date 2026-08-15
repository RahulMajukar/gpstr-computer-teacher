# Chapter OS-3 — CPU Scheduling

**Paper:** Paper-II OS  
**Time:** 65 minutes  
**Week:** 2, Day 12  

---

## Today's goal

1. Why we schedule  
2. Criteria: TAT, WT, RT  
3. FCFS, SJF, Priority, Round Robin  
4. Preemptive vs non-preemptive  
5. Solve one small Gantt chart  

---

## 1. Simple explanation

Many processes want the CPU. Only one core can run one process now.

The **scheduler** is the period-allotment clerk. Different schools use different rules:

- First come first served (queue at the office)  
- Shortest work first (quick signatures first)  
- Priority (HM’s file first)  
- Time table slices (every class gets 10 minutes) — **Round Robin**

---

## 2. Definitions

> **CPU scheduling** is the method by which the OS selects the next ready process for the CPU.

| Word | Meaning |
|------|---------|
| **Preemptive** | OS can snatch CPU before the process finishes |
| **Non-preemptive** | Process keeps CPU until it waits or ends |
| **Arrival time (AT)** | When process enters ready queue |
| **Burst time (BT)** | CPU time the process needs |
| **Completion time (CT)** | When it finishes |
| **Turnaround time (TAT)** | CT − AT (total time in system) |
| **Waiting time (WT)** | TAT − BT (time in ready queue)  
| **Response time** | First CPU chance − AT |
| **Throughput** | Processes finished per unit time |
| **Gantt chart** | Time-line bar of who used CPU |

**Goals:** high CPU use, high throughput, low WT and TAT, fairness.

---

## 3. Algorithms

### 3.1 FCFS — First Come First Served

- Non-preemptive  
- Queue order  
- Simple  
- **Convoy effect:** one long process makes short ones wait  

### 3.2 SJF — Shortest Job First

- Pick smallest burst  
- Best average WT (among non-preemptive)  
- **Starvation:** long jobs may wait forever  
- Need to know burst in advance (hard in real life)

**SRTF** = Shortest Remaining Time First = preemptive SJF.

### 3.3 Priority scheduling

- Highest priority runs first (note: some books use “low number = high priority”)  
- Can be preemptive or not  
- **Starvation** of low priority  
- **Ageing:** slowly raise priority of waiting jobs  

### 3.4 Round Robin (RR)

- Each process gets a **time quantum** (e.g. 4 ms)  
- If not finished, go to the tail of the queue  
- Preemptive  
- Fair; good for time-sharing  
- Too small quantum → too many context switches  
- Too large → becomes like FCFS  

### 3.5 Multilevel queue / feedback (name only)

Different queues for system / interactive / batch. Feedback can move a process between queues.

---

## 4. Worked example (learn the method)

Processes (all arrive at 0):

| Process | Burst |
|---------|-------|
| P1 | 5 |
| P2 | 3 |
| P3 | 1 |

**FCFS order P1, P2, P3**

```
|  P1  | P2 |P3|
0      5    8  9
```

TAT: P1=5, P2=8, P3=9. Average TAT = 22/3 ≈ 7.33  
WT: P1=0, P2=5, P3=8. Average WT = 13/3 ≈ 4.33

**SJF order P3, P2, P1**

```
|P3| P2 |  P1  |
0  1    4      9
```

WT: 0, 1, 4. Average WT = 5/3 ≈ 1.67 (better than FCFS)

**RR quantum = 2**, order P1, P2, P3…

```
P1(2), P2(2), P3(1), P1(2), P2(1), P1(1)
```

Practise drawing this once in the notebook.

---

## 5. School teaching tip

Give 3 students “work times” 5, 3, 1 minutes and one chair. Try FCFS then SJF. Children *feel* waiting time. This is a pedagogy gold example.

---

## 6. Practice MCQs

**1.** Convoy effect is in:  
a) SJF  b) FCFS  c) RR only  d) Paging  

**2.** Time quantum is used in:  
a) FCFS  b) Round Robin  c) Only SJF  d) Disk format  

**3.** Starvation can happen in:  
a) Only FCFS  b) Priority / SJF  c) Only cold boot  d) Only GUI  

**4.** Ageing is used to:  
a) Cool CPU  b) Prevent starvation  c) Increase RAM chips  d) Draw Gantt in Excel only  

**5.** TAT =  
a) BT − AT  b) CT − AT  c) WT − BT  d) AT − CT  

**6.** Which is preemptive?  
a) FCFS  b) Non-preemptive SJF  c) Round Robin  d) None  

**7.** Very small RR quantum causes:  
a) Fewer switches  b) Many context switches  c) No processes  d) ROM wipe  

**8.** Waiting time =  
a) TAT − BT  b) BT − TAT  c) CT + AT  d) Quantum only  

### Answers

1-b, 2-b, 3-b, 4-b, 5-b, 6-c, 7-b, 8-a

---

## 7. Descriptive 5-mark answer

**Question:** Explain any three CPU scheduling algorithms.

Write FCFS, SJF, RR: rule + one merit + one demerit each. Mention preemptive/non-preemptive. Optional tiny Gantt.

---

## Quick revision box

- TAT = CT−AT; WT = TAT−BT  
- FCFS convoy  
- SJF low average wait; starvation  
- Priority + ageing  
- RR + quantum  
- Gantt chart  

---

## Homework

Solve FCFS and SJF for bursts 8, 4, 2, 1 (all AT=0). Find average WT.

**Next:** [04 — Memory Management](04-memory-management.md)
