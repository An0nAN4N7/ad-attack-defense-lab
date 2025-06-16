# 🧩 WIN10 – Domain-Joined Client (Windows 10)

> 🎯 **Purpose**: Simulates a real-world Windows 10 workstation joined to the `corp.local` domain. Used for red/blue teaming, vulnerability exploitation, endpoint hardening, and Active Directory attack simulations.

---

## 🖥️ System Configuration

| Setting           | Value                          |
|-------------------|---------------------------------|
| Hostname          | `WIN10-1`                      |
| OS                | Windows 10 Pro                 |
| Domain            | `corp.local`                   |
| IP Address        | `192.168.10.11`                |
| Subnet Mask       | `255.255.255.0`                |
| Default Gateway   | `192.168.10.1` *(optional)*    |
| DNS Server        | `192.168.10.10` (→ DC01)       |
| Network Type      | Internal (`ADLabNet`)          |

---

## ⚙️ Configuration & Setup

### 🖊️ Rename the Computer

```cmd
wmic computersystem where name="%computername%" call rename name="WIN10-1"
shutdown /r /t 0
```

---

### 🌐 Set Static IP & DNS

```cmd
netsh interface ip set address name="Ethernet" static 192.168.10.11 255.255.255.0 192.168.10.1
netsh interface ip set dns name="Ethernet" static 192.168.10.10
```

---

### 🔗 Join Domain `corp.local`

1. Open:
   ```cmd
   systempropertiescomputername
   ```
2. Click **Change Settings → Change**  
3. Select **Domain**, enter: `corp.local`  
4. Use credentials: `corp\Administrator`  
5. Reboot after successful join

---

### ✅ Post-Join Verification

```cmd
systeminfo | findstr /B /C:"Domain"
whoami
echo %USERDOMAIN%
ping dc01.corp.local
whoami /fqdn
net config workstation
```

---

## 🔍 Notes

- Logged in **locally** on `WIN10-1` using a **domain account**
- ❌ This is *not* a Remote Desktop session into DC01
- ❌ Internet traffic does *not* go through DC01
- ✅ DNS queries (for domain names like `corp.local`) are handled by DC01 at `192.168.10.10`
- Accurate internal resolution requires DC01 as primary DNS

---

## 🖼️ Screenshots

<details>
<summary><strong>📸 Static IP & DNS Configuration</strong></summary>
<img src="../screenshots/win10-ipconfig.png" alt="Static IP Configuration">
</details>

<details>
<summary><strong>📸 Successful Domain Join</strong></summary>
<img src="../screenshots/win10-domain-joined.png" alt="Domain Join Confirmation">
</details>

---

## ⏱️ Time Tracking

| Task                              | Status  | Time Taken |
|-----------------------------------|---------|-------------|
| WIN10 Installation                | ✅ Done | ~15 mins    |
| Network Configuration (IP/DNS)    | ✅ Done | ~10 mins    |
| Domain Join Process               | ✅ Done | ~20 mins    |
| Restart & First Login             | ✅ Done | ~5 mins     |
| Domain Connectivity Verification  | ✅ Done | ~10 mins    |
| Screenshot Captures               | ✅ Done | ~10 mins    |
| Final Documentation Update        | ✅ Done | ~15 mins    |

> 📌 **Milestone:** `Week 2` – WIN10 successfully domain-joined and fully documented.
