# Chapter PR-6 — Stacks and Queues

**Paper:** Paper-II Data Structures  
**Time:** 55 minutes  
**Week:** 3, Day 20  

---

## Today's goal

1. Define stack LIFO and queue FIFO  
2. Operations: push/pop, enqueue/dequeue  
3. Overflow / underflow  
4. Applications  
5. Draw both  

---

## 1. Stack — plate stand

The last plate you put is the first you take. **LIFO — Last In First Out.**

```
        | 30 |  <-- TOP
        | 20 |
        | 10 |
        +----+
```

> A **stack** is a linear data structure that allows insertion and deletion only at one end called the **top**.

| Operation | Meaning |
|-----------|---------|
| **Push** | Add at top |
| **Pop** | Remove from top |
| **Peek / Top** | See top without remove |
| **isEmpty** | Underflow check |
| **isFull** | Overflow (array stack) |

**Overflow:** push when full.  
**Underflow:** pop when empty.

### Applications of stack (memorise 5)

1. Undo in Word  
2. Browser **Back** button  
3. Recursion / function calls  
4. Evaluating expressions / parentheses matching  
5. Reverse a string  

---

## 2. Queue — school lunch line

First child in line is first served. **FIFO — First In First Out.**

```
FRONT --> 10 --> 20 --> 30 --> REAR
```

> A **queue** is a linear data structure that inserts at the **rear** and deletes at the **front**.

| Operation | Meaning |
|-----------|---------|
| **Enqueue** | Insert at rear |
| **Dequeue** | Delete at front |
| **Peek** | See front |

### Types of queue

| Type | Idea |
|------|------|
| **Simple** | One line |
| **Circular** | End connects to start (uses space better) |
| **Priority** | High priority served first |
| **Deque** | Double ended — insert/delete both ends |

### Applications of queue

1. Printer spooler  
2. Ticket / lunch line  
3. CPU scheduling (FCFS, RR ready queue)  
4. Call centre waiting  
5. Breadth-first search (name only)

---

## 3. Stack vs Queue

| Point | Stack | Queue |
|-------|-------|-------|
| Principle | LIFO | FIFO |
| Ends | One (top) | Two (front, rear) |
| Insert | Push | Enqueue |
| Delete | Pop | Dequeue |
| Example | Plates, undo | Queue at office |

---

## 4. Dry-run stack

Empty. Push 5, Push 8, Pop, Push 3.

| Step | Stack (bottom→top) |
|------|---------------------|
| Push 5 | 5 |
| Push 8 | 5, 8 |
| Pop | 5 (8 removed) |
| Push 3 | 5, 3 |

---

## 5. MCQs

1. LIFO is: a) Queue b) Stack c) Tree only d) OS  
2. Pop from empty stack: a) Overflow b) Underflow c) Compile d) Boot  
3. Undo uses: a) Queue b) Stack c) MICR d) ROM  
4. Printer jobs use: a) Stack mainly b) Queue c) XOR d) Cache only  
5. Deque allows: a) only one end b) both ends c) no insert d) only ROM  
6. Circular queue helps: a) waste less space b) LIFO c) compilers only d) hex  

**Answers:** 1-b, 2-b, 3-b, 4-b, 5-b, 6-a

---

## 6. 5-mark answer

Define stack + LIFO + push/pop + 2 applications + small diagram.  
OR compare stack and queue in a table + one application each.

---

## Homework

Dry-run: queue enqueue 1,2,3 dequeue twice enqueue 4. Write remaining elements.

**Next:** [07 — OOPs Concepts](07-oops-concepts.md)
