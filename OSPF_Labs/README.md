🌐 OSPF Single Area Lab (Cisco Packet Tracer)
👤 Author
Iqbal Hussain

📘 Overview
This project demonstrates OSPF (Open Shortest Path First) configuration in a single area (Area 0) using Cisco Packet Tracer.
It is part of CCNA practice labs focusing on dynamic routing fundamentals.

🎯 Objectives
Configure IP addressing on routers and PCs
Enable OSPF routing protocol (Area 0)
Establish neighbor relationships between routers
Verify routing tables and connectivity
Test end-to-end communication between different networks
🖧 Network Topology
PC1 --- R1 --- R2 --- R3 --- PC2
📍 IP Addressing Table
🔹 R1
G0/0 → 192.168.1.1/24
G0/1 → 10.0.12.1/24
🔹 R2
G0/0 → 10.0.12.2/24
G0/1 → 10.0.23.2/24
🔹 R3
G0/0 → 10.0.23.3/24
G0/1 → 192.168.2.1/24
🔹 PCs
PC1 → 192.168.1.10/24
PC2 → 192.168.2.10/24
⚙️ OSPF Configuration
Example (R1)
router ospf 1
network 192.168.1.0 0.0.0.255 area 0
network 10.0.12.0 0.0.0.255 area 0
R2 & R3 configured similarly for connected networks.
🔍 Verification Commands
show ip ospf neighbor
show ip route
ping <destination IP>
📡 Expected Result
All routers form OSPF adjacency
Routes appear with O (OSPF) in routing table
PC1 can ping PC2 successfully
🛠 Tools Used
Cisco Packet Tracer
Cisco Routers (IOS)
Basic networking concepts
🚀 Learning Outcome
After completing this lab, you will understand:

How OSPF builds routing tables dynamically
How routers share network information
How multi-router networks communicate without static routes
📌 Next Labs
OSPF Multi-Area
NAT/PAT Configuration
ACL Security Lab
DHCP Advanced Lab
⭐ If you find this useful, star the repository and follow for more CCNA + Cybersecurity labs.
