# Chapter DB-1 — Data, Databases, and Tables

**Paper:** Paper-I basic SQL idea + Paper-II DBMS  
**Time:** 50 minutes  
**Week:** 5, Day 29  

---

## Today's goal

1. Data vs information vs database  
2. Why DBMS, not just Excel  
3. Table, row, column, key  
4. DBMS vs file system  
5. Instances: MySQL, Oracle, MS Access  

---

## 1. Simple explanation

A school diary of marks on 20 papers gets lost, duplicated, and inconsistent.

A **database** is an organised collection of related data.  
A **DBMS** is software that stores, retrieves, and protects that data.

**Table** = spreadsheet-like grid:

| Roll | Name | Class | Marks |
|------|------|-------|-------|
| 1 | Asha | 7A | 78 |
| 2 | Ravi | 7A | 65 |

- **Row / Tuple / Record** = one student  
- **Column / Attribute / Field** = Name, Marks  
- **Cell** = one value  

---

## 2. Definitions

> **Data:** raw facts.  
> **Information:** processed, useful data.  
> **Database:** organised collection of related data.  
> **DBMS:** software to define, create, query, update, and administer databases.  
> **RDBMS:** DBMS based on tables (relations) — Codd’s relational model.

Examples: **MySQL, Oracle, SQL Server, PostgreSQL, SQLite, MS Access.**

---

## 3. Why DBMS? (advantages — 5 marks)

1. **Less redundancy** — one student address, not 10 copies  
2. **Consistency** — update once  
3. **Sharing** — many users with permissions  
4. **Security** — passwords, roles  
5. **Integrity** — rules (marks 0–100)  
6. **Backup and recovery**  
7. **Query language (SQL)** — powerful questions  
8. **Independence** — programs do not break if storage method changes  

**Disadvantages:** cost, trained staff, complexity for a tiny school list (Excel may be enough).

---

## 4. DBMS vs file system

| File system | DBMS |
|-------------|------|
| Separate files | Integrated database |
| Redundancy high | Controlled |
| Weak security | Stronger |
| No standard query | SQL |
| Concurrent access hard | Transactions |

---

## 5. Keys (learn now; used in ER and SQL)

| Key | Meaning |
|-----|---------|
| **Candidate** | Can uniquely identify a row |
| **Primary (PK)** | Chosen candidate; unique, not NULL |
| **Alternate** | Candidate not chosen as PK |
| **Foreign (FK)** | Column that refers to PK of another table |
| **Composite** | Key made of two+ columns |
| **Super key** | Any set that uniquely identifies (may have extras) |

Example: `Roll` is PK of Student. In Marks table, `Roll` is FK.

---

## 6. School teaching tip

Create a paper table of 5 students. Ask: *Which column can be primary key — Name or Roll? Why not Name?*

---

## 7. MCQs

1. Raw facts are: a) information b) data c) DBMS d) SQL  
2. Row is also called: a) attribute b) tuple c) schema only d) OS  
3. RDBMS stores data in: a) trees only b) tables c) only ROM d) stacks only  
4. Primary key can be NULL: a) yes b) no c) always d) only Friday  
5. MySQL is: a) a printer b) a DBMS c) a topology d) a gate  
6. Foreign key refers to: a) random file b) another table’s key c) ALU d) BIOS  

**Answers:** 1-b, 2-b, 3-b, 4-b, 5-b, 6-b

---

## 8. 5-mark answer

Define database + DBMS. Four advantages. Define table, PK. One school example (student marks).

---

**Next:** [02 — ER Models](02-er-models.md)
