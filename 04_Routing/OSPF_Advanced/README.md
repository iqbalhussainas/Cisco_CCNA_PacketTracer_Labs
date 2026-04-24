# OSPF Advanced Lab (Cost & Path Selection)

## Objective
Configure OSPF and manipulate path selection using OSPF cost.

## Topology
Three routers connected in a triangle:
R1 - R2 - R3

## IP Addressing
- R1: 10.0.12.1 /30, 10.0.13.1 /30
- R2: 10.0.12.2 /30, 10.0.23.1 /30
- R3: 10.0.23.2 /30, 10.0.13.2 /30

## Configuration Steps
1. Assign IP addresses to all interfaces
2. Enable OSPF (Process ID 1, Area 0)
3. Advertise networks using network command
4. Verify routes using `show ip route`

## OSPF Cost Configuration
- Increased cost on R1 → R3 link
- Forced traffic to take alternate path via R2

## Verification
- `show ip route`
- `show ip ospf neighbor`
- Successful path change observed

## Result
Traffic successfully rerouted using OSPF cost manipulation.
