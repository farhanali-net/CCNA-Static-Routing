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
| Router R1 | G0/0 | 192.168.1.1/24 |
| PC0 | NIC | 192.168.1.2 |
| Laptop1 | NIC | 192.168.1.3 |

### LAN 2

| Device | Interface | IP Address |
|---------|-----------|------------|
| Router R2 | G0/0 | 192.168.2.1/24 |
| PC1 | NIC | 192.168.2.10 |
| Laptop | NIC | 192.168.2.11 |

### WAN

| Device | Interface | IP Address |
|---------|-----------|------------|
| Router R1 | S0/0/0 | 10.0.0.1/30 |
| Router R2 | S0/0/0 | 10.0.0.2/30 |

---

## Configuration Steps

### 1. Build the Network

- Add routers
- Add switches
- Add PCs
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

#### Router R1

```
ip route 192.168.2.0 255.255.255.0 10.0.0.2
```

#### Router R2

```
ip route 192.168.1.0 255.255.255.0 10.0.0.1
```

---

## Verification

Connectivity was verified successfully using:

- PC1 → PC3
- PC2 → PC4

Include ping screenshots inside the **images** folder.

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
├── README.md
├── packet-tracer/
├── documentation/
├── configs/
└── images/
```

---

## Author

**Farhan Ali**

BS Computer Science

University of Central Punjab (UCP)

---

⭐ If you found this project useful, feel free to star the repository.
