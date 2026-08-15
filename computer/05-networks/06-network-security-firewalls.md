# Chapter NET-6 — Network Security and Firewalls

**Paper:** Paper-II Networks + Paper-I cyber awareness  
**Time:** 50 minutes  
**Week:** 6, Day 40 (second half)  

---

## Today's goal

1. CIA triad  
2. Threats: virus, worm, trojan, phishing  
3. Firewall, antivirus, encryption  
4. Authentication vs authorization  
5. School-safe rules  

---

## 1. CIA triad (write first in any security answer)

| Letter | Meaning |
|--------|---------|
| **C**onfidentiality | Only the right people read |
| **I**ntegrity | Data not secretly changed |
| **A**vailability | Systems usable when needed |

---

## 2. Malware types

| Type | Behaviour |
|------|-----------|
| **Virus** | Attaches to a file; needs a host; spreads when file runs |
| **Worm** | Spreads by itself on the network |
| **Trojan** | Looks useful; hides harm |
| **Ransomware** | Locks files; asks money |
| **Spyware / adware** | Spies / ads |
| **Keylogger** | Records keys (do not teach how to make one) |

**Antivirus:** detects and removes malware (signatures + behaviour).  
Update definitions regularly on lab PCs.

---

## 3. Attacks (names + one line)

| Attack | Idea |
|--------|------|
| **Phishing** | Fake mail/site to steal password |
| **DoS / DDoS** | Flood so service dies |
| **Man-in-the-middle** | Secret listener |
| **SQL injection** | Bad input into database (name only) |
| **Brute force** | Try many passwords |
| **Social engineering** | Trick humans, not computers |

---

## 4. Firewall

> A **firewall** is hardware and/or software that filters traffic between a trusted network (school LAN) and an untrusted network (Internet) using rules.

- Allow / deny by IP, port, protocol  
- **Packet filter** vs **stateful** vs **application / proxy** (names)  
- Windows Defender Firewall is software; school may have a hardware box  

Firewall ≠ antivirus. They work **together**.

---

## 5. Other controls

| Control | Idea |
|---------|------|
| **Password policy** | Long, not shared, not “1234” |
| **Encryption** | Cipher text; HTTPS, WhatsApp lock |
| **Digital signature** | Prove sender + integrity |
| **VPN** | Encrypted tunnel |
| **Backup** | 3-2-1 idea: copies, media, offsite |
| **Updates / patches** | Close holes |
| **Authentication** | Who are you? (password, OTP, fingerprint) |
| **Authorization** | What may you do? (student ≠ admin) |

---

## 6. School teaching tip

Never demonstrate attack tools. Teach **defence**: lock screen, HTTPS padlock, do not click unknown links, report to the teacher.

---

## 7. MCQs

1. Worm: a) needs a file always b) self-replicates on network c) only a printer d) a topology  
2. Firewall: a) cools CPU b) filters network traffic c) compiles C d) draws ER  
3. Phishing: a) fishing virus in RAM only b) fake site/mail for secrets c) a cable d) OSI layer 1 only  
4. CIA ‘C’ is: a) Compiler b) Confidentiality c) Cache d) Class C IP only  
5. HTTPS gives: a) encryption in transit b) free RAM c) a new CPU d) FAT32  
6. Authentication asks: a) what you may do b) who you are c) only IP class d) only topology  

**Answers:** 1-b, 2-b, 3-b, 4-b, 5-a, 6-b

---

## 8. 5-mark answer

CIA. Virus vs worm. Firewall definition + 3 rules examples (block port, allow 443). Antivirus + password + HTTPS for a school lab.

---

**Next:** [07 — Cyber Safety](07-cyber-safety.md)
