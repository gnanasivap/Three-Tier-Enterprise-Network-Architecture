# 🌐 Three-Tier Enterprise Network Architecture | Cisco Packet Tracer

## 📌 Project Overview

This project focuses on designing an enterprise network using the **Three-Tier Network Architecture** model in Cisco Packet Tracer.

The main objective of this lab is to understand hierarchical network design, VLAN segmentation, routing, EtherChannel, network redundancy, and communication between network devices.

This project is part of my **CCNA Hands-on Networking Practice**.

## 🎯 Project Objectives

- Understand Three-Tier Network Architecture.
- Explore Core, Distribution, and Access layers.
- Configure VLANs and trunk connections.
- Understand Inter-VLAN Routing.
- Explore Layer 3 switching.
- Understand EtherChannel and network redundancy.
- Verify end-to-end network connectivity.
- Develop network troubleshooting skills.

## 🖥️ Network Architecture

### Conceptual Network Diagram

```text
               CORE LAYER
             +-------------+
             | Core Switch |
             +-------------+
                /       \
               /         \
       DISTRIBUTION LAYER
      +---------+   +---------+
      | L3 SW 1 |   | L3 SW 2 |
      +---------+   +---------+
          |              |
          |              |
            ACCESS LAYER
      +---------+   +---------+
      | Switch  |   | Switch  |
      +---------+   +---------+
        |     |       |     |
       PC1   PC2     PC3   PC4
```

## 🏗️ Three-Tier Architecture Layers

### 1. Core Layer

- Provides high-speed network connectivity.
- Connects distribution layer devices.
- Supports efficient traffic forwarding.

### 2. Distribution Layer

- Connects the Access and Core layers.
- Supports Inter-VLAN Routing.
- Provides Layer 3 connectivity.
- Supports network policies and redundancy.

### 3. Access Layer

- Connects end-user devices.
- Provides VLAN-based network segmentation.
- Supports access and trunk port configurations.

## 🛠️ Tools & Technologies

| Technology | Purpose |
|---|---|
| Cisco Packet Tracer | Network simulation |
| Layer 3 Switch | Routing and switching |
| Layer 2 Switch | End-device connectivity |
| VLAN | Network segmentation |
| 802.1Q Trunking | Multiple VLAN communication |
| EtherChannel | Link aggregation |
| STP | Loop prevention |
| IPv4 | Network addressing |
| Cisco IOS CLI | Configuration and verification |

## ⚙️ Network Configuration

The following commands are example configurations for enterprise network practice.

### 1. VLAN Creation

```bash
enable
configure terminal

vlan 10
vlan 20
vlan 30
exit
```

### 2. Access Port Configuration

```bash
interface fa0/1
switchport mode access
switchport access vlan 10
exit
```

### 3. Trunk Configuration

```bash
interface gigabitEthernet 0/1
switchport mode trunk
exit
```

### 4. Layer 3 Routing

```bash
ip routing
```

This command enables routing functionality on a supported Layer 3 switch.

### 5. Inter-VLAN Routing

```bash
interface vlan 10
ip address 192.168.10.1 255.255.255.0
no shutdown
exit
```

### 6. EtherChannel Configuration

```bash
interface range fa0/1 - 2
switchport mode trunk
channel-group 1 mode active
exit

interface port-channel 1
switchport mode trunk
exit
```

EtherChannel combines multiple physical links into a single logical connection to improve aggregate bandwidth and redundancy.

### 7. Layer 3 Point-to-Point Connection

```bash
interface gigabitEthernet 0/2
no switchport
ip address 10.0.0.1 255.255.255.252
no shutdown
exit
```

**Note:** Interface numbers and IP addresses are illustrative examples. Actual configurations depend on the network topology.

## 🔍 Network Verification Commands

### Verify VLAN Configuration

```bash
show vlan brief
```

### Verify Trunk Connections

```bash
show interfaces trunk
```

### Verify EtherChannel

```bash
show etherchannel summary
```

### Verify IP Interface Status

```bash
show ip interface brief
```

### Verify Routing Table

```bash
show ip route
```

### Verify Spanning Tree

```bash
show spanning-tree
```

### Test Network Connectivity

```bash
ping <destination-ip>
```

### Verify Packet Path

```bash
tracert <destination-ip>
```

## 🚀 Benefits of Three-Tier Architecture

- Improved network scalability.
- Efficient network management.
- Better network segmentation.
- Improved network redundancy.
- High-speed network communication.
- Easier network troubleshooting.
- Structured enterprise network design.

## 📚 Key Learnings

Through this project, I focused on understanding:

- Hierarchical network architecture.
- Core, Distribution, and Access layers.
- VLAN configuration and trunking.
- Inter-VLAN Routing.
- Layer 3 switching.
- EtherChannel and Port-Channel interfaces.
- Network redundancy and loop prevention.
- IPv4 addressing and routing.
- End-to-end connectivity testing.
- Network troubleshooting.

## 📁 Project File

**Three-Tier Enterprise Network Architecture.pkt**

Open this file using **Cisco Packet Tracer** to explore the complete network topology and configurations.

## 💻 Skills Practiced

- Cisco Packet Tracer
- Enterprise Network Design
- Layer 2 and Layer 3 Switching
- VLAN and Trunking
- Inter-VLAN Routing
- EtherChannel
- Spanning Tree Protocol
- IPv4 Addressing
- Cisco IOS CLI
- Network Troubleshooting

## 👨‍💻 CCNA Journey

This project is part of my ongoing CCNA learning journey.

As an aspiring Network Engineer, I am developing practical networking skills through hands-on Cisco Packet Tracer projects and improving my understanding of enterprise network infrastructure.

**Learning Networking One Lab at a Time! 🌐🚀**
