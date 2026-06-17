# Exploiting vsFTPd 2.3.4 Vulnerability (Metasploitable Lab)

## 🧠 Overview
This project demonstrates a full end-to-end exploitation of a vulnerable FTP service (vsFTPd 2.3.4) on the Metasploitable virtual machine using Kali Linux and Metasploit.

The objective was to identify a vulnerable service, exploit it using a known backdoor, and gain root-level access.

This project highlights practical penetration testing skills including reconnaissance, enumeration, exploitation, and post-exploitation.


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
