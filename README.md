 Network Topology Project

Overview
This project demonstrates the configuration and connectivity of a small-scale network using Cisco Packet Tracer. The network consists of two Local Area Networks (LANs) interconnected by a router to simulate communication between different IP subnets.

 Network Components

 Routers
Router0 (1941) – Serves as the gateway between the two LANs.

 Switches
Switch0 (2960-24TT) – Connects the devices in the left LAN.
Switch1 (2960-24TT) – Connects the devices in the right LAN.

 End Devices
Left LAN
  - PC: GCTU (192.168.1.10)
  - PC: Kesse (192.168.1.11)
  - Server: Server1 (192.168.1.20)
Right LAN
  - PC: Brzzy (192.168.2.10)
  - PC: Kelvin (192.168.2.11)
  - Server: Server0 (192.168.2.20)



 IP Addressing Scheme

| Device       | Interface          | IP Address       | Subnet Mask      | Default Gateway  |
|-------------|------------------|----------------|----------------|----------------|
| GCTU        | FastEthernet0     | 192.168.1.11   | 255.255.255.0  | 192.168.1.1    |
| Kesse       | FastEthernet0     | 192.168.1.10   | 255.255.255.0  | 192.168.1.1    |
| Server1     | FastEthernet0     | 192.168.1.13   | 255.255.255.0  | 192.168.1.1    |
| Bizzy       | FastEthernet0     | 192.168.2.10   | 255.255.255.0  |  192.168.2.1   |
| Kelvin      | FastEthernet0     | 192.168.2.11   | 255.255.255.0  | 192.168.2.1    |
| Server0     | FastEthernet0     | 192.168.2.13   | 255.255.255.0  | 192.168.2.1    |
| Router0     | GigabitEthernet0/0| 192.168.1.1    | 255.255.255.0  | N/A            |
| Router0     | GigabitEthernet0/1| 192.168.2.1    | 255.255.255.0  | N/A            |





Configuration Summary

 Switch Configuration
- Configured hostnames for identification.
- Set console passwords for secure access.
- Configured VLAN1 IP addresses for management.
- Saved configurations to startup-config.

Router Configuration
- Assigned IP addresses to router interfaces.
- Activated interfaces with no shutdown.
- Configured routing between LANs (static routes / default gateway).

 End Device Configuration
- Each PC and server assigned a static IP address.
- Default gateways set to the respective router interface.


 Testing & Verification

Ping tests
  - Same LAN: GCTU → Kesse (successful)
  - Cross-LAN: GCTU → Brzzy / Server0 (successful via Router0)
Switch verification
  - show vlan brief
  - show running-config
- Router verification
  - show ip interface brief
  - show ip route



 Conclusion
This network demonstrates proper VLAN management, IP addressing, and inter-LAN routing using a Cisco router and switches. The topology supports communication both within the same LAN and across LANs through the router, reinforcing fundamental concepts of networking and routing.



 Tools Used
- Cisco Packet Tracer
- Cisco 2960-24TT Switch

- Cisco 1941 Router 
