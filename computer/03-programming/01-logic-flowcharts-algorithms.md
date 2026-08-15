# Chapter PR-1 — Logic, Algorithms, and Flowcharts

**Paper:** Paper-II Programming Concepts  
**Time:** 60 minutes  
**Week:** 3, Day 15  

---

## Today's goal

1. Define algorithm, flowchart, pseudocode  
2. Draw standard flowchart symbols  
3. Write algorithms for start-level problems  
4. Dry-run a loop on paper  
5. Know sequence, selection, iteration  

---

## 1. Simple explanation

Before C or Python, a teacher must think in **steps**.

**Algorithm** = step-by-step method (like a recipe).  
**Flowchart** = the same recipe as boxes and arrows.  
**Program** = recipe typed in a language the computer accepts.

If the algorithm is wrong, every language will be wrong. This is why Week 3 starts here.

---

## 2. Definitions

> **Algorithm:** a finite, clear, step-by-step procedure to solve a problem.  
> **Flowchart:** a diagram that shows an algorithm using standard symbols.  
> **Pseudocode:** English-like steps that look like a program but are not tied to one language.  
> **Dry run:** executing the steps on paper with sample data to check logic.

**Properties of a good algorithm (exam list):** input, output, finiteness, definiteness (clear), effectiveness, language independence.

---

## 3. Three building blocks of logic

| Structure | Meaning | Example |
|-----------|---------|---------|
| **Sequence** | Steps one after another | Input → add → print |
| **Selection** | Decision | if marks ≥ 35 then Pass |
| **Iteration / loop** | Repeat | print 1 to 10 |

These three are enough for almost all school programs.

---

## 4. Flowchart symbols (draw neatly)

| Symbol | Shape | Use |
|--------|-------|-----|
| Terminator | Oval | Start / Stop |
| Input / Output | Parallelogram | Read, Print |
| Process | Rectangle | Calculate, assign |
| Decision | Diamond | Yes/No question |
| Connector | Small circle | Join arrows |
| Arrow | Arrow | Flow of control |
| Preparation | Hexagon (sometimes) | Loop index |

**Rules:** one Start; flow top to bottom or left to right; every diamond has Yes and No.

---

## 5. Worked algorithms (copy into notebook)

### A. Add two numbers

```
1. Start
2. Read A, B
3. Set S = A + B
4. Print S
5. Stop
```

### B. Largest of two numbers

```
1. Start
2. Read A, B
3. If A > B then Print A
   Else Print B
4. Stop
```

### C. Sum of first N natural numbers (loop)

```
1. Start
2. Read N
3. Set I = 1, S = 0
4. Repeat while I <= N
      S = S + I
      I = I + 1
5. Print S
6. Stop
```

**Dry run for N = 3**

| I | S | I<=3? |
|---|---|-------|
| 1 | 0+1=1 | yes |
| 2 | 1+2=3 | yes |
| 3 | 3+3=6 | yes |
| 4 | | no → print 6 |

This table is what “dry-running loops” in your 60-day plan means.

### D. Even or odd

```
If N modulo 2 = 0 then Even else Odd
```

### E. Factorial of N (N!)

```
F = 1
For I from 1 to N: F = F * I
Print F
```

---

## 6. Errors (short)

| Error | When |
|-------|------|
| **Syntax** | Language grammar wrong (`prnt`) |
| **Logical** | Runs but wrong answer (used + instead of *) |
| **Runtime** | Crashes while running (divide by zero) |

---

## 7. School teaching tip

Class 6: flowchart of “brush teeth” or “get ready for school”.  
Class 7–8: marks → pass/fail diamond.  
Do **not** start Class 6 with factorial.

---

## 8. Practice

**Draw flowcharts for:**

1. Area of rectangle  
2. Positive / negative / zero  
3. Print numbers 1 to 10  
4. Largest of three numbers  

**MCQs**

1. Diamond is used for: a) Start b) Decision c) Input only d) Stop only  
2. An algorithm must be: a) Infinite b) Finite c) Vague d) Hardware  
3. Dry run means: a) Compile b) Paper execution c) Format disk d) Boot  
4. Loop is: a) Sequence only b) Iteration c) Only GUI d) OS kernel  

**Answers:** 1-b, 2-b, 3-b, 4-b

---

## 9. Descriptive 5-mark answer

**Question:** What is an algorithm? Draw a flowchart to find the largest of two numbers.

Define + 4 properties. Draw oval-parallelogram-diamond-rectangles-oval. Label Yes/No.

---

## Quick revision box

- Algorithm finite + clear  
- Sequence / selection / iteration  
- Oval, parallelogram, rectangle, diamond  
- Dry-run table  
- Syntax vs logic vs runtime  

---

## Homework

Five flowcharts in the notebook. Dry-run the sum-of-N algorithm for N=5.

**Next:** [02 — C Fundamentals](02-c-fundamentals.md)
