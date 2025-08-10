# Firewall Configuration and Testing

## Objective
Configure and test basic firewall rules to allow or block network traffic on Windows/Linux as part of the internship task.

---

##  Tools Used
- **Operating System:** Windows 10 / Ubuntu 20.04 (choose your OS here)
- **Firewall Tool:**
  - Windows: Windows Defender Firewall with Advanced Security
  - Linux: UFW (Uncomplicated Firewall)

---

##  Steps Performed

### 1. **Checked Existing Firewall Rules**
- **Windows:** Opened `Windows Defender Firewall with Advanced Security` → Checked `Inbound Rules` and `Outbound Rules`.
- **Linux:** Ran:
```bash
sudo ufw status verbose
```

---

### 2. **Blocked Port 23 (Telnet)**
- **Windows:** Created a new inbound rule for TCP port 23 → Chose "Block the connection" → Saved the rule.
- **Linux:** Ran:
```bash
sudo ufw deny 23/tcp
```

---

### 3. **Tested the Rule**
- Tried to connect to port 23 using:
```bash
telnet <IP> 23
```
- Connection was blocked as expected.

---

### 4. **Allowed SSH (Linux only)**
```bash
sudo ufw allow 22/tcp
```
---

### 5. **Removed the Test Rule**
- **Windows:** Deleted the inbound block rule for port 23.
- **Linux:**
```bash
sudo ufw delete deny 23/tcp
```
---



## Key Learning
- How to check existing firewall rules.
- How to block/allow ports using Windows Firewall and UFW.
- Understanding inbound and outbound rules.
- The importance of port management for security.


