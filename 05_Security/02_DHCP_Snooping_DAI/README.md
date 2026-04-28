# DHCP Snooping & Dynamic ARP Inspection Lab

## Objective
Implement Layer 2 security using DHCP Snooping and DAI to prevent:
- Rogue DHCP attacks
- ARP spoofing

## Technologies Used
- DHCP Snooping
- Dynamic ARP Inspection (DAI)

## Key Configuration
- Trusted uplink port (Router)
- Rate limiting on access ports
- ARP validation using DHCP binding table

## Verification
- show ip dhcp snooping
- show ip dhcp snooping binding
- show ip arp inspection

## Result
- Legitimate DHCP works
- Rogue DHCP blocked
- ARP spoofing prevented
