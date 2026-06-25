# 📋 Structured Cabling Notes
### *Based on: "Create Realistic Structured Cabling in the Physical Workspace and Cabling Devices in a Rack" — Cisco Packet Tracer Lab*

---

## 📌 Table of Contents
1. [What is Structured Cabling?](#1-what-is-structured-cabling)
2. [Why Structured Cabling Matters](#2-why-structured-cabling-matters)
3. [TIA/EIA Standards](#3-tiaeia-standards)
4. [The 6 Subsystems of Structured Cabling](#4-the-6-subsystems-of-structured-cabling)
5. [Types of Cables Used](#5-types-of-cables-used)
6. [Rack and Patch Panel Setup](#6-rack-and-patch-panel-setup)
7. [Physical Workspace in Packet Tracer](#7-physical-workspace-in-packet-tracer)
8. [Cabling Devices in a Rack](#8-cabling-devices-in-a-rack)
9. [Color Coding Standards](#9-color-coding-standards)
10. [Key Terms Glossary](#10-key-terms-glossary)

---

## 1. What is Structured Cabling?

**Structured cabling** is a standardized system of cabling and hardware that provides a comprehensive telecommunications infrastructure for a building or campus. It serves as the "nervous system" of a network.

> 💡 Think of it like the electrical wiring in a building — it's planned, organized, and follows standards so that any device can plug in anywhere.

**Key characteristics:**
- Organized and standardized
- Vendor-independent (works with any network equipment)
- Supports multiple types of services (data, voice, video)
- Scalable and easy to troubleshoot

---

## 2. Why Structured Cabling Matters

| Problem (Without Structured Cabling) | Solution (With Structured Cabling) |
|--------------------------------------|-------------------------------------|
| Spaghetti cabling — messy and confusing | Organized, labeled cable runs |
| Hard to trace faults | Easy to identify and fix issues |
| Downtime during upgrades | Minimal disruption with patch panel |
| Proprietary locks with one vendor | Open standards — use any equipment |
| Difficult to expand the network | Easily scalable |

---

## 3. TIA/EIA Standards

The two main bodies that define structured cabling standards:

| Standard | Description |
|----------|-------------|
| **TIA-568** | Commercial Building Telecommunications Cabling Standard |
| **TIA-569** | Pathways and Spaces Standard |
| **TIA-606** | Administration Standard (labeling) |
| **TIA-607** | Grounding and Bonding Standard |
| **ISO/IEC 11801** | International cabling standard |

> 📌 In Pakistan/South Asia, **TIA-568** is the most commonly referenced standard.

---

## 4. The 6 Subsystems of Structured Cabling

This is the most important concept — structured cabling is divided into **6 subsystems**:

```
┌─────────────────────────────────────────────────┐
│              STRUCTURED CABLING SYSTEM           │
│                                                 │
│  1. Entrance Facility (EF)                      │
│         ↓                                       │
│  2. Equipment Room (ER)                         │
│         ↓                                       │
│  3. Backbone / Vertical Cabling                 │
│         ↓                                       │
│  4. Telecommunications Room (TR)                │
│         ↓                                       │
│  5. Horizontal Cabling                          │
│         ↓                                       │
│  6. Work Area (WA)                              │
└─────────────────────────────────────────────────┘
```

### 1️⃣ Entrance Facility (EF)
- Where outside cables (from ISP/telephone company) enter the building
- Contains protectors, demarcation point, and connecting hardware
- Also called the **"demarc"** (demarcation point)

### 2️⃣ Equipment Room (ER)
- Centralized space for major networking equipment
- Contains **main distribution frame (MDF)**, servers, routers, large switches
- Climate controlled (AC), secure, restricted access
- Usually on the ground floor or basement

### 3️⃣ Backbone Cabling (Vertical Cabling)
- Connects the Equipment Room to Telecommunications Rooms on each floor
- Runs vertically through risers/conduits between floors
- Uses **fiber optic** or high-category UTP cables
- Also called **riser cabling**

### 4️⃣ Telecommunications Room (TR)
- Also called **IDF** (Intermediate Distribution Frame)
- Found on each floor
- Contains patch panels, switches, and horizontal cable terminations
- Connects backbone to horizontal cabling

### 5️⃣ Horizontal Cabling
- Runs from the Telecommunications Room to each work area outlet
- Maximum length: **90 meters** (295 feet) for permanent link
- Total channel length: **100 meters** including patch cords
- Uses **Cat5e, Cat6, or Cat6A UTP** cables
- Runs through ceiling tiles, conduits, or cable trays

### 6️⃣ Work Area (WA)
- The end-user space — desks, cubicles, offices
- Contains wall outlet/jack (RJ-45)
- Connected to device using a **patch cord** (max 10m)

---

## 5. Types of Cables Used

### 🔵 Copper Cables (UTP — Unshielded Twisted Pair)

| Category | Max Speed | Max Distance | Use |
|----------|-----------|--------------|-----|
| Cat5e | 1 Gbps | 100m | Basic office networks |
| Cat6 | 10 Gbps | 55m (10G) / 100m (1G) | Modern networks |
| Cat6A | 10 Gbps | 100m | Data centers, high-performance |
| Cat7 | 10 Gbps | 100m | Shielded, industrial use |
| Cat8 | 40 Gbps | 30m | Data centers |

### 🟡 Fiber Optic Cables

| Type | Core Size | Distance | Use |
|------|-----------|----------|-----|
| **OM1** (Multimode) | 62.5µm | Up to 275m | Short runs, older |
| **OM3/OM4** (Multimode) | 50µm | Up to 300–550m | Modern buildings |
| **OS1/OS2** (Single-mode) | 9µm | Up to 10km+ | Long distance, campus |

### Cable Connector Types
- **RJ-45** — Standard copper Ethernet connector (8P8C)
- **LC** — Small fiber connector (most common today)
- **SC** — Square fiber connector
- **ST** — Bayonet-style fiber connector (older)

---

## 6. Rack and Patch Panel Setup

### 🗄️ Network Rack (Cabinet)
A rack is a standardized metal frame that holds networking equipment.

```
┌─────────────────────────┐
│  1U  │  Patch Panel     │  ← Cable management
│  1U  │  Patch Panel     │
│  2U  │  24-port Switch  │  ← Active equipment
│  1U  │  Blank Panel     │
│  2U  │  Router / FW     │
│  1U  │  Cable Manager   │
│  2U  │  UPS (Battery)   │  ← Power backup
└─────────────────────────┘
```

**Rack unit (U):** 1U = 1.75 inches (44.45mm) of vertical space

### 🔌 Patch Panel
- A passive panel with RJ-45 ports on the front
- Connects to wall outlets via **punch-down blocks** on the rear
- Allows flexible cable management — connect any port to any switch port
- Common sizes: 12-port, 24-port, 48-port

**How it works:**
```
[Wall Outlet] ──horizontal cable──► [Patch Panel rear punch-down]
                                          ↓
                                    [Patch Panel front port]
                                          ↓ (patch cord)
                                    [Switch Port]
                                          ↓
                                    [Network / Internet]
```

---

## 7. Physical Workspace in Packet Tracer

In Cisco Packet Tracer's **Physical View**, you can simulate a real building layout:

### Navigating Physical Workspace
1. Open Packet Tracer → Click **Physical** tab (top left)
2. You'll see: **Intercity → City → Building → Wiring Closet**

### Levels of Physical Hierarchy
```
🌍 Intercity
    └── 🏙️ City
          └── 🏢 Building
                ├── 🏠 Home Office
                ├── 📦 Wiring Closet (where rack lives)
                └── 🖥️ Office Space (work areas)
```

### Adding Devices to Physical Space
1. Go to **Physical** view
2. Navigate into a building/room
3. Drag devices from the **Device List** to the workspace
4. Connect cables between devices

---

## 8. Cabling Devices in a Rack

### Step-by-Step: Setting Up a Rack in Packet Tracer

**Step 1 — Enter the Wiring Closet**
- In Physical view, double-click Building → double-click Wiring Closet
- You'll see the rack frame

**Step 2 — Add Devices to Rack**
- Drag devices (switches, patch panels, routers) into the rack
- Devices snap into rack units (U slots)

**Step 3 — Connect Patch Panel to Switch**
- Use a **copper straight-through cable**
- Connect Patch Panel port → Switch port (this is the patch cord)

**Step 4 — Connect Wall Outlets to Patch Panel**
- In logical view, horizontal cables run from wall jacks → patch panel rear
- In physical view, you can see these cable runs

**Step 5 — Connect End Devices**
- Work area devices (PCs, phones) connect to wall outlet via patch cord

### Best Practices for Rack Organization
- ✅ Place **patch panels at top** of rack
- ✅ Use **cable managers** (1U horizontal organizers) between active equipment
- ✅ Keep **switches just below** patch panels
- ✅ Place **heavy equipment (UPS)** at the bottom
- ✅ **Label everything** — ports, cables, panels
- ✅ Use **velcro straps** (not zip ties) inside racks for cable management
- ✅ Maintain **front-to-back airflow** — cold air in front, hot air exhausted at rear

---

## 9. Color Coding Standards

TIA-606 recommends color coding for easy identification:

| Color | Use |
|-------|-----|
| 🔵 Blue | Horizontal cabling (most common) |
| 🟡 Yellow | Fiber optic or crossover cables |
| 🟢 Green | Network cables (patch cords at switch) |
| 🔴 Red | Power, emergency, or security systems |
| ⚪ White | First-level backbone |
| 🟠 Orange | Demarcation point / ISP connections |
| 🟣 Purple | Common equipment cables |
| 🩶 Gray | Second-level backbone |

---

## 10. Key Terms Glossary

| Term | Definition |
|------|------------|
| **MDF** | Main Distribution Frame — central point for all building cabling |
| **IDF** | Intermediate Distribution Frame — floor-level distribution point |
| **Patch Panel** | Passive panel that organizes and terminates horizontal cables |
| **Patch Cord** | Short flexible cable connecting patch panel to switch, or outlet to device |
| **Punch-down** | Method of terminating wire into a keystone jack or patch panel using a punch-down tool |
| **RJ-45** | Standard 8-pin connector for Ethernet cables |
| **U (Rack Unit)** | Unit of measurement for rack space; 1U = 1.75 inches |
| **TIA/EIA** | Telecommunications Industry Association / Electronic Industries Alliance |
| **Demarc** | Demarcation point where ISP responsibility ends and customer network begins |
| **Horizontal run** | Cable path from wall outlet to telecommunications room |
| **Backbone** | Cabling that connects floors or buildings |
| **UTP** | Unshielded Twisted Pair — most common copper cable type |
| **STP** | Shielded Twisted Pair — has shielding to reduce EMI |
| **EMI** | Electromagnetic Interference — signal distortion from nearby electrical sources |
| **Channel** | Complete path from device to device (max 100m for copper) |
| **Permanent Link** | Fixed portion of horizontal cabling excluding patch cords (max 90m) |

---

## 📝 Quick Summary

```
ISP → Entrance Facility → Equipment Room (MDF)
                               ↓ (Backbone/Fiber)
                    Telecom Room (IDF/Rack)
                               ↓ (Horizontal Cable - max 90m)
                         Wall Outlet (RJ-45 jack)
                               ↓ (Patch cord - max 10m)
                           End Device (PC/Phone)
```

**Total maximum channel length = 90m (horizontal) + 10m (patch cords) = 100m**

---

## 🔗 Useful References

- [Cisco Packet Tracer — NetAcad](https://www.netacad.com/courses/packet-tracer)
- [TIA-568 Standard Overview](https://www.tiaonline.org/)
- [Structured Cabling Wikipedia](https://en.wikipedia.org/wiki/Structured_cabling)
- [Fluke Networks — Cabling Guides](https://www.flukenetworks.com/knowledge-base)

---

*Notes prepared while studying Cisco Packet Tracer — Physical Workspace & Rack Cabling Lab*
