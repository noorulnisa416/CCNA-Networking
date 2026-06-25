# 🌐 Exploring Networking with Cisco Packet Tracer

A hands-on learning journey through computer networking fundamentals using Cisco Packet Tracer — the industry-standard network simulation tool.

---

## 📖 About This Project

This repository documents my exploration of computer networking concepts using **Cisco Packet Tracer**. Starting from the basics, I am building, simulating, and troubleshooting real network topologies to develop practical networking skills.

---

## 🎯 Learning Objectives

- Understand core networking concepts (OSI model, TCP/IP, IP addressing)
- Design and simulate network topologies
- Configure Cisco routers and switches using CLI
- Implement VLANs, routing protocols, and network security basics
- Troubleshoot connectivity issues using Packet Tracer tools

---

## 🛠️ Tools & Requirements

| Tool | Details |
|------|---------|
| **Cisco Packet Tracer** | Version 8.x or later (free via Cisco NetAcad) |
| **OS** | Windows / macOS / Linux |
| **Account** | [Cisco NetAcad](https://www.netacad.com/) account (free) |

---

## 📁 Project Structure

```
📦 networking-with-packet-tracer/
├── 📂 01_basic_topologies/
│   ├── peer_to_peer.pkt
│   └── star_topology.pkt
├── 📂 02_ip_addressing/
│   ├── static_ip_config.pkt
│   └── subnetting_practice.pkt
├── 📂 03_vlans/
│   └── vlan_setup.pkt
├── 📂 04_routing/
│   ├── static_routing.pkt
│   └── rip_protocol.pkt
├── 📂 05_dhcp_dns/
│   └── dhcp_server_config.pkt
├── 📂 notes/
│   └── concepts.md
└── README.md
```

---

## 🚀 Topics Covered

### ✅ Completed
- [ ] Installing and navigating Cisco Packet Tracer
- [ ] Building a basic peer-to-peer network
- [ ] Star and bus topology simulation

### 🔄 In Progress
- [ ] IP addressing and subnetting
- [ ] Switch configuration (hostname, passwords, VLANs)
- [ ] Router basic configuration

### 📌 Upcoming
- [ ] Inter-VLAN routing
- [ ] DHCP & DNS server setup
- [ ] Static and dynamic routing (RIP, OSPF)
- [ ] Network security basics (ACLs, port security)
- [ ] Wireless networking simulation

---

## 📚 Key Concepts Learned

### OSI Model Layers
The **7-layer OSI model** helps understand how data travels across a network:
1. Physical → 2. Data Link → 3. Network → 4. Transport → 5. Session → 6. Presentation → 7. Application

### IP Addressing
- **IPv4** format: `192.168.x.x` — 32-bit addresses divided into network and host portions
- **Subnet mask** determines which part is the network vs. host
- **Private IP ranges**: `10.0.0.0/8`, `172.16.0.0/12`, `192.168.0.0/16`

### Basic Router CLI Commands
```bash
Router> enable                        # Enter privileged mode
Router# configure terminal            # Enter config mode
Router(config)# hostname MyRouter     # Set hostname
Router(config)# interface g0/0        # Select interface
Router(config-if)# ip address 192.168.1.1 255.255.255.0
Router(config-if)# no shutdown        # Activate interface
```

---

## 📸 Screenshots

> *(Add screenshots of your Packet Tracer topologies here as you build them)*

---

## 🔗 Resources

- [Cisco NetAcad — Free Networking Courses](https://www.netacad.com/)
- [Packet Tracer Download](https://www.netacad.com/courses/packet-tracer)
- [Cisco IOS Command Reference](https://www.cisco.com/c/en/us/support/ios-nx-os-software/ios-15-4m-t/products-command-reference-list.html)
- [Subnetting Practice Tool](https://subnettingpractice.com/)

---

## 👩‍💻 About Me

**Amna** — BS Botany graduate with a strong interest in bioinformatics and computational skills, now expanding into networking and IT fundamentals.

---

## 📝 License

This project is for educational purposes. Packet Tracer files (`.pkt`) are created using Cisco Packet Tracer software.

---

> *"The network is the computer." — Sun Microsystems*
