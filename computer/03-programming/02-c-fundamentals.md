# Chapter PR-2 — C Language Fundamentals

**Paper:** Paper-II Programming  
**Time:** 70 minutes  
**Week:** 3, Day 16  

---

## Today's goal

1. Know C history one-liners  
2. Write a full C program structure  
3. Use data types, operators, if, switch, loops  
4. Know arrays at intro level  
5. Write 5 programs on paper  

---

## 1. Simple explanation

**C** is a high-level language created by **Dennis Ritchie** at Bell Labs (1972). It is the mother of many languages (C++, Java style).

C is compiled. You write `file.c` → compiler (Turbo C, gcc) → `file.exe` → run.

For GPSTR you need **foundation**, not pointers-to-pointers.

---

## 2. Structure of a C program

```c
#include <stdio.h>

int main()
{
    printf("Hello School\n");
    return 0;
}
```

| Part | Meaning |
|------|---------|
| `#include` | Preprocessor — add header |
| `stdio.h` | Standard input output (`printf`, `scanf`) |
| `main()` | Execution starts here |
| `{ }` | Block |
| `;` | End of statement |
| `return 0` | Success to OS |

**Tokens:** keywords, identifiers, constants, strings, operators, special symbols.  
**Keywords (some):** `int`, `float`, `char`, `if`, `else`, `for`, `while`, `do`, `return`, `void`, `switch`, `case`, `break`.

---

## 3. Data types

| Type | Typical size | Example |
|------|--------------|---------|
| `char` | 1 byte | `'A'` |
| `int` | 2 or 4 bytes | `35` |
| `float` | 4 bytes | `3.14` |
| `double` | 8 bytes | `3.141592` |
| `void` | none | empty |

`printf` / `scanf` codes: `%d` int, `%f` float, `%c` char, `%s` string, `%lf` double.

```c
int m;
scanf("%d", &m);   /* & = address */
```

---

## 4. Operators

| Kind | Symbols |
|------|---------|
| Arithmetic | `+ - * / %` |
| Relational | `== != < > <= >=` |
| Logical | `&& \|\| !` |
| Assignment | `= += -= *=` |
| Increment | `++ --` |
| Conditional | `? :` |

`/` on integers truncates (5/2 = 2). `%` is remainder (5%2 = 1).

---

## 5. Control statements

### if-else

```c
if (marks >= 35)
    printf("Pass");
else
    printf("Fail");
```

### switch

```c
switch(choice) {
    case 1: printf("Add"); break;
    case 2: printf("Sub"); break;
    default: printf("Wrong");
}
```

### loops

```c
for (i = 1; i <= 10; i++)
    printf("%d ", i);

i = 1;
while (i <= 10) { printf("%d ", i); i++; }

i = 1;
do { printf("%d ", i); i++; } while (i <= 10);
```

**for** — count known. **while** — check first. **do-while** — runs at least once.

`break` leaves the loop. `continue` skips this round.

---

## 6. Must-write programs (paper practice)

**1. Add two numbers**

```c
#include <stdio.h>
int main() {
    int a, b;
    scanf("%d %d", &a, &b);
    printf("%d", a + b);
    return 0;
}
```

**2. Largest of two** — use `if`.  
**3. Even or odd** — `if (n % 2 == 0)`.  
**4. Factorial** — loop multiply.  
**5. Sum of n numbers** — loop.  
**6. Simple interest** — `SI = P*T*R/100`.  
**7. Swap two numbers** — with third variable, and without (`a=a+b; b=a-b; a=a-b`).

---

## 7. Functions (short)

```c
int add(int x, int y) {
    return x + y;
}
```

**Library functions:** `printf`, `scanf`, `sqrt`, `strlen`.  
**User-defined:** you write them.  
**Recursion:** function calls itself (factorial) — definition enough.

---

## 8. Array teaser (full chapter later)

```c
int m[5] = {10, 20, 30, 40, 50};
printf("%d", m[0]);  /* 10 — index starts at 0 */
```

---

## 9. Common mistakes

- Forgetting `&` in `scanf`  
- Using `=` instead of `==`  
- Missing `;`  
- `i` not declared  

---

## 10. MCQs

1. C was developed by: a) Gosling b) Ritchie c) Guido d) Babbage  
2. Execution starts at: a) include b) main c) printf d) header  
3. `%d` is for: a) float b) int c) string d) char  
4. `5 % 2` is: a) 2.5 b) 1 c) 2 d) 0  
5. `do-while` runs: a) never b) at least once c) only twice d) only in Linux  
6. `==` is: a) assign b) equal compare c) increment d) include  
7. Index of first array element: a) 1 b) 0 c) -1 d) 2  
8. Header for printf: a) math.h b) stdio.h c) conio.h only d) os.h  

**Answers:** 1-b, 2-b, 3-b, 4-b, 5-b, 6-b, 7-b, 8-b

---

## 11. 5-mark answer

**Question:** Explain the structure of a C program with an example that adds two numbers.

Write include, main, declarations, scanf, process, printf. Explain each line. Mention C is compiled (Ritchie).

---

## Quick revision box

- Ritchie, 1972, compiled  
- main + stdio.h  
- %d %f %c %s and &  
- if, switch, for, while, do-while  
- % remainder; == compare  
- Array index 0  

---

## Homework

Write programs 1–7 on paper **without looking**. Dry-run factorial for n=4.

**Next:** [03 — Python Fundamentals](03-python-fundamentals.md)
