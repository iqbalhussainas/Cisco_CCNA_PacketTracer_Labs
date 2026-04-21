# VLAN Lab (4 PCs - Basic VLAN Segmentation)

## 🎯 Objective
Create and configure multiple VLANs on a switch and understand network segmentation.

---

## 🖧 Topology
4 PCs connected to a single switch.


---

## 🏷️ VLAN Configuration

| VLAN ID | Name  | Devices        |
|----------|------|----------------|
| 10       | SALES | PC1, PC2       |
| 20       | IT    | PC3, PC4       |

---

## 🌐 IP Addressing Plan

| Device | IP Address       | VLAN |
|--------|------------------|------|
| PC1    | 192.168.10.10    | 10   |
| PC2    | 192.168.10.11    | 10   |
| PC3    | 192.168.20.10    | 20   |
| PC4    | 192.168.20.11    | 20   |

---

## ⚙️ Configuration Steps

1. Create VLANs on switch
2. Assign switch ports to VLANs
3. Configure IP addresses on PCs
4. Test connectivity

---

## ❗ Expected Result

- PC1 ↔ PC2 = Ping Successful ✔
- PC3 ↔ PC4 = Ping Successful ✔
- VLAN 10 ↔ VLAN 20 = Ping Failed ❌ (no routing)

---

## 🧠 Learning Outcome

- VLAN segmentation
- Layer 2 isolation
- Basic switch configuration
