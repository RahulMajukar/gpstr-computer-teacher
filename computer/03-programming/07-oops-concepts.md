# Chapter PR-7 — Object-Oriented Programming (OOPs)

**Paper:** Paper-II Programming  
**Time:** 65 minutes  
**Week:** 4, Days 22–24 (read twice)  

---

## Today's goal

1. Why OOP exists  
2. Class vs object  
3. Four pillars: encapsulation, abstraction, inheritance, polymorphism  
4. Constructor, method, access specifiers  
5. Write school examples for every pillar  

---

## 1. Simple explanation

**Procedural** programming (plain C) is a list of functions. When the program grows, data and functions get lost.

**OOP** packs **data + functions** into a **class**, like a school “Student file” that also knows how to print itself.

- **Class** = blueprint (Student form)  
- **Object** = real thing (Ravi’s filled form)

Languages: **C++**, **Java**, **Python** (all objects-friendly). C is mainly procedural.

---

## 2. Definitions

> **Class:** a user-defined blueprint that groups data members and member functions.  
> **Object:** an instance of a class created in memory.  
> **OOP:** a programming model based on objects that have data and behaviour.

```python
class Student:
    def __init__(self, name, marks):
        self.name = name
        self.marks = marks

    def show(self):
        print(self.name, self.marks)

ravi = Student("Ravi", 80)   # object
ravi.show()
```

---

## 3. Four pillars (must give school examples)

### 3.1 Encapsulation

Wrapping data and methods in one unit. Hide internal data; use getters/setters.

**School:** Marks are inside the student record. Outsiders cannot scribble; they ask the teacher (method) to update.

### 3.2 Abstraction

Show only needed details; hide complexity.

**School:** You **drive** a projector remote (on/off). You do not see the lamp circuit.

In code: abstract class / interface — “Shape has area()” without saying how.

### 3.3 Inheritance

A new class (**child / derived**) reuses an old class (**parent / base**).

```
Person
  ↑
Student   (Student is-a Person)
```

**Types (names):** single, multiple (C++), multilevel, hierarchical, hybrid.  
Java: no multiple inheritance of classes (uses interfaces).

### 3.4 Polymorphism

“Many forms.” Same name, different behaviour.

- **Compile time:** function **overloading** (same name, different parameters)  
- **Run time:** function **overriding** (child replaces parent method)

**School:** The word **“play”** — Class 1 plays rhymes, Class 8 plays cricket. Same instruction, different action.

---

## 4. Other exam words

| Word | Meaning |
|------|---------|
| **Constructor** | Special method that runs when object is created; same name as class (C++/Java) |
| **Destructor** | Cleans when object dies (`~Class` in C++) |
| **this / self** | Current object |
| **private / public / protected** | Access specifiers |
| **Method** | Function inside a class |
| **Message passing** | One object calls another’s method |
| **static** | Belongs to class, not one object |

**Access (typical):**

- **private:** only inside class  
- **public:** everywhere  
- **protected:** class + children  

---

## 5. Procedural vs OOP

| Procedural | OOP |
|------------|-----|
| Functions + data separate | Data + methods together |
| C | C++, Java, Python |
| Harder reuse | Inheritance reuse |
| Less mapping to real world | Objects map to real things |

---

## 6. MCQs

1. Blueprint is: a) object b) class c) stack d) OS  
2. Instance of class: a) class b) object c) compiler d) gate  
3. Hiding data is: a) polymorphism b) encapsulation c) paging d) FIFO  
4. is-a relationship: a) inheritance b) stack c) compiler d) MICR  
5. Overloading is: a) runtime only always b) compile-time polymorphism c) OS boot d) deadlock  
6. C is mainly: a) OOP only b) procedural c) a distro d) a printer  
7. Constructor is called: a) when object is created b) only at shutdown c) only in Excel d) never  
8. Abstraction means: a) show all wires b) hide complexity c) LIFO d) FAT32  

**Answers:** 1-b, 2-b, 3-b, 4-a, 5-b, 6-b, 7-a, 8-b

---

## 7. 5-mark answer

**Question:** Explain the four features of OOP with examples.

One definition line + four headings (2–3 lines each) with **school examples**. Mention class and object in the introduction.

---

## Quick revision box

- Class = blueprint; object = instance  
- Encapsulation wrap; abstraction hide  
- Inheritance reuse; polymorphism many forms  
- Overload vs override  
- Constructor  
- C procedural; C++/Java/Python OOP  

---

## Homework

Write one school example for each pillar without looking. Draw Person → Student → Monitor inheritance.

**Next:** [08 — Programming Chapter Practice](08-chapter-practice.md)
