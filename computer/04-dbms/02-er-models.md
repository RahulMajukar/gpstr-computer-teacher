# Chapter DB-2 — ER Models

**Paper:** Paper-II DBMS  
**Time:** 55 minutes  
**Week:** 5, Day 30  

---

## Today's goal

1. Entity, attribute, relationship  
2. Draw ER symbols  
3. 1:1, 1:N, M:N  
4. Strong vs weak entity  
5. Convert a school story to ER  

---

## 1. Simple explanation

Before making tables, we **draw the world**.

- **Entity** = a real thing we store (Student, Teacher, Course)  
- **Attribute** = property (Name, DOB)  
- **Relationship** = how they connect (Student **enrols in** Course)

This drawing is the **ER diagram** (Entity–Relationship) by **Peter Chen** (1976) — name sometimes asked.

---

## 2. Symbols

| Idea | Shape |
|------|-------|
| Entity | Rectangle |
| Weak entity | Double rectangle |
| Attribute | Oval |
| Key attribute | Underlined oval |
| Multivalued attribute | Double oval (phone numbers) |
| Derived attribute | Dashed oval (age from DOB) |
| Relationship | Diamond |
| Connecting line | Link; crow’s foot or 1/N labels for cardinality |

---

## 3. Cardinality (must draw)

| Type | Meaning | School |
|------|---------|--------|
| **1 : 1** | One to one | One teacher ↔ one unique cabin |
| **1 : N** | One to many | One class has many students |
| **M : N** | Many to many | Students ↔ Courses (need extra table later) |

**Participation:** total (every student must have a class) vs partial.

---

## 4. Strong vs weak

**Strong entity:** has its own PK (Student + Roll).  
**Weak entity:** depends on another (Exam_Attempt depends on Student). Identified by **partial key + owner’s key**.

---

## 5. Worked school ER (draw this)

```
[STUDENT] ----<enrols>---- [COURSE]
   |                         |
 roll (PK)                 code (PK)
 name                      title
 class                     credits
```

- Student to Course is **M:N** via **enrols**.  
- Later we make three tables: STUDENT, COURSE, ENROLS(roll, code, date).

Another: DEPARTMENT 1—N TEACHER (one dept, many teachers).

---

## 6. ER → tables (preview)

- Entity → table  
- Attributes → columns  
- 1:N → FK on the N side  
- M:N → new table with both PKs  

---

## 7. MCQs

1. Entity is drawn as: a) oval b) rectangle c) diamond d) circle only  
2. Relationship shape: a) rectangle b) diamond c) triangle d) star  
3. Primary key attribute is: a) dashed b) underlined c) square d) bold only  
4. Many students many courses: a) 1:1 b) 1:N c) M:N d) 0:0  
5. Weak entity: a) own full PK always b) depends on strong entity c) a stack d) an OS  
6. ER model proposed by: a) Codd only b) Chen (often cited) c) Babbage d) Torvalds  

**Answers:** 1-b, 2-b, 3-b, 4-c, 5-b, 6-b

---

## 8. 5-mark answer

Define ER. Draw Student–Course with enrols (M:N). Explain entity, attribute, relationship, PK underline. Mention 1:1, 1:N, M:N in one line each.

---

## Homework

Draw ER: Library — Book, Member, Issue. Decide cardinalities.

**Next:** [03 — Relational Algebra](03-relational-algebra.md)
