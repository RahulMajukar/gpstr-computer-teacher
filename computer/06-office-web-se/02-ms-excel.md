# Chapter OF-2 — MS Excel (Spreadsheet)

**Paper:** Paper-I + useful for marks lists  
**Time:** 60 minutes  
**Week:** 7, Day 44  

---

## Today's goal

1. Workbook, worksheet, cell, range  
2. Formulas start with `=`  
3. SUM, AVERAGE, MAX, MIN, COUNT, IF  
4. Charts  
5. Cell references: relative vs absolute  

---

## 1. Definition

> A **spreadsheet** is an application that stores data in rows and columns and can calculate using formulas.

**MS Excel, Google Sheets, LibreOffice Calc.**

- **Workbook** = the file (`.xlsx`)  
- **Worksheet** = one sheet tab  
- **Cell** = intersection (A1)  
- **Range** = A1:A10  
- **Active cell** = selected  

Rows 1,2,3… Columns A,B,C…

---

## 2. Formula rules

- Always start with `=`  
- `=A1+B1`  
- `=SUM(A1:A10)`  
- Fill handle (small square) copies formula down  

**Relative:** `A1` changes when copied (`A2`, `A3`).  
**Absolute:** `$A$1` stays.  
**Mixed:** `$A1` or `A$1`.

---

## 3. Must-know functions

| Function | Use |
|----------|-----|
| SUM | Total |
| AVERAGE | Mean |
| MAX / MIN | Highest / lowest |
| COUNT | Count numbers |
| COUNTA | Count non-empty |
| IF | `=IF(B2>=35,"Pass","Fail")` |
| COUNTIF | Count if condition |
| ROUND | Round off |

**Order:** like maths — brackets, then * /, then + −.

---

## 4. Formatting and tools

Merge cells, wrap text, alignment, number format (₹, %), borders, freeze panes, sort, filter, print area, print preview, page break preview.

**Charts:** column/bar, line, pie — Insert → Chart.  
School: pie of pass/fail; bar of subject averages.

---

## 5. Shortcuts

Ctrl+N/O/S, Home / Ctrl+Home (A1), Ctrl+End, F2 edit cell, Alt+= AutoSum, Ctrl+; date.

---

## 6. School mark register (practise on paper)

| A (Name) | B (Marks) | C (Result) |
|----------|-----------|------------|
| Asha | 78 | `=IF(B2>=35,"Pass","Fail")` |
| Ravi | 30 | … |

`=AVERAGE(B2:B31)` class average.

---

## 7. MCQs

1. Excel file is a: a) slide b) workbook c) only PDF d) kernel  
2. Formulas begin with: a) # b) = c) @ only d) /  
3. $A$1 is: a) relative b) absolute c) a URL d) a virus  
4. Pie chart is best for: a) parts of a whole b) only time series always c) topology d) OS  
5. IF is: a) a chart b) a logical function c) a port d) a deadlock  

**Answers:** 1-b, 2-b, 3-b, 4-a, 5-b

---

## 8. 5-mark answer

Define spreadsheet. Cell/row/column. Five functions. Relative vs absolute. One chart + school marks example.

---

**Next:** [03 — MS PowerPoint](03-ms-powerpoint.md)
