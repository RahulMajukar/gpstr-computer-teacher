# Chapter DB-4 — SQL Queries (Write on Paper)

**Paper:** Paper-I basic SQL + Paper-II  
**Time:** 80 minutes (Days 32–33) — this is a **drill chapter**  

---

## Today's goal

1. DDL vs DML vs DCL vs TCL  
2. CREATE, INSERT, SELECT, UPDATE, DELETE  
3. WHERE, ORDER BY, GROUP BY, JOIN  
4. Write 25 queries on a school table  
5. No computer needed — paper is the exam  

---

## 1. What is SQL?

> **SQL (Structured Query Language)** is the standard language to talk to a relational database.

Not a full programming language like C; it is a **query + definition** language (4GL in some books).

---

## 2. SQL command families

| Family | Job | Commands |
|--------|-----|----------|
| **DDL** | Define structure | CREATE, ALTER, DROP, TRUNCATE |
| **DML** | Change / read data | SELECT, INSERT, UPDATE, DELETE |
| **DCL** | Rights | GRANT, REVOKE |
| **TCL** | Transactions | COMMIT, ROLLBACK, SAVEPOINT |
| **DQL** | Some books put SELECT alone | SELECT |

**TRUNCATE** removes all rows (DDL-ish); structure stays.  
**DROP** removes the table itself.

---

## 3. School database we will use

```sql
CREATE TABLE student (
    roll INT PRIMARY KEY,
    name VARCHAR(40) NOT NULL,
    class VARCHAR(10),
    marks INT,
    city VARCHAR(20)
);
```

Imagine rows:

| roll | name | class | marks | city |
|------|------|-------|-------|------|
| 1 | Asha | 7A | 78 | Mysuru |
| 2 | Ravi | 7A | 65 | Bengaluru |
| 3 | Kiran | 8B | 91 | Mysuru |
| 4 | Divya | 8B | 40 | Hubballi |

---

## 4. INSERT / UPDATE / DELETE

```sql
INSERT INTO student VALUES (5, 'Naveen', '7A', 55, 'Belagavi');

UPDATE student SET marks = 70 WHERE roll = 2;

DELETE FROM student WHERE roll = 4;
```

**Danger:** `DELETE FROM student;` without WHERE deletes **all rows**.

---

## 5. SELECT patterns (memorise)

```sql
SELECT * FROM student;
SELECT name, marks FROM student;
SELECT DISTINCT city FROM student;
SELECT * FROM student WHERE marks >= 60;
SELECT * FROM student WHERE city = 'Mysuru' AND marks > 70;
SELECT * FROM student WHERE name LIKE 'A%';
SELECT * FROM student WHERE class IN ('7A', '8B');
SELECT * FROM student WHERE marks BETWEEN 60 AND 80;
SELECT * FROM student ORDER BY marks DESC;
SELECT class, COUNT(*) FROM student GROUP BY class;
SELECT class, AVG(marks) FROM student GROUP BY class HAVING AVG(marks) > 70;
```

| Clause | Job |
|--------|-----|
| WHERE | Filter rows |
| ORDER BY | Sort (ASC / DESC) |
| GROUP BY | Cluster for aggregates |
| HAVING | Filter **groups** (after GROUP BY) |

**Aggregates:** `COUNT SUM AVG MIN MAX`

**LIKE:** `%` any string, `_` one character.

---

## 6. Constraints (CREATE)

`PRIMARY KEY`, `FOREIGN KEY`, `UNIQUE`, `NOT NULL`, `CHECK (marks BETWEEN 0 AND 100)`, `DEFAULT`

---

## 7. JOIN (two tables)

```sql
CREATE TABLE enrol (
    roll INT,
    code VARCHAR(10),
    PRIMARY KEY (roll, code)
);

SELECT student.name, enrol.code
FROM student, enrol
WHERE student.roll = enrol.roll;

-- or
SELECT s.name, e.code
FROM student s INNER JOIN enrol e ON s.roll = e.roll;
```

---

## 8. Twenty-five paper drills (do all)

On `student` table write SQL for:

1. All rows  
2. Only names  
3. Students of 7A  
4. Marks above 75  
5. Mysuru students with marks ≥ 70  
6. Names starting with K  
7. Sorted by name  
8. Highest marks first  
9. Count of students  
10. Average marks  
11. Maximum marks  
12. Count per class  
13. Classes whose average > 70  
14. Distinct cities  
15. Marks between 50 and 80  
16. Insert one new student  
17. Increase all 7A marks by 5  
18. Delete students below 35  
19. Add column `phone`  
20. Students not from Mysuru (`<>` or `NOT`)  
21. Topper name (`ORDER BY marks DESC` + idea of limit)  
22. Rename table (syntax `RENAME` / `ALTER`)  
23. Students in 7A **or** 8B  
24. Null city list (`IS NULL`)  
25. Inner join names with course codes  

Write answers in the notebook. Sample for (3):

```sql
SELECT * FROM student WHERE class = '7A';
```

---

## 9. MCQs

1. SELECT is mainly: a) DDL b) DML/DQL c) DCL d) hardware  
2. WHERE filters: a) columns b) rows c) databases d) users only  
3. HAVING is used with: a) ORDER only b) GROUP BY c) INSERT d) DROP  
4. PRIMARY KEY implies: a) duplicates ok b) unique + not null c) always text d) always 10  
5. `LIKE 'A%'` matches: a) ending A b) starting A c) only AAA d) none  
6. DROP TABLE: a) deletes rows only b) removes table c) only sorts d) grants  

**Answers:** 1-b, 2-b, 3-b, 4-b, 5-b, 6-b

---

## 10. 5-mark answer

**Question:** Write SQL to create a student table and display students who scored more than 60, sorted by marks.

Write CREATE + INSERT one row + SELECT with WHERE and ORDER BY. Label DDL and DML.

---

## Homework

Finish all 25 queries. Re-write any 10 the next morning from memory.

**Next:** [05 — Normalization](05-normalization.md)
