# Chapter 4 — CPU Organization

**Paper:** Paper-II Computer Organization (also Paper-I “CPU organization”)  
**Time:** 65 minutes  
**Week:** 1, Day 4  

---

## Today's goal

1. Expand CPU and name its three parts  
2. Explain fetch–decode–execute  
3. Know registers by name  
4. Know instruction cycle, clock, word  
5. Draw a CPU block diagram for 5 marks  

---

## 1. Simple explanation

**CPU** = **C**entral **P**rocessing **U**nit = the **brain**.

It does not store your 10-year school records (that is the hard disk).  
It does the **thinking of this second**: add two numbers, compare marks, decide the next instruction.

If the CPU is an office head:

- **ALU** = the accountant (calculates)  
- **CU** = the head teacher (gives orders)  
- **Registers** = the small notepad on the desk (very fast, very small)

---

## 2. Exam definition

> The **CPU** is the hardware that fetches instructions from memory, decodes them, and executes them. It contains the **ALU**, **Control Unit**, and **registers**.

**Microprocessor:** a CPU on a single IC (4th generation onwards).

---

## 3. Three parts of CPU (must draw)

```
                    +---------------------------+
                    |           CPU             |
                    |  +---------+ +---------+  |
                    |  |   CU    | |   ALU   |  |
                    |  +----+----+ +----+----+  |
                    |       |           |       |
                    |  +----v-----------v----+  |
                    |  |     REGISTERS       |  |
                    |  | PC IR ACC MAR MDR   |  |
                    |  +---------------------+  |
                    +------------+--------------+
                                 |
                          SYSTEM BUS
                       (data/address/control)
                                 |
                              MEMORY
```

### 3.1 ALU — Arithmetic Logic Unit

- **Arithmetic:** add, subtract, multiply, divide  
- **Logic:** AND, OR, NOT, XOR, compare (greater / equal)  
- **Shift:** left/right bit shifts  

ALU does not “decide the next program step”. It only computes. CU decides.

### 3.2 CU — Control Unit

- Takes instruction from memory  
- Decodes opcode  
- Sends control signals: read RAM, write RAM, ALU add, store result  
- Does **not** calculate 2+2; it tells ALU to calculate  

Two designs (advanced MCQ):

| Type | How |
|------|-----|
| **Hardwired CU** | Fixed electronic circuits; faster; difficult to change |
| **Microprogrammed CU** | Control stored as micro-instructions; flexible |

### 3.3 Registers — ultra-fast CPU memory

| Register | Full name | Job |
|----------|-----------|-----|
| **PC / IP** | Program Counter | Address of **next** instruction |
| **IR** | Instruction Register | Holds the **current** instruction |
| **ACC** | Accumulator | Holds result of ALU (simple CPUs) |
| **MAR** | Memory Address Register | Address to read/write in memory |
| **MDR / MBR** | Memory Data Register | Data coming from or going to memory |
| **SP** | Stack Pointer | Top of stack in memory |
| **Flag / PSW** | Status flags | Zero, Carry, Sign, Overflow |
| **GPR** | General Purpose | AX, BX… or R0–R15 |

**Exam trap:** Registers are **inside CPU**. RAM is **outside** CPU (on motherboard). Cache is between.

---

## 4. Instruction cycle (fetch–decode–execute)

Every instruction goes through this loop. Draw the arrows.

```
  +--------+     +--------+     +---------+     +--------+
  | FETCH  | --> | DECODE | --> | EXECUTE | --> | STORE  | --+
  +--------+     +--------+     +---------+     +--------+   |
       ^                                                     |
       +-----------------------------------------------------+
```

**Fetch**

1. CU looks at **PC** for the address  
2. Address goes to **MAR** → memory  
3. Instruction bits come to **MDR** → copied to **IR**  
4. **PC** is increased to point to the next instruction  

**Decode**

- CU reads opcode in IR  
- Finds what to do (ADD, MOV, JMP…)  

**Execute**

- ALU / memory / IO does the work  
- Flags may change  

**Store / write-back** (sometimes listed separately)

- Result written to register or memory  

**Interrupt:** an urgent signal (keyboard, I/O) can pause the cycle; CPU saves state and runs ISR (Interrupt Service Routine), then returns.

---

## 5. Instruction format (short)

A machine instruction has:

- **Opcode** — what to do  
- **Operand** — on which data / address  

Addressing modes (names only for GPSTR):

| Mode | Meaning |
|------|---------|
| Immediate | Data is inside the instruction (`ADD 5`) |
| Direct | Instruction has the memory address |
| Indirect | Instruction has address of address |
| Register | Data in a register |
| Indexed | Base + index (arrays) |

---

## 6. Speed words

| Term | Meaning |
|------|---------|
| **Clock speed** | Pulses per second (GHz). 3 GHz ≈ 3 billion cycles/sec |
| **CPI** | Cycles Per Instruction |
| **MIPS** | Million Instructions Per Second |
| **FLOPS** | Floating Point Operations Per Second (supercomputers) |
| **Word size** | Bits CPU handles at once (32 / 64) |
| **Core** | Separate processing unit inside one chip (dual, quad, octa) |
| **Thread** | Sequence of instructions; hyper-threading shares a core |
| **Pipeline** | Overlap fetch of next instruction while current executes |
| **RISC** | Reduced Instruction Set — simple, fast instructions (ARM) |
| **CISC** | Complex Instruction Set — rich instructions (x86) |

**Moore’s law (MCQ):** number of transistors on a chip roughly doubles about every 18–24 months (historical observation).

---

## 7. Types of processors / architectures

| Idea | Note |
|------|------|
| **Von Neumann** | Shared memory for program + data; one bus — bottleneck |
| **Harvard** | Separate memories/buses for program and data |
| **Serial vs Parallel** | One after another vs many at once |
| **GPU** | Many small cores for graphics / parallel work |

---

## 8. School teaching tip

Class 7 demo (no opening the PC):

> “I am the CU. Two students are ALU. One student is RAM holding a card that says ADD 4 5. I fetch the card, tell ALU to add, they show 9.”

This role-play becomes a **pedagogy 5-mark** example later.

---

## 9. Practice MCQs

**1.** ALU performs:  
a) Only printing  b) Arithmetic and logic  c) Only storing files  d) Cooling  

**2.** Program Counter holds:  
a) Last result always  b) Address of next instruction  c) User password  d) OS name  

**3.** Which is **not** a part of CPU?  
a) ALU  b) CU  c) Hard disk  d) Register  

**4.** Fetch–decode–execute is called:  
a) Booting  b) Instruction cycle  c) Compiling  d) Formatting  

**5.** MAR is used to:  
a) Store the result of addition only  b) Hold memory address  c) Display output  d) Connect USB  

**6.** RISC means:  
a) Random Instruction Set Computer  b) Reduced Instruction Set Computer  c) Remote Internet System Card  d) Read Internal Software Code  

**7.** A 64-bit CPU typically has word size:  
a) 8 bits  b) 16 bits  c) 32 bits  d) 64 bits  

**8.** Control Unit:  
a) Adds numbers  b) Generates control signals  c) Is a printer  d) Stores 1 TB  

**9.** Pipeline is used to:  
a) Cool water  b) Overlap instruction stages  c) Draw charts  d) Block viruses  

**10.** Von Neumann bottleneck is due to:  
a) Separate data and program buses  b) Shared bus/memory for data and instructions  c) Too many ALUs  d) No clock  

### Answers

1-b, 2-b, 3-c, 4-b, 5-b, 6-b, 7-d, 8-b, 9-b, 10-b

---

## 10. Descriptive 5-mark answer

**Question:** Explain the organisation of CPU with a neat diagram.

1. CPU = ALU + CU + registers.  
2. **ALU:** arithmetic and logic.  
3. **CU:** fetches, decodes, controls.  
4. **Registers:** PC, IR, ACC, MAR, MDR — fastest storage.  
5. Connected to memory by **system bus**.  
6. Works in **fetch–decode–execute** cycle.  
7. Diagram as in section 3.

---

## Quick revision box

- CPU = ALU + CU + Registers  
- PC = next instruction  
- IR = current instruction  
- MAR = address; MDR = data  
- Instruction cycle  
- Clock / core / RISC-CISC  
- Von Neumann vs Harvard  

---

## Homework

1. Draw CPU and label 6 parts.  
2. Write 6 register names and jobs.  
3. Explain fetch-decode-execute in 6 lines.

**Next:** [05 — Memory Hierarchy](05-memory-hierarchy.md)
