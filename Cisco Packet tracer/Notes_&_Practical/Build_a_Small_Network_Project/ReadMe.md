# 🌐 Build a Small Network — My First Networking Project

> **Course:** Getting Started with Cisco Packet Tracer | Cisco Networking Academy  
> **Score:** 🏆 4/4 Perfect | **Completed:** 22 June 2026  

---

## 💡 About This Project

This is my **very first hands-on networking project**, completed as part of the *Getting Started with Cisco Packet Tracer* course on **Cisco Networking Academy (NetAcad)**. The goal was to build, configure, and verify a small home network entirely inside **Cisco Packet Tracer** — a powerful network simulation tool used by networking students and professionals worldwide.

In this project, I designed a complete home network from scratch that includes a **wired PC**, a **wireless Laptop**, a **Wireless Router**, a **Cable Modem**, an **Internet cloud**, and a remote **cisco.srv server**. I configured IP addressing, enabled DHCP, set up wireless connectivity, and verified end-to-end communication using the `ping` command and a web browser — all without touching a single piece of real hardware.

---

## ✨ What Inspired Me

I have always been curious about how the Internet works — how a message typed on one device somehow reaches another device across the world in milliseconds. That curiosity is what drew me toward networking and cybersecurity. When I discovered Cisco NetAcad offered free beginner courses with real simulation tools, I knew this was where I needed to start.

This project was my first real taste of *doing* rather than just reading. Seeing the ping replies come back successfully — **4 out of 4** — after configuring everything from scratch gave me a feeling I cannot describe. It was the moment I realized: *I can actually do this.* That feeling is what keeps pushing me forward.

---

## 🗺️ Network Topology

```
[PC] ──Ethernet──► [Wireless Router] ──Coaxial──► [Cable Modem] ──► [Internet] ──► [cisco.srv]
                          │
                    (Wi-Fi 📶)
                          │
                      [Laptop]
```

### Devices Used

| Device | Role | Connection Type |
|---|---|---|
| PC | Wired client | Copper Ethernet |
| Laptop | Wireless client | Wi-Fi (WPC300N Module) |
| Wireless Router | DHCP Server + Gateway | LAN + WAN |
| Cable Modem | ISP connection | Coaxial Cable |
| Internet Cloud | WAN simulation | — |
| cisco.srv | Remote web server | — |

---

## 🛠️ Special Features

### 🔌 Dual Connectivity — Wired + Wireless
This project showcases both wired and wireless connectivity working simultaneously on the same network. The PC connects via a **Copper Ethernet cable**, while the Laptop connects wirelessly after a **hardware module swap** (replacing the Ethernet NIC with a WPC300N wireless module) — mimicking real-world device configuration.

### ⚙️ DHCP Auto-Configuration
Rather than manually assigning IP addresses, the **Wireless Router acts as a DHCP server** and automatically assigns IP addresses, subnet masks, default gateways, and DNS settings to both devices — just like a real home router does.

### 🌐 End-to-End Connectivity Verification
Connectivity was verified at multiple levels:
- **Layer 3 (Network):** `ping cisco.srv` → 4/4 replies ✅
- **Layer 7 (Application):** Web browser on Laptop navigated to `cisco.srv` successfully ✅

### 📊 Perfect Assessment Score
The project was assessed by Cisco Packet Tracer's built-in grading system, checking both IP addresses and subnet masks on all devices — and achieved a **perfect score of 4/4**.

---

## ⚔️ Challenges I Faced

### 1. Wireless Module Swap
The trickiest part was replacing the Laptop's Ethernet module with the wireless WPC300N module. I had to:
- Power OFF the Laptop first (it won't allow changes while powered on)
- Drag the Ethernet module out
- Drag the WPC300N module in from the modules panel
- Power ON again

Missing the power-off step is an easy mistake to make as a beginner — and I learned it the hard way!

### 2. Understanding Cable Types
At first, I was confused about which cable to use between which devices. I had to learn the difference between:
- **Copper Straight-Through** (for different device types)
- **Coaxial** (Router → Cable Modem)
- **Wireless** (no cable needed)

Choosing the wrong cable type causes the connection to fail — so getting this right was an important early lesson.

### 3. Understanding DHCP vs Static IP
I initially did not understand why the IP addresses showed up automatically without me typing them in. Learning about **DHCP** and the DORA process (Discover → Offer → Request → Acknowledge) was a breakthrough moment for me.

### 4. Reading ipconfig /all Output
The `ipconfig /all` command returns a lot of information. Learning what each field means — Physical Address, IPv4, Subnet Mask, Default Gateway, DHCP Server, DNS Servers — helped me understand how all the pieces of a network fit together.

---

## 📂 Repository Contents

```
📁 CCNA-Networking/
└── 📁 Cisco Packet Tracer/
    ├── 📄 README.md                        ← Full course documentation
    ├── 🌐 certificate.html                 ← Visual certificate showcase
    ├── 📘 Cisco-Packet-Tracer-Notes.md     ← Detailed course notes
    └── 📘 PT-File-Types-Notes.md           ← Notes on PT file types
```

---

## 📚 What I Learned

- 🔌 Connecting devices using Ethernet, Coaxial, and Wireless connections
- 🖥️ Configuring wired and wireless network clients
- 📡 Understanding DHCP and automatic IP assignment
- 🔢 IPv4 addressing, subnet masks, and default gateways
- 🔍 Using `ipconfig /all` to inspect network settings
- 🏓 Testing connectivity with `ping`
- 🌍 Verifying web access through a browser
- 🔧 Swapping hardware modules in Packet Tracer
- 🗺️ Understanding Star network topology
- 📁 Learning Packet Tracer file types (.pka, .pkt, .pksz, .pkz)

---

## 🏅 Certificate

> 🎓 Issued by **Cisco Networking Academy** | Lynn Bloomer, Director  
> 📅 Date: **22 June 2026**  
> 🆔 Cert ID: `46a8be14-6dfd-48f7-a9ed-07c0a74d1cac`  

👉 [View Certificate Visually](https://noorulnisa416.github.io/CCNA-Networking/Cisco%20Packet%20tracer/certificate.html)

---

## 👩‍💻 About Me

Hi! I'm **Noor Ul Nisa**, a student at **Virtual University of Pakistan**, on a journey into the world of **Networking, Cybersecurity, and Information Technology**.

I came to GitHub because I believe in **learning in public** — sharing my projects, notes, and progress so that others who are just starting out can see that it is okay to begin from zero. Every expert was once a beginner, and this repository is proof that I am committed to growing every single day.

### 🎯 My Goals:
- 🏆 Earn my **Cisco CCNA Certification**
- 🔐 Build expertise in **Cybersecurity**
- ☁️ Explore **Cloud Networking** (AWS, Azure)
- 💻 Build and document real-world networking projects
- 🌍 Contribute to the tech community and inspire other students — especially women in tech

### 🚀 What Brings Me to GitHub:
I want this GitHub profile to be my **living portfolio** — a record of everything I learn, build, and achieve. Every commit is a step forward. Every project is a new skill. I want future employers, collaborators, and fellow learners to look at this profile and see someone who is **serious, consistent, and passionate** about technology.

This is just the beginning. 💙

---

## 🔗 Connect With Me

| Platform | Link |
|---|---|
| 🌐 GitHub | [github.com/noorulnisa416](https://github.com/noorulnisa416) |
| 💼 LinkedIn | *https://www.linkedin.com/in/noorulnisa416/* |
| 🏫 NetAcad | Cisco Networking Academy |

---

## 🚀 What's Next

- [ ] Complete **CCNA 1 — Introduction to Networks**
- [ ] Build a **multi-switch LAN** topology
- [ ] Configure **VLANs** and inter-VLAN routing
- [ ] Learn **subnetting** and CIDR notation
- [ ] Explore **Cybersecurity Essentials** course
- [ ] Document every project here on GitHub 📁

---

> *"Every great network engineer started somewhere — and this is where my journey begins."* 🌐💙

---

*⭐ If this project inspired you or helped you, consider giving it a star — it means the world to a beginner!*
