
# 🛡️ Active Directory Attack-Defense Lab

> A full simulation of an enterprise-grade AD environment to practice real-world attacks (red teaming) and build effective detection strategies (blue teaming).

---

## 📌 Project Goals

- Build a local AD domain (corp.local)
- Simulate attacks like Kerberoasting, DCSync, Pass-the-Hash
- Detect and respond using Sysmon, ELK, PowerShell
- Document MITRE ATT&CK mapping and defenses

---

## 🧱 Lab Topology

| Machine       | Hostname | Role              | OS            |
|---------------|----------|-------------------|---------------|
| Domain Controller | DC01     | AD + DNS          | Windows Server 2019 |
| Client         | WIN10-1  | Domain User       | Windows 10 Enterprise |
| Attacker       | KALI     | Red Team Tools    | Kali Linux    |

![Topology Diagram](docs/topology-diagram.png)

---

## 🧪 Simulated Attacks

- ✅ Kerberoasting
- ✅ Pass-the-Hash
- ✅ DCSync (with Mimikatz or SecretsDump)
- ✅ AS-REP Roasting
- ✅ Privilege Escalation via GPP

Details in the [`/attacks`](./attacks) folder.

---

## 🔎 Detection Stack

- Sysmon (Windows logging)
- ELK Stack
- Custom PowerShell log scripts
- Sigma Rules

More in [`/detection`](./detection).

---

## 📖 How to Use

> Want to recreate this lab? Follow [`setup/lab-setup.md`](./setup/lab-setup.md)

---

## 📚 MITRE ATT&CK Mapping

Included in [`docs/mitre-attack-mapping.png`](./docs/mitre-attack-mapping.png)

---

## 🧠 Key Learnings

- Windows Domain Internals
- Credential dumping and detection
- Event log analysis
- Threat hunting basics

---

## 👥 Authors

- Anant Pandey (Red Team)
- [Your Friend’s Name] (Blue Team)

---

## 📄 License

MIT License
