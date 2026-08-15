# Chapter NET-4 — Routing Basics and Network Devices

**Paper:** Paper-II Networks  
**Time:** 45 minutes  
**Week:** 6, Day 39  

---

## Today's goal

1. What routing means  
2. Router vs switch vs hub vs gateway  
3. Static vs dynamic routing  
4. Default route  
5. One 5-mark comparison table  

---

## 1. Simple explanation

Inside one classroom LAN, a **switch** delivers frames using **MAC** (who is on which wire).

To leave the classroom and reach another school or the Internet, you need a **router**. Routing is **choosing a path** using **IP**.

Think: switch = corridor prefect; router = traffic police at the highway junction.

---

## 2. Definitions

> **Routing:** the process of selecting a path for packets to travel from source network to destination network.  
> **Router:** a device (or software) that forwards packets between different networks using a routing table.

---

## 3. Device comparison (write this table in every paper)

| Device | Address used | Broadcast? | Networks |
|--------|--------------|------------|----------|
| **Hub** | None (bits to all) | Yes, always | Same LAN, dumb |
| **Switch** | MAC | Only as needed | Same LAN, smart |
| **Router** | IP | Not flooded like hub | **Different** networks |
| **Gateway** | May translate | — | Different protocols / to Internet |
| **Modem** | Signal convert | — | To ISP line |
| **Repeater** | None | — | Extend cable distance |

---

## 4. Routing table idea

Each router stores: destination network → next hop + interface.

**Default route `0.0.0.0`:** “If I do not know, send to this ISP router.”

| Type | Meaning |
|------|---------|
| **Static** | Admin types routes; small school |
| **Dynamic** | Routers share info (RIP, OSPF, BGP — names) |

**RIP:** distance vector, hop count (max 15).  
**OSPF:** link state, faster, larger nets.  
**BGP:** between ISPs on the Internet.

**Hop:** one router-to-router jump.

---

## 5. Packet journey (exam story)

1. PC checks: is destination IP in my LAN?  
2. Yes → ARP finds MAC, switch delivers.  
3. No → send to **default gateway** (router).  
4. Router looks up table, forwards to next router… until destination network.  
5. Last LAN switch delivers to the host.

---

## 6. MCQs

1. Router works mainly with: a) MAC only b) IP c) only HTTP d) toner  
2. Switch uses: a) IP only b) MAC c) only port 80 d) roll numbers  
3. RIP hop limit often: a) 2 b) 15 c) 128 d) 1024  
4. Default gateway is: a) a printer b) way out of LAN c) a compiler d) BIOS  
5. Static routing is: a) automatic always b) manually configured c) a virus d) only IPv6  
6. Hub sends data: a) to one MAC always b) to all ports c) to Internet only d) to ROM  

**Answers:** 1-b, 2-b, 3-b, 4-b, 5-b, 6-b

---

## 7. 5-mark answer

Define routing. Table: hub / switch / router. Static vs dynamic. Default gateway in a school lab.

---

**Next:** [05 — Internet and Browsers](05-internet-browsers.md)
