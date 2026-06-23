# 🌐 Cisco Packet Tracer — Getting Started Course

> A complete beginner-friendly networking course using Cisco Packet Tracer, covering network fundamentals, IP configuration, device setup, and connectivity testing.

---

## 📋 Table of Contents

- [About the Course](#about-the-course)
- [Course Project](#course-project)
- [What I Learned](#what-i-learned)
- [Network Topology](#network-topology)
- [Technologies Used](#technologies-used)
- [Project Results](#project-results)
- [Key Commands](#key-commands)
- [IP Addressing Table](#ip-addressing-table)
- [Author](#author)

---

## 📖 About the Course

**Course Name:** Getting Started with Cisco Packet Tracer  
**Platform:** Cisco NetAcad / Packet Tracer  
**Level:** Beginner  
**Status:** ✅ Completed  
**Score:** 🏆 4/4 (Perfect Score)  
**Time Elapsed:** 01:32:40  

This course introduces learners to the fundamentals of computer networking using Cisco Packet Tracer — a powerful network simulation tool. It covers how devices communicate, how to configure routers and end devices, and how to verify network connectivity.

---

## 🏗️ Course Project

### Project Title: **Build a Small Network**

The hands-on project involved building and configuring a complete home network from scratch inside Cisco Packet Tracer. The goal was to connect multiple devices through a Wireless Router and Cable Modem and verify connectivity to a remote server (`cisco.srv`).

---

## 📚 What I Learned

### 🌐 Network Fundamentals
- How to connect devices using different cable types:
  - 🔌 **Ethernet (Copper Straight-Through)**
  - 📺 **Coaxial** (Router ↔ Cable Modem)
  - 📶 **Wireless** (Laptop via WPC300N module)
- Setting up a home network with a Wireless Router, Cable Modem & Internet cloud
- Difference between **wired** (PC via Ethernet) and **wireless** (Laptop via WPC300N) connections

### ⚙️ IP Configuration
- Assigning **IPv4 addresses** and **subnet masks** to network devices
- Understanding **DHCP** — how routers assign IP addresses automatically
- Using `ipconfig /all` to inspect network settings from the Command Prompt
- Difference between **IPv4** and **IPv6** addressing

### 🔗 Connectivity Testing
- Running a successful **ping** to `cisco.srv` (209.165.200.225) — 4/4 replies received
- Verifying end-to-end connectivity across the entire network
- Accessing `cisco.srv` through a **Web Browser** from the Laptop wirelessly
- Troubleshooting basic network connectivity issues

### 🛠️ Hands-On Device Configuration
- Powering off the Laptop and swapping the Ethernet module for a **Wireless WPC300N** module
- Connecting the Laptop to the **"HomeNetwork"** SSID using PC Wireless
- Configuring PC wireless settings and verifying DHCP-assigned addresses
- Using **PC Wireless** tool to scan and connect to available SSIDs

---

## 🗺️ Network Topology

```
[PC] ──Ethernet──► [Wireless Router] ──Coaxial──► [Cable Modem] ──► [Internet] ──► [cisco.srv]
                          │
                    (Wireless 📶)
                          │
                      [Laptop]
```

### Devices in the Network

| Device          | Connection Type | Interface       |
|-----------------|-----------------|-----------------|
| PC              | Wired (Ethernet)| FastEthernet0   |
| Laptop          | Wireless        | WPC300N Module  |
| Wireless Router | Hub device      | LAN + WAN ports |
| Cable Modem     | Coaxial         | Coax port       |
| Internet Cloud  | WAN             | —               |
| cisco.srv       | Remote Server   | —               |

---

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| **Cisco Packet Tracer** | Network simulation environment |
| **Wireless Router** | Local network hub, DHCP server |
| **Cable Modem** | WAN connectivity to internet |
| **WPC300N Module** | Wireless NIC for Laptop |
| **DHCP** | Automatic IP address assignment |
| **IPv4** | Network layer addressing |
| **Ping** | Connectivity testing tool |
| **ipconfig** | Windows IP configuration utility |
| **Web Browser** | Application layer connectivity test |

---

## ✅ Project Results

### Assessment Score: **4 / 4** 🏆

| Device  | Interface     | Check Item  | Status  | Points |
|---------|---------------|-------------|---------|--------|
| Laptop  | Wireless0     | IP Address  | ✅ Correct | 1 |
| Laptop  | Wireless0     | Subnet Mask | ✅ Correct | 1 |
| PC      | FastEthernet0 | IP Address  | ✅ Correct | 1 |
| PC      | FastEthernet0 | Subnet Mask | ✅ Correct | 1 |

**Completion:** 100%

---

## 💻 Key Commands

```bash
# View full IP configuration on a device
ipconfig /all

# Test connectivity to cisco.srv
ping cisco.srv

# Test connectivity using IP address
ping 209.165.200.225
```

### Sample Ping Output
```
Pinging 209.165.200.225 with 32 bytes of data:
Reply from 209.165.200.225: bytes=32 time=2ms TTL=127
Reply from 209.165.200.225: bytes=32 time=29ms TTL=127
Reply from 209.165.200.225: bytes=32 time=1ms TTL=127
Reply from 209.165.200.225: bytes=32 time=1ms TTL=127
```
✅ All 4 replies received — Network is working!

---

## 🔢 IP Addressing Table

| Device         | IPv4 Address     | Subnet Mask   | Default Gateway |
|----------------|------------------|---------------|-----------------|
| PC             | 192.168.0.x (DHCP)| 255.255.255.0 | 192.168.0.1    |
| Laptop         | 192.168.0.x (DHCP)| 255.255.255.0 | 192.168.0.1    |
| Wireless Router| 192.168.0.1      | 255.255.255.0 | —              |
| cisco.srv      | 209.165.200.225  | —             | —              |

> 📝 *IP addresses for PC and Laptop were assigned automatically via DHCP from the Wireless Router.*

---

## 👩‍💻 Author

**Course Completed By:** *NOOR UL NISA* 

**Institution:** Virtual University of Pakistan  
**Date:** June 2026  
**LinkedIn:** https://www.linkedin.com/in/noorulnisa416/ 

**Course:** Getting Started with Cisco Packet Tracer — Cisco NetAcad  

---

## 🚀 What's Next?

- [ ] Complete CCNA 1 — Introduction to Networks
- [ ] Build a multi-switch LAN topology
- [ ] Configure VLANs and inter-VLAN routing
- [ ] Learn about subnetting and CIDR notation
- [ ] Explore cybersecurity fundamentals

---

> *"Every expert was once a beginner. This is just the start of my networking journey!"* 🌐💙
