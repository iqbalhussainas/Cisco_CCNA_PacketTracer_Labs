# 🔐 Port Security Lab (Layer 2 Security)

## 📌 Overview

This lab demonstrates how to configure **Port Security** on a Cisco switch to prevent unauthorized access at Layer 2.
Port Security allows only specific MAC addresses to connect to a switch port, protecting the network from rogue devices.

---

## 🎯 Objectives

* Configure Port Security on access ports
* Limit the number of allowed MAC addresses
* Implement Sticky MAC address learning
* Configure violation modes (shutdown, restrict, protect)
* Test and verify security behavior

---

## 🖥️ Topology

```
PC1 -------- Fa0/1 (S1)
PC2 -------- Fa0/2 (S1)
```

* **S1** → Cisco Switch
* **PC1, PC2** → End Devices

---

## ⚙️ Configuration

### 🔹 Basic Setup

```bash
enable
configure terminal
hostname S1
```

---

### 🔹 Port Security on Fa0/1

```bash
interface fa0/1
switchport mode access
switchport port-security
switchport port-security maximum 1
switchport port-security mac-address sticky
switchport port-security violation shutdown
```

---

### 🔹 Port Security on Fa0/2 (Optional)

```bash
interface fa0/2
switchport mode access
switchport port-security
switchport port-security maximum 1
switchport port-security mac-address sticky
switchport port-security violation restrict
```

---

## 🔍 Verification Commands

```bash
show port-security
show port-security interface fa0/1
show port-security address
```

---

## 🧪 Testing

### ✅ Normal Operation

* Connect PC1 to Fa0/1
* MAC address is learned automatically (sticky)
* Communication works normally

### ❌ Security Violation

* Disconnect PC1
* Connect PC2 to Fa0/1

**Result:**

* Port enters **err-disabled (shutdown)** state

---

## 🔄 Recovery

```bash
interface fa0/1
shutdown
no shutdown
```

---

## 🧠 Key Concepts

| Feature         | Description                                |
| --------------- | ------------------------------------------ |
| Port Security   | Restricts access based on MAC address      |
| Sticky MAC      | Automatically learns and saves MAC address |
| Maximum MAC     | Limits number of devices per port          |
| Violation Modes | Defines action on unauthorized access      |

### 🚨 Violation Modes

* **Shutdown** → Port disabled (default)
* **Restrict** → Drops packets + logs
* **Protect** → Drops packets silently

---

## 📁 Project Structure

```
05_Security/
 └── 01_Port_Security/
      ├── Port_Security.pkt
      ├── topology.png
      └── README.md
```

---

## 🚀 Skills Gained

* Layer 2 Security Implementation
* Cisco Switch Configuration
* Network Attack Prevention Basics

---

## 💡 Author

**Iqbal Hussain**
🔗 GitHub: https://github.com/iqbalhussainas

---

## ⭐ Notes

This lab is part of my **CCNA & Cybersecurity Practice Series**.
More labs coming soon covering:

* DHCP Snooping
* Dynamic ARP Inspection (DAI)
* Layer 2 Attack Mitigation

---
