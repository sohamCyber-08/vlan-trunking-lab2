# vlan-trunking-lab2
# 🧪 VLAN_TRUNKING_LAB

## 🎯 Objective

Build a multi-switch LAN using VLANs and 802.1Q trunking
to understand VLAN segmentation, access ports, trunk links,
VLAN communication, and Layer 2 isolation.

## 🖥️ Topology

PC1 ─── SW1 ═════ SW2 ═════ SW3 ─── PC4
         │         Trunk       │
        PC2                   PC3
       VLAN 10               VLAN 20
       
## 🌐 IP Addressing

| Device | VLAN | IP Address | Subnet Mask |
|---|---:|---|---|
| Cyber_EMPLOYER_1 | 10 | 10.1.1.1 | 255.255.255.0 |
| Cyber_EMPLOYER_2 | 10 | 10.1.1.2 | 255.255.255.0 |
| IT_EMPLOYER_1 | 20 | 10.2.2.1 | 255.255.255.0 |
| IT_EMPLOYER_2 | 20 | 10.2.2.2 | 255.255.255.0 |

## 🔧 Technologies

- EVE-NG
- Cisco IOS
- VPCS
- IPv4
- VLAN
- Ethernet
- IEEE 802.1Q
- ICMP
- MAC Address Table
  


## 📊 Communication Process

PC1
 ↓
Checks destination subnet
 ↓
Determines PC2 is local
 ↓
ARP Request
 ↓
ARP Reply
 ↓
Ethernet Frame
 ↓
ICMP Echo Request
 ↓
ICMP Echo Reply
 ↓
Successful communication

## ✅ Result

PC1 and PC2 successfully communicated through
the Layer 2 switch within the same IPv4 subnet.

<img width="1826" height="857" alt="Screenshot 2026-09-20 051045" src="https://github.com/user-attachments/assets/889d2d16-f679-4477-a5ba-f17de4012a53" />


<img width="1826" height="857" alt="Screenshot 2026-09-20 051045" src="https://github.com/user-attachments/assets/c21b2615-3f5f-46d8-a155-68a05b8d65e4" />







## 📚 Key Learning

- VLAN segmentation
- VLAN 10 and VLAN 20
- Access ports
- 802.1Q trunking
- Allowed VLANs
- MAC address learning
- Broadcast domains
- Layer 2 communication
- VLAN isolation
- Basic Layer 2 troubleshooting
