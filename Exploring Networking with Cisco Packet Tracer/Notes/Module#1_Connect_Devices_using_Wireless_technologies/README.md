# 📘 Module 1 — Complete Notes
## Exploring Networking with Cisco Packet Tracer

> **Module:** 1.1 — Connect Devices using Wireless Technologies
> **Course:** Exploring Networking with Cisco Packet Tracer | Cisco NetAcad
> **Student:** Noor Ul Nisa | Virtual University of Pakistan
> **Score:** ✅ 8/8 All Topics Completed
> **Date:** June 2026

---

## 📋 Table of Contents

| # | Topic | Type |
|---|---|---|
| [1.1.1](#111-topology-overview) | Topology Overview | 🎥 Video |
| [1.1.2](#112-structured-cabling) | Structured Cabling | 📖 Reading |
| [1.1.3](#113-structured-cabling-in-the-physical-workspace) | Structured Cabling in the Physical Workspace and Cabling Devices in a Rack | 🎥 Video |
| [1.1.4](#114-packet-tracer--create-realistic-structured-cabling) | Create Realistic Structured Cabling in the Physical Workspace | 🖥️ Packet Tracer |
| [1.1.5](#115-connect-devices-using-wired-and-wireless-technologies) | Connect Devices using Wired and Wireless Technologies | 📖 Reading |
| [1.1.6](#116-packet-tracer--connect-devices-using-wireless-technologies) | Connect Devices using Wireless Technologies | 🖥️ Packet Tracer |
| [1.1.7](#117-explore-device-configuration-using-the-cli-console) | Explore Device Configuration Using the CLI (Console) | 🎥 Video |
| [1.1.8](#118-packet-tracer--explore-device-configuration-using-the-cli) | Explore Device Configuration Using the CLI (Console) | 🖥️ Packet Tracer |

---

---

# 1.1.1 — Topology Overview
> 🎥 Video

## 🔹 What is a Network Topology?
**Definition:** A **network topology** describes the **arrangement of devices and connections** in a network — both physically (how they are placed) and logically (how data flows between them).

## 🔹 Types of Topologies

### Physical Topology
Shows the **actual physical layout** of cables, devices, and connections in the real world.

### Logical Topology
Shows **how data flows** through the network — the logical path data takes between devices.

---

## 🔹 Common Topology Types

### ⭐ Star Topology *(Most Common)*
```
        [PC1]
          │
[PC2]──[Switch/Router]──[PC3]
          │
        [PC4]
```
- All devices connect to a **central device** (switch or router)
- Most widely used in homes and offices
- If one device fails → others still work
- If the central switch fails → all devices lose connection
- **Used in this course**

### 🚌 Bus Topology
```
[PC1]──[PC2]──[PC3]──[PC4]
```
- All devices on a **single cable (bus)**
- Old and rarely used today
- If main cable fails → entire network fails

### 🔄 Ring Topology
```
[PC1]──[PC2]
  │          │
[PC4]──[PC3]
```
- Devices in a **circular loop**
- Data travels in one direction
- One break can affect the whole network

### 🕸️ Mesh Topology
```
Every device connects to every other device
```
- Most **reliable** — multiple paths available
- Most **expensive** — many cables needed
- Used in critical infrastructure (internet backbone)

### 🔀 Hybrid Topology
- **Combination** of two or more topology types
- Used in large enterprise networks

---

## 🔹 Network Topology in Packet Tracer
- **Logical Mode** → shows the network topology diagram (default view)
- **Physical Mode** → shows devices in a real-world physical location (building, office, city)

---

# 1.1.2 — Structured Cabling
> 📖 Reading

## 🔹 What is Structured Cabling?
**Definition:** A **standardized, organized system** of cables, connectors, and hardware that provides the complete telecommunications infrastructure for a building. It replaces messy, random wiring with a planned, labeled, and scalable system.

> 💡 **Analogy:** Like the electrical wiring inside your walls — it runs through a breaker box (patch panel) to every outlet (wall mount) in an organized way.

**Benefits:**
- ✅ Easy to manage and troubleshoot
- ✅ Scalable — easy to add new connections
- ✅ Reduces downtime and confusion
- ✅ Professional and standardized

---

## 🔹 Key Components

### 📦 Equipment Cabinet / Rack
A **metal frame or enclosure** that houses all networking equipment (switches, patch panels, servers) in an organized, space-saving way. All structured cabling runs back here.

### 🔌 Patch Panel
A **passive rack-mounted device** that acts as the central connection hub between:
- Switch ports (in the rack)
- Wall outlets around the office

| Part | Description |
|---|---|
| **Front — Jacks** | Where patch cables plug in (Jack13, Jack14…) |
| **Back — Punchdowns** | Where solid wall cables terminate |

### 🖼️ Wall Mount (Keystone Jack)
A **network outlet installed on a wall** providing RJ45 ports for devices. Connects to the patch panel through in-wall cabling.

| Part | Description |
|---|---|
| **Front — Jacks** | Where device cables (PC, printer) plug in |
| **Back — Punchdowns** | Connects to the patch panel |

### 🔧 Punchdown Connection
**Method of permanently terminating a wire** into a block — wire is "punched" in and the slot cuts through insulation to make contact.

---

## 🔹 Structured Cabling Path (End-to-End)
```
[PC / Printer]
      │ Copper Straight-Through
      ▼
[Wall Mount — Jack]
      │ Wall Mount PunchDown (inside wall)
      ▼
[Patch Panel — PunchDown]
      │ Copper Straight-Through
      ▼
[Patch Panel — Jack]
      │ Copper Straight-Through
      ▼
[Switch Port (GigabitEthernet)]
      │
      ▼
[Server / Internet]
```

---

# 1.1.3 — Structured Cabling in the Physical Workspace
> 🎥 Video

## 🔹 Physical Workspace in Packet Tracer
**Packet Tracer Physical Mode** simulates real-world structured cabling by letting you:
- Place devices in a rack inside an Equipment Cabinet
- Run cables from wall mounts to patch panels
- Simulate real office cabling using BendPoints

## 🔹 Key Tools in Physical Mode

| Tool / Feature | What It Does |
|---|---|
| **Equipment Cabinet** | Opens the simulated Wiring Closet with the rack |
| **Cable Pegboard** | Palette for selecting cable types |
| **Inspect Front** | Zooms into device front panel to see ports |
| **BendPoint** | Routes cables along walls (simulates in-wall cabling) |
| **Color Cable** | Assigns a color to a cable for easy identification |
| **Manage All Cables on Rack** | Auto-organizes all rack cables in one click |
| **Back Level (Alt-Left)** | Navigates back in the Physical workspace |

---

## 🔹 Cable Types in Structured Cabling

| Cable | Used For |
|---|---|
| Copper Straight-Through | Switch → Patch Panel Jack; PC → Wall Mount Jack; Wall Mount → Patch Panel Punchdown |
| Coaxial | Router → Cable Modem |
| Fiber Optic | Long-distance, high-speed connections |

---

# 1.1.4 — Packet Tracer: Create Realistic Structured Cabling
> 🖥️ Packet Tracer Activity

## 🎯 Objectives
- Install a **Patch Panel** in the Wiring Closet rack
- Connect **Office-SW1** to the Patch Panel
- Install a **Wall Mount** on the office wall
- Connect Wall Mounts to the Patch Panel via punchdown connections
- Connect end devices and verify connectivity to **office.srv**

---

## 🔧 Part 1 — Install a Patch Panel in the Wiring Closet

### Step 1: Install Patch Panel in the Rack
| Step | Action |
|---|---|
| a | Click **Equipment Cabinet** → opens Wiring Closet |
| b | Click **Connections** → **Structured Cabling** |
| c | Click **Copper Patch Panel** (first option) |
| d | Click a location in the **Rack** to install it |

> ⚠️ **Name must be:** `Patch Panel0`

### Step 2: Connect Office-SW1 to Patch Panel0

| Office-SW1 Port | Patch Panel0 Jack |
|:---:|:---:|
| G1/0/13 | Jack13 |
| G1/0/14 | Jack14 |
| G1/0/15 | Jack15 |
| G1/0/16 | Jack16 |

---

## 🔧 Part 2 — Attach a Wall Mount in the Office

> ⚠️ **Name must be:** `Wall Mount0`

| Wall Mount0 PunchDown | Patch Panel0 PunchDown |
|:---:|:---:|
| PunchDown1 | Punchdown13 |
| PunchDown2 | Punchdown14 |
| PunchDown3 | Punchdown15 |
| PunchDown4 | Punchdown16 |

- Connect **Office-Admin PC** and **Printer0** to Wall Mount0 Jacks
- Wait 1–2 mins for DHCP → verify via **office.srv**

---

## 🔧 Part 3 — Connect an Additional Wall Mount and Cables

> ⚠️ **Name must be:** `Wall Mount1`

**New Switch-to-Panel connections:**

| Office-SW1 Port | Patch Panel0 Jack |
|:---:|:---:|
| G1/0/21 | Jack21 |
| G1/0/22 | Jack22 |
| G1/0/23 | Jack23 |
| G1/0/24 | Jack24 |

**Wall Mount1 (next to window) → Patch Panel0:**

| Wall Mount1 PunchDown | Patch Panel0 PunchDown |
|:---:|:---:|
| PunchDown1 | Punchdown21 |
| PunchDown2 | Punchdown22 |
| PunchDown3 | Punchdown23 |
| PunchDown4 | Punchdown24 |

- Connect **Office-User PC** to Wall Mount1
- Verify connectivity to `office.srv` ✅

---

# 1.1.5 — Connect Devices using Wired and Wireless Technologies
> 📖 Reading

## 🔹 Wired Technologies

### Ethernet (Copper Cable)
- Most common wired connection type
- Uses **RJ45 connectors**
- Speeds: 10 Mbps → 100 Mbps → 1 Gbps → 10 Gbps
- **Reliable, fast, secure**

### Fiber Optic
- Transmits data as **pulses of light**
- Much faster and longer range than copper
- Used for building-to-building or ISP backbone
- Immune to electromagnetic interference

### Coaxial Cable
- Used for **cable TV and cable internet**
- Connects Cable Modem to the ISP
- Has a central copper conductor surrounded by shielding

---

## 🔹 Wireless Technologies

### 📶 Wi-Fi (WLAN — IEEE 802.11)
| Standard | Max Speed | Frequency |
|---|---|---|
| 802.11b | 11 Mbps | 2.4 GHz |
| 802.11g | 54 Mbps | 2.4 GHz |
| 802.11n | 300 Mbps | 2.4 / 5 GHz |
| 802.11ac | 1.3 Gbps | 5 GHz |
| 802.11ax (Wi-Fi 6) | 9.6 Gbps | 2.4 / 5 / 6 GHz |

### 🔵 Bluetooth
- Short-range (~10 meters)
- Used for: headphones, speakers, keyboards, file transfer, tethering
- Requires **pairing** between devices
- Frequency: 2.4 GHz

### 📱 Cellular (3G/4G/5G)
- Provided by telecom companies (ISP)
- Wide area coverage (city-wide, country-wide)
- Used for: mobile internet, tethering
- SIM card required

---

## 🔹 Wired vs Wireless Comparison

| Feature | Wired (Ethernet) | Wireless (Wi-Fi) |
|---|---|---|
| Speed | Very fast | Fast |
| Reliability | Very high | Medium (interference possible) |
| Security | High | Medium (needs encryption) |
| Mobility | ❌ No — fixed location | ✅ Yes — move freely |
| Setup | Cables needed | No cables needed |
| Range | Length of cable | ~100 meters |
| Cost | Moderate | Moderate |
| Best for | Desktops, servers | Laptops, phones, tablets |

---

## 🔹 NIC (Network Interface Card)
**Definition:** Hardware component that allows a device to connect to a network.
- **Wired NIC** → uses Ethernet cable (RJ45)
- **Wireless NIC** → uses Wi-Fi radio signal

**In Packet Tracer:**
- **PT-LAPTOP-NM-1CFE** = wired Ethernet NIC
- **WPC300N** = wireless Wi-Fi NIC (802.11n)

---

# 1.1.6 — Packet Tracer: Connect Devices using Wireless Technologies
> 🖥️ Packet Tracer Activity

## 🎯 Objectives
| Part | Task |
|---|---|
| Part 1 | Connect a Laptop to the Office WLAN via Wi-Fi |
| Part 2 | Connect a Bluetooth Speaker to an Office Tablet |
| Part 3 | Tether a Laptop to a Smartphone's Cellular Network via Bluetooth |

> ⚠️ **Entire activity performed in Physical Mode only!**

---

## 🔧 Part 1 — Connect Laptop to Office WLAN (Wi-Fi)

### Step 1: Swap Laptop Module
| Step | Action |
|---|---|
| a | Click **Laptop** → **Physical** tab → **Power OFF** |
| b | Remove **PT-LAPTOP-NM-1CFE** (wired) → drag to module list |
| c | Insert **WPC300N** (wireless) → drag to Laptop |
| d | **Power ON** the Laptop |

### Step 2: Connect to Wi-Fi
| Step | Action |
|---|---|
| a | Desktop tab → **PC Wireless** tool |
| b | Connect tab → wait for **Employee SSID** → click **Refresh** if needed |
| c | Select **Employee SSID** → click **Connect** |
| d | Enter password: **`Cisco123`** → click **Connect** |
| e | Verify: Config tab → **Wireless0** → IP address assigned ✅ |
| f | Test: Desktop → **Web Browser** → navigate to **`office.srv`** ✅ |

**Wi-Fi Credentials:**
| Setting | Value |
|---|---|
| SSID | Employee SSID |
| Password | Cisco123 |
| Module | WPC300N |

---

## 🔧 Part 2 — Bluetooth: Speaker ↔ Tablet

### Step 1: Enable Bluetooth on Speaker
- Click **Bluetooth Speaker** → Config tab → Bluetooth → Port Status: **ON**

### Step 2: Pair from Office Tablet
| Step | Action |
|---|---|
| a | Open **Office Tablet** → Config tab → Bluetooth → **ON** |
| b | Click **Discover** → Bluetooth Speaker appears |
| c | Select **Bluetooth Speaker** → click **Pair** → click **Yes** |
| d | Status: **"Paired, Connected"** ✅ |
| e | Test: Desktop → **Music Player** → **Play/Stop** 🎵 |

---

## 🔧 Part 3 — Cellular Tethering: Smartphone → Laptop

### Step 1: Enable Bluetooth on User-Laptop
- Click **User-Laptop** → Config tab → Bluetooth → **ON** → leave window open

### Step 2: Configure Smartphone
| Step | Action |
|---|---|
| a | Click **Smartphone** → Config tab |
| b | Global Settings → **Cellular Tethering: ON** |
| c | Check **3G/4G Cell1** → verify IP address from cellular network |
| d | Click **Bluetooth** → Port Status: **ON** |

### Step 3: Pair and Tether
| Step | Action |
|---|---|
| a | Smartphone → Bluetooth → click **Discover** → User-Laptop appears |
| b | Select **User-Laptop** → click **Pair** → click **Yes** ✅ |
| c | Go to **User-Laptop** → Config → Bluetooth → highlight **Smartphone** → click **Tether** |
| d | Laptop obtains **IP address** from smartphone's cellular network ✅ |
| e | Test: Desktop → **Web Browser** → `office.srv` ✅ |

> 💡 Click **Fast Forward Time** to speed up the process!

---

# 1.1.7 — Explore Device Configuration Using the CLI (Console)
> 🎥 Video

## 🔹 Device Configuration Tabs in Packet Tracer

| Tab | Description | Available On |
|---|---|---|
| 🖥️ **Physical** | Physical device view — modules, power | All devices |
| ⚙️ **Config** | Graphical UI for basic settings (PT only) | Routers, Switches |
| 💻 **CLI** | Command Line Interface — direct IOS access | Routers, Switches |
| 🖱️ **Desktop** | Simulated PC apps (Terminal, Web Browser) | PCs, Laptops |
| 🌐 **Services** | Configure server services (DHCP, DNS, HTTP) | Servers |

---

## 🔹 3 Ways to Access Device Configuration

| Method | Description | Real Hardware? |
|---|---|---|
| **Config Tab** | Graphical UI — point and click | ❌ PT only |
| **CLI Tab** | Direct command line in PT | ✅ Yes |
| **PC Terminal** | Console cable → PC → Terminal app | ✅ Most realistic |

> 💡 In the Config tab, as you change settings, the **equivalent IOS commands** appear in the "Equivalent IOS Commands" window — great for learning CLI syntax!

---

## 🔹 Cisco IOS Modes

```
Power ON → IOS Loads → "Press Return to Get Started"
        │
        ▼
  USER EXEC MODE          Switch>       (monitoring only)
        │ enable
        ▼
  PRIVILEGED EXEC MODE    Switch#       (full monitoring + save)
        │ configure terminal
        ▼
  GLOBAL CONFIG MODE      Switch(config)#   (make changes)
        │ interface [type][num]
        ▼
  INTERFACE CONFIG MODE   Switch(config-if)#  (configure port)
```

| Mode | Prompt | Enter Command | Purpose |
|---|---|---|---|
| User EXEC | `Switch>` | Default | Monitoring only |
| Privileged EXEC | `Switch#` | `enable` | Full access |
| Global Config | `Switch(config)#` | `configure terminal` | Make changes |
| Interface Config | `Switch(config-if)#` | `interface [x]` | Configure ports |

---

## 🔹 Essential CLI Commands

### Navigation
```bash
Switch> enable                    # Enter Privileged EXEC
Switch# configure terminal        # Enter Global Config
Switch(config)# exit              # Go back one level
Switch(config)# end               # Return to Privileged EXEC
Switch# ?                         # List all available commands
```

### Change Hostname
```bash
Switch(config)# hostname Office-SW1
Office-SW1(config)#    ← Prompt changes immediately!
```

### Save Configuration
```bash
# MOST IMPORTANT COMMAND!
Switch# copy running-config startup-config
```

### View Configuration
```bash
Switch# show running-config     # View active config (RAM)
Switch# show startup-config     # View saved config (NVRAM)
Switch# show version            # IOS version + hardware info
Switch# show ip interface brief # Quick interface status
```

---

## 🔹 Running Config vs Startup Config

| | Running Config | Startup Config |
|---|---|---|
| **Stored in** | RAM (temporary) | NVRAM (permanent) |
| **Lost on restart?** | ✅ YES — if not saved | ❌ No — survives restarts |
| **View command** | `show running-config` | `show startup-config` |
| **Updated when** | Every CLI change | Only after `copy run start` |

> ⚠️ **Always save!** `copy running-config startup-config` after making any changes!

---

# 1.1.8 — Packet Tracer: Explore Device Configuration Using the CLI
> 🖥️ Packet Tracer Activity

## 🎯 What You Practice
- Access the CLI via **PC Terminal** (console connection)
- Navigate between IOS modes
- Use `?` to explore available commands
- Change the device hostname
- View the running configuration
- Save configuration with `copy running-config startup-config`

## 🔧 Complete CLI Session Workflow

```bash
# Device boots up
Press RETURN to get started.

# Default: User EXEC mode
Switch>

# Step 1: Enter Privileged EXEC
Switch> enable
Switch#

# Step 2: View available commands
Switch# ?

# Step 3: Enter Global Configuration mode
Switch# configure terminal
Switch(config)#

# Step 4: Change hostname
Switch(config)# hostname Office-SW1
Office-SW1(config)#        ← Changed immediately! ✅

# Step 5: Exit to Privileged EXEC
Office-SW1(config)# exit
Office-SW1#

# Step 6: Save the configuration — CRITICAL!
Office-SW1# copy running-config startup-config
Destination filename [startup-config]?
Building configuration...
[OK]
Office-SW1#    ✅ Configuration saved!
```

---

# 📊 Module 1 — Complete Summary Table

| Topic | Key Concept | Key Command / Action |
|---|---|---|
| 1.1.1 Topology | Star topology = most common | All devices → central switch/router |
| 1.1.2 Structured Cabling | Patch Panel + Wall Mount system | Cable path: Device → Wall Mount → Patch Panel → Switch |
| 1.1.3 Physical Workspace | BendPoints simulate real wall cabling | Right-click cable → Create BendPoint |
| 1.1.4 PT Activity | Naming critical for grading | Patch Panel0, Wall Mount0, Wall Mount1 |
| 1.1.5 Wired vs Wireless | Ethernet = reliable, Wi-Fi = mobile | WPC300N = wireless module |
| 1.1.6 PT Activity | 3 wireless types used | Wi-Fi (Employee SSID/Cisco123), Bluetooth (Pair), Cellular (Tether) |
| 1.1.7 CLI | 4 IOS modes | `>` → `#` → `(config)#` → `(config-if)#` |
| 1.1.8 PT Activity | Save config = critical | `copy running-config startup-config` |

---

# 📌 Module 1 — Master Key Points

### Structured Cabling
> ✅ Cable path: **Device → Wall Mount Jack → Punchdown → Patch Panel Punchdown → Jack → Switch**
> ✅ Naming is CRITICAL: **`Patch Panel0`**, **`Wall Mount0`**, **`Wall Mount1`**
> ✅ Always use **Copper Straight-Through** cable throughout
> ✅ Wait **1–2 minutes** for DHCP after connections

### Wireless Technologies
> ✅ Must **power OFF** Laptop before swapping NIC modules
> ✅ Replace **PT-LAPTOP-NM-1CFE** with **WPC300N** for Wi-Fi
> ✅ Wi-Fi: SSID = **Employee SSID** | Password = **Cisco123**
> ✅ Bluetooth: Enable on both → Discover → Pair → Yes → "Paired, Connected"
> ✅ Tethering: Smartphone → Cellular Tethering ON + BT ON → Pair → Tether button on Laptop
> ✅ Verify ALL connections via **`office.srv`** in Web Browser

### CLI & IOS
> ✅ **`>`** = User EXEC | **`#`** = Privileged EXEC | **`(config)#`** = Global Config
> ✅ Config tab = **PT only** — not on real hardware
> ✅ Changes go to **running-config (RAM)** first — lost on restart if not saved
> ✅ Save with: **`copy running-config startup-config`** — writes to NVRAM
> ✅ **`?`** = help command — lists all available commands in current mode
> ✅ **`hostname [name]`** changes the device name immediately

---

# 🧠 Module 1 — Quick Revision Q&A

| Question | Answer |
|---|---|
| What is the most common network topology? | Star topology |
| What is a Patch Panel? | Rack-mounted hub connecting switch ports to wall outlets |
| What naming is required for grading? | Patch Panel0, Wall Mount0, Wall Mount1 |
| What cable is used throughout structured cabling? | Copper Straight-Through |
| Which module replaces the wired Ethernet module? | WPC300N |
| What is the SSID in the activity? | Employee SSID |
| What is the Wi-Fi password? | Cisco123 |
| How do you connect Bluetooth devices? | Enable BT on both → Discover → Pair → Yes |
| What does tethering do? | Shares smartphone's cellular internet with laptop |
| What prompt shows User EXEC mode? | Switch> |
| What prompt shows Privileged EXEC mode? | Switch# |
| What prompt shows Global Config mode? | Switch(config)# |
| How do you enter Privileged EXEC? | Type `enable` |
| How do you enter Global Config? | Type `configure terminal` |
| How do you save the configuration? | `copy running-config startup-config` |
| Where is running-config stored? | RAM (temporary) |
| Where is startup-config stored? | NVRAM (permanent) |
| What does `?` do in CLI? | Lists all available commands in current mode |
| What website verifies connectivity? | office.srv |
| What does BendPoint do in PT? | Routes cables along walls (simulates in-wall cabling) |

---

*📝 Notes by: Noor Ul Nisa | Cisco NetAcad | June 2026*
*© 2017–2022 Cisco and/or its affiliates. All rights reserved. Cisco Public.*
