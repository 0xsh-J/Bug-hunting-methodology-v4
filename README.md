# Bug Bounty Methodology v4

*A practical, real‑world bug bounty workflow — from recon to report.*

---

## 0. Mindset (Very Important)

* Think like an **attacker**, report like a **professional**
* Automate boring tasks, **manually analyze critical parts**
* Always ask: **“What can go wrong here?”**
* Low severity findings → skill building → future criticals

---

## 1. Scope Analysis

### 1.1 Read Program Rules

* In‑scope / Out‑of‑scope assets
* Allowed testing methods
* Rate limits & DoS rules
* Safe harbor

### 1.2 Asset Categorization

* Domains / Subdomains
* IPs
* Mobile / API / Web apps
* Third‑party integrations

> 🎯 Goal: Know *what you are legally allowed to break*

---

## 2. Reconnaissance (Recon)

### 2.1 Passive Recon (No Touch)

**Domains & Subdomains**

* amass
* subfinder
* assetfinder
* crt.sh
* github dorks

**IP & ASN**

* whois
* bgp.he.net
* Shodan (passive)

**Tech Stack Discovery**

* BuiltWith
* Wappalyzer
* HTTP headers

---

### 2.2 Active Recon (Touching Target)

**Subdomain Validation**

* httpx
* httprobe

**Port Scanning**

* nmap (top ports first)
* masscan (careful)

**Directory & File Discovery**

* feroxbuster
* ffuf
* dirsearch

**JS File Collection**

* gau
* waybackurls
* katana

> 🎯 Goal: Increase attack surface

---

## 3. Surface Mapping

Create a map of:

* Auth vs Unauth areas
* Admin panels
* APIs & endpoints
* File uploads
* Payment flows
* Role based features

> 🧠 Draw it on paper or notes — hackers visualize systems

---

## 4. Vulnerability Hunting (Core Phase)

### 4.1 Authentication & Authorization

* IDOR
* Broken access control
* Role bypass
* Privilege escalation
* JWT manipulation

### 4.2 Input‑Based Vulnerabilities

* XSS (Reflected, Stored, DOM)
* SQL Injection
* SSTI
* Command Injection
* XPath Injection

### 4.3 Business Logic Bugs ⭐

* Price manipulation
* Coupon abuse
* Race conditions
* Workflow bypass
* Feature abuse

### 4.4 File Handling

* File upload bypass
* LFI / RFI
* Path traversal
* Image processing bugs

### 4.5 API Security

* Mass assignment
* Missing auth
* Rate limit bypass
* Object level auth issues

---

## 5. JavaScript & Frontend Analysis

* Hardcoded secrets
* Hidden endpoints
* Feature flags
* Client‑side validation bypass

Tools:

* LinkFinder
* JSBeautifier
* Burp

---

## 6. Advanced Testing

* Race conditions (Burp Turbo Intruder)
* HTTP request smuggling
* Cache poisoning
* OAuth misconfigurations
* WebSockets

---

## 7. Exploitation (Proof of Impact)

Ask:

* Can I access another user’s data?
* Can I perform admin actions?
* Can I steal money / tokens?

> 🚫 Do NOT destroy data. Keep it safe.

---

## 8. Validation & Triage

Before reporting:

* Reproduce bug 2–3 times
* Confirm it’s in scope
* Check for duplicates
* Measure real impact

---

## 9. Reporting (This Gets You Paid)

### 9.1 Perfect Report Structure

* Title (clear + impactful)
* Summary
* Steps to reproduce
* Proof (screenshots / video)
* Impact
* Suggested fix

### 9.2 Writing Tips

* Simple English
* No assumptions
* Show business impact

---

## 10. Post‑Report Phase

* Answer triager questions
* Provide extra PoC if asked
* Learn from rejected reports

---

## 11. Skill Upgrade Loop

After every bug:

* What did I miss?
* What worked?
* New payloads learned?

> 🔁 Repeat → Skill → Reputation → Bounties

---

## Recommended Daily Workflow

1. Recon (30–40%)
2. Manual testing (40%)
3. Learning & notes (20%)

---

## Final Hacker Advice 🧠

* Tools don’t find bugs — **YOU do**
* Logic > Automation
* Consistency beats talent

---

If you want:

* 🔥 **Bug Bounty Methodology v4 (PDF)**
* 🎯 **Beginner → Advanced roadmap**
* 🧪 **Real bug case studies**

Just tell me.
