# CCNA Static Routing Configuration

![Cisco](https://img.shields.io/badge/Cisco-Packet%20Tracer-blue)
![Routing](https://img.shields.io/badge/Routing-Static-success)
![CCNA](https://img.shields.io/badge/CCNA-Lab-red)

## Overview 
             
This project demonstrates the implementation of Static Routing using Cisco Packet Tracer.

The network consists of two LANs connected through two Cisco routers over a serial WAN link. Static routes are configured manually to enable communication between devices located in different networks.

---
 
## Objectives

- Design a network topology
- Configure router interfaces
- Configure IPv4 addressing
- Configure Serial WAN connection
- Implement Static Routing
- Verify connectivity using Ping

---

## Network Topology

<img width="716" height="402" alt="image" src="https://github.com/user-attachments/assets/4c8eb91b-76ab-4637-b503-7cb2066d8177" />


---

## Devices Used

| Device | Quantity |
|---------|---------:|
| Cisco Router | 2 |
| Cisco Switch | 2 |
| PCs | 2 |
| Laptops | 2 |
| Serial Connection | 1 |

---

## IP Addressing Plan

### LAN 1

| Device | Interface | IP Address |
|---------|-----------|------------|
| Router R0 | Fa0/0 | 192.168.1.1/24 |
| PC0 | NIC | 192.168.1.2 |
| Laptop0 | NIC | 192.168.1.3 |

### LAN 2

| Device | Interface | IP Address |
|---------|-----------|------------|
| Router R1 | Fa0/1 | 192.168.2.1/24 |
| PC1 | NIC | 192.168.2.2 |
| Laptop1 | NIC | 192.168.2.3 |

### WAN

| Device | Interface | IP Address |
|---------|-----------|------------|
| Router R0 |Fa0/1 | 10.0.0.1/30 |
| Router R1 |Fa0/0 | 10.0.0.2/30 |

---

## Configuration Steps

### 1. Build the Network

- Add routers
- Add switches
- Add PCs
- Add Laptops
- Connect all devices

---

### 2. Configure Interfaces

Assign IPv4 addresses and enable interfaces.

```
interface g0/0
ip address ...
no shutdown
```

---

### 3. Configure Serial Interface

```
interface s0/0/0
ip address ...
clock rate 64000
no shutdown
```

---

### 4. Configure Static Routing

#### Router R0

```
ip route 192.168.2.0 255.255.255.0 10.0.0.2
```

#### Router R1

```
ip route 192.168.1.0 255.255.255.0 10.0.0.1
```

---

## Verification

Connectivity was verified successfully using:

- PC0 → PC1

<img width="586" height="413" alt="image" src="https://github.com/user-attachments/assets/cb346409-104d-4a1b-a7e9-86e7771a9f30" />

- Laptop0 → Laptop1

<img width="597" height="399" alt="image" src="https://github.com/user-attachments/assets/cecd2fbb-dbd3-4d48-93df-c858004b4089" />



---

## Skills Demonstrated

- Cisco Packet Tracer
- Static Routing
- IPv4 Addressing
- WAN Configuration
- Router Configuration
- Troubleshooting

---

## Repository Structure

```
CCNA-Static-Routing
│
├── LICENSE
├── README.md
├── Static Routing Configuration in Cisco Packet Tracer.pdf
└── Static-Routing.pkt

```

---

## Author

**Farhan Ali**

BS Computer Science

University of Central Punjab (UCP)

---

⭐ If you found this project useful, feel free to star the repository.
