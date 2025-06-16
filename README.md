<p align="center">
  <img src="https://img.shields.io/badge/Active%20Directory%20Lab-%F0%9F%94%92%20Red%20%26%20Blue%20Team%20Project-informational?style=for-the-badge&color=purple&logo=windows" alt="AD Lab Badge"/>
</p>

<h1 align="center">🧠 Active Directory Attack-Defense Lab</h1>

<p align="center">
  🚀 Built by <a href="https://github.com/An0nAN4N7">An0nAN4N7</a> to simulate enterprise-grade AD attacks and defenses.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Windows_Server-2019-blue?style=flat-square&logo=windows&logoColor=white" />
  <img src="https://img.shields.io/badge/Windows_10-Pro-blue?style=flat-square&logo=windows10" />
  <img src="https://img.shields.io/badge/Kali_Linux-Attacker-critical?style=flat-square&logo=kali-linux" />
  <img src="https://img.shields.io/badge/Stage-Week%202-green?style=flat-square&logo=github" />
</p>

---

## 📁 Project Overview

This repository contains a full AD Attack-Defense Lab setup with:

- ✅ Domain Controller (`DC01`) on Windows Server 2019
- ✅ Client Workstation (`WIN10-1`) joined to domain
- 🔜 Kali Linux as attacker machine *(coming soon)*

Designed for:

- 🧠 Learning Active Directory fundamentals
- ⚔️ Practicing Red & Blue Team skills
- 🛡️ Offensive & Defensive simulations
- 💼 Resume-boosting hands-on experience

---

## 🗺️ Lab Topology

```
        +----------------+
        |    Attacker    |
        |    (Kali)      |
        +----------------+
                |
        +----------------+
        |    WIN10-1     | <-- Domain-Joined Client
        +----------------+
                |
        +----------------+
        |     DC01       | <-- Domain Controller (AD DS + DNS)
        +----------------+

      Network: Internal (ADLabNet)
```

---

## 🖥️ Machines Summary

| Hostname   | OS                  | Role                          | IP Address     |
|------------|---------------------|-------------------------------|----------------|
| DC01       | Windows Server 2019 | Domain Controller + DNS       | 192.168.10.10  |
| WIN10-1    | Windows 10 Pro       | Domain-Joined Client Machine  | 192.168.10.11  |
| Kali       | Kali Linux          | Attacker Box *(Coming Soon)*  | 192.168.10.100 |

---

## 🔧 Tools & Technologies Used

- **VirtualBox / VMware** – Virtualization
- **Windows Server Manager / PowerShell** – Domain Configuration
- **CMD & netsh** – Network Setup
- **AD DS / DNS Roles** – Directory Services
- **Screenshots** – For visual verification

---

## 📁 Repository Structure

```
ActiveDirectoryLab/
├── DC01/               # Domain Controller setup
│   └── README.md
├── WIN10/              # Domain-joined Client setup
│   └── README.md
├── KALI/               # Attacker machine setup (Coming Soon)
│   └── README.md
├── screenshots/        # Screenshots for documentation
├── setup/              # Lab overview & guide
│   └── README.md
├── README.md           # Main project entry point
└── LICENSE             # Project license (MIT)
```

---

## 🧠 Use Cases

- ✅ **Red Teaming:** Kerberoasting, Pass-the-Hash, Enumeration
- ✅ **Blue Teaming:** Event Logs, Sysmon, Winlogbeat
- ✅ **AD Fundamentals:** GPOs, User/Group/OUs management
- ✅ **DNS & Internal Recon Practice**

---

## 📌 Project Status

| Component     | Status        | Notes                            |
|---------------|---------------|----------------------------------|
| `DC01`        | ✅ Complete    | Domain setup & verification      |
| `WIN10-1`     | ✅ Complete    | Joined to domain                 |
| `Kali`        | 🔜 Coming Soon | Attacker tools & scenarios       |
| Users/OUs     | 🔜 Pending     | For attack surface               |
| Attack Chains | 🔜 Planned     | Real-world AD attack simulation  |
| Detection     | 🔜 Planned     | Blue team tooling                |

---

## ✍️ Author

**An0nAN4N7**  
Cybersecurity enthusiast & aspiring VAPT engineer  
GitHub: [@An0nAN4N7](https://github.com/An0nAN4N7)

---

## 📜 License

This project is licensed under the **MIT License**.  
Feel free to fork, modify, and share it for learning or demonstration purposes.

---
