📘 NAT (PAT) Configuration Lab
🎯 Objective

The purpose of this lab is to configure NAT Overload (PAT) so that multiple internal devices can access the internet using a single public IP address.

🖧 Topology Overview
LAN Network: 192.168.1.0/24
Router: R1
Inside Interface: G0/0
Outside Interface: G0/1
End Devices: PCs in LAN
⚙️ IP Addressing Scheme
Device	Interface	IP Address
R1	G0/0	192.168.1.1
R1	G0/1	ISP/Public IP
PC1	NIC	192.168.1.2
PC2	NIC	192.168.1.3
🛠️ Configuration Steps
1️⃣ Interface Configuration
interface g0/0
 ip address 192.168.1.1 255.255.255.0
 ip nat inside
 no shutdown
interface g0/1
 ip address <ISP-IP> <SUBNET-MASK>
 ip nat outside
 no shutdown
2️⃣ Access Control List (ACL)
access-list 1 permit 192.168.1.0 0.0.0.255
3️⃣ NAT Overload (PAT) Configuration
ip nat inside source list 1 interface g0/1 overload
🔍 Verification Commands
show ip nat translations
show ip nat statistics
