# Chapter DB-6 — Transaction Management

**Paper:** Paper-II DBMS  
**Time:** 50 minutes  
**Week:** 5, Day 35  

---

## Today's goal

1. Define transaction  
2. ACID  
3. States: active → committed / aborted  
4. Commit / rollback  
5. Concurrency problems (names)  

---

## 1. Simple explanation

Transfer ₹100 from School A/c to Vendor A/c: subtract here, add there. If the power fails after subtract but before add, money vanishes.

A **transaction** is a bundle of steps that must **all happen or none**.

---

## 2. Definition

> A **transaction** is a single logical unit of work that may contain several database operations. It must leave the database consistent.

---

## 3. ACID (mandatory)

| Letter | Word | Meaning |
|--------|------|---------|
| **A** | Atomicity | All or nothing |
| **C** | Consistency | Rules remain true (totals balance) |
| **I** | Isolation | Concurrent transactions do not mess each other |
| **D** | Durability | After COMMIT, data survives crash |

---

## 4. States

```
         +--------+
         | ACTIVE |
         +---+----+
             |
        +----+-----+
        |          |
        v          v
  PARTIALLY     FAILED
   COMMITTED        |
        |           v
        v        ABORTED ---- undo (rollback)
   COMMITTED
```

- **COMMIT:** make changes permanent  
- **ROLLBACK:** undo to the start (or savepoint)  

---

## 5. Concurrency problems (MCQ names)

If two users edit the same row without control:

| Problem | Idea |
|---------|------|
| **Lost update** | One write overwrites another |
| **Dirty read** | Read uncommitted data |
| **Non-repeatable read** | Same read, different value |
| **Phantom** | New rows appear in a range |

**Control:** locks (shared/exclusive), timestamps, isolation levels.

**Deadlock** can happen with locks — same idea as OS deadlock.

---

## 6. Log and recovery (short)

DBMS writes a **log** before changing data (**WAL** — write ahead log, name optional). After crash, REDO committed, UNDO uncommitted.

---

## 7. MCQs

1. Atomicity means: a) slow b) all or nothing c) many copies d) no SQL  
2. After COMMIT, property is: a) isolation only b) durability c) dirty read d) phantom only  
3. ROLLBACK does: a) save forever b) undo c) GRANT d) DROP OS  
4. Dirty read is: a) read committed only b) read uncommitted c) a virus d) a stack  
5. ACID ‘I’ is: a) Index b) Isolation c) Internet d) Insert  
6. Transaction is: a) a picture b) a logical unit of work c) a printer d) a gate  

**Answers:** 1-b, 2-b, 3-b, 4-b, 5-b, 6-b

---

## 8. 5-mark answer

Define transaction. Expand ACID with one line each. Draw states. Mention COMMIT and ROLLBACK. Bank/school fee example.

---

**Next:** [07 — DBMS Practice](07-chapter-practice.md)
