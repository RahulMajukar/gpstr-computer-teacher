# Chapter DB-5 — Normalization

**Paper:** Paper-II DBMS  
**Time:** 60 minutes  
**Week:** 5, Day 34  

---

## Today's goal

1. Why we normalise  
2. Anomaly types  
3. 1NF, 2NF, 3NF, BCNF  
4. Functional dependency idea  
5. Normalise a bad school table  

---

## 1. Simple explanation

If one table stores student + all subjects + teacher phone + class teacher address, then:

- Changing a teacher phone means **many rows**  
- Deleting the last student of a course **loses the course**  
- Adding a new course **needs a fake student**

These are **anomalies**. **Normalization** splits tables so each fact is stored once.

---

## 2. Definitions

> **Normalization:** a process of organising attributes into tables to reduce redundancy and improve integrity, using normal forms.

> **Functional dependency (FD):** A → B means B is determined by A (Roll → Name).

**Anomalies:** insertion, deletion, update.

---

## 3. Normal forms (memorise the test)

### 1NF — First Normal Form

- Atomic (single) values — no lists in a cell  
- No repeating groups  

Bad: `subjects = "Maths, Science"`  
Good: one subject per row, or a separate table.

### 2NF — Second Normal Form

- Must be in 1NF  
- **No partial dependency** of non-key on part of a composite key  

If key is (Roll, Subject) and Name depends only on Roll, Name must leave this table.

### 3NF — Third Normal Form

- Must be in 2NF  
- **No transitive dependency** (non-key → another non-key)  

If Roll → TeacherId and TeacherId → TeacherPhone, phone should be in TEACHER table, not STUDENT.

### BCNF — Boyce–Codd

- Stronger 3NF  
- For every FD X → Y, X must be a **super key**  
- Rare extra cases where 3NF is not enough  

Higher names (4NF, 5NF) — **name only** for this exam.

---

## 4. Worked example

**Unnormalised**

| roll | name | subject | teacher | teacher_phone |
|------|------|---------|---------|---------------|
| 1 | Asha | Maths | Rao | 999 |
| 1 | Asha | Science | Iyer | 888 |

**1NF:** already atomic if one subject per row.

**2NF:** Name depends only on roll → `STUDENT(roll, name)` and `MARKS(roll, subject, teacher…)`

**3NF:** teacher_phone depends on teacher → `TEACHER(teacher, phone)` and `TEACHES(roll, subject, teacher)`

---

## 5. Denormalization (one line)

Sometimes we **join tables back** for speed in reports. Exam: know the word.

---

## 6. MCQs

1. 1NF needs: a) lists in cells b) atomic values c) only 3 tables d) no keys  
2. Partial dependency is removed in: a) 1NF b) 2NF c) only BCNF d) SQL  
3. Transitive dependency removed in: a) 1NF b) 2NF c) 3NF d) OS  
4. Update anomaly means: a) virus b) same fact changed in many places c) boot fail d) deadlock always  
5. BCNF is: a) weaker than 1NF b) stronger than 3NF c) a Linux command d) a port  
6. FD A→B means: a) B determines A always b) A determines B c) no relation d) join only  

**Answers:** 1-b, 2-b, 3-c, 4-b, 5-b, 6-b

---

## 7. 5-mark answer

Define normalization + 3 anomalies. Write 1NF, 2NF, 3NF rules. Give the student-subject-teacher split as example.

---

**Next:** [06 — Transactions](06-transactions.md)
