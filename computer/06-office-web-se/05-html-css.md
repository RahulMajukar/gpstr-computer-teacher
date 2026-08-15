# Chapter OF-5 — HTML and CSS Basics

**Paper:** Paper-II Web Technologies  
**Time:** 55 minutes  
**Week:** 7, Day 46  

---

## Today's goal

1. HTML is not a programming language (markup)  
2. Skeleton of a page  
3. Common tags  
4. CSS idea  
5. Write a 10-line page on paper  

---

## 1. Definitions

> **HTML (HyperText Markup Language)** structures web page content using tags.  
> **CSS (Cascading Style Sheets)** styles that content (colour, font, layout).  
> **Tag:** `<p>Hello</p>` — opening and closing.

HTML is **markup**, not like C (no loops required for basics). Browser **interprets** it.

---

## 2. Page skeleton (memorise)

```html
<!DOCTYPE html>
<html>
<head>
  <title>My School</title>
</head>
<body>
  <h1>GPSTR Lab</h1>
  <p>Welcome to Class 7 Computer.</p>
</body>
</html>
```

- `<head>` — not visible title/meta  
- `<body>` — visible content  
- `<title>` — browser tab  

---

## 3. Tag list

| Tag | Use |
|-----|-----|
| h1…h6 | Headings |
| p | Paragraph |
| br | Line break |
| hr | Line |
| b / strong, i / em | Bold, italic |
| u | Underline |
| a href="" | Link |
| img src="" alt="" | Image |
| ul / ol / li | Lists |
| table, tr, th, td | Table |
| div / span | Containers |
| form, input | Forms |

**Attribute:** extra info — `href`, `src`, `alt`.

```html
<a href="https://diksha.gov.in">DIKSHA</a>
<img src="lab.jpg" alt="Computer lab">
```

---

## 4. CSS three ways

1. **Inline:** `<p style="color:red">`  
2. **Internal:** `<style>` in head  
3. **External:** `.css` file linked  

```css
h1 { color: navy; text-align: center; }
```

---

## 5. School teaching tip

Class 8: students write a “My School” page with heading, one picture, one link. Save as `.html` and open in Chrome. This is a complete **lab practical**.

---

## 6. MCQs

1. HTML is: a) DBMS b) markup language c) OS d) compiler  
2. Visible part is: a) head only b) body c) title only d) CSS file only  
3. Link tag: a) p b) a c) br d) hr  
4. CSS is for: a) style b) only SQL c) only routing d) only Excel  
5. alt on img is: a) virus b) alternate text c) IP d) primary key  

**Answers:** 1-b, 2-b, 3-b, 4-a, 5-b

---

## 7. 5-mark answer

Define HTML + CSS. Write a 8-line page with h1, p, a, img. Mention body vs head. One use in school (class website).

---

**Next:** [06 — Client–Server](06-client-server.md)
