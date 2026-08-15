# Chapter 7 — Digital Logic Fundamentals

**Paper:** Paper-II Computer Organization  
**Time:** 70 minutes  
**Week:** 1, Day 7 (Sunday — practise tables until they are automatic)  

---

## Today's goal

1. Know why computers use binary  
2. Draw AND, OR, NOT, NAND, NOR, XOR, XNOR symbols  
3. Write truth tables from memory  
4. Know De Morgan’s laws  
5. Know bit, gate, flip-flop at definition level  

---

## 1. Simple explanation

A bulb is **ON** or **OFF**. A computer switch (transistor) is the same: **1** or **0**.

**Digital logic** is the set of rules for combining 0s and 1s to make decisions — exactly like “if both teachers are present, open the lab.”

- AND = both conditions true  
- OR = at least one true  
- NOT = opposite  

All of Excel’s `IF`, all of programming `if`, and all of the ALU sit on these gates.

---

## 2. Definitions

> **Bit:** binary digit, 0 or 1.  
> **Logic gate:** an electronic circuit with one or more inputs and one output that follows a Boolean rule.  
> **Boolean algebra:** algebra of truth values (0 and 1) by George Boole.  
> **Truth table:** list of all input combinations and the output.

---

## 3. Basic gates (memorise symbol + table + English)

Use 0 = False / OFF, 1 = True / ON.

### NOT (Inverter) — 1 input

| A | Y = A' |
|---|--------|
| 0 | 1 |
| 1 | 0 |

English: output is the opposite.

### AND

| A | B | Y = A·B |
|---|---|---------|
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

English: **all inputs 1** → output 1.  
School: Lab opens only if **teacher AND electricity** are present.

### OR

| A | B | Y = A+B |
|---|---|---------|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 1 |

English: **at least one 1** → output 1.  
School: You can enter if you have **ID OR a pass**.

### NAND (NOT of AND) — universal

| A | B | AND | NAND |
|---|---|-----|------|
| 0 | 0 | 0 | 1 |
| 0 | 1 | 0 | 1 |
| 1 | 0 | 0 | 1 |
| 1 | 1 | 1 | 0 |

**Universal gate:** you can build AND, OR, NOT using only NAND.

### NOR (NOT of OR) — also universal

| A | B | OR | NOR |
|---|---|----|-----|
| 0 | 0 | 0 | 1 |
| 0 | 1 | 1 | 0 |
| 1 | 0 | 1 | 0 |
| 1 | 1 | 1 | 0 |

Output 1 only when **all inputs 0**.

### XOR — exclusive OR

| A | B | Y |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

English: **1 if inputs are different**. Used in binary addition (sum bit).

### XNOR — exclusive NOR / equivalence

| A | B | Y |
|---|---|---|
| 0 | 0 | 1 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

English: **1 if inputs are same**.

---

## 4. Boolean identities (short list for MCQ)

```
A + 0 = A          A · 1 = A
A + 1 = 1          A · 0 = 0
A + A = A          A · A = A
A + A' = 1         A · A' = 0
(A')' = A
A + B = B + A      A · B = B · A        (commutative)
```

**De Morgan’s laws (must write):**

```
(A · B)' = A' + B'
(A + B)' = A' · B'
```

In words:

- NOT (A AND B) = (NOT A) OR (NOT B)  
- NOT (A OR B) = (NOT A) AND (NOT B)  

---

## 5. Combinational vs sequential (definition level)

| Type | Memory? | Output depends on | Examples |
|------|---------|-------------------|----------|
| **Combinational** | No | Present inputs only | Adder, multiplexer, encoder |
| **Sequential** | Yes | Inputs + past state | Flip-flop, register, counter |

**Flip-flop:** 1-bit memory. Types: SR, JK, D, T (names enough for this exam).  
**Half adder:** adds 2 bits → Sum (XOR) and Carry (AND).  
**Full adder:** adds 3 bits (A, B, carry-in).

**MUX (multiplexer):** many inputs, one output, select lines.  
**DEMUX:** one input, many outputs.  
**Encoder:** 2^n inputs → n outputs.  
**Decoder:** n inputs → 2^n outputs.

---

## 6. Why this matters in a computer

- ALU = many gates  
- Memory cells = flip-flops / capacitors  
- Control signals = AND/OR combinations of opcode bits  

You do **not** need to design a processor. You **do** need truth tables and half-adder.

---

## 7. School teaching tip

Class 8: three students hold cards 0/1. One student is AND (stands up only if both show 1). This is a **lab-free logic practical**.

Never start with Boolean algebra formulas for Class 6. Start with switch stories.

---

## 8. Practice MCQs

**1.** AND output is 1 when:  
a) Any input is 1  b) All inputs are 1  c) All inputs are 0  d) Inputs differ  

**2.** Universal gates are:  
a) AND and OR  b) NAND and NOR  c) XOR and XNOR  d) Only NOT  

**3.** XOR of 1 and 1 is:  
a) 1  b) 0  c) 2  d) 10  

**4.** De Morgan: (A+B)' =  
a) A'+B'  b) A'·B'  c) A·B  d) A+B  

**5.** Half adder Sum is:  
a) AND  b) OR  c) XOR  d) NOT  

**6.** A flip-flop stores:  
a) 1 bit  b) 1 GB  c) A file  d) An OS  

**7.** Combinational circuit has:  
a) Memory  b) No memory of past  c) Only speakers  d) Only ROM disks  

**8.** NOT 0 is:  
a) 0  b) 1  c) 10  d) −1  

**9.** NAND of 1 and 1 is:  
a) 1  b) 0  c) 11  d) 2  

**10.** Boolean algebra was given by:  
a) Babbage  b) Boole  c) Turing  d) von Neumann  

### Answers

1-b, 2-b, 3-b, 4-b, 5-c, 6-a, 7-b, 8-b, 9-b, 10-b

---

## 9. Descriptive 5-mark answer

**Question:** Explain basic logic gates with truth tables.

1. Define logic gate.  
2. Draw AND, OR, NOT (symbols if you can).  
3. Write three truth tables.  
4. One line each: NAND universal, XOR for addition.  
5. Conclude: CPU uses these gates for all decisions.

---

## Quick revision box

- AND all 1s; OR any 1; NOT flip  
- NAND/NOR universal  
- XOR different = 1  
- De Morgan  
- Half adder = XOR + AND  
- Flip-flop = 1-bit memory  

---

## Homework

1. Write **all seven** truth tables from memory.  
2. Write De Morgan twice.  
3. Draw half adder (XOR and AND).

**Next:** [08 — Number Systems](08-number-systems.md)
