# 📡 Packet Tracer — Connect Devices using Wireless Technologies

> **Activity Type:** Packet Tracer Hands-On Lab
> **Course:** Exploring Networking with Cisco Packet Tracer | Cisco NetAcad
> **Student:** Noor Ul Nisa | Virtual University of Pakistan
> **Date:** June 2026
> **Mode:** Physical Mode Only

---

## 📋 Table of Contents

1. [Key Definitions](#1-key-definitions)
2. [Objectives & Background](#2-objectives--background)
3. [Wireless Technologies Covered](#3-wireless-technologies-covered)
4. [Part 1 — Connect a Laptop to the Office WLAN](#4-part-1--connect-a-laptop-to-the-office-wlan)
5. [Part 2 — Connect Devices with Bluetooth Technology](#5-part-2--connect-devices-with-bluetooth-technology)
6. [Part 3 — Tether a Laptop via Smartphone Cellular Network](#6-part-3--tether-a-laptop-via-smartphone-cellular-network)
7. [Comparison of Wireless Technologies](#7-comparison-of-wireless-technologies)
8. [Quick Revision Glossary](#8-quick-revision-glossary)
9. [Key Points to Remember](#9-key-points-to-remember)

---

## 1. Key Definitions

### 🔹 Wireless Technology
**Definition:** A method of transmitting data between devices using **radio waves, infrared, or other electromagnetic signals** — without the need for physical cables.

**Examples used in this activity:**
- 📶 **Wi-Fi** — wireless LAN (office network)
- 🔵 **Bluetooth** — short-range device pairing
- 📱 **Cellular (3G/4G)** — mobile internet tethering

---

### 🔹 WLAN (Wireless Local Area Network)
**Definition:** A **local area network** that uses wireless signals (Wi-Fi) instead of cables to connect devices within a limited area like an office, home, or campus.

**In this activity:** The **Employee SSID WLAN** is the office wireless network that the Laptop connects to.

---

### 🔹 SSID (Service Set Identifier)
**Definition:** The **name of a wireless network** broadcast by a wireless router or access point — what you see when you search for Wi-Fi on your phone or laptop.

**In this activity:** The SSID is **`Employee SSID`**

---

### 🔹 Pre-Shared Key (PSK / Wi-Fi Password)
**Definition:** A **password used to authenticate and encrypt** a wireless connection. Both the router and the connecting device must use the same key.

**In this activity:** The pre-shared key is **`Cisco123`**

---

### 🔹 WPC300N Module
**Definition:** A **wireless network adapter module** for laptops in Cisco Packet Tracer that enables Wi-Fi (802.11n) connectivity. Replaces the wired Ethernet NIC.

**Full name:** PT-LAPTOP-NM-1W (WPC300N)
**Replaces:** PT-LAPTOP-NM-1CFE (wired Ethernet module)

---

### 🔹 PT-LAPTOP-NM-1CFE
**Definition:** The **default wired Ethernet module** on a Laptop in Packet Tracer. It must be removed and replaced with the WPC300N to enable wireless connectivity.

---

### 🔹 Bluetooth
**Definition:** A **short-range wireless technology** (approximately 10 meters / 30 feet) used to connect and exchange data between devices such as phones, tablets, speakers, headphones, and laptops.

**Key characteristics:**
- Short range (~10 meters)
- Low power consumption
- Uses 2.4 GHz radio frequency
- Requires **Pairing** between devices
- Used for: speakers, headphones, keyboards, file transfer, tethering

---

### 🔹 Bluetooth Pairing
**Definition:** The process of **establishing a trusted connection** between two Bluetooth devices so they can communicate with each other.

**Steps:**
1. Both devices must have Bluetooth **ON**
2. One device **Discovers** nearby Bluetooth devices
3. Select the target device → click **Pair**
4. Accept the connection permission → click **Yes**
5. Status changes to **"Paired, Connected"** ✅

---

### 🔹 Cellular Network (3G/4G)
**Definition:** A **mobile wireless network** provided by a telecommunications company (ISP) that allows smartphones and cellular devices to access the Internet from almost anywhere using radio towers.

**In this activity:** The Smartphone is connected to the cellular network via the **3G/4G Cell1** interface.

---

### 🔹 Tethering
**Definition:** The process of **sharing a smartphone's cellular (mobile) internet connection** with another device (like a laptop) via Bluetooth, USB, or Wi-Fi hotspot.

**In this activity:** The Smartphone shares its 3G/4G internet with the User-Laptop via **Bluetooth Tethering**.

**Types of Tethering:**
| Type | Method |
|---|---|
| 🔵 Bluetooth Tethering | Share via Bluetooth (used in this activity) |
| 🔌 USB Tethering | Share via USB cable |
| 📶 Wi-Fi Hotspot | Share via Wi-Fi (device becomes a hotspot) |

---

### 🔹 PC Wireless Tool
**Definition:** A **Packet Tracer application** on the Desktop tab of a laptop/PC that simulates a wireless network manager — used to scan for, connect to, and manage wireless networks.

**Location:** Laptop → Desktop tab → PC Wireless

---

### 🔹 IP Configuration / Wireless0
**Definition:** In Packet Tracer, **Wireless0** is the wireless interface on a Laptop. After connecting to a Wi-Fi network, you can verify the assigned IP address here.

**Location:** Laptop → Config tab → Wireless0 → IP Configuration section

---

### 🔹 office.srv
**Definition:** The **web server** used in this activity to verify that a device has working internet/network connectivity. After connecting via any wireless method, browse to `office.srv` to confirm it works.

---

## 2. Objectives & Background

### 🎯 Objectives
| Part | Task |
|---|---|
| **Part 1** | Connect a Laptop to the Office WLAN using Wi-Fi (WPC300N module) |
| **Part 2** | Connect a Bluetooth Speaker to a Tablet using Bluetooth pairing |
| **Part 3** | Tether a Laptop to a Smartphone's Cellular Network via Bluetooth |

### 📖 Background
In this Packet Tracer activity, you will use **three different wireless technologies** to connect end devices in an office environment. The entire activity is performed in **Packet Tracer Physical Mode only**.

---

## 3. Wireless Technologies Covered

```
┌──────────────────────────────────────────────────────────────────┐
│               WIRELESS TECHNOLOGIES IN THIS ACTIVITY             │
│                                                                  │
│  📶 Wi-Fi (WLAN)          🔵 Bluetooth         📱 Cellular 3G/4G │
│  ─────────────────        ──────────────       ──────────────── │
│  • Office network         • Device pairing     • Mobile internet │
│  • Long range (100m)      • Short range (10m)  • Wide area       │
│  • High speed             • Low power          • ISP provided    │
│  • Needs router           • No router needed   • SIM-based       │
│  • Requires password      • Requires pairing   • Always on       │
└──────────────────────────────────────────────────────────────────┘
```

---

## 4. Part 1 — Connect a Laptop to the Office WLAN

### 🔧 Step 1: Install a Wireless Module on the Laptop

> **Why?** The Laptop comes with a wired Ethernet module by default. To use Wi-Fi, we must swap it for a wireless module — just like adding a Wi-Fi card to a real computer.

| Step | Action |
|---|---|
| **a** | Click the **Laptop** → opens the configuration window |
| **b** | Click the **Physical** tab → click the **power button** to **power OFF** the Laptop |
| **c** | Remove the **PT-LAPTOP-NM-1CFE** (Ethernet module) by **dragging it** from the Laptop to the module list on the left |
| **d** | Insert the **WPC300N** wireless module by **dragging it** from the module list on the left to the Laptop |
| **e** | Click the **power button** again to **power ON** the Laptop |

> ⚠️ **Important:** You MUST power OFF the Laptop before removing or inserting modules — it won't work while powered on!

---

### 🔧 Step 2: Connect the Laptop to the Office WLAN

| Step | Action |
|---|---|
| **a** | Click the **Desktop** tab → select **PC Wireless** tool |
| **b** | Click the **Connect** tab → wait for **Employee SSID WLAN** to appear. Click **Refresh** if needed |
| **c** | Click **Employee SSID** to select it → click **Connect** |
| **d** | Enter **`Cisco123`** as the pre-shared key → click **Connect** |
| **e** | Close the **PC Wireless** window |
| **f** | Click the **Config** tab → select **Wireless0** in the left pane → verify that an **IP address has been assigned** in the IP Configuration section |
| **g** | Open **Web Browser** from the Desktop → navigate to **`office.srv`** → verify the Laptop has connectivity ✅ |
| **h** | Close the **Laptop** window |

**Summary of Wi-Fi Connection Details:**
| Setting | Value |
|---|---|
| Network Name (SSID) | Employee SSID |
| Password (Pre-Shared Key) | Cisco123 |
| Wireless Module | WPC300N |
| Verify IP at | Config tab → Wireless0 |
| Test Connectivity | Browse to `office.srv` |

---

## 5. Part 2 — Connect Devices with Bluetooth Technology

> **Scenario:** Connect a **Bluetooth Speaker** to an **Office Tablet** so the tablet can play music through the speaker wirelessly.

### 🔧 Step 1: Enable Bluetooth Ports on Devices

| Step | Action |
|---|---|
| **a** | Click the **Bluetooth Speaker** → opens configuration window |
| **b** | Click the **Config** tab |
| **c** | Click **Bluetooth** in the left pane → check that **Port Status is ON** → note the speaker is **NOT yet paired** with the Office Tablet |

---

### 🔧 Step 2: Connect (Pair) Bluetooth Devices

| Step | Action |
|---|---|
| **a** | Open the **Office Tablet** |
| **b** | Click the **Config** tab |
| **c** | Click **Bluetooth** in the left pane → check the **On** box for Port Status |
| **d** | Click **Discover** → the **Bluetooth Speaker** device should appear in the discovered devices list |
| **e** | Select **Bluetooth Speaker** from the Devices list → click **Pair** → if prompted for permission → click **Yes** → status changes to **"Paired, Connected"** ✅ |
| **f** | To test: click **Desktop** tab → select **Music Player** → click **Play/Stop** to start music through the speaker |
| **g** | Click **Play/Stop** again to stop |

> ⚠️ **Note:** Make sure the Bluetooth Speaker is powered **ON** before attempting to pair!

**Bluetooth Pairing Flow:**
```
[Bluetooth Speaker]          [Office Tablet]
        │                          │
  Port Status: ON            Port Status: ON
        │                          │
        │         Discover ◄────── │
        │ ──────────────────────► │
        │    (Speaker appears)     │
        │                          │
        │  ◄─── Select + Pair ──── │
        │                          │
        └──── "Paired, Connected" ─┘ ✅
                                   │
                            Music Player →
                           Play/Stop Music 🎵
```

---

## 6. Part 3 — Tether a Laptop via Smartphone Cellular Network

> **Scenario:** The **User-Laptop** has no Wi-Fi or wired connection. Instead, it will use a **Smartphone's 3G/4G cellular internet** connection shared via **Bluetooth Tethering**.

---

### 🔧 Step 1: Enable Bluetooth on the Laptop

| Step | Action |
|---|---|
| **a** | Click the **User-Laptop** → click the **Config** tab |
| **b** | Click **Bluetooth** in the left panel → click **On** for the Port Status |
| **c** | Leave the **User-Laptop** Bluetooth window **open** |

---

### 🔧 Step 2: Connect Smartphone to the Cellular Network and Enable Bluetooth

| Step | Action |
|---|---|
| **a** | Click the **Smartphone** → opens configuration window |
| **b** | Click the **Config** tab → check the **On** box for **Cellular Tethering** in the **Global Settings** section |
| **c** | Click the **3G/4G Cell1** interface → verify the Smartphone has an **IP address** from the cellular network |
| **d** | Click **Bluetooth** in the left pane → check the **On** box for the **Port Status** on the Smartphone |

---

### 🔧 Step 3: Connect Bluetooth Devices and Enable Tethering

| Step | Action |
|---|---|
| **a** | In the Smartphone's **Bluetooth** configuration → click **Discover** to search for nearby Bluetooth devices |
| **b** | Select **User-Laptop** from the discovered devices → click **Pair** → a pop-up asks for permission → click **Yes** → devices are now connected via Bluetooth ✅ |
| **c** | Return to the **User-Laptop** → Config tab → Bluetooth panel → highlight **Smartphone** → click **Tether** |
| **d** | At the bottom of the Bluetooth configuration pane, notice that **User-Laptop has now obtained an IP address** (via the Smartphone's cellular connection) |
| **e** | Test connectivity: **Desktop → Web Browser** → enter **`office.srv`** in the URL field → click **Go** ✅ |

> 💡 **Tip:** You can click **Fast Forward Time** in Packet Tracer to speed up the connection process if it takes too long!

**Tethering Flow:**
```
[Cellular Tower / ISP]
        │
        │ 3G/4G Signal
        ▼
  [Smartphone]
  ├── 3G/4G Cell1: IP Address ✅
  ├── Bluetooth: ON
  └── Cellular Tethering: ON
        │
        │ Bluetooth Pairing + Tether
        ▼
  [User-Laptop]
  ├── Bluetooth: ON
  ├── Paired with Smartphone ✅
  ├── IP Address Obtained ✅
  └── Browse to office.srv ✅
```

---

## 7. Comparison of Wireless Technologies

| Feature | Wi-Fi (WLAN) | Bluetooth | Cellular (3G/4G) |
|---|---|---|---|
| **Range** | ~100 meters | ~10 meters | Kilometers (city-wide) |
| **Speed** | High (100+ Mbps) | Low-Medium (1–3 Mbps) | Medium (1–100 Mbps) |
| **Frequency** | 2.4 GHz / 5 GHz | 2.4 GHz | 800 MHz – 2.6 GHz |
| **Requires** | Router + Password | Pairing only | SIM card + ISP |
| **Power usage** | Medium | Very Low | High |
| **Best for** | Internet access | Short-range device pairing | Mobile internet anywhere |
| **Used in Part** | Part 1 | Part 2 & 3 | Part 3 |
| **Security** | WPA2/Pre-shared key | Pairing permission | ISP-controlled |
| **Real examples** | Home/Office Wi-Fi | Headphones, speakers, keyboard | Mobile data on phone |

---

## 8. Quick Revision Glossary

| Term | Definition |
|---|---|
| **WLAN** | Wireless Local Area Network — Wi-Fi based network |
| **SSID** | Name of a wireless network (Wi-Fi network name) |
| **Pre-Shared Key** | Wi-Fi password for authentication |
| **WPC300N** | Wireless NIC module for Laptop in Packet Tracer |
| **PT-LAPTOP-NM-1CFE** | Default wired Ethernet module on Laptop in PT |
| **PC Wireless** | PT Desktop app for managing Wi-Fi connections |
| **Wireless0** | Wireless network interface on the Laptop in PT |
| **Bluetooth** | Short-range wireless technology for device pairing |
| **Bluetooth Pairing** | Process of connecting two Bluetooth devices |
| **Discover** | Bluetooth function to search for nearby devices |
| **Pair** | Bluetooth function to establish a trusted connection |
| **"Paired, Connected"** | Status confirming successful Bluetooth connection |
| **Cellular Network** | 3G/4G mobile internet provided by telecom company |
| **Tethering** | Sharing smartphone internet with another device |
| **3G/4G Cell1** | Cellular interface on the Smartphone in PT |
| **Cellular Tethering** | Setting to enable internet sharing on smartphone |
| **Tether (button)** | PT button to activate tethering from laptop side |
| **office.srv** | Web server used to verify network connectivity |
| **Music Player** | PT Desktop app to test Bluetooth audio connection |
| **Physical Mode** | PT workspace showing real-world device placement |

---

## 9. Key Points to Remember

> ✅ This activity covers **3 wireless technologies:** Wi-Fi, Bluetooth, and Cellular Tethering
> ✅ **Must power OFF** the Laptop before swapping NIC modules
> ✅ Replace **PT-LAPTOP-NM-1CFE** (wired) with **WPC300N** (wireless) to enable Wi-Fi
> ✅ Wi-Fi SSID = **`Employee SSID`** | Password = **`Cisco123`**
> ✅ Verify Wi-Fi: **Config tab → Wireless0** → check IP address assigned
> ✅ **Bluetooth Pairing steps:** Enable BT on both devices → Discover → Select → Pair → Yes
> ✅ Bluetooth status must show **"Paired, Connected"** to confirm successful pairing
> ✅ Test Bluetooth audio via **Desktop → Music Player → Play/Stop**
> ✅ **Tethering** = Smartphone shares its cellular internet with Laptop via Bluetooth
> ✅ For tethering: enable **Cellular Tethering** on Smartphone → pair → click **Tether** on Laptop
> ✅ After tethering, check Laptop obtained an **IP address** in Bluetooth config pane
> ✅ Verify ALL wireless connections by browsing to **`office.srv`**
> ✅ Use **Fast Forward Time** in PT if the connection process is slow
> ✅ **Entire activity** is done in **Physical Mode only** — no Logical mode needed
> ✅ Wi-Fi = longest range | Bluetooth = shortest range | Cellular = widest coverage

---

*📝 Notes by: Noor Ul Nisa | Cisco NetAcad | June 2026*
*© 2017–2022 Cisco and/or its affiliates. All rights reserved. Cisco Public.*
