# Chapter 2 — Hardware Components

**Paper:** Paper-I + Paper-II Computer Organization  
**Time:** 60 minutes  
**Week:** 1, Day 2  

---

## Today's goal

1. Define hardware vs software  
2. Name every major part inside and outside the cabinet  
3. Explain motherboard, CPU, SMPS, ports  
4. Classify devices as input / output / storage / processing  
5. Write a labelled diagram of a computer system  

---

## 1. Simple explanation

**Hardware** is anything you can **touch**.

Keyboard, mouse, monitor, CPU box, printer, pendrive — all hardware.

**Software** is the set of **instructions** you cannot touch — Windows, Chrome, Nudi, Python.

A computer is useful only when **hardware + software** work together. Hardware is the body; software is the mind.

---

## 2. Exam definitions

> **Hardware:** The physical, electronic and mechanical parts of a computer.

> **Software:** A set of programs that tell the hardware what to do.

> **Firmware:** Permanent program stored in ROM/flash (BIOS/UEFI). It sits between hardware and OS.

---

## 3. Block diagram of a computer (must draw)

```
                    +------------------+
                    |   CONTROL UNIT   |
                    |  (inside CPU)    |
                    +--------+---------+
                             |
     INPUT                   |                   OUTPUT
   Keyboard,          +------v-------+         Monitor,
   Mouse,             |     ALU      |         Printer,
   Scanner   ------>  |  (CPU core)  | ------> Speaker
                      +------+-------+
                             |
                      +------v-------+
                      |   MEMORY     |
                      | RAM / ROM    |
                      +------+-------+
                             |
                      +------v-------+
                      | SECONDARY    |
                      | STORAGE      |
                      | HDD / SSD    |
                      +--------------+
```

**Von Neumann idea:** program and data both sit in memory. CPU fetches instruction, decodes, executes. (Full CPU chapter is next.)

---

## 4. Inside the system unit (CPU cabinet)

Students say “CPU” for the box. As a teacher you must correct this gently:

- **Cabinet / system unit** = the box  
- **CPU** = the chip on the motherboard (processor)

### 4.1 Motherboard (main board / system board)

The large green (or brown) PCB that connects everything.

Important parts on motherboard:

| Part | Job |
|------|-----|
| **CPU socket** | Holds the processor |
| **Chipset** | Traffic controller between CPU, RAM, devices |
| **RAM slots** | DIMM slots for memory modules |
| **SATA / M.2** | Connect HDD / SSD |
| **PCIe slots** | Graphics card, extra cards |
| **BIOS/UEFI chip** | Starts the computer |
| **CMOS battery** | Small cell; keeps date/time and some settings |
| **I/O panel** | USB, HDMI, audio, LAN ports |

### 4.2 Processor (CPU)

Brain of the computer. Brands in exams: **Intel**, **AMD**. School PCs: Core i3/i5, Ryzen, or Celeron/Pentium.

Details in [Chapter 4 — CPU Organization](04-cpu-organization.md).

### 4.3 SMPS (Switch Mode Power Supply)

Converts 230 V AC (wall) to low DC voltages (3.3 V, 5 V, 12 V) for components.  
**Exam line:** SMPS is the power house of the cabinet.

### 4.4 Cooling

Heat sink + fan, sometimes liquid cooling. Overheating slows or shuts the PC.

### 4.5 Storage drives (inside)

| Drive | Full form / note |
|-------|------------------|
| **HDD** | Hard Disk Drive — magnetic platters, cheaper, slower |
| **SSD** | Solid State Drive — flash chips, faster, no moving parts |
| **ODD** | Optical Disk Drive — CD/DVD (older labs) |

---

## 5. Ports and cables (high MCQ area)

| Port | Use | Look / note |
|------|-----|-------------|
| **USB** | Keyboard, mouse, pendrive | Universal Serial Bus; USB 2.0 / 3.0 / Type-C |
| **HDMI** | Monitor / TV | Digital video + audio |
| **VGA** | Old monitor | Blue 15-pin |
| **DisplayPort** | Modern monitor | |
| **Ethernet (RJ-45)** | LAN cable | Network |
| **Audio jack** | Mic / speaker | 3.5 mm |
| **PS/2** | Old keyboard (purple), mouse (green) | Rare now |
| **Serial / Parallel** | Very old printer / modem | COM, LPT |
| **Thunderbolt** | Fast data + video (laptops) | |

**USB inventor / popularisation:** often linked to Intel-led standard (1990s).  
**Plug and Play:** OS detects device automatically.

---

## 6. Hardware groups (classify every device)

| Group | Meaning | Examples |
|-------|---------|----------|
| **Input** | Send data in | Keyboard, mouse, scanner, mic, webcam, barcode, MICR, OMR, joystick, touch screen, biometric |
| **Output** | Show result | Monitor, printer, speaker, projector, plotter |
| **Processing** | Work on data | CPU, GPU |
| **Storage** | Keep data | HDD, SSD, pen drive, memory card, CD/DVD |
| **Communication** | Connect | NIC, modem, router, Bluetooth adapter |
| **Both I/O** | In and out | Touch screen, pendrive, network card, headsets with mic |

Full I/O list: [Chapter 6](06-io-devices.md). Memory: [Chapter 5](05-memory-hierarchy.md).

---

## 7. Other hardware words examiners love

| Term | Meaning |
|------|---------|
| **Peripheral** | Extra device connected to computer (printer, scanner) |
| **Bus** | Highway for data inside the computer (data, address, control bus) |
| **Clock** | Timing pulse; speed in GHz |
| **Cache** | Super-fast memory inside/near CPU |
| **GPU** | Graphics Processing Unit — pictures, video, some AI |
| **NIC** | Network Interface Card |
| **Modem** | Modulator-Demodulator — analog telephone line ↔ digital |
| **UPS** | Uninterruptible Power Supply — battery backup for lab |
| **Plotter** | Large drawings (maps, CAD) |

**Bus types (short):**

- **Data bus:** carries data (bidirectional)  
- **Address bus:** carries memory address (unidirectional, CPU → memory)  
- **Control bus:** read/write/interrupt signals  

---

## 8. Brands often seen in options

- Processors: Intel, AMD  
- OS: Microsoft, various Linux, Apple  
- Office: Microsoft Office, LibreOffice  
- Printers: HP, Canon, Epson  
- Indian supercomputer: PARAM (C-DAC)

---

## 9. School lab hardware checklist (pedagogy + practical)

A government school lab should ideally have:

- Working UPS / stabilizer  
- One server or teacher PC + student PCs  
- Projector or large display  
- Printer  
- LAN or controlled Wi-Fi  
- Keyboard covers, mouse pads  
- Dust covers, earthing  
- Stock register of every CPU, monitor, mouse  

You will use this again in [Lab Management](../07-computer-pedagogy/03-lab-management.md).

---

## 10. School teaching tip

Bring a **dead mouse and an old RAM stick** (if allowed) to class. Let Class 6–8 **see and name** parts. Do not open a live SMPS — high voltage.

Game: put 12 chits (keyboard, RAM, Windows, Chrome, printer…). Students sort into Hardware / Software.

---

## 11. Practice MCQs

**1.** Which is hardware?  
a) MS Word  b) Linux  c) Scanner  d) Python  

**2.** SMPS converts:  
a) DC to AC  b) AC to DC (low voltage)  c) Sound to text  d) Analog to USB  

**3.** CMOS battery is on the:  
a) Monitor  b) Motherboard  c) Printer  d) Speaker  

**4.** HDMI carries:  
a) Only power  b) Only audio  c) Video and audio  d) Only network  

**5.** The physical board that connects CPU, RAM and slots is:  
a) SMPS  b) Motherboard  c) ALU  d) Cache  

**6.** Address bus is generally:  
a) Bidirectional  b) Unidirectional  c) Wireless only  d) Optical only  

**7.** SSD is faster than HDD because:  
a) It is heavier  b) No moving parts, flash memory  c) It uses more electricity  d) It is analog  

**8.** UPS is used to:  
a) Increase RAM  b) Provide backup power  c) Cool the CPU  d) Connect to internet  

**9.** A plotter is mainly an:  
a) Input device  b) Output device  c) OS  d) Storage device  

**10.** Firmware is typically stored in:  
a) RAM  b) Cache  c) ROM / flash  d) Register only  

### Answers

1-c, 2-b, 3-b, 4-c, 5-b, 6-b, 7-b, 8-b, 9-b, 10-c

---

## 12. Descriptive 5-mark answer

**Question:** Explain the main hardware components of a computer with a neat diagram.

**Write:**

1. Hardware = physical parts.  
2. **Input devices** — keyboard, mouse.  
3. **CPU** — CU + ALU + registers; processes data.  
4. **Memory** — RAM (temporary), ROM (permanent start-up).  
5. **Output** — monitor, printer.  
6. **Secondary storage** — HDD/SSD.  
7. **Motherboard + SMPS** — connection and power.  
8. Diagram: IPOS block with CPU in the centre.

---

## Quick revision box

- Hardware = touchable  
- Cabinet ≠ CPU chip  
- Motherboard = all connections  
- SMPS = AC → DC  
- USB, HDMI, RJ-45  
- Data / Address / Control bus  
- UPS for lab  
- Firmware in ROM  

---

## Homework

1. Draw and label a system unit (motherboard, SMPS, HDD, RAM, CPU fan).  
2. List 10 devices under Input / Output / Storage.  
3. Write 8 port names.

**Next:** [03 — Software Types](03-software-types.md)
