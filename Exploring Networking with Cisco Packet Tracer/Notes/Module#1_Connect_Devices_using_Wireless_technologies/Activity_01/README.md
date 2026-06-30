# 🔌 Packet Tracer — Create Realistic Structured Cabling in the Physical Workspace

> **Activity Type:** Packet Tracer Hands-On Lab  
> **Course:** Exploring Networking with Cisco Packet Tracer | Cisco NetAcad  
> **Student:** Noor Ul Nisa | Virtual University of Pakistan  
> **Date:** June 2026  
> **Final Score: 22/22 ✅**

---

## 📋 Table of Contents

1. [Key Definitions](#1-key-definitions)
2. [Objectives](#2-objectives)
3. [Required Resources](#3-required-resources)
4. [Part 1 — Install a Patch Panel in the Wiring Closet](#4-part-1--install-a-patch-panel-in-the-wiring-closet)
5. [Part 2 — Attach a Wall Mount in the Office](#5-part-2--attach-a-wall-mount-in-the-office)
6. [Part 3 — Connect an Additional Wall Mount and Cables](#6-part-3--connect-an-additional-wall-mount-and-cables)
7. [Complete Connection Tables](#7-complete-connection-tables)
8. [Full Network Path Diagram](#8-full-network-path-diagram)
9. [Activity Screenshots](#9-activity-screenshots)
10. [Important Tips & Warnings](#10-important-tips--warnings)
11. [Quick Revision Glossary](#11-quick-revision-glossary)
12. [Key Points to Remember](#12-key-points-to-remember)

---

## 1. Key Definitions

### 🔹 Structured Cabling
**Definition:** A **standardized, organized system** of cables, connectors, and hardware that provides the complete telecommunications infrastructure for a building. It replaces messy, random wiring with a planned and labeled system.

> 💡 **Real-world analogy:** Think of electrical wiring inside your walls — it follows a plan, goes through a breaker box (like a patch panel), and connects neatly to every outlet (like wall mounts).

**Benefits:**
- Easy to manage and troubleshoot
- Scalable — easy to add more connections
- Reduces downtime
- Looks professional and organized

---

### 🔹 Wiring Closet / Equipment Closet
**Definition:** A **dedicated room or cabinet** that houses all the core networking equipment — switches, patch panels, servers, and cable management tools. All cables from around the office run back here.

- In Packet Tracer → accessed by clicking the **Equipment Cabinet**
- Also called: **IDF (Intermediate Distribution Frame)** or **MDF (Main Distribution Frame)**

---

### 🔹 Equipment Cabinet / Rack
**Definition:** A **standardized metal frame or enclosure** used to mount networking equipment in an organized, space-saving way.

- Equipment height is measured in **Rack Units (U)** — 1U = 1.75 inches
- Keeps all equipment in one place
- Makes cabling neat and manageable

---

### 🔹 Patch Panel
**Definition:** A **passive rack-mounted device** that acts as the central connection hub between:
- The **switch ports** (coming from inside the rack)
- The **wall outlets** across the office (coming from the walls)

**Structure:**
- **Front side:** Has numbered Jacks (Jack13, Jack14…) → where patch cables plug in
- **Back side:** Has Punchdown blocks (Punchdown13, Punchdown14…) → where solid cables terminate

> 💡 **Analogy:** A telephone switchboard — all lines from different rooms come in, and you can connect any line to any other line by plugging in patch cables at the front.

**In this activity:** Named **`Patch Panel0`** — *must use this exact name for grading!*

---

### 🔹 Jack
**Definition:** A **numbered port/socket on the front of a patch panel** where RJ45 patch cables are plugged in. Each jack corresponds to a punchdown port on the back.

**In this activity:** Jack13, Jack14, Jack15, Jack16, Jack21, Jack22, Jack23, Jack24

---

### 🔹 Punchdown / Punchdown Port
**Definition:** A method of **permanently terminating a wire** into a connector block. The wire is "punched" into a slot that pierces through the insulation to make electrical contact — no stripping needed.

**Found on:**
- Back of patch panels → `Punchdown13`, `Punchdown14`…
- Back of wall mounts → `PunchDown1`, `PunchDown2`…

---

### 🔹 Wall Mount (Keystone Jack Outlet)
**Definition:** A **network outlet installed on a wall** that provides RJ45 ports for connecting end devices (PCs, printers) to the network. Connects to the patch panel through cabling routed inside the walls.

**Structure:**
- **Front:** Has Jack ports → where devices plug in (PC, printer)
- **Back:** Has PunchDown ports → connects to patch panel

**In this activity:**
- **`Wall Mount0`** → installed next to the Equipment Cabinet
- **`Wall Mount1`** → installed next to the window

---

### 🔹 Cable Pegboard
**Definition:** In Cisco Packet Tracer's Physical mode, the **Cable Pegboard** is the tool panel where you select which type of cable to use — like picking a tool from a toolbox.

---

### 🔹 Copper Straight-Through Cable
**Definition:** A standard Ethernet cable used to connect **different types of devices** together. Used throughout this activity.

**Used for:**
- Switch port → Patch Panel Jack
- Wall Mount PunchDown → Patch Panel PunchDown
- PC/Printer → Wall Mount Jack

---

### 🔹 GigabitEthernet Port
**Definition:** A **1 Gbps (Gigabit per second) network port** on a switch, identified with a specific number.

**Format:** `G[slot]/[module]/[port]`  
**Examples:** `G1/0/13`, `G1/0/14`, `G1/0/21`, `G1/0/24`

---

### 🔹 BendPoint
**Definition:** A feature in Packet Tracer Physical mode that lets you **redirect a cable's path** by creating an anchor point and dragging it along the wall or floor — simulating real cable routing inside walls.

> 💡 **Real-world equivalent:** Running a cable through a conduit along the baseboard or inside a wall instead of letting it dangle across the room.

---

### 🔹 DHCP (Dynamic Host Configuration Protocol)
**Definition:** A service that **automatically assigns IP addresses** and other network settings to devices when they connect to the network.

**In this activity:** The **Office-Server** inside the Equipment Closet runs DHCP. Once devices are properly cabled, they **automatically receive IP addresses** — no manual configuration needed.

> ⏳ **Takes 1–2 minutes** after connection for DHCP to assign addresses.

---

### 🔹 office.srv
**Definition:** The **web server** used in this activity to verify network connectivity. After completing all connections, you can browse to `http://office.srv` from Office-Admin or Office-User to confirm the network is working end-to-end.

---

## 2. Objectives

In this activity you will:

- ✅ **Part 1:** Install a **Copper Patch Panel** in the Wiring Closet rack and connect it to **Office-SW1**
- ✅ **Part 2:** Install a **Copper Wall Mount** on the office wall, connect it to the patch panel, connect end devices, and verify connectivity
- ✅ **Part 3:** Add **more switch-to-patch-panel connections**, install a **second Wall Mount** near the window, and connect **Office-User PC**

---

## 3. Required Resources

- 🖥️ **Latest version of Cisco Packet Tracer**

---

## 4. Part 1 — Install a Patch Panel in the Wiring Closet

### 🔧 Step 1: Install a Patch Panel in the Rack

| Step | What to Do |
|---|---|
| **a** | Click the **Equipment Cabinet** → opens the simulated **Wiring Closet** |
| **b** | Click **Connections** in the Device-Type Selection Box → click **Structured Cabling** |
| **c** | In the Device-Specific Selection Box → click **Copper Patch Panel** (first option) |
| **d** | Click a desired location inside the **Rack** to place the patch panel |

> ⚠️ **Grading Note:** The patch panel must be named **`Patch Panel0`** for correct scoring!

---

### 🔧 Step 2: Connect Office-SW1 to the Patch Panel

| Step | What to Do |
|---|---|
| **a** | From the **Cable Pegboard**, select a **Copper Straight-Through** cable |
| **b** | Click switch **Office-SW1** → select **GigabitEthernet 1/0/13** → click **Jack13** on **Patch Panel0** |
| **c** | Complete all remaining connections using the table below |
| **d** | *(Optional)* Right-click any cable → **Color Cable** → choose a color for organization |
| **e** | *(Optional)* Right-click white space in rack → **Manage All Cables on Rack** → auto-organizes cables |
| **f** | Click **Back level (Alt-Left)** to return to the Office |

**📊 Connection Table — Office-SW1 ↔ Patch Panel0:**

| Office-SW1 Port | Patch Panel0 Jack |
|:---:|:---:|
| G1/0/13 | Jack13 |
| G1/0/14 | Jack14 |
| G1/0/15 | Jack15 |
| G1/0/16 | Jack16 |

> 💡 **Pro Tip:** Right-click the switch or patch panel → **Inspect Front** to zoom in and see small port numbers clearly.

---

## 5. Part 2 — Attach a Wall Mount in the Office

### 🔧 Step 1: Install a Wall Mount

| Step | What to Do |
|---|---|
| **a** | Click **Connections** → **Structured Cabling** |
| **b** | In Device-Specific Selection Box → click **Copper Wall Mount** |
| **c** | Click the desired location on the **wall next to the Equipment Cabinet** |
| **d** | In Device-Type Selection Box → click **Connections** → click **Copper Straight-Through** cable |
| **e** | Click **Wall Mount0** → select **PunchDown1** → click **Equipment Cabinet** → **Rack → Patch Panel0 → Punchdown13** |
| **f** | Repeat for all remaining punchdowns using the table below |
| **g** | Connect **Office-Admin PC** and **Printer0** to available jacks on Wall Mount0 using Copper Straight-Through cables |
| **h** | Verify connectivity: **Office-Admin → Desktop → Web Browser** → type `http://office.srv` → click **Go** |

> ⚠️ **Grading Note:** The wall mount must be named **`Wall Mount0`** for correct scoring!

**📊 Connection Table — Wall Mount0 ↔ Patch Panel0:**

| Wall Mount0 (Next to Equipment Cabinet) | Patch Panel0 |
|:---:|:---:|
| PunchDown1 | Punchdown13 |
| PunchDown2 | Punchdown14 |
| PunchDown3 | Punchdown15 |
| PunchDown4 | Punchdown16 |

> ⏳ **Wait 1–2 minutes** after connecting Office-Admin and Printer0 for DHCP to assign IP addresses.

---

### 🔧 Step 2: Organize the Cables (BendPoints)

| Step | What to Do |
|---|---|
| **a** | Right-click the desired cable → select **Create BendPoint** |
| **b** | Drag the black square to the wall or floor to route the cable along the surface |
| **c** | Repeat until no cables are crossing the middle of the room |

> 💡 Using BendPoints in Packet Tracer **simulates running cables through walls** — the same effect as real in-wall cable routing!

---

## 6. Part 3 — Connect an Additional Wall Mount and Cables

Now that Office-Admin and Printer0 are connected, add more switch-to-panel connections and connect Office-User PC via a second wall mount.

| Step | What to Do |
|---|---|
| **a** | Return to **Equipment Closet** → make new connections between Office-SW1 and Patch Panel0 (see table below) |
| **b** | In the Office → add a new **Wall Mount** next to the **window** → connect it to Patch Panel0 (see table below) |
| **c** | Connect **Office-User PC** to the new Wall Mount1 |
| **d** | Wait 1–2 minutes → verify Office-User PC received IP via DHCP → browse to `office.srv` ✅ |
| **e** | *(Optional)* Create BendPoints in new cables and organize them |

> ⚠️ **Grading Note:** The new wall mount must be named **`Wall Mount1`** for correct scoring!

**📊 New Switch-to-Panel Connections — Office-SW1 ↔ Patch Panel0:**

| Office-SW1 Port | Patch Panel0 Jack |
|:---:|:---:|
| G1/0/21 | Jack21 |
| G1/0/22 | Jack22 |
| G1/0/23 | Jack23 |
| G1/0/24 | Jack24 |

**📊 New Wall Mount1 ↔ Patch Panel0 Connections:**

| Wall Mount1 (Next to Window) | Patch Panel0 |
|:---:|:---:|
| PunchDown1 | Punchdown21 |
| PunchDown2 | Punchdown22 |
| PunchDown3 | Punchdown23 |
| PunchDown4 | Punchdown24 |

---

## 7. Complete Connection Tables

### 📊 All Switch-to-Patch-Panel Connections

| Office-SW1 Port | Patch Panel0 Jack | Used By |
|:---:|:---:|:---:|
| G1/0/13 | Jack13 | Wall Mount0 → Office-Admin |
| G1/0/14 | Jack14 | Wall Mount0 → Printer0 |
| G1/0/15 | Jack15 | Wall Mount0 (spare) |
| G1/0/16 | Jack16 | Wall Mount0 (spare) |
| G1/0/21 | Jack21 | Wall Mount1 → Office-User |
| G1/0/22 | Jack22 | Wall Mount1 (spare) |
| G1/0/23 | Jack23 | Wall Mount1 (spare) |
| G1/0/24 | Jack24 | Wall Mount1 (spare) |

### 📊 All Wall-Mount-to-Patch-Panel Connections

| Wall Mount | PunchDown Port | Patch Panel0 PunchDown |
|:---:|:---:|:---:|
| Wall Mount0 | PunchDown1 | Punchdown13 |
| Wall Mount0 | PunchDown2 | Punchdown14 |
| Wall Mount0 | PunchDown3 | Punchdown15 |
| Wall Mount0 | PunchDown4 | Punchdown16 |
| Wall Mount1 | PunchDown1 | Punchdown21 |
| Wall Mount1 | PunchDown2 | Punchdown22 |
| Wall Mount1 | PunchDown3 | Punchdown23 |
| Wall Mount1 | PunchDown4 | Punchdown24 |

---

## 8. Full Network Path Diagram

```
END DEVICES (Office)
      │
[Office-Admin PC]  [Printer0]        [Office-User PC]
      │                 │                    │
      └────────┬─────────┘                   │
               │  Copper Straight-Through     │  Copper Straight-Through
               ▼                             ▼
        [Wall Mount0 Jack]           [Wall Mount1 Jack]
        (Next to Equip. Cabinet)     (Next to Window)
               │                             │
               │ PunchDown1-4               │ PunchDown1-4
               │ (inside wall)              │ (inside wall)
               ▼                             ▼
        [Wall Mount0 Back]           [Wall Mount1 Back]
               │                             │
               │ Copper Straight-Through     │ Copper Straight-Through
               ▼                             ▼
     [Patch Panel0 Punchdown13-16]  [Patch Panel0 Punchdown21-24]
               │                             │
               └──────────┬──────────────────┘
                          │ Copper Straight-Through
                          ▼
               [Patch Panel0 Jack13-16 / Jack21-24]
                          │
                          │ Copper Straight-Through
                          ▼
               [Office-SW1 G1/0/13-16 / G1/0/21-24]
                          │
                          ▼
               [Office-Server] ← DHCP + Web Server
               (Inside Equipment Closet)
                          │
                          ▼
                    [office.srv] ✅
```

---

## 9. Activity Screenshots

### Screenshot 1 — Wiring Closet: Rack with Patch Panel, Switch, Router, LAP, WLC
*Shows the equipment rack in the Wiring Closet with cables organized. The Cable Pegboard on the right shows the patch cables available for connections. Completion: 59%*

![Wiring Closet Rack](img6.jpeg)

---

### Screenshot 2 — Office Physical View: Wall Mount0, Office-Admin, Printer0 with Cable BendPoints
*Shows the Office room in Physical mode. Office-Admin and Printer0 are connected to Wall Mount0. Green cables with BendPoints route neatly along the walls toward the Equipment Cabinet. Completion: 59%*

![Office with Wall Mount0 and BendPoints](img7.jpeg)

---

### Screenshot 3 — Wiring Closet: Rack After Part 3 Connections (G1/0/21–24 added)
*Shows the Wiring Closet rack after adding the second set of patch panel connections (G1/0/21–24 → Jack21–24). The rack now has a full set of colored patch cables organized neatly. Completion: 77%*

![Wiring Closet with additional connections](img5.jpeg)

---

### Screenshot 4 — Office: Adding Wall Mount1 (Next to Window) — Port Context Menu
*Shows the context menu when connecting Wall Mount1's punchdown ports to Patch Panel0. The right-side panel lists all available PunchDown and Jack ports. Completion: 77%*

![Wall Mount1 connection context menu](img4.jpeg)

---

### Screenshot 5 — Office: Final Physical Layout with Wall Mount1 Connected (View 1)
*Shows the completed Office view with Wall Mount0 and Wall Mount1 both installed and connected. Office-Admin, Printer0, and Office-User PC are all linked to the network through their respective wall mounts. Completion: 100%*

![Final Office Layout - View 1](img1.jpeg)

---

### Screenshot 6 — Office: Final Physical Layout with Wall Mount1 Connected (View 2)
*An alternate zoomed-out view of the completed Office showing all devices connected, cables organized, and the full structured cabling implementation. Completion: 100%*

![Final Office Layout - View 2](img2.jpeg)

---

### Screenshot 7 — Activity Results: Score 22/22 ✅
*The Activity Results panel showing a perfect score of 22/22. All assessment items marked Correct — IP addresses, port types, patch panel connections (Jack13–24), and wall mount links all verified.*

![Activity Results 22/22](img3.jpeg)

---

### Screenshot 8 — Final Complete Structured Cabling Overview
*The complete structured cabling implementation showing the full physical office environment with all connections made, cables organized with BendPoints, and both wall mounts active.*

![Final Complete Structured Cabling](final.jpeg)

---

## 10. Important Tips & Warnings

> ⚠️ **Naming is CRITICAL for grading:**
> - Patch Panel → must be **`Patch Panel0`**
> - First Wall Mount → must be **`Wall Mount0`**
> - Second Wall Mount → must be **`Wall Mount1`**

> 💡 **Can't see the port numbers?**
> Right-click the device → **Inspect Front** → zoom in for a better view. Also use the global **Zoom In** tool on the toolbar.

> ⏳ **DHCP is not instant:**
> After connecting a device, wait **1–2 minutes** before testing. The Office-Server needs time to assign IP addresses via DHCP.

> 🌐 **How to verify connectivity:**
> Click **Office-Admin** or **Office-User** → **Desktop** → **Web Browser** → type `http://office.srv` → click **Go**. If the page loads → network is working! ✅

> 🎨 **Color coding cables:**
> Right-click any cable → **Color Cable** → select a color → helps you visually track which cable goes where in a busy rack.

> 🗂️ **Tidying the rack:**
> Right-click white space in the Rack → **Manage All Cables on Rack** → all dangling cables are instantly organized.

> 🔄 **BendPoints = real-world wall routing:**
> Creating BendPoints and dragging cables along walls simulates how cables are run inside walls, ceilings, and floors in a real office.

---

## 11. Quick Revision Glossary

| Term | One-Line Definition |
|---|---|
| **Structured Cabling** | Organized, standardized building-wide cabling system |
| **Wiring Closet** | Central room housing all networking equipment |
| **Equipment Cabinet** | Rack enclosure for networking devices |
| **Rack** | Metal frame for organizing and mounting devices |
| **Patch Panel** | Central rack-mounted hub between switch and wall outlets |
| **Jack** | Port on the front of a patch panel |
| **Punchdown** | Method of permanently terminating a wire into a block |
| **Wall Mount** | Wall-installed network outlet for end devices |
| **PunchDown Port** | Termination point on the back of a wall mount |
| **Cable Pegboard** | Cable selection palette in PT Physical mode |
| **Copper Straight-Through** | Standard cable for connecting different device types |
| **GigabitEthernet** | 1 Gbps switch port (e.g., G1/0/13) |
| **BendPoint** | Anchor point for routing cables along walls in PT |
| **DHCP** | Auto-assigns IP addresses to connected devices |
| **office.srv** | Web server used to verify end-to-end connectivity |
| **Inspect Front** | PT option to zoom into device front ports |
| **Manage All Cables** | PT option to auto-organize all cables in the rack |
| **Color Cable** | PT option to assign a color to a specific cable |
| **Back level (Alt-Left)** | Navigation shortcut to go back in PT Physical mode |

---

## 12. Key Points to Remember

> ✅ Structured cabling routes all connections through **patch panels and wall mounts** for organization

> ✅ The cable path is: **Device → Wall Mount Jack → Wall Mount PunchDown → Patch Panel PunchDown → Patch Panel Jack → Switch Port**

> ✅ Always use **Copper Straight-Through** cable in this activity

> ✅ Device naming is **critical** for correct grading: `Patch Panel0`, `Wall Mount0`, `Wall Mount1`

> ✅ **DHCP takes 1–2 minutes** after connection — be patient before testing!

> ✅ Verify connectivity by browsing to **`http://office.srv`** from a Web Browser

> ✅ Use **Inspect Front** + **Zoom In** to read small port labels

> ✅ **BendPoints** simulate running cables inside walls and floors

> ✅ **Manage All Cables on Rack** organizes all rack cables in one click

> ✅ **Color Cable** helps identify specific cables in a busy wiring environment

> ✅ Press **Alt-Left (Back level)** to navigate back in the Physical workspace

---

*📝 Notes by: Noor Ul Nisa | Cisco NetAcad | June 2026*  
*© 2017–2022 Cisco and/or its affiliates. All rights reserved. Cisco Public.*
