# 🛡️ Active Directory Attack & Defense Lab

This project sets up a virtualized **Active Directory Lab** with a Domain Controller (`DC01`), client machine (`WIN10-1`), and attacker machine (`Kali`). Designed for offensive and defensive security practice, red teaming, and VAPT skill-building.

---

## 💻 Machines Overview

| Hostname  | Role               | OS                    | IP Address      | Domain      |
|-----------|--------------------|------------------------|------------------|-------------|
| DC01      | Domain Controller  | Windows Server 2019    | 192.168.10.10    | corp.local  |
| WIN10-1   | Domain Client       | Windows 10 Pro         | 192.168.10.11    | corp.local  |
| Kali      | Attacker            | Kali Linux             | 192.168.10.30    | N/A         |

---

## ✅ Current Progress

- [x] 🧱 Setup `DC01` (Windows Server 2019)
- [x] 🖥️ Setup `WIN10-1` (Windows 10)
- [ ] 🐍 Setup Kali Attacker VM
- [ ] 👥 Create AD Users, Groups, and OUs
- [ ] ⚔️ Attack Scenarios (LAPS, Kerberoasting, Pass-the-Hash)
- [ ] 🔐 Detection & Hardening Techniques

---

## 📁 Subdirectories

- [`/DC01`](./DC01/README.md): Configuration and setup for the Domain Controller  
- [`/WIN10`](./WIN10/README.md): Setup for domain-joined Windows 10 client  
- [`/KALI`](./KALI/README.md): Offensive Kali Linux attacker machine *(Coming Soon)*  
- [`/setup`](./setup/README.md): Lab networking and VirtualBox setup overview  
- [`/screenshots`](./screenshots): Visual walkthroughs for each stage

---

## 🧠 About the Lab

This is a self-contained Active Directory environment where you can:

- Simulate Red Team attacks (kerberoasting, DCSync, etc.)
- Practice detection with event logs and tools
- Implement Group Policy Objects (GPOs) and hardening techniques
- Test various TTPs using tools like BloodHound, Mimikatz, etc.

> 🔐 Ideal for VAPT learners, OSCP prep, or Blue Team practice.

---

## 📌 Requirements

- VirtualBox / VMware
- Windows Server 2019 ISO
- Windows 10 Pro ISO
- Kali Linux ISO
- 8–12 GB RAM recommended

---

## 🕒 Timeline

| Week | Milestone                        | Status  |
|------|----------------------------------|---------|
| 1    | Setup DC01 + WIN10 + Networking  | ✅ Done |
| 2    | Add Users, Groups, Policies      | 🔜 Next |
| 3    | Begin Attacks & Detection        | 🔜 Next |

---

## 🙋‍♂️ Author

> Built by [An0nAN4N7](https://github.com/An0nAN4N7) for deep Active Directory learning and portfolio impact.

