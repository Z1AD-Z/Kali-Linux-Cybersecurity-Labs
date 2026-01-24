# Nmap — Network Scanning Basics

---

## Introduction

**Nmap (Network Mapper)** is one of the most important tools in cybersecurity.

It is used for:

- Discovering devices on a network  
- Scanning open ports  
- Detecting services and versions  
- Basic reconnaissance before penetration testing  

---

## ⚠️ Legal Reminder

Use Nmap only on:

Your own network  
Authorized lab environments (TryHackMe, HackTheBox)

---

## Key Concepts

| Term           | Meaning                                |
|----------------|----------------------------------------|
| Port           | Entry point for network services       |
| Scan           | Checking which ports are open          |
| Service        | Program running on a port (HTTP, SSH…) |
| Reconnaissance | Information gathering phase            |

---

## Basic Commands

### 1. Scan a Target IP

  nmap 192.168.1.1

### 2. Scan Specific Ports

  nmap -p 22,80,443 192.168.1.10

### 3. Scan All Ports

  nmap -p- 192.168.1.10

### 4. Detect Services and Versions

  nmap -sV 192.168.1.10

### 5.Detect Operating System (OS Fingerprinting)
  
  nmap -O 192.168.1.10

### 6. Aggressive Scan (Full Recon)

  nmap -A 192.168.1.10

### Includes:

Version detection

OS detection

Script scanning

Traceroute

---

## Scan Types

| Scan Type      | Command | Description                     |
|----------------|---------|---------------------------------|
| SYN Scan       |   -sS   | Stealth scan (most common)      |
| TCP Connect    |   -sT   | Full connection scan            |
| UDP Scan       |   -sU   | Scan UDP ports                  |

---

## Simple Example Lab

### Target Scan

  nmap -sV 192.168.1.20

## Example Output May Show

Port 22 → SSH

Port 80 → HTTP

Port 443 → HTTPS

# This helps identify the attack surface of the target system.

 ##  Summary — What to Remember

✔ Nmap is used for scanning and reconnaissance
✔ Open ports reveal running services
✔ Version detection helps identify vulnerabilities
✔ Always scan legally and ethically

  # Nmap is the first step in most penetration testing workflows.
