# Chapter OF-6 — Client–Server Concepts

**Paper:** Paper-II Web Technologies  
**Time:** 40 minutes  
**Week:** 7, Day 46  

---

## Today's goal

1. Client vs server  
2. Request–response  
3. Examples: web, email, school server  
4. Peer-to-peer contrast  
5. 5-mark answer  

---

## 1. Simple explanation

When you open DIKSHA in Chrome:

- **Chrome is the client** — it **asks**  
- **DIKSHA computer is the server** — it **answers** with the page  

Many clients can ask one server (whole class browsing one site).

---

## 2. Definitions

> **Client:** a computer or program that requests a service.  
> **Server:** a computer or program that provides a service.  
> **Client–server model:** tasks are split between service requesters and service providers, usually on a network.

---

## 3. Request–response

```
Client  --HTTP GET /page-->  Server
Client  <--HTML + images---  Server
```

**Web server** software: Apache, Nginx, IIS.  
**Mail server, file server, print server, database server, DNS server.**

---

## 4. School lab picture

- Student PCs = clients  
- One machine shares files/printer = server (or a real server)  
- Login authentication can sit on a server  

---

## 5. Peer-to-peer (P2P)

Every computer is equal; they share without a dedicated server (old two-PC file share). Simple but weaker control than client–server.

---

## 6. Thin vs thick client (MCQ)

**Thin:** mostly display; work on server (browser, some labs).  
**Thick / fat:** lots of work on the local PC (full Excel).

---

## 7. MCQs

1. Browser is usually a: a) server b) client c) switch d) BIOS  
2. Client–server uses: a) request and response b) only LIFO c) only 1NF d) only XOR  
3. Apache is: a) a mouse b) web server software c) a topology name only d) a stack  
4. P2P means: a) only one server king b) peers share without dedicated server c) only IPv6 d) only Word  

**Answers:** 1-b, 2-a, 3-b, 4-b

---

## 8. 5-mark answer

Define client and server. Draw request–response. School example (file server + student PCs). One line P2P. Mention HTTP.

---

**Next:** [07 — SDLC and Testing](07-sdlc-testing.md)
