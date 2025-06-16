# 🛡️ Active Directory Attack & Defense Lab

> 🎯 **Objective**: Simulate an enterprise-grade AD environment with offensive & defensive capabilities. Built for Red Teamers, Blue Teamers, VAPT learners, and OSCP aspirants.

---

## 💻 Machines Overview

| Hostname  | Role               | OS                    | IP Address      | Domain      |
|-----------|--------------------|------------------------|------------------|-------------|
| `DC01`    | Domain Controller  | Windows Server 2019    | 192.168.10.10    | corp.local  |
| `WIN10-1` | Domain Client      | Windows 10 Pro         | 192.168.10.11    | corp.local  |
| `Kali`    | Attacker           | Kali Linux             | 192.168.10.30    | N/A         |

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

| Path             | Description                                          |
|------------------|------------------------------------------------------|
| [`/DC01`](../script/DC01/README.md)     | Domain Controller setup & configuration           |
| [`/WIN10`](../script/WIN10-1/README.md) | Windows 10 domain-joined workstation setup        |
| [`/KALI`](../script/KALI/README.md)     | Offensive attacker Kali Linux VM *(Coming Soon)* |
| [`/setup`](./README.md)                 | Lab topology, host setup, and virtualization info |
| [`/screenshots`](../screenshots)        | Visual reference and verification steps          |

---

## 🧠 Lab Capabilities

This self-contained AD lab allows you to:

- ⚔️ **Perform Red Team simulations**: Kerberoasting, Pass-the-Hash, DCSync, LAPS bypass
- 🧵 **Practice detection**: Analyze logs, monitor event triggers
- 🔐 **Test GPOs & hardening techniques**: Real-world defense strategies
- 🛠️ **Experiment with tools**: Mimikatz, BloodHound, PingCastle, Sysmon, etc.

> 🔐 Perfect for: **VAPT Engineers**, **OSCP Preppers**, **SOC Analysts**, and **Home Lab Enthusiasts**

---

## ⚙️ Requirements

- VirtualBox or VMware (Virtualization Platform)
- Windows Server 2019 ISO
- Windows 10 Pro ISO
- Kali Linux ISO (Rolling)
- Minimum **8–12 GB RAM** recommended for smooth performance

---

## 🕒 Project Timeline

| Week | Milestone                         | Status     |
|------|-----------------------------------|------------|
| 1    | Setup `DC01`, `WIN10-1`, Networking | ✅ Done     |
| 2    | Add AD Users, Groups, OUs, Policies| 🔜 Upcoming |
| 3    | Launch Attacks, Enable Detection  | 🔜 Upcoming |

---

## 🙋‍♂️ Author

> 👨‍💻 Built with 💻 & ❤️ by [An0nAN4N7](https://github.com/An0nAN4N7)  
> 🧠 For hands-on Active Directory mastery and a **resume-boosting portfolio project**
