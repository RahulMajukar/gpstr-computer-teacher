# Chapter PR-4 — Arrays and Strings

**Paper:** Paper-II Data Structures  
**Time:** 55 minutes  
**Week:** 3, Day 18  

---

## Today's goal

1. Define array and index  
2. Traverse, find max, sum, linear search  
3. 1-D vs 2-D  
4. String basics in C and Python  
5. Dry-run a search  

---

## 1. Simple explanation

An **array** is a row of lockers with numbers 0, 1, 2… All lockers hold the **same type** (all marks, all names).

```
Index:  0    1    2    3    4
Value: 45   67   80   33   90
```

`marks[2]` is 80.

---

## 2. Definition

> An **array** is a linear data structure that stores a fixed-size sequence of elements of the same type in contiguous memory. Elements are accessed by **index**.

**Advantages:** fast access by index, easy loops.  
**Disadvantages:** fixed size (classic array), insert/delete in the middle is costly, same type only.

---

## 3. Operations (write loops)

**Traversal / sum (C idea)**

```c
int a[5] = {45, 67, 80, 33, 90};
int i, s = 0, max = a[0];
for (i = 0; i < 5; i++) {
    s = s + a[i];
    if (a[i] > max) max = a[i];
}
```

**Linear search:** walk from 0 to n-1; if `a[i] == key` found.

**Binary search (idea):** array must be **sorted**; look at middle; cut half each time. Faster. (O(log n) vs O(n) — big-O name is enough.)

---

## 4. Two-dimensional array

A table: `m[row][col]`

```
Marks of 3 students in 2 subjects
m[0][0] m[0][1]
m[1][0] m[1][1]
m[2][0] m[2][1]
```

School use: seating chart, matrix.

---

## 5. Strings

**String** = sequence of characters.

**C:** array of char ending with `'\0'`.

```c
char name[20] = "Ravi";
```

Useful: `strlen`, `strcpy`, `strcmp`, `strcat` (`string.h`).

**Python:**

```python
s = "Karnataka"
print(s[0])       # K
print(len(s))     # 9
print(s.lower())
print(s[0:5])     # Karna  (slice)
```

---

## 6. Dry-run linear search

Array: 10, 20, 30, 40. Key = 30.

| i | a[i] | equal 30? |
|---|------|-----------|
| 0 | 10 | no |
| 1 | 20 | no |
| 2 | 30 | yes — found at index 2 |

---

## 7. MCQs

1. First index of array is usually: a) 1 b) 0 c) n d) -1  
2. Array stores: a) mixed types in C int array b) same type c) only OS d) only gates  
3. Binary search needs: a) unsorted b) sorted c) 2-D only d) strings only  
4. `'\0'` in C string means: a) space b) end of string c) start d) error  
5. `strlen` is in: a) stdio only b) string.h c) math.h d) os.h  
6. Access time by index is: a) slow sequential always b) random/direct c) only disk d) compile  

**Answers:** 1-b, 2-b, 3-b, 4-b, 5-b, 6-b

---

## 8. 5-mark answer

Define array + diagram of 5 boxes. Write steps of linear search. Mention one limitation (fixed size) and that linked list solves insert (next chapter).

---

## Homework

Dry-run: find max of 12, 7, 19, 4. Write Python list version of sum.

**Next:** [05 — Linked Lists](05-linked-lists.md)
