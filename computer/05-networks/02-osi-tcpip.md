# Chapter NET-2 — OSI and TCP/IP Models

**Paper:** Paper-II Networks  
**Time:** 60 minutes  
**Week:** 6, Day 37  

---

## Today's goal

1. Why layered models  
2. 7 OSI layers + one job + one protocol/device  
3. 4 TCP/IP layers  
4. Encapsulation idea  
5. Write both stacks from memory  

---

## 1. Simple explanation

Sending a letter: write → cover → stamp → van → plane → van → cover off → read.

Networks do the same in **layers**. Each layer talks to the same layer on the other computer and uses the layer below as a post office.

**OSI** (Open Systems Interconnection) — **ISO**, 7 layers, a **reference** model.  
**TCP/IP** — the model the **Internet actually uses**, 4 layers.

---

## 2. OSI 7 layers (memorise top→bottom or bottom→top)

Memory: **A**ll **P**eople **S**eem **T**o **N**eed **D**ata **P**rocessing  
(Application → Physical)

Or bottom-up: **P**lease **D**o **N**ot **T**hrow **S**ausage **P**izza **A**way

| # | Layer | Job | Examples |
|---|-------|-----|----------|
| 7 | **Application** | User services | HTTP, FTP, SMTP, DNS, Telnet |
| 6 | **Presentation** | Format, encrypt, compress | JPEG, SSL/TLS (often discussed here/app), ASCII |
| 5 | **Session** | Start/end conversation | Dialogs, RPC (idea) |
| 4 | **Transport** | End-to-end; reliability | **TCP**, **UDP**, ports |
| 3 | **Network** | Path; logical address | **IP**, routers, ICMP |
| 2 | **Data Link** | Hop; frames; MAC | Ethernet, switch, PPP |
| 1 | **Physical** | Bits on wire | Cable, hub, repeater, voltage |

**PDU names (MCQ):** Application data → Transport **segment** (TCP) → Network **packet** → Data link **frame** → Physical **bits**.

---

## 3. TCP vs UDP (transport)

| TCP | UDP |
|-----|-----|
| Connection-oriented | Connectionless |
| Reliable, ACK, order | Fast, no guarantee |
| Web, email, file transfer | Video, DNS, games |

---

## 4. TCP/IP 4 layers

| TCP/IP | Maps to OSI |
|--------|-------------|
| **Application** | App + Presentation + Session |
| **Transport** | Transport |
| **Internet** | Network |
| **Network Access / Link** | Data link + Physical |

---

## 5. Encapsulation

Sender: data + headers at each layer.  
Receiver: remove headers layer by layer.

```
[App data]
[TCP header | data]
[IP header | TCP | data]
[MAC header | IP | TCP | data | trailer]
```

---

## 6. Port numbers (common)

HTTP 80, HTTPS 443, FTP 21, SSH 22, SMTP 25, DNS 53, POP3 110, IMAP 143.

---

## 7. MCQs

1. OSI has: a) 4 b) 5 c) 7 d) 10 layers  
2. IP works at: a) Physical b) Network c) Session d) only App  
3. TCP is: a) unreliable b) reliable connection-oriented c) a cable d) a topology  
4. HTTP is: a) Physical b) Application c) Data link d) Hub  
5. Switch mainly: a) Network/IP b) Data link / MAC c) Application d) Presentation  
6. OSI is a: a) cable brand b) reference model c) DBMS d) CPU  

**Answers:** 1-c, 2-b, 3-b, 4-b, 5-b, 6-b

---

## 8. 5-mark answer

Draw 7 boxes. One line each layer. Then 4-layer TCP/IP mapping. Mention TCP vs UDP in one line.

---

## Homework

Write 7 layers twice from memory. List 8 protocols next to the correct layer.

**Next:** [03 — IP Addressing](03-ip-addressing.md)
