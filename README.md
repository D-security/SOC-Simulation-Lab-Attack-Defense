# End-to-End SOC Simulation: Attack, Detection & Response (pfSense + Splunk)


## TL;DR
Simulated a real-world cyber attack, detected malicious activity using Splunk SIEM, and blocked it using pfSense firewall rules.

## Lab Architecture
This diagram shows how traffic flows through the environment during the attack and detection process.
``` 
Kali Linux Attacker → Target VM (Metasploitable)
           ↓
      pfSense Firewall
           ↓
        Splunk SIEM
``` 

## 🧠 Overview
This project simulates a real-world cyber attack against a vulnerable server, 
followed by detection and response using SIEM and firewall controls.

The goal was to identify how an attacker gains access, 
how the attack appears in logs, 
and how security controls can prevent it.

The objective was to simulate a real-world attack scenario, 
observe how the attack appears within system and network logs, 
and implement security controls to detect and prevent it.

This project focuses on both offensive and defensive perspectives, 
mirroring how a SOC analyst investigates and responds to threats.

## Key Skills Demonstrated
- Web exploitation (SQL injection)
- Privilege escalation (Metasploit)
- Network security (pfSense firewall)
- SIEM monitoring (Splunk)
- Incident response lifecycle


## Attack & Defense Workflow

1. Reconnaissance (Nmap scan to identify open services)
2. Exploitation (Metasploit used to exploit vsFTPd vulnerability)
3. Privilege Escalation (Root access obtained)
4. Detection Gap (No alerts triggered initially)
5. Defensive Implementation
   - pfSense firewall rules configured
   - Splunk SIEM configured for log monitoring
6. Detection & Response
   - Suspicious activity logged in Splunk
   - Alerts generated based on attack patterns
   - Attack traffic blocked via firewall rules
---

## ⚙️ Lab Environment

- Attacker: Kali Linux
- Target: Metasploitable 2
- Platform: VirtualBox
- Network: Host-only network (192.168.56.0)

---

## 🔎 Reconnaissance

The initial scan was performed using Nmap:

```bash
nmap -sV 192.168.56.103
```
### Nmap Scan Result
![Nmap Scan](nmap.png)

## 💥 Exploitation

### Exploit Execution

![Exploit](exploit.png)

![Exploit Step](exploit2.png)

## 🧪 Post-Exploitation

### Root Access

![Root Shell](root.png)

### Exploit Search

![Search Result](https://github.com/D-security/D-Security-Lab/blob/main/search.png))


## 🚀 Future Work

- Implement firewall rules to block the FTP exploit
- Perform additional testing on web vulnerabilities (DVWA, Mutillidae)
- Explore intrusion detection techniques
``
