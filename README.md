
# 🧪 VLAN_TRUNKING_LAB

## 🎯 Objective

Build a multi-switch LAN using VLANs and 802.1Q trunking
to understand VLAN segmentation, access ports, trunk links,
VLAN communication, and Layer 2 isolation.

## 🖥️ Topology

<img width="1826" height="857" alt="Screenshot 2026-09-20 051045" src="https://github.com/user-attachments/assets/889d2d16-f679-4477-a5ba-f17de4012a53" />
       
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
  
<img width="1817" height="898" alt="Screenshot 2026-09-20 053445" src="https://github.com/user-attachments/assets/468a2d3c-50f7-4fd5-a242-618d8768fcfa" />
.
.
.
.
<img width="1897" height="955" alt="Screenshot 2026-09-20 053654" src="https://github.com/user-attachments/assets/d778d4aa-821b-4e1c-a7a5-4adc6d4c956c" />
.
.
.
.
<img width="1890" height="980" alt="Screenshot 2026-09-20 053759" src="https://github.com/user-attachments/assets/7967c27a-b1ed-40e2-ab51-15f2a8e3d19a" />
.
.
.
.
<img width="1897" height="1003" alt="Screenshot 2026-09-20 053835" src="https://github.com/user-attachments/assets/20134de8-cf23-41ba-bafd-15997448f139" />
.


## 📊 Communication Process

### Same VLAN Communication

## 📊 Communication Process

### Same VLAN Communication — Cyber Team

```mermaid
flowchart TD
    A[Cyber_TEAM_EMPLOYER_1<br/>10.1.1.1<br/>VLAN 10] --> B[Check Destination IP]
    B --> C{Same VLAN?}
    C -->|Yes| D[Check ARP Table]
    D --> E{MAC Address Known?}

    E -->|No| F[ARP Request]
    F --> G[ARP Reply]
    G --> H[Create Ethernet Frame]

    E -->|Yes| H

    H --> I[First_Floor_Switch<br/>Gi0/2<br/>Access Port]
    I --> J[Gi0/0<br/>802.1Q Trunk]
    J --> K[Main_Switch<br/>Gi0/0 → Gi0/1]
    K --> L[Gi0/0<br/>802.1Q Trunk]
    L --> M[Second_Floor_Switch<br/>Gi0/2<br/>Access Port]
    M --> N[Cyber_TEAM_EMPLOYER_2<br/>10.1.1.2<br/>VLAN 10]

    N --> O[ICMP Echo Request]
    O --> P[ICMP Echo Reply]
    P --> Q[Successful Same-VLAN Communication]
```
## ✅ Result

Cyber_EMPLOYER_1 and Cyber_EMPLOYER_2 successfully communicated with each other within VLAN 10.
IT_EMPLOYER_1 and IT_EMPLOYER_2 successfully communicated with each other within VLAN 20.
Communication between the Cyber and IT teams was blocked because they belong to different VLANs and no Layer 3 routing was configured.
This successfully demonstrated same-VLAN communication and Layer 2 VLAN isolation.



<img width="1868" height="936" alt="Screenshot 2026-09-20 054048" src="https://github.com/user-attachments/assets/2f06ee68-1862-4673-ac64-9572d6f4c9fb" />




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



