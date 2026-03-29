# Active Directory Home Lab

## 📌 Overview

This project demonstrates the implementation of a home lab using Active Directory on Windows Server 2022 and a Windows 10 client machine.

The lab simulates a real-world enterprise environment, including domain services, DNS configuration, Group Policy, and user management.

---

## 🖥️ Lab Environment

* **Server:** Windows Server 2022 (Domain Controller)
* **Client:** Windows 10 Pro
* **Virtualization:** Oracle VirtualBox
* **Network:** NAT Network (10.0.2.0/24)

---

## ⚙️ Key Configurations

* Installed Active Directory Domain Services (AD DS)
* Promoted server to Domain Controller
* Configured DNS
* Joined Windows 10 client to domain (`lab.local`)
* Verified connectivity using `ping` and DNS resolution
* Configured firewall rules (ICMP)
* Created domain users via CLI

---

## 🧪 Commands Used

```powershell
ipconfig /all
ping lab.local
gpupdate /force
net user jOrtiz P@ssw0rd123 /add /domain
netsh advfirewall firewall add rule name="Allow ICMP" protocol=icmpv4:8,any dir=in action=allow
```

---

## 🚧 Issues Encountered

* DNS resolution failure when joining domain
* Group Policy update errors
* Password policy restrictions

### ✅ Solutions

* Configured correct DNS server
* Used `ipconfig /flushdns`
* Applied `gpupdate /force`
* Updated password to meet complexity requirements

---

## 📸 Screenshots

*(Add screenshots here later)*

---

## 🎯 Skills Demonstrated

* Active Directory Administration
* DNS Troubleshooting
* Windows Networking
* Group Policy Management
* Command Line (CLI) Usage
* Problem Solving

---

## 🚀 Next Steps

* Create Organizational Units (OUs)
* Implement Group Policy Objects (GPOs)
* Simulate helpdesk scenarios (password reset, user lockout)
