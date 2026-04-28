# Static EtherChannel Lab

## Objective
Configure EtherChannel using manual mode (no protocol).

## Configuration
interface range fa0/1 - 2
switchport mode trunk
channel-group 1 mode on

## Verification
show etherchannel summary

## Result
- EtherChannel formed without negotiation protocol
- Requires exact configuration on both sides
