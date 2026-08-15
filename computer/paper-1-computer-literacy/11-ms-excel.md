# Literacy 11 — MS Excel

**Syllabus line:** Simple mathematical formulas – alignment – formatting sheet – merge cells – wrapping – charts (pie, bar, line) – print preview  
**Time:** 55 minutes  

---

## Today's goal

Every Excel word in the official syllabus, with one example each.

---

## 1. Definition

> **MS Excel** is spreadsheet software. Data is stored in **rows** and **columns**. You can calculate with **formulas** and draw **charts**.

File: `.xlsx` (new), `.xls` (old).

- **Workbook** = the whole file  
- **Worksheet** = one tab (Sheet1)  
- **Cell** = one box, address **A1** (column A, row 1)  
- **Range** = A1:A10  
- **Active cell** = the selected cell  

---

## 2. Simple mathematical formulas

A formula **always starts with `=`**.

| Formula | Meaning |
|---------|---------|
| `=A1+B1` | Add two cells |
| `=A1-B1` | Subtract |
| `=A1*B1` | Multiply |
| `=A1/B1` | Divide |
| `=SUM(A1:A10)` | Total |
| `=AVERAGE(A1:A10)` | Mean |
| `=MAX(A1:A10)` | Highest |
| `=MIN(A1:A10)` | Lowest |
| `=COUNT(A1:A10)` | How many numbers |
| `=IF(B2>=35,"Pass","Fail")` | Decision |

**AutoSum:** often **Alt+=** on a column of numbers.

**Fill handle:** small square at the cell corner — drag down to copy the formula.

**Relative address:** `A1` becomes `A2` when copied down.  
**Absolute:** `$A$1` does not change.

Order of work: brackets, then * and /, then + and −.

---

## 3. Alignment and formatting the sheet

| Tool | Use |
|------|-----|
| **Alignment** | Left, centre, right; top / middle / bottom in the cell |
| **Merge cells** | Join A1:C1 into one title cell (e.g. “Class 7A Marks”) |
| **Wrap text** | Long sentence stays **inside** the cell (shows on many lines) |
| **Bold / font / colour / borders** | Make the sheet readable |
| **Number format** | Number, % , ₹ currency, date |
| **Column width / row height** | Drag the line between A and B |
| **Freeze panes** | Keep heading row visible while scrolling |

---

## 4. Charts (syllabus names all three)

Select the data → Insert → Chart.

| Chart | Best for |
|-------|----------|
| **Pie chart** | Parts of a **whole** (pass % vs fail %) |
| **Bar / column chart** | Compare subjects or students |
| **Line chart** | Change over **time** (monthly attendance) |

You can add a **chart title** and **legend**.

---

## 5. Print preview settings

**File → Print** (or Ctrl+P) opens **Print Preview**.

Check before printing:

- Portrait or landscape  
- Fit sheet on one page / scaling  
- Margins  
- Print area (only the marks table, not empty cells)  
- Header / footer (school name)  
- Gridlines on or off  

**Print Preview** shows how the paper will look — saves paper in the school lab.

---

## 6. School example

| A | B | C |
|---|---|---|
| Name | Marks | Result |
| Asha | 78 | `=IF(B2>=35,"Pass","Fail")` |
| Ravi | 30 | `=IF(B3>=35,"Pass","Fail")` |

`=AVERAGE(B2:B3)` in a totals row. Pie chart of Pass/Fail.

---

## 7. MCQs

**1.** Excel is:  
a) A browser  b) A spreadsheet  c) An OS  d) A scanner  

**2.** Formulas begin with:  
a) #  b) =  c) @  d) /  

**3.** Merge cells means:  
a) Delete the sheet  b) Join two or more cells  c) A virus  d) Lock Windows  

**4.** Wrap text:  
a) Hides the file  b) Shows long text on many lines in one cell  c) Prints only  d) Sorts A–Z only  

**5.** Pie chart is best for:  
a) Parts of a whole  b) Only time always  c) Only IP  d) Only wallpaper  

**6.** Line chart is best for:  
a) Only names  b) Trend over time  c) Only merge  d) Only Recycle Bin  

**7.** Print Preview shows:  
a) BIOS  b) How the page will print  c) Only RAM  d) Only email  

**8.** `=SUM(A1:A5)` :  
a) Multiplies  b) Adds A1 to A5  c) Draws a pie only  d) Sends mail  

**9.** Cell address of column C row 4 is:  
a) 4C  b) C4  c) 4-C  d) RowC  

**10.** .xlsx is:  
a) Word  b) Excel  c) PowerPoint  d) Paint  

### Answers

1-b, 2-b, 3-b, 4-b, 5-a, 6-b, 7-b, 8-b, 9-b, 10-b

---

## Quick revision

=SUM AVERAGE MAX MIN IF. Align, merge, wrap. Pie / bar / line. Print Preview. A1 = column+row.

**Next:** [12-ms-paint.md](12-ms-paint.md)
