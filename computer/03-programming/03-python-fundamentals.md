# Chapter PR-3 — Python Fundamentals

**Paper:** Paper-II Programming  
**Time:** 60 minutes  
**Week:** 3, Day 17  

---

## Today's goal

1. Python one-liners (Guido, interpreted, indentation)  
2. Rewrite the same C programs in Python  
3. Know list vs tuple vs dictionary at surface  
4. Write 5 programs on paper  

---

## 1. Simple explanation

**Python** (Guido van Rossum, 1991) is an **interpreted**, high-level language. Schools like it because there is less punctuation than C.

**Indentation (spaces) is compulsory.** It replaces `{ }`.

```python
print("Hello School")
```

No `main` required for simple scripts. No semicolon needed.

---

## 2. Why both C and Python?

| Need | Use |
|------|-----|
| Older textbooks / many papers | C |
| Fast writing, Class 6–8 labs | Python |
| Exam says “C, C++, Java or Python” | Foundation of **C + Python** is enough |

If the paper asks only one language, pick the one you write cleaner. Prepare both at basic level.

---

## 3. Variables and types

Python types appear automatically:

```python
a = 10          # int
x = 3.14        # float
name = "Ravi"   # str
ok = True       # bool
```

`type(a)` shows the type.  
Input is **string** by default:

```python
n = int(input("Enter n: "))
```

---

## 4. Operators

Same ideas as C: `+ - * / % // **`  
`//` integer divide, `**` power.  
`and or not` instead of `&& || !`.

---

## 5. if and loops

```python
if marks >= 35:
    print("Pass")
elif marks >= 0:
    print("Fail")
else:
    print("Invalid")

for i in range(1, 11):
    print(i)

i = 1
while i <= 10:
    print(i)
    i = i + 1
```

`range(1, 11)` → 1 to 10 (end not included).

---

## 6. Same programs in Python

**Add**

```python
a = int(input())
b = int(input())
print(a + b)
```

**Even odd**

```python
n = int(input())
print("Even" if n % 2 == 0 else "Odd")
```

**Factorial**

```python
n = int(input())
f = 1
for i in range(1, n + 1):
    f = f * i
print(f)
```

**Largest of three**

```python
a, b, c = 5, 9, 3
print(max(a, b, c))
```

---

## 7. Collections (names for MCQ)

| Type | Mutable? | Example |
|------|----------|---------|
| **list** | Yes | `[1, 2, 3]` |
| **tuple** | No | `(1, 2, 3)` |
| **str** | No | `"GPSTR"` |
| **dict** | Yes | `{"ravi": 80}` |
| **set** | Yes | `{1, 2, 3}` unique |

```python
m = [10, 20, 30]
print(m[0])      # 10
print(len(m))    # 3
```

---

## 8. Function

```python
def add(x, y):
    return x + y
```

---

## 9. MCQs

1. Python creator: a) Ritchie b) Guido van Rossum c) Gosling d) Torvalds  
2. Python is mainly: a) Only compiled like C always b) Interpreted c) An OS d) A printer  
3. Block is shown by: a) only {} b) indentation c) only GOTO d) BIOS  
4. `range(1,5)` gives: a) 1–5 b) 1–4 c) 0–5 d) 5 only  
5. Tuple is: a) mutable b) immutable c) a CPU d) a gate  
6. `input()` returns: a) always int b) str c) only float d) list  
7. `**` means: a) comment b) power c) AND d) divide  
8. Comment in Python: a) // only b) # c) <!-- d) ::  

**Answers:** 1-b, 2-b, 3-b, 4-b, 5-b, 6-b, 7-b, 8-b

---

## 10. 5-mark answer

**Question:** Write a Python program to find factorial and explain indentation.

Write the program. Say: Python uses spaces instead of braces; same indent = same block. Mention interpreted language.

---

## Quick revision box

- Guido 1991, interpreted  
- Indentation  
- int(input())  
- range(start, stop) stop excluded  
- list mutable; tuple not  
- and/or/not  

---

## Homework

Rewrite all 7 C programs from yesterday in Python on paper.

**Next:** [04 — Arrays and Strings](04-arrays-and-strings.md)
