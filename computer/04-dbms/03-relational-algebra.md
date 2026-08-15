# Chapter DB-3 — Relational Algebra

**Paper:** Paper-II DBMS  
**Time:** 50 minutes  
**Week:** 5, Day 31  

---

## Today's goal

1. Relation = table  
2. Select, project, union, set difference, cartesian, rename  
3. Join types at idea level  
4. Connect algebra to SQL  

---

## 1. Simple explanation

**Relational algebra** is a set of operations on tables that produce new tables. It is the **math behind SQL**.

You do not need long proofs. You need **symbols and one example each**.

---

## 2. Core operations (Codd)

### Selection σ (sigma) — choose **rows**

```
σ marks>70 (STUDENT)
```

SQL cousin: `WHERE marks > 70`

### Projection π (pi) — choose **columns**

```
π name, marks (STUDENT)
```

SQL cousin: `SELECT name, marks`

### Union ∪

Rows in A or B (same columns). Duplicates removed.

### Set difference −

Rows in A but not in B.

### Cartesian product ×

Every row of A with every row of B. Usually too big; we then select matching keys (that becomes join).

### Rename ρ (rho)

Give a new name to a relation or attributes.

---

## 3. Join (very important)

**Join** = combine related rows.

| Join | Idea |
|------|------|
| **Inner / equi** | Only matching keys |
| **Natural join ⋈** | Match common attribute names |
| **Left outer** | All left rows; right may be NULL |
| **Right outer** | All right rows |
| **Full outer** | All from both |
| **Theta join** | Any condition, not only = |

Example: Student ⋈ Enrol (on roll) → names with course codes.

---

## 4. Mini example

STUDENT

| roll | name | class |
|------|------|-------|
| 1 | Asha | 7A |
| 2 | Ravi | 7B |

```
σ class='7A' (STUDENT)     → only Asha
π name (STUDENT)           → Asha, Ravi
```

---

## 5. MCQs

1. σ selects: a) columns b) rows c) databases d) OS  
2. π selects: a) rows b) columns c) users d) ports  
3. SQL WHERE is like: a) π b) σ c) ∪ d) ρ  
4. Cartesian product: a) matching only b) all combinations c) delete all d) sort  
5. ⋈ often means: a) divide b) join c) stack d) deadlock  
6. Union needs: a) different structure b) compatible / same structure c) only numbers d) no columns  

**Answers:** 1-b, 2-b, 3-b, 4-b, 5-b, 6-b

---

## 6. 5-mark answer

Define relational algebra. Explain σ, π, ⋈ with one line and one tiny table example each. Say SQL is based on this.

---

**Next:** [04 — SQL Queries](04-sql-queries.md)
