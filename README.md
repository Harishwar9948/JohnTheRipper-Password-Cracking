# 🔐 John the Ripper – Cracking MD5Crypt Passwords

## 📌 Overview
This repository documents a hands-on ethical hacking exercise using **John the Ripper** to crack MD5Crypt hashed passwords in a **controlled lab environment**.  
The exercise demonstrates both command-line and GUI-based approaches, highlighting password security risks.

---

## ⚠️ Disclaimer
> This project was conducted in a **legal and isolated lab environment** for **educational purposes only**.  
> No real-world or unauthorized systems were targeted.

---

## 🧪 Objectives
- Demonstrate Single Mode and Wordlist Mode attacks
- Perform password cracking for single-user and multiple-user accounts
- Validate successful password recovery
- Compare command-line and GUI performance
- Explore strengths and limitations of John the Ripper

---

## 🛠️ Tools Used
- **John the Ripper** (Community Edition)
- **Johnny** (GUI for John the Ripper)
- **RockYou** wordlist
- **Kali Linux 2024.1**

---

## 📂 Lab Environment
- **OS:** Kali Linux 2024.1 (Attacker machine)
- **Hash Format:** MD5Crypt (`$1$` prefix)
- **Scope:** User accounts created for simulation

---

## 📄 Report Contents
- Overview of John the Ripper & MD5Crypt
- Environment setup
- Step-by-step cracking process (CLI & GUI)
- Syntax summary for key commands
- Attack results & cracked password validation
- Limitations & conclusions

---

## 🎯 Key Results
| Mode           | Target Type       | Result      |
|----------------|-------------------|-------------|
| Single Mode    | Single user       | ✅ Cracked  |
| Wordlist Mode  | Multiple users    | ✅ Cracked  |
| Incremental    | Not tested        | ❌ Skipped  |
| External       | Not tested        | ❌ Skipped  |

---

## 📜 Common Commands Cheat Sheet
```bash
# Crack in Single Mode
john --single hashes.txt

# Crack using Wordlist
john --wordlist=rockyou.txt hashes.txt

# Apply rules with Wordlist
john --wordlist=rockyou.txt --rules hashes.txt

# View cracked passwords
john --show hashes.txt

# Detect hash format
john --list=formats

# Launch Johnny GUI
johnny
