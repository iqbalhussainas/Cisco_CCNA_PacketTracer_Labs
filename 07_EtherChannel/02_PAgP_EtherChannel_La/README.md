# PAgP EtherChannel Lab

## Objective
Configure EtherChannel using Cisco PAgP protocol.

## Topology
- 2 switches (S1, S2)
- 2 links (Fa0/1 - Fa0/2)

## Configuration

### S1
interface range fa0/1 - 2
switchport mode trunk
channel-group 1 mode desirable

### S2
interface range fa0/1 - 2
switchport mode trunk
channel-group 1 mode auto

## Verification
show etherchannel summary

## Result
- EtherChannel formed using PAgP
- Links bundled successfully
