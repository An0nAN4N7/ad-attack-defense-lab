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
  <img src="https://img.shields.io/badge/Stage-Week%201-green?style=flat-square&logo=github" />
</p>

---

## 📁 Project Structure

| Machine         | Purpose                             | Status    |
|------------------|-------------------------------------|-----------|
| `DC01`           | Domain Controller (`corp.local`)    | ✅ Done    |
| `WIN10-1`        | Domain Workstation (Client)         | ✅ Done    |
| `KALI-ATTACKER`  | Offensive Attack Simulation Machine | 🔜 Coming |


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

## 🖥️ Machines

| Hostname   | OS                  | Role                          | IP Address     |
|------------|---------------------|-------------------------------|----------------|
| DC01       | Windows Server 2019 | Domain Controller + DNS       | 192.168.10.10  |
| WIN10-1    | Windows 10          | Domain-Joined Client Machine  | 192.168.10.11  |
| (Kali)     | Kali Linux          | Attacker Box *(Optional)*     | 192.168.10.100 |

---

## 🛠️ Tools Used

- VirtualBox (Virtualization)
- Windows Server Manager / PowerShell
- CMD & netsh for networking
- AD DS, DNS, netdom for domain setup

---

## 📁 Repository Structure

```
ActiveDirectoryLab/
├── DC01/               # Domain Controller setup
│   └── README.md
├── WIN10/              # Domain-joined Client setup
│   └── README.md
├── screenshots/        # All configuration and verification screenshots
├── README.md           # Main project overview
└── LICENSE             # (Optional) Licensing info
```

---

## 🧑‍💻 Use Cases

- ✅ Red Teaming / Attack Simulation (Kerberoasting, Enumeration, etc.)
- ✅ Blue Teaming / Detection Lab (Event Logs, Sysmon, Winlogbeat, etc.)
- ✅ Active Directory Basics & GPO Testing
- ✅ DNS Enumeration / Pivoting Practice

---

## 📝 Authors

**An0nAN4N7**  
Cybersecurity enthusiast & aspiring VAPT engineer  
GitHub: [An0nAN4N7](https://github.com/An0nAN4N7)

---

## 📌 Status

- ✅ DC01 – Configured & Documented  
- ✅ WIN10 – Domain Joined & Documented  
- ⏳ Kali – Coming Soon (Optional Setup)

---

## 🛡️ License

This project is licensed under the MIT License. Feel free to fork, enhance, and share!

---

