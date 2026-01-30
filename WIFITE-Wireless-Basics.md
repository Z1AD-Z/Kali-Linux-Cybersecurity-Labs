#  WiFite — Wireless Basics (Kali Linux)

##  Overview

**WiFite** is a Kali Linux tool used to **audit wireless network security** in a simplified and automated way.  
It helps students and security professionals understand how Wi-Fi protections (WEP/WPA/WPA2/WPS) can be misconfigured and how to improve defenses.

⚠️ **Ethical use only:** Use WiFite *only* on networks you own or have explicit written permission to test.

---

##  What WiFite Is Used For (High-Level)

WiFite is commonly used in authorized lab environments to:

- Discover nearby Wi-Fi access points
- Identify networks using **WEP**, **WPA/WPA2**, or **WPS**
- Assist in **capturing wireless authentication traffic** (e.g., WPA handshakes) for security testing
- Highlight weak configurations (such as risky WPS settings)

WiFite is essentially a “workflow automation” tool that coordinates several wireless utilities under one interface.

---

##  Core Wireless Concepts

### 1) Monitor Mode
To observe wireless traffic, a compatible Wi-Fi adapter must support **monitor mode**.  
This allows the adapter to capture frames in the air instead of just connecting to a network.

### 2) WPA/WPA2 Handshake (Authentication Capture)
In security labs, capturing a **WPA handshake** is used to demonstrate:
- why strong passphrases matter  
- how weak passwords can be guessed offline

### 3) WPS Risks
**WPS (Wi-Fi Protected Setup)** can be convenient but may reduce security if poorly implemented.  
WiFite can help identify WPS-enabled networks so administrators can evaluate whether WPS should be disabled.

---

##  Requirements (Typical Lab Setup)

To use WiFite in a legal testing lab, you usually need:

- Kali Linux (or equivalent environment)
- A Wi-Fi adapter that supports **monitor mode** (and often packet injection)
- Root privileges (`sudo`)

---

##  Basic Launch (Educational)

WiFite is typically started like this:
> sudo wifite

After launching, it scans and lists nearby wireless networks, then guides the user through audit options.

## Defensive Takeaways (How to Stay Secure)
 If you manage a wireless network, key hardening steps include:

Use WPA2-AES or WPA3 (when available).
Disable WEP entirely (obsolete and insecure).
Consider disabling WPS if not needed.
Use long, unique passphrases (high entropy).
Keep router firmware updated.

## Legal & Ethical Notice
 *WiFite* can be used to demonstrate real attack techniques.
Using it without authorization can be illegal and harmful.
 
 **Use it only for:**
Your own networks.
Authorized penetration tests.
Approved classroom/lab environments.

## Skills Gained (Student Perspective)
  Studying WiFite supports learning in:
Wireless security fundamentals (WEP/WPA/WPS).
Practical auditing workflow understanding.
Risk assessment of wireless configurations.
Defensive hardening strategies.

 
