# Chapter 8 — Number Systems and Conversions

**Paper:** Paper-II (also Paper-I “language of computers”)  
**Time:** 75 minutes + daily 15 min drill this week  
**Week:** 1–2, Day 8  

---

## Today's goal

1. Know bases: 2, 8, 10, 16  
2. Convert in all common directions  
3. Do binary addition  
4. Know 1’s and 2’s complement  
5. Score full marks on a 5-mark conversion question  

---

## 1. Simple explanation

Humans count in **ten** because we have ten fingers. That is **decimal (base 10)** — digits 0–9.

Computers have two states, so they count in **two**: **binary (base 2)** — digits 0 and 1.

**Octal (base 8)** uses 0–7.  
**Hexadecimal (base 16)** uses 0–9 and **A–F** (A=10 … F=15). Hex is a short way to write long binary.

---

## 2. Place values (the only idea you need)

A number `d2 d1 d0` in base *b* means:

```
d2 × b²  +  d1 × b¹  +  d0 × b⁰
```

Example: `101` in binary

```
1×2² + 0×2¹ + 1×2⁰ = 4 + 0 + 1 = 5 (decimal)
```

Example: `2F` in hex

```
2×16¹ + 15×16⁰ = 32 + 15 = 47 (decimal)
```

---

## 3. Conversion methods

### 3.1 Any base → Decimal

Multiply each digit by place value, add. (See above.)

### 3.2 Decimal → Binary / Octal / Hex

**Divide** the decimal number by the new base. Write **remainders from bottom to top**.

Example: 25 to binary

```
25 ÷ 2 = 12 remainder 1
12 ÷ 2 =  6 remainder 0
 6 ÷ 2 =  3 remainder 0
 3 ÷ 2 =  1 remainder 1
 1 ÷ 2 =  0 remainder 1
```

Remainders bottom→top: **11001₂**  
Check: 16+8+1 = 25. Always check.

### 3.3 Binary ↔ Octal (group of 3)

```
11010111  →  pad left: 011 010 111  →  3 2 7  →  327₈
```

Octal to binary: each octal digit → 3 bits.

```
5₈ = 101₂    7₈ = 111₂
```

### 3.4 Binary ↔ Hex (group of 4)

```
11010111 → 1101 0111 → D 7 → D7₁₆
```

Hex digit table (memorise):

| Hex | Dec | Bin |
|-----|-----|-----|
| 0 | 0 | 0000 |
| 1 | 1 | 0001 |
| 2 | 2 | 0010 |
| 3 | 3 | 0011 |
| 4 | 4 | 0100 |
| 5 | 5 | 0101 |
| 6 | 6 | 0110 |
| 7 | 7 | 0111 |
| 8 | 8 | 1000 |
| 9 | 9 | 1001 |
| A | 10 | 1010 |
| B | 11 | 1011 |
| C | 12 | 1100 |
| D | 13 | 1101 |
| E | 14 | 1110 |
| F | 15 | 1111 |

### 3.5 Decimal fraction → binary (extra, if asked)

Multiply fraction by 2. Record integer part. Repeat.

0.625 × 2 = 1.25 → 1  
0.25 × 2 = 0.5 → 0  
0.5 × 2 = 1.0 → 1  
So 0.625₁₀ = 0.101₂

---

## 4. Binary addition

```
0+0=0
0+1=1
1+0=1
1+1=0 carry 1
1+1+1=1 carry 1
```

Example:

```
  1011
+ 0110
------
 10001
```

---

## 5. Complements (negative numbers — short)

**1’s complement:** flip every bit.  
1010 → 0101

**2’s complement:** 1’s complement + 1.  
1010 → 0101 + 1 = 0110

Computers store negative integers mostly in **2’s complement**.

To subtract: add 2’s complement of the subtrahend.

---

## 6. BCD and ASCII (MCQ)

| Code | Idea |
|------|------|
| **BCD** | Each decimal digit stored as 4 bits (9 = 1001) |
| **ASCII** | 7-bit (or 8-bit) character code. `'A'` = 65, `'a'` = 97, `'0'` = 48 |
| **Unicode / UTF-8** | World scripts including Kannada |
| **EBCDIC** | Old IBM 8-bit code |
| **Gray code** | Adjacent values differ by 1 bit |

---

## 7. Prefixes in questions

```
(1010)₂   (72)₈   (255)₁₀   (A3)₁₆
```

Sometimes written `1010B`, `72O`, `255D`, `A3H`.

---

## 8. Worked set (do these on paper now)

1. (11011)₂ = ?₁₀  
2. (45)₁₀ = ?₂  
3. (101101)₂ = ?₈  
4. (101101)₂ = ?₁₆  
5. (2A)₁₆ = ?₁₀  
6. 1010 + 1101 = ?  
7. 1’s and 2’s complement of 10011000  

**Answers:**  
1) 27  
2) 101101  
3) 55₈  
4) 2D₁₆  
5) 42  
6) 10111  
7) 1’s = 01100111; 2’s = 01101000  

---

## 9. School teaching tip

Class 6–7: only decimal vs binary with **25 rupees** and **divide by 2**.  
Class 8: add hex after they are comfortable with groups of 4.

Never dump all bases in one period.

---

## 10. Practice MCQs

**1.** Hex digit F equals decimal:  
a) 15  b) 16  c) 14  d) 8  

**2.** Binary of 8 is:  
a) 100  b) 1000  c) 10000  d) 111  

**3.** Octal uses digits:  
a) 0–9  b) 0–7  c) 0–1  d) 0–F  

**4.** ASCII of ‘A’ is:  
a) 97  b) 65  c) 48  d) 32  

**5.** Group binary into ___ bits for hex:  
a) 2  b) 3  c) 4  d) 8 always only  

**6.** 1’s complement of 0101 is:  
a) 1010  b) 0110  c) 0101  d) 1111  

**7.** (1111)₂ =  
a) 14  b) 15  c) 16  d) 8  

**8.** BCD for decimal 25 is:  
a) 11001  b) 0010 0101  c) 25  d) 110010  

### Answers

1-a, 2-b, 3-b, 4-b, 5-c, 6-a, 7-b, 8-b

---

## 11. Descriptive 5-mark answer

**Question:** Convert (45)₁₀ to binary, octal and hexadecimal. Show steps.

Write the division method three times (÷2, ÷8, ÷16).  
45 = 101101₂ = 55₈ = 2D₁₆.  
Box the three answers.

---

## Quick revision box

- Base 2 / 8 / 10 / 16  
- To decimal: expand place values  
- From decimal: divide, remainders reverse  
- Bin↔oct = 3 bits; bin↔hex = 4 bits  
- A–F = 10–15  
- 2’s complement = flip + 1  
- ASCII A=65, a=97, 0=48  

---

## Homework (do 20 conversions this week)

Mix: dec→bin, bin→dec, bin→hex, hex→dec, two additions.

**Next:** [09 — Chapter Practice Test](09-chapter-practice.md)
