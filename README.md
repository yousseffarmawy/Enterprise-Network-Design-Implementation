# 🌐 Enterprise Network Design & Implementation

## 📌 Overview

This project demonstrates the design and implementation of a scalable enterprise network using Cisco Packet Tracer.
It simulates a real-world corporate environment with multiple departments segmented using VLANs and connected through a hierarchical network architecture.

---

## 🚀 Key Features

* 🔀 VLAN segmentation for multiple departments
* 🔁 Inter-VLAN Routing using Layer 3 switch (SVI)
* 📡 DHCP Server for automatic IP assignment
* 🔒 Network security (Port Security, BPDU Guard, PortFast)
* 🌐 Trunking between switches
* 🔗 EtherChannel for redundancy and load balancing
* ⚡ Rapid Spanning Tree Protocol (RSTP) for fast convergence

---

## 🏢 Network Structure

### Departments:

* Sales
* Marketing
* HR
* Customer Service

Each department is divided into separate VLANs to improve performance and security.

---

## 🛠️ Technologies Used

* Cisco Packet Tracer
* VLAN (Virtual LAN)
* STP (Rapid PVST)
* DHCP
* EtherChannel
* Inter-VLAN Routing
* Cisco IOS CLI

---

## 📂 Project Structure

```id="p1"
network-design-lab/
│
├── topology/        # Packet Tracer file (.pkt)
├── configs/         # Switch & router configurations
├── screenshots/     # Network design images
└── README.md
```

---

## ⚙️ Core Configuration

### VLAN Example

```id="p2"
vlan 10
name SALES
```

### Inter-VLAN Routing

```id="p3"
ip routing

interface vlan 10
ip address 192.168.10.1 255.255.255.0
```

### DHCP Configuration

```id="p4"
ip dhcp pool VLAN10
network 192.168.10.0 255.255.255.0
default-router 192.168.10.1
```

---

## 🔒 Security Features

* Port Security (MAC limitation)
* BPDU Guard (loop protection)
* PortFast (faster device connection)

---

## 📊 Testing & Verification

* Connectivity tested using `ping`
* DHCP verified using `ipconfig`
* STP status checked via:

```
show spanning-tree
```

* EtherChannel verification:

```
show etherchannel summary
```

## 👨‍💻 Author

Youssef Farmawy

---

## 🎯 Conclusion

This project represents a complete enterprise-level network implementation with scalability, redundancy, and security best practices.
