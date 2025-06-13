
#  Home Network Simulation Lab (VLAN + Wireless + ACL)
![Lab Diagram PNG](<Screenshot 2025-06-13 124412.png>)
##  Purpose
Simulate a realistic home network using Cisco Packet Tracer, segmented with VLANs, secured with ACLs, and extended with wireless access points. The goal was to create a home lab I could later replicate physically to strengthen my practical IT support skills.

##  Lab Components
- Cisco Router (2911)
- Layer 3 Switch (3560)
- 2 Desktops (wired)
- 2 Gaming Consoles (wired)
- 3 Smart TVs (wired or wireless)
- 5 Laptops (wireless)
- 2 Wireless Access Points (Access Point-PT)
- DHCP, Inter-VLAN Routing, ACLs, Port Security

##  VLAN Structure
| VLAN | Purpose    | Subnet           |
|------|------------|------------------|
| 10   | Desktops   | 192.168.10.0/24  |
| 20   | Consoles   | 192.168.20.0/24  |
| 30   | Laptops    | 192.168.30.0/24  |
| 40   | TVs        | 192.168.40.0/24  |
| 99   | Management | 192.168.99.0/24  |

##  Step-by-Step Setup
1. Place and connect devices in Packet Tracer.
2. Create VLANs and assign access ports for each device group.
3. Configure trunk port between switch and router.
4. Create router subinterfaces and assign IPs.
5. Set up DHCP pools for each VLAN.
6. Connect Access Points to the switch, disable internal DHCP, assign VLANs.
7. Add WPC300N cards to laptops, connect to wireless SSID.
8. Configure and apply ACLs on router to restrict inter-VLAN access (e.g., block TVs).
9. Test IP assignments, pings, and device communication.

##  Testing & Results
- Each VLAN device received proper DHCP assignment.
- Laptops successfully connected via Wi-Fi and pinged their gateways.
- ACLs blocked TVs from reaching desktops, laptops, and consoles.
- Switch trunking, DHCP, routing, and ACLs all functioned as intended.

##  Screenshots
![alt text](COnfig1.PNG)
![alt text](config2.PNG)
![Communication Initiation](<ping output1.PNG>)
![Communication Initiation](<ping output2.PNG>)
![alt text](<Screenshot 2025-06-13 124605.png>)
![Trunk](<Screenshot 2025-06-13 124949.png>)
![Router Running-Config](<Screenshot 2025-06-13 125713.png>)
![Switch Running-Config](<Screenshot 2025-06-13 125952.png>)
![ACLs](<Screenshot 2025-06-13 130119.png>)
![Laptop IP Config](<Screenshot 2025-06-13 124605-1.png>)
![TV](<Screenshot 2025-06-13 131120.png>)
![PC](<Screenshot 2025-06-13 131149.png>)
##  Files Included
- `home-network-lab.pkt`
(<../Cisco Packet Tracer 9.0.0/saves/Home LAB Virtual.pkt>)
- `router-config.txt`
(../Documents/router-config.txt)
- `switch-config.txt`
(../Documents/switch-config.txt)
