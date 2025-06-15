# 🛡️ Active Directory Attack & Defense Lab

This project sets up a virtualized **Active Directory Lab** with a Domain Controller (`DC01`), client machine (`WIN10-1`), and attacker machine (`Kali`). Designed for offensive and defensive security practice, red teaming, and VAPT skill-building.

---

## 💻 Machines Overview

| Hostname | Role               | OS                    | IP Address      | Domain      |
|----------|--------------------|------------------------|------------------|-------------|
| DC01     | Domain Controller  | Windows Server 2019    | 192.168.10.10    | corp.local  |
| WIN10-1  | Domain Client       | Windows 10 Pro         | 192.168.10.20    | corp.local  |
| Kali     | Attacker            | Kali Linux             | 192.168.10.30    | N/A         |

---

## ✅ Current Progress

- [x] 🧱 Setup `DC01` (Windows Server 2019)
- [ ] 🖥️ Setup `WIN10-1` (Windows 10)
- [ ] 🐍 Setup Kali Attacker VM
- [ ] 👥 Create AD Users, Groups, and OUs
- [ ] ⚔️ Attack Scenarios (LAPS, Kerberoasting, Pass-the-Hash)
- [ ] 🔐 Detection & Hardening Techniques

---

## 📁 Repositories

- [`DC01`](./DC01/README.md): Setup instructions and config for the Domain Controller
