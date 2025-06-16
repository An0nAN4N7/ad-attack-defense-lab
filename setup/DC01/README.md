# 🧱 DC01 – Domain Controller (Windows Server 2019)

> 🎯 **Purpose**: This machine serves as the root of the Active Directory domain `corp.local`. It acts as both the **AD DS** and **DNS server** for the entire lab environment.

---

## 🖥️ Base Configuration

| Parameter        | Value                     |
|------------------|---------------------------|
| Hostname         | `DC01`                    |
| OS               | Windows Server 2019       |
| CPU / RAM        | 2 Cores / 2 GB            |
| Network Adapter  | Internal (`ADLabNet`)     |
| IP Address       | `192.168.10.10`           |
| DNS Server       | `127.0.0.1` (local DNS)   |

---

## ⚙️ Active Directory Setup

- **Domain:** `corp.local`
- **Installed Roles:**
  - Active Directory Domain Services (AD DS)
  - DNS Server (included with AD DS)

### 🛠️ Forest Creation Command

```powershell
Install-ADDSForest -DomainName "corp.local"
```

---

## ✅ Verification Commands

Run these in PowerShell to validate the AD setup:

```powershell
(Get-ADDomain).DNSRoot              # Should return: corp.local
(Get-ADForest).RootDomain           # Should return: corp.local
(Get-ADDomainController).Name       # Should return: DC01
Resolve-DnsName corp.local          # DNS resolution check
```

---

## 🔍 Notes

- `DC01` is the **first and primary Domain Controller** for `corp.local`.
- Acts as both:
  - 🧠 **AD DS**: Active Directory Domain Services
  - 🌐 **DNS Resolver**: Internal domain name resolution
- Other machines in the lab (e.g., `WIN10`, `Kali`) will point to `192.168.10.10` as their **primary DNS**.
- `SafeModeAdminPassword` was set during the forest creation process.
- AD tools were installed using `-IncludeManagementTools`.

---

## 🖼️ Screenshots

<details>
<summary><strong>🧪 AD & Forest Verification</strong></summary>
<img src="../screenshots/dc01-verification.png" alt="AD Verified">
</details>

<details>
<summary><strong>🌐 DNS Resolution</strong></summary>
<img src="../screenshots/dc01-dns-test.png" alt="DNS Resolution">
</details>

---

## ⏱️ Time Tracking

| Task                             | Status  | Time Spent |
|----------------------------------|---------|------------|
| Windows Installation & Networking| ✅ Done | ~30 mins   |
| AD DS Role Installation & Promotion | ✅ Done | ~25 mins |
| Post-Install Verification        | ✅ Done | ~5 mins    |

> 📌 **Milestone Achieved:** `Week 1` – Domain Controller fully operational.
