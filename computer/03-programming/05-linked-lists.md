# Chapter PR-5 — Linked Lists

**Paper:** Paper-II Data Structures  
**Time:** 55 minutes  
**Week:** 3, Day 19  

---

## Today's goal

1. Define node and linked list  
2. Compare with array  
3. Draw insert at beginning / end / after a node  
4. Know types: singly, doubly, circular  
5. Write a 5-mark comparison  

---

## 1. Simple explanation

An array is a **row of attached desks**. To insert a child in the middle, everyone must shift.

A **linked list** is children holding the **next child’s shoulder**. To insert, you only change two hands. Desks (memory) need not be next to each other.

Each child is a **node**:

```
+---------+------+
|  DATA   | NEXT |-----> next node
+---------+------+
```

Last node’s NEXT is **NULL** (no one).

---

## 2. Definition

> A **linked list** is a linear data structure where each element (node) contains data and a pointer to the next node. Nodes are connected by links and need not be stored in contiguous memory.

**Head** = pointer to the first node. If head is NULL, the list is empty.

---

## 3. Array vs Linked list

| Point | Array | Linked list |
|-------|-------|-------------|
| Memory | Contiguous | Scattered |
| Size | Fixed (classic) | Grows easily |
| Access | Fast by index | Must walk from head |
| Insert/Delete middle | Shift many | Change pointers |
| Extra memory | No pointer field | Pointer in every node |

---

## 4. Types

| Type | Link |
|------|------|
| **Singly** | Only next |
| **Doubly** | Next and previous |
| **Circular** | Last points to first |
| **Circular doubly** | Both + circle |

---

## 5. Operations (draw, do not memorise long C code)

**Traverse:** start at head; while node ≠ NULL; print data; go to next.

**Insert at beginning:**

1. Create new node  
2. new.next = head  
3. head = new  

**Insert at end:**

1. Walk to last node  
2. last.next = new  
3. new.next = NULL  

**Insert after a given node:**

1. new.next = given.next  
2. given.next = new  

**Delete first:**

1. temp = head  
2. head = head.next  
3. free temp  

**Delete a value:** find the previous node, skip the target (`prev.next = target.next`).

---

## 6. Picture to redraw in exam

```
HEAD --> [10| ] --> [20| ] --> [30| ] --> NULL
```

After insert 15 at beginning:

```
HEAD --> [15| ] --> [10| ] --> [20| ] --> [30| ] --> NULL
```

---

## 7. MCQs

1. Last node of singly list points to: a) head always b) NULL c) 0 only d) OS  
2. Head is: a) last node b) pointer to first c) array index d) CPU  
3. Linked list insert in middle is generally: a) shift all b) pointer change c) format disk d) compile  
4. Doubly list has: a) only next b) next and prev c) only data d) 7 links  
5. Random access is easier in: a) linked list b) array c) both equal always d) neither ever  
6. Empty list: a) head = NULL b) head = 1 c) head = OS d) head = RAM  

**Answers:** 1-b, 2-b, 3-b, 4-b, 5-b, 6-a

---

## 8. 5-mark answer

Define + node diagram. Array vs list table (4 points). Types (singly/doubly/circular). One insert-at-beginning diagram.

---

## Homework

Draw insert at beginning, at end, and delete first. Teach the “shoulder” story to someone.

**Next:** [06 — Stacks and Queues](06-stacks-and-queues.md)
