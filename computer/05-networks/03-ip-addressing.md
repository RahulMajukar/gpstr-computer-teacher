# Chapter NET-3 — IP Addressing

**Paper:** Paper-II Networks  
**Time:** 60 minutes  
**Week:** 6, Day 38  

---

## Today's goal

1. IPv4 dotted decimal  
2. Classes A, B, C (D, E names)  
3. Public vs private  
4. Subnet mask, default gateway, DNS  
5. IPv6 one-liners  

---

## 1. Simple explanation

An **IP address** is the **postal address** of a computer on a network.

**IPv4:** 32 bits = 4 numbers 0–255, e.g. `192.168.1.5`

**MAC** is the burned-in NIC number (like Aadhaar of the card).  
**IP** can change (like a rented house address).

---

## 2. IPv4 classes (classic exam)

First octet decides class (classful idea):

| Class | First octet | Default mask | Use |
|-------|-------------|--------------|-----|
| **A** | 1–126 | 255.0.0.0 | Huge networks |
| **B** | 128–191 | 255.255.0.0 | Medium |
| **C** | 192–223 | 255.255.255.0 | Small (schools) |
| **D** | 224–239 | — | Multicast |
| **E** | 240–255 | — | Research |

**127.0.0.1** = loopback (this computer). 127 is not Class A for hosts.

---

## 3. Private addresses (must memorise)

These are **not** routed on the public Internet:

- `10.0.0.0` – `10.255.255.255`  
- `172.16.0.0` – `172.31.255.255`  
- `192.168.0.0` – `192.168.255.255`  

School labs use `192.168.x.x` very often.

---

## 4. Mask, network, host

**Subnet mask** marks which part is network, which is host.

`192.168.1.10` with `255.255.255.0`  
- Network: `192.168.1.0`  
- Host: `.10`  
- Broadcast: `192.168.1.255`  

**CIDR:** `/24` means 24 network bits = 255.255.255.0

**Default gateway:** the router IP that leads outside the LAN.  
**DNS:** converts `www.google.com` → IP.  
**DHCP:** automatic IP from a server.

---

## 5. IPv6

- 128 bits, hex, colons: `2001:0db8:85a3::8a2e:0370:7334`  
- Why: IPv4 addresses running out  
- `::1` = loopback  

---

## 6. Static vs dynamic IP

Static: typed by admin (server).  
Dynamic: DHCP (student PCs).

---

## 7. Practice conversions

1. Class of `10.2.3.4` → A (private)  
2. Class of `202.12.5.1` → C  
3. Class of `172.16.0.5` → B private  
4. `/24` mask → 255.255.255.0  

---

## 8. MCQs

1. IPv4 bits: a) 16 b) 32 c) 48 d) 128  
2. IPv6 bits: a) 32 b) 64 c) 128 d) 256  
3. 192.168.0.1 is: a) public always b) private c) Class D d) MAC  
4. 127.0.0.1 is: a) printer b) loopback c) default Class E host d) DNS  
5. DNS converts: a) IP to MAC only b) name to IP c) only hex d) files  
6. DHCP gives: a) automatic IP b) only passwords c) only HTML d) toner  

**Answers:** 1-b, 2-c, 3-b, 4-b, 5-b, 6-a

---

## 9. 5-mark answer

Define IP. IPv4 format. Table of Class A/B/C. Private ranges. One line IPv6. Mention gateway and DNS.

---

**Next:** [04 — Routing Basics](04-routing-basics.md)
