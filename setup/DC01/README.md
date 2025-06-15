# 🧱 DC01 – Domain Controller (Windows Server 2019)

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
- **Roles Installed:** `AD-Domain-Services` (includes DNS)
- **AD Forest Installation:**
  ```powershell
  Install-ADDSForest -DomainName "corp.local"
  ```

---

## ✅ Verification Commands

```powershell
(Get-ADDomain).DNSRoot              # corp.local
(Get-ADForest).RootDomain           # corp.local
(Get-ADDomainController).Name       # DC01
Resolve-DnsName corp.local          # DNS check
```

---

## 🔍 Notes

- DC01 is the **first Domain Controller** for `corp.local`
- Acts as **AD DS + DNS server**
- Other machines (e.g., WIN10, Kali) will use `192.168.10.10` as their DNS
- `SafeModeAdminPassword` set during forest creation
- AD tools installed via `-IncludeManagementTools`

---

## 🖼️ Screenshots

<details>
<summary><strong>AD & Forest Verification</strong></summary>
<img src="../screenshots/dc01-verification.png" alt="AD Verified">
</details>

<details>
<summary><strong>DNS Resolution</strong></summary>
<img src="../screenshots/dc01-dns-test.png" alt="DNS Resolution">
</details>

---

## ⏱️ Time Tracking

| Task                             | Status  | Time     |
|----------------------------------|---------|----------|
| Windows Setup & Networking       | ✅ Done | ~30 mins |
| AD DS Role & Promotion           | ✅ Done | ~25 mins |
| Post-Install Checks              | ✅ Done | ~5 mins  |

> 📌 **Milestone:** Week 1 – DC01 setup complete.
