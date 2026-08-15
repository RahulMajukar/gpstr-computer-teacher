# Chapter NET-1 — Networks, LAN/WAN, and Topologies

**Paper:** Paper-I + Paper-II  
**Time:** 55 minutes  
**Week:** 6, Day 36  

---

## Today's goal

1. Define computer network  
2. PAN, LAN, MAN, WAN  
3. Draw 5 topologies  
4. Hub vs switch vs router (preview)  
5. Guided vs unguided media  

---

## 1. Simple explanation

A **computer network** is two or more computers connected to share **data, hardware, and software** (files, printer, internet).

A school lab LAN is a small village road. The **Internet** is the world highway (biggest WAN).

---

## 2. Definitions

> **Computer network:** a collection of interconnected computers and devices that share resources using communication protocols.

---

## 3. Types by area

| Type | Full form | Span | Example |
|------|-----------|------|---------|
| **PAN** | Personal Area Network | Few metres | Bluetooth headset |
| **LAN** | Local Area Network | Room / campus | School lab |
| **MAN** | Metropolitan Area Network | City | Cable TV / city network |
| **WAN** | Wide Area Network | Country / world | Internet, railway booking |
| **CAN** | Campus Area Network | Multi-building campus | University |
| **VPN** | Virtual Private Network | Secure tunnel over public net | Work from home |

**Internet** ≠ **intranet** (private school network) ≠ **extranet** (limited outside access).

---

## 4. Topologies (draw all five)

| Topology | Shape | Merit | Demerit |
|----------|-------|-------|---------|
| **Bus** | One backbone cable | Cheap, simple | Cable cut = many fail; collisions |
| **Star** | All to a hub/switch | Easy to add; one cable fail is ok | Central device fail = all fail |
| **Ring** | Circle | Equal access (token) | One break can stop ring |
| **Mesh** | Many-to-many | Very reliable | Costly cables |
| **Tree** | Stars joined | Hierarchical school labs | Depends on root |
| **Hybrid** | Mix | Flexible | Complex |

**School labs almost always use STAR** (switch in the middle).

```
          [PC]
            |
   [PC]---[SWITCH]---[PC]
            |
          [PC]
```

---

## 5. Transmission media

**Guided (wired):** twisted pair (CAT5/CAT6), coaxial, optical fibre (fastest, light, long distance).  
**Unguided (wireless):** radio, microwave, infrared, satellite, Wi-Fi.

**NIC:** Network Interface Card.  
**MAC address:** 48-bit hardware address of NIC.  
**IP address:** logical address (next chapters).

---

## 6. Devices (one line)

| Device | Layer-ish job |
|--------|----------------|
| **Repeater** | Boosts signal (physical) |
| **Hub** | Dumb box; sends to all |
| **Switch** | Sends to the correct port (MAC) |
| **Bridge** | Joins similar LANs |
| **Router** | Joins networks; uses IP |
| **Gateway** | Joins different architectures |
| **Modem** | Analog ↔ digital |
| **Access point** | Wi-Fi |

---

## 7. MCQs

1. School lab is usually: a) WAN b) LAN c) PAN only d) satellite only  
2. Internet is a: a) LAN b) WAN c) only PAN d) printer  
3. Best lab topology today: a) bus only b) star c) ring only d) mesh home  
4. Fibre uses: a) copper only b) light c) steam d) only Wi-Fi  
5. Hub is: a) intelligent like router always b) broadcasts to all c) a CPU d) an OS  
6. Bluetooth is typically: a) WAN b) PAN c) MAN only d) satellite  

**Answers:** 1-b, 2-b, 3-b, 4-b, 5-b, 6-b

---

## 8. 5-mark answer

Define network. LAN vs WAN (2 points). Draw star and bus. Say school uses star + switch. One line on fibre vs Wi-Fi.

---

**Next:** [02 — OSI and TCP/IP](02-osi-tcpip.md)
