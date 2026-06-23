# 📘 Getting Started with Cisco Packet Tracer — Complete Course Notes

> **Course:** Getting Started with Cisco Packet Tracer  
> **Platform:** Cisco Networking Academy (NetAcad)  
> **Student:** Noor Ul Nisa  
> **Completed:** 22 June 2026  
> **Score:** 🏆 4/4 Perfect  

---

## 📋 Table of Contents

1. [What is Cisco Packet Tracer?](#1-what-is-cisco-packet-tracer)
2. [Network Basics & Key Definitions](#2-network-basics--key-definitions)
3. [Types of Networks](#3-types-of-networks)
4. [Network Devices — Definitions](#4-network-devices--definitions)
5. [Cable Types](#5-cable-types)
6. [IP Addressing](#6-ip-addressing)
7. [DHCP](#7-dhcp)
8. [Wireless Networking](#8-wireless-networking)
9. [Network Topology](#9-network-topology)
10. [Key Commands](#10-key-commands)
11. [Connectivity Testing](#11-connectivity-testing)
12. [Logical vs Physical Mode](#12-logical-vs-physical-mode)
13. [Project — Build a Small Network](#13-project--build-a-small-network)
14. [Quick Revision Glossary](#14-quick-revision-glossary)

---

## 1. What is Cisco Packet Tracer?

**Definition:**  
Cisco Packet Tracer is a **network simulation software** developed by Cisco Systems. It allows students and professionals to design, build, configure, and troubleshoot virtual computer networks without needing real physical hardware.

**Key Features:**
- Simulate real Cisco routers, switches, and end devices
- Test network configurations safely in a virtual environment
- Supports both **Logical** (diagram) and **Physical** (real-world) views
- Used worldwide by CCNA and NetAcad students
- Free to use for Cisco NetAcad enrolled students

**Why use Packet Tracer?**
- No expensive hardware needed
- Safe environment to make and learn from mistakes
- Realistic simulation of real network behavior
- Great for practicing for Cisco certifications (CCNA, CCNP)

---

## 2. Network Basics & Key Definitions

### 🔹 Network
A **network** is a collection of two or more devices (computers, phones, printers) that are connected together to share data and resources.

### 🔹 Computer Network
A system where multiple devices are **interconnected** using wires, cables, or wireless signals to **communicate and share information**.

### 🔹 Node
Any **device connected to a network** — such as a computer, laptop, printer, router, or switch.

### 🔹 Host
A **host** is any device that sends or receives data on a network. Examples: PC, Laptop, Server.

### 🔹 Server
A **server** is a computer that **provides services or resources** (like files, websites, emails) to other devices (clients) on the network.  
Example: `cisco.srv` in our project is a web server.

### 🔹 Client
A **client** is a device that **requests and uses services** from a server.  
Example: The PC and Laptop in our project are clients.

### 🔹 Client-Server Model
A networking model where:
- **Servers** provide resources/services
- **Clients** request and consume those resources
- Example: You open a browser (client) → it connects to Google's web server → Google sends back the webpage

### 🔹 Protocol
A **protocol** is a set of **rules that govern how data is transmitted** between devices on a network.  
Examples: TCP/IP, HTTP, DHCP, DNS

### 🔹 Bandwidth
**Bandwidth** is the **maximum amount of data** that can be transmitted over a network in a given time period. Measured in bits per second (bps, Kbps, Mbps, Gbps).

### 🔹 Latency
**Latency** is the **time delay** between sending and receiving data over a network. Lower latency = faster network response.

---

## 3. Types of Networks

### 🔹 LAN (Local Area Network)
**Definition:** A network that covers a **small geographical area** like a home, office, or school building.  
- Fast speeds (up to 10 Gbps)
- Low cost
- Example: Home Wi-Fi network, school computer lab

### 🔹 WAN (Wide Area Network)
**Definition:** A network that covers a **large geographical area** like cities, countries, or the entire world.  
- The Internet is the largest WAN
- Uses leased lines, fiber optics, satellites
- Slower than LAN, higher cost

### 🔹 WLAN (Wireless Local Area Network)
**Definition:** A LAN that uses **wireless radio signals** instead of cables to connect devices.  
- Uses Wi-Fi technology (IEEE 802.11)
- Example: Connecting a laptop via Wi-Fi to a router

### 🔹 MAN (Metropolitan Area Network)
**Definition:** A network that covers a **city or large campus**.  
- Larger than LAN, smaller than WAN
- Example: City-wide Wi-Fi network

### 🔹 PAN (Personal Area Network)
**Definition:** A very small network for **personal devices** within a few meters.  
- Example: Bluetooth connection between phone and headphones

### 🔹 Internet
**Definition:** The **global network of networks** — millions of interconnected computers and devices worldwide.  
- Uses TCP/IP protocols
- Allows access to websites, email, streaming, etc.

### 🔹 Intranet
**Definition:** A **private network** inside an organization, accessible only to employees.

### 🔹 Extranet
**Definition:** A private network that allows **limited access to outside users** like partners or customers.

---

## 4. Network Devices — Definitions

### 🔹 Router
**Definition:** A router is a networking device that **forwards data packets between different networks**. It connects your home network to the Internet.

**Functions:**
- Connects LAN to WAN (Internet)
- Assigns IP addresses (via DHCP)
- Routes traffic between devices
- Acts as a firewall/security gateway

**In our project:** The **Wireless Router** connected the PC and Laptop to the Cable Modem and Internet.

---

### 🔹 Wireless Router
**Definition:** A router that includes a **built-in wireless access point**, allowing both wired and wireless devices to connect to the network.

**Features:**
- Has LAN ports (for wired devices)
- Has Wi-Fi antenna (for wireless devices)
- Broadcasts an SSID (network name)
- Assigns IPs via DHCP

---

### 🔹 Switch
**Definition:** A switch is a device that **connects multiple devices within the same network (LAN)** and directs data only to the intended recipient device.

**Difference from Hub:**
- Hub sends data to ALL devices → wastes bandwidth
- Switch sends data only to the **correct destination** → efficient

---

### 🔹 Hub
**Definition:** A basic networking device that **connects multiple devices** in a network and broadcasts data to ALL connected ports. Now mostly replaced by switches.

---

### 🔹 Cable Modem
**Definition:** A **modem** (Modulator-Demodulator) converts digital data from your network into a format that can travel over the **cable TV (coaxial) infrastructure** provided by your ISP.

**In our project:** The Cable Modem connected the Wireless Router to the Internet cloud using a Coaxial cable.

---

### 🔹 Access Point (AP)
**Definition:** A device that creates a **wireless local area network (WLAN)**. It connects to a wired router and transmits Wi-Fi signals.

---

### 🔹 Firewall
**Definition:** A security device (hardware or software) that **monitors and controls incoming and outgoing network traffic** based on security rules. Blocks unauthorized access.

---

### 🔹 NIC (Network Interface Card)
**Definition:** A hardware component that **allows a device to connect to a network**.
- Wired NIC → connects via Ethernet cable
- Wireless NIC → connects via Wi-Fi

**In our project:** We replaced the Laptop's wired Ethernet NIC with a **Wireless WPC300N module** to enable Wi-Fi.

---

### 🔹 WPC300N Module
**Definition:** A **wireless network adapter module** for laptops in Cisco Packet Tracer that enables wireless connectivity. It supports the 802.11n Wi-Fi standard.

**Steps used in project:**
1. Power off Laptop
2. Remove Ethernet (copper) module
3. Insert WPC300N wireless module
4. Power on Laptop
5. Connect to HomeNetwork SSID

---

## 5. Cable Types

### 🔹 Ethernet Cable (Copper Straight-Through)
**Definition:** A standard networking cable used to connect **different types of devices**.  
**Used for:** PC/Laptop → Switch, Switch → Router  
**Color in Packet Tracer:** Black  
**In our project:** Connected PC to Wireless Router

---

### 🔹 Crossover Cable (Copper Cross-Over)
**Definition:** A cable used to connect **same types of devices directly**.  
**Used for:** PC → PC, Switch → Switch, Router → Router  
**Color in Packet Tracer:** Black (dashed)

---

### 🔹 Coaxial Cable
**Definition:** A type of cable with a **central copper conductor surrounded by insulation and shielding**, used for cable TV and internet connections.  
**Used for:** Router → Cable Modem  
**In our project:** Connected Wireless Router to Cable Modem  
**Color in Packet Tracer:** Blue/dark

---

### 🔹 Fiber Optic Cable
**Definition:** A cable that transmits data as **pulses of light** through glass or plastic fibers. Very fast and used for long distances.  
**Used for:** Long-distance, high-speed connections  
**Speed:** Up to 100 Gbps+

---

### 🔹 Serial Cable (DCE/DTE)
**Definition:** Used to connect **routers over WAN links** in Packet Tracer simulations.  
**Types:** Serial DCE (provides clock signal), Serial DTE

---

### 🔹 Console Cable
**Definition:** Used to connect a **computer directly to a router or switch for initial configuration** via the console port. Not used for data transfer.

---

### 🔹 Wireless Connection
**Definition:** Data transmitted via **radio waves (Wi-Fi)** without physical cables.  
**Standard:** IEEE 802.11 (a/b/g/n/ac/ax)  
**In our project:** Laptop connected wirelessly to the Wireless Router via WPC300N module

---

## 6. IP Addressing

### 🔹 IP Address (Internet Protocol Address)
**Definition:** A **unique numerical label** assigned to every device on a network that uses the Internet Protocol for communication. It identifies the device's location on the network.

Think of it like a **home address** — every house has a unique address so mail can be delivered to the right place.

---

### 🔹 IPv4 (Internet Protocol Version 4)
**Definition:** The **4th version of the Internet Protocol**, using **32-bit addresses** written as four groups of numbers separated by dots.

**Format:** `192.168.0.1`  
**Range:** 0.0.0.0 to 255.255.255.255  
**Total addresses:** About 4.3 billion  
**Example from project:** `209.165.200.225` (cisco.srv)

**Structure:**
```
192  .  168  .  0  .  1
[8 bits] [8 bits] [8 bits] [8 bits]
         = 32 bits total
```

---

### 🔹 IPv6 (Internet Protocol Version 6)
**Definition:** The **6th and newer version** of the Internet Protocol, using **128-bit addresses** written in hexadecimal.

**Why needed?** IPv4 addresses ran out → IPv6 provides virtually unlimited addresses  
**Format:** `2001:0db8:85a3:0000:0000:8a2e:0370:7334`  
**Total addresses:** 340 undecillion (340 trillion trillion trillion)

---

### 🔹 Subnet Mask
**Definition:** A **32-bit number** that divides an IP address into the **network portion** and the **host portion**.

**Common Subnet Masks:**

| Subnet Mask | CIDR | Hosts per Network |
|---|---|---|
| 255.0.0.0 | /8 | 16,777,214 |
| 255.255.0.0 | /16 | 65,534 |
| 255.255.255.0 | /24 | 254 |

**In our project:** All devices used `255.255.255.0` — meaning up to 254 devices can be on the same network.

---

### 🔹 Default Gateway
**Definition:** The **IP address of the router** that a device uses to communicate with devices on other networks (like the Internet).

**Example:** If PC is `192.168.0.10`, the Default Gateway is usually `192.168.0.1` (the router's IP).

---

### 🔹 DNS (Domain Name System)
**Definition:** A system that **translates human-readable domain names** (like `cisco.srv`, `google.com`) into IP addresses that computers understand.

**Example:**  
You type `cisco.srv` → DNS says → `209.165.200.225` → browser connects

---

### 🔹 Private IP Addresses
Ranges reserved for **internal/private networks** (not routable on the Internet):

| Class | Range | Common Use |
|---|---|---|
| Class A | 10.0.0.0 – 10.255.255.255 | Large networks |
| Class B | 172.16.0.0 – 172.31.255.255 | Medium networks |
| Class C | 192.168.0.0 – 192.168.255.255 | Home/small office |

**In our project:** Devices received `192.168.0.x` addresses from the router (Class C private).

---

### 🔹 Public IP Address
**Definition:** An IP address **assigned by your ISP** that is accessible from the Internet. Every home network has one public IP.

---

## 7. DHCP

### 🔹 DHCP (Dynamic Host Configuration Protocol)
**Definition:** A network protocol that **automatically assigns IP addresses** and other network settings to devices when they join a network.

**What DHCP assigns:**
- IP Address
- Subnet Mask
- Default Gateway
- DNS Server address

**How it works (DORA process):**

```
1. DISCOVER  → Device broadcasts: "I need an IP address!"
2. OFFER     → DHCP Server replies: "I can give you 192.168.0.10"
3. REQUEST   → Device says: "Yes, I want 192.168.0.10"
4. ACK       → Server confirms: "192.168.0.10 is yours!"
```

**In our project:** The Wireless Router acted as the DHCP server and automatically assigned IP addresses to both the PC and Laptop.

**DHCP vs Static IP:**

| DHCP (Dynamic) | Static (Manual) |
|---|---|
| Assigned automatically | Set manually |
| Can change each time | Always stays the same |
| Easy to manage | Better for servers |
| Used for PCs, phones | Used for routers, servers |

---

## 8. Wireless Networking

### 🔹 Wi-Fi
**Definition:** A **wireless networking technology** that uses radio waves to provide network and Internet access to devices within range of a wireless access point.

**Wi-Fi Standards (IEEE 802.11):**

| Standard | Speed | Frequency |
|---|---|---|
| 802.11b | 11 Mbps | 2.4 GHz |
| 802.11g | 54 Mbps | 2.4 GHz |
| 802.11n | 300 Mbps | 2.4/5 GHz |
| 802.11ac | 1.3 Gbps | 5 GHz |
| 802.11ax (Wi-Fi 6) | 9.6 Gbps | 2.4/5/6 GHz |

---

### 🔹 SSID (Service Set Identifier)
**Definition:** The **name of a wireless network** that is broadcast by a wireless router or access point.

**In our project:** The SSID was **"HomeNetwork"** — the Laptop connected to this network using PC Wireless.

---

### 🔹 PC Wireless (in Packet Tracer)
**Definition:** A tool in Cisco Packet Tracer used to **configure and connect a device to a wireless network**.

**Steps to connect:**
1. Click on Laptop → Desktop tab → PC Wireless
2. Click the **Connect** tab
3. See available networks (SSIDs)
4. Click **Refresh** to update list
5. Select **HomeNetwork** → Click **Connect**

---

### 🔹 WPA/WPA2 (Wi-Fi Protected Access)
**Definition:** **Security protocols** that encrypt wireless network traffic to protect it from unauthorized access.
- WPA2 is the most commonly used today
- WPA3 is the newest and most secure

---

## 9. Network Topology

### 🔹 Network Topology
**Definition:** The **physical or logical arrangement** of devices and connections in a network.

### Types of Topology:

**🔹 Bus Topology**  
All devices connected to a single central cable (bus). If the main cable fails, entire network fails.

**🔹 Star Topology** ⭐ (Most Common)  
All devices connect to a **central device (switch/router)**. If one device fails, others still work.  
*Our project uses Star topology.*

**🔹 Ring Topology**  
Devices connected in a **circular loop**. Data travels in one direction around the ring.

**🔹 Mesh Topology**  
Every device connected to **every other device**. Most reliable but expensive.

**🔹 Hybrid Topology**  
A **combination** of two or more topology types.

---

### Our Project Topology:

```
           [PC] ────────────────────────┐
                                   [Wireless Router] ─── [Cable Modem] ─── [Internet] ─── [cisco.srv]
           [Laptop] ·····Wi-Fi·····────┘
```

---

## 10. Key Commands

### `ipconfig`
**Definition:** A Windows command that **displays the current IP configuration** of network adapters.

```cmd
C:\> ipconfig
```
Shows: IPv4 Address, Subnet Mask, Default Gateway

---

### `ipconfig /all`
**Definition:** Displays the **full detailed IP configuration** including MAC address, DHCP server, DNS servers, lease information.

```cmd
C:\> ipconfig /all
```

**Sample Output:**
```
Physical Address.........: D0-BC-0E-C5-D6
IPv4 Address.............: 192.168.0.10
Subnet Mask..............: 255.255.255.0
Default Gateway..........: 192.168.0.1
DHCP Server..............: 192.168.0.1
DNS Servers..............: 209.165.200.225
```

---

### `ping`
**Definition:** A command used to **test connectivity** between two devices. It sends ICMP echo request packets and waits for replies.

```cmd
C:\> ping cisco.srv
C:\> ping 209.165.200.225
```

**Sample Output:**
```
Pinging 209.165.200.225 with 32 bytes of data:
Reply from 209.165.200.225: bytes=32 time=2ms TTL=127
Reply from 209.165.200.225: bytes=32 time=1ms TTL=127
Reply from 209.165.200.225: bytes=32 time=1ms TTL=127
Reply from 209.165.200.225: bytes=32 time=29ms TTL=127
```

✅ 4 replies = network is working perfectly!

**Ping Output Meanings:**

| Result | Meaning |
|---|---|
| `Reply from...` | ✅ Connection successful |
| `Request timed out` | ❌ Device unreachable |
| `Destination host unreachable` | ❌ No route to host |
| `TTL expired in transit` | ❌ Routing loop or too many hops |

---

### `TTL (Time To Live)`
**Definition:** A value in IP packets that **limits how many routers (hops) a packet can pass through**. Each router decreases TTL by 1. When TTL = 0, packet is discarded.

---

## 11. Connectivity Testing

### 🔹 End-to-End Connectivity
**Definition:** The ability for data to travel **from the source device all the way to the destination device** through the entire network path successfully.

**In our project:** We verified that both PC and Laptop could:
1. Get an IP from DHCP ✅
2. Ping cisco.srv ✅
3. Browse cisco.srv via Web Browser ✅

---

### 🔹 ICMP (Internet Control Message Protocol)
**Definition:** A protocol used by network devices to **send error messages and operational information**. The `ping` command uses ICMP.

---

### 🔹 Web Browser Test
**Definition:** Opening a web browser and navigating to a server URL or IP address to **verify HTTP/web connectivity**.

**In our project:** Opened Web Browser on Laptop → navigated to `cisco.srv` → page loaded ✅

---

## 12. Logical vs Physical Mode

### 🔹 Logical Mode
**Definition:** The **default view** in Cisco Packet Tracer showing the **network diagram** — how devices are connected logically with icons and lines.

- Shows device icons and connection lines
- Used for designing and configuring the network
- Doesn't show physical location

---

### 🔹 Physical Mode
**Definition:** Shows a **realistic physical representation** of devices in real-world locations (home, city, country).

- Shows actual building/room layouts
- Useful for understanding real-world deployment
- Allows physical management of devices

---

### 🔹 Realtime Mode vs Simulation Mode

**Realtime Mode:** Network operates at **real speed** — packets travel instantly. Used for normal configuration.

**Simulation Mode:** **Slows down** packet travel so you can see each packet move step by step. Used for **detailed troubleshooting and learning**.

---

## 13. Project — Build a Small Network

### Project Overview
| Item | Detail |
|---|---|
| Course | Getting Started with Cisco Packet Tracer |
| Project | Build a Small Network |
| Score | 4/4 ✅ |
| Completion | 100% |

### Devices Used
| Device | Role | Connection |
|---|---|---|
| PC | Wired client | Ethernet → Router |
| Laptop | Wireless client | Wi-Fi → Router |
| Wireless Router | DHCP server + gateway | LAN + WAN |
| Cable Modem | ISP connection | Coaxial |
| Internet Cloud | WAN simulation | — |
| cisco.srv | Web/DNS server | Remote |

### Step-by-Step What Was Done

**Step 1 — Explored the topology**
- Identified all devices: PC, Laptop, Wireless Router, Cable Modem, Internet, cisco.srv
- Understood how they were connected

**Step 2 — Configured the PC**
- PC received IP via DHCP from Wireless Router
- Ran `ipconfig /all` to verify settings
- Ran `ping cisco.srv` → 4/4 replies ✅

**Step 3 — Configured the Laptop for Wireless**
1. Clicked Laptop → Physical tab
2. Powered OFF the Laptop
3. Removed Ethernet copper module
4. Inserted **WPC300N wireless module**
5. Powered ON the Laptop
6. Desktop tab → PC Wireless → Connect tab
7. Selected **HomeNetwork** SSID → Connected ✅
8. Verified IP via `ipconfig /all`
9. Opened Web Browser → navigated to `cisco.srv` ✅

### Assessment Results
| Device | Port | Item | Score |
|---|---|---|---|
| Laptop | Wireless0 | IP Address | 1/1 ✅ |
| Laptop | Wireless0 | Subnet Mask | 1/1 ✅ |
| PC | FastEthernet0 | IP Address | 1/1 ✅ |
| PC | FastEthernet0 | Subnet Mask | 1/1 ✅ |
| **Total** | | | **4/4** 🏆 |

---

## 14. Quick Revision Glossary

| Term | Definition |
|---|---|
| **Network** | Group of connected devices sharing data |
| **Router** | Connects different networks together |
| **Switch** | Connects devices within the same network |
| **Modem** | Converts signals between ISP and network |
| **IP Address** | Unique identifier for a device on a network |
| **IPv4** | 32-bit IP address (e.g. 192.168.0.1) |
| **IPv6** | 128-bit IP address (next generation) |
| **Subnet Mask** | Defines network and host portion of IP |
| **Default Gateway** | Router IP used to reach other networks |
| **DHCP** | Auto-assigns IP addresses to devices |
| **DNS** | Translates domain names to IP addresses |
| **SSID** | Name of a Wi-Fi network |
| **WPC300N** | Wireless module for laptops in PT |
| **Ping** | Tests connectivity between two devices |
| **TTL** | Limits how far a packet travels |
| **ICMP** | Protocol used by ping command |
| **LAN** | Local network (home/office) |
| **WAN** | Wide network (Internet) |
| **WLAN** | Wireless local area network |
| **Packet Tracer** | Cisco network simulation software |
| **Topology** | Arrangement of devices in a network |
| **Star Topology** | All devices connect to a central device |
| **Protocol** | Rules for data communication |
| **Bandwidth** | Maximum data transfer rate |
| **Latency** | Delay in network communication |
| **NIC** | Hardware to connect device to network |
| **Firewall** | Security device that filters traffic |
| **Client** | Device that requests services |
| **Server** | Device that provides services |
| **Coaxial Cable** | Cable used from modem to router |
| **Ethernet Cable** | Wired cable for LAN connections |
| **Fiber Optic** | Light-based cable for high speed links |
| **Console Cable** | Cable for device initial configuration |

---

## 📌 Important Notes for Exam/Quiz

> ✅ **DHCP** automatically assigns IP — no manual entry needed  
> ✅ **Ping 4 replies** = successful connectivity  
> ✅ **Default Gateway** = always the Router's IP address  
> ✅ **Subnet mask 255.255.255.0** = up to 254 hosts on the network  
> ✅ **IPv4** = 32 bits | **IPv6** = 128 bits  
> ✅ **WPC300N** = wireless module (replaces Ethernet module on Laptop)  
> ✅ **SSID** = Wi-Fi network name ("HomeNetwork" in our project)  
> ✅ **Star topology** used in home networks  
> ✅ **Coaxial cable** connects Router → Cable Modem  
> ✅ **ipconfig /all** shows full network details including MAC address  

---

*📝 Notes prepared by: Noor Ul Nisa | Cisco NetAcad | June 2026*
