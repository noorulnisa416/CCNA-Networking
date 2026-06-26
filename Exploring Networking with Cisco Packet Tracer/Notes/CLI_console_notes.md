# 💻 Explore Device Configuration Using the CLI (Console)

> **Topic:** Device Configuration Using CLI Console
> **Course:** Exploring Networking with Cisco Packet Tracer | Cisco NetAcad
> **Student:** Noor Ul Nisa | Virtual University of Pakistan
> **Date:** June 2026

---

## 📋 Table of Contents

1. [Key Definitions](#1-key-definitions)
2. [Device Configuration Tabs in Packet Tracer](#2-device-configuration-tabs-in-packet-tracer)
3. [Ways to Access Device Configuration](#3-ways-to-access-device-configuration)
4. [Config Tab vs CLI Tab](#4-config-tab-vs-cli-tab)
5. [Cisco IOS Modes](#5-cisco-ios-modes)
6. [Essential CLI Commands](#6-essential-cli-commands)
7. [Running Config vs Startup Config](#7-running-config-vs-startup-config)
8. [Step-by-Step CLI Workflow](#8-step-by-step-cli-workflow)
9. [Quick Revision Glossary](#9-quick-revision-glossary)
10. [Key Points to Remember](#10-key-points-to-remember)

---

## 1. Key Definitions

### 🔹 CLI (Command Line Interface)
**Definition:** A **text-based interface** where users type commands to configure, monitor, and manage a networking device. There are no buttons or menus — everything is done by typing specific commands.

> 💡 **Analogy:** Like texting commands to your device — instead of clicking icons, you type instructions and the device responds.

**Why is CLI important?**
- Required for **real Cisco hardware** — no graphical interface exists on actual routers/switches
- Gives **full control** over every device setting
- **Mandatory skill** for CCNA and all advanced networking certifications
- Faster and more powerful than GUI-based configuration

---

### 🔹 Cisco IOS (Internetwork Operating System)
**Definition:** The **operating system** that runs on Cisco routers and switches — just like Windows runs on your PC or Android runs on your phone. IOS controls all the functions of the device.

**Key facts:**
- Loads first when a device powers on
- Then loads the saved device configuration
- Provides CLI access through different **modes**
- When fully loaded → shows message: **`Press Return to Get Started`**

---

### 🔹 Console Connection
**Definition:** A **direct physical connection** from a PC to a network device using a **Console Cable** (rollover cable) that allows initial configuration of the device before any network connectivity exists.

**Used for:**
- Initial setup of a new device
- Password recovery
- Troubleshooting when remote access is unavailable

**In Packet Tracer:** Access via **Desktop tab → Terminal** on a PC connected to the switch/router via console cable.

---

### 🔹 Terminal Emulator
**Definition:** A **software application on a PC** that allows you to connect to and interact with the CLI of a network device through a console connection.

**In Packet Tracer:** Click **PC → Desktop tab → Terminal** to open the terminal emulator.

**Real-world tools:** PuTTY, SecureCRT, Tera Term, HyperTerminal

---

### 🔹 Running Configuration
**Definition:** The **active configuration currently loaded in the device's RAM (memory)**. Any changes made via CLI take effect immediately in the running configuration — but this is **lost when the device restarts** unless saved.

**Location:** Stored in **RAM** (temporary memory)
**Command to view:** `show running-config`

---

### 🔹 Startup Configuration
**Definition:** The **saved configuration stored in the device's NVRAM (permanent storage)**. This is the configuration that loads every time the device boots up.

**Location:** Stored in **NVRAM** (non-volatile memory — permanent)
**Command to view:** `show startup-config`

---

### 🔹 User EXEC Mode
**Definition:** The **default mode** when you first access a Cisco IOS device. It provides limited, **monitoring-only** capabilities — you can view basic information but cannot make any changes.

**Prompt looks like:** `Switch>`
**Symbol:** `>` (greater than sign)

---

### 🔹 Privileged EXEC Mode (Enable Mode)
**Definition:** An **elevated access mode** that provides full monitoring capabilities and access to more commands than User EXEC mode. Required before entering Configuration mode.

**Prompt looks like:** `Switch#`
**Symbol:** `#` (hash/pound sign)
**Command to enter:** `enable`

---

### 🔹 Global Configuration Mode
**Definition:** The mode used to **make changes to the device's configuration**. Commands entered here affect the entire device.

**Prompt looks like:** `Switch(config)#`
**Command to enter:** `configure terminal` (or `conf t`)

---

## 2. Device Configuration Tabs in Packet Tracer

Cisco Packet Tracer provides **5 configuration tabs** for devices. The tabs shown depend on the type of device being configured.

| Tab | Description | Available On |
|---|---|---|
| 🖥️ **Physical** | Shows the physical device — add/remove modules, power on/off | All devices |
| ⚙️ **Config** | Graphical user interface for basic configuration (PT-only) | Routers, Switches |
| 💻 **CLI** | Command Line Interface — direct IOS access | Routers, Switches |
| 🖱️ **Desktop** | Simulated PC applications (Terminal, Web Browser, IP Config) | PCs, Laptops |
| 🌐 **Services** | Configure server services (DHCP, DNS, HTTP, FTP, etc.) | Servers |

---

## 3. Ways to Access Device Configuration

For **intermediate devices** (routers and switches), there are **3 ways** to access configuration in Packet Tracer:

```
┌─────────────────────────────────────────────────────────────┐
│           WAYS TO ACCESS DEVICE CONFIGURATION               │
│                                                             │
│  1. Config Tab ────────► Graphical Interface (PT only)      │
│                                                             │
│  2. CLI Tab ───────────► Direct CLI in Packet Tracer        │
│                                                             │
│  3. PC Terminal ───────► Console cable → PC → Terminal app  │
│                          (Simulates real-world access)      │
└─────────────────────────────────────────────────────────────┘
```

### Method 1 — Config Tab (GUI)
- Graphical point-and-click interface
- **Only exists in Packet Tracer** — not available on real hardware
- Great for beginners who don't know CLI yet
- Shows equivalent IOS commands in the **"Equivalent IOS Commands"** window

### Method 2 — CLI Tab
- Direct access to IOS command line inside Packet Tracer
- Simulates the actual CLI of a real Cisco device
- Requires knowledge of IOS commands

### Method 3 — PC Terminal (Console)
- Most realistic — simulates real-world access
- Connect PC to switch/router via **Console Cable**
- Open **Desktop → Terminal** on the PC
- Type IOS commands in the terminal emulator

---

## 4. Config Tab vs CLI Tab

| Feature | Config Tab (GUI) | CLI Tab |
|---|---|---|
| Interface type | Graphical (buttons, fields) | Text-based (type commands) |
| Available on real hardware? | ❌ No — Packet Tracer only | ✅ Yes — real Cisco devices |
| Requires IOS knowledge? | ❌ No | ✅ Yes |
| Shows IOS commands? | ✅ Yes — in "Equivalent IOS Commands" window | ✅ Yes — you type them |
| Full device control? | ❌ Limited (basic settings only) | ✅ Full control |
| Best for | Beginners learning CLI syntax | Intermediate/advanced users |
| Changes take effect? | ✅ Immediately | ✅ Immediately |

> 💡 **Key insight:** As you change settings in the **Config tab**, the actual CLI commands appear in the **"Equivalent IOS Commands"** window — this is a great way to **learn CLI syntax** by doing!

> ⚠️ **Important:** The Config tab is **unique to Packet Tracer**. On real Cisco hardware, you MUST use the CLI.

---

## 5. Cisco IOS Modes

Cisco IOS has a **hierarchy of modes**. Each mode gives access to different commands and levels of control.

```
POWER ON DEVICE
      │
      ▼
Press Return to Get Started
      │
      ▼
┌─────────────────────────┐
│   USER EXEC MODE        │  Switch>
│   (Monitoring only)     │
│   Limited commands      │
└───────────┬─────────────┘
            │  Type: enable
            ▼
┌─────────────────────────┐
│  PRIVILEGED EXEC MODE   │  Switch#
│  (Full monitoring)      │
│  All show commands      │
│  Can save config        │
└───────────┬─────────────┘
            │  Type: configure terminal
            ▼
┌─────────────────────────┐
│  GLOBAL CONFIG MODE     │  Switch(config)#
│  Make device-wide       │
│  configuration changes  │
└───────────┬─────────────┘
            │  (sub-modes available)
            ▼
┌─────────────────────────┐
│  INTERFACE CONFIG MODE  │  Switch(config-if)#
│  Configure specific     │
│  interfaces/ports       │
└─────────────────────────┘
```

### Mode Summary Table

| Mode | Prompt | Access Command | What You Can Do |
|---|---|---|---|
| User EXEC | `Switch>` | Default on login | View basic info, limited monitoring |
| Privileged EXEC | `Switch#` | `enable` | Full monitoring, save config, view all |
| Global Config | `Switch(config)#` | `configure terminal` | Change device-wide settings |
| Interface Config | `Switch(config-if)#` | `interface [type] [number]` | Configure specific ports |

---

## 6. Essential CLI Commands

### 🔑 Navigation Commands

| Command | Mode | What it Does |
|---|---|---|
| `enable` | User EXEC → | Enters Privileged EXEC mode |
| `configure terminal` | Privileged EXEC → | Enters Global Configuration mode |
| `exit` | Any mode → | Goes back one mode level |
| `end` or `Ctrl+Z` | Any config mode → | Returns directly to Privileged EXEC |
| `?` | Any mode | Lists all available commands in current mode |
| `[command] ?` | Any mode | Shows help for a specific command |

---

### 🏷️ Device Name (Hostname) Command

```bash
Switch(config)# hostname [new-name]
```

**Example:**
```bash
Switch(config)# hostname Office-SW1
Office-SW1(config)#
```
> ✅ The prompt changes **immediately** to show the new hostname — this is how you know the command worked!

---

### 💾 Save Configuration Commands

```bash
# View current running configuration (RAM)
Switch# show running-config

# View saved startup configuration (NVRAM)
Switch# show startup-config

# Save running config to startup config (MOST IMPORTANT!)
Switch# copy running-config startup-config
```

> ⚠️ **Critical:** If you do NOT save with `copy running-config startup-config`, all your changes will be **LOST** when the device restarts!

---

### 🔍 Useful Show Commands (Privileged EXEC Mode)

```bash
# View full configuration in RAM
Switch# show running-config

# View saved configuration in NVRAM
Switch# show startup-config

# View IOS version and hardware info
Switch# show version

# View all interfaces and their status
Switch# show interfaces

# View IP interface brief (quick overview)
Switch# show ip interface brief

# View MAC address table (switches)
Switch# show mac address-table
```

---

### ❓ The Help System ( ? )

```bash
# List ALL commands in current mode
Switch# ?

# List commands starting with "sh"
Switch# sh?

# Show options after a command
Switch# show ?
```

> 💡 **The `?` is your best friend in CLI!** Use it whenever you are unsure of a command or its options.

---

## 7. Running Config vs Startup Config

This is one of the **most important concepts** in Cisco IOS!

```
┌─────────────────────────────────────────────────────────┐
│                    DEVICE MEMORY                        │
│                                                         │
│  ┌─────────────────────────────────┐                    │
│  │       RAM (Temporary)           │                    │
│  │   running-config                │◄── Active config   │
│  │   (changes take effect here     │    All CLI changes  │
│  │    immediately)                 │    go here first   │
│  └──────────────┬──────────────────┘                    │
│                 │  copy running-config startup-config   │
│                 ▼                                       │
│  ┌─────────────────────────────────┐                    │
│  │       NVRAM (Permanent)         │                    │
│  │   startup-config                │◄── Saved config    │
│  │   (survives restart)            │    Loads on boot   │
│  └─────────────────────────────────┘                    │
└─────────────────────────────────────────────────────────┘
```

| | Running Config | Startup Config |
|---|---|---|
| **Stored in** | RAM (temporary) | NVRAM (permanent) |
| **Lost on restart?** | ✅ Yes — unless saved | ❌ No — survives restarts |
| **Contains** | Current active settings | Last saved settings |
| **View command** | `show running-config` | `show startup-config` |
| **When updated** | Every CLI change | Only when you save |

---

## 8. Step-by-Step CLI Workflow

### 🚀 Complete CLI Session — Changing Hostname & Saving

```bash
# Step 1 — Device boots, IOS loads
# Message appears:
Press RETURN to get started.

# Step 2 — Default mode: User EXEC
Switch>

# Step 3 — List available commands with ?
Switch> ?

# Step 4 — Enter Privileged EXEC mode
Switch> enable
Switch#

# Step 5 — List all available commands
Switch# ?

# Step 6 — Enter Global Configuration mode
Switch# configure terminal
Enter configuration commands, one per line.  End with CNTL/Z.
Switch(config)#

# Step 7 — Change the hostname
Switch(config)# hostname Office-SW1
Office-SW1(config)#        ← Prompt changes immediately! ✅

# Step 8 — Exit back to Privileged EXEC
Office-SW1(config)# exit
Office-SW1#

# Step 9 — Save the configuration (VERY IMPORTANT!)
Office-SW1# copy running-config startup-config
Destination filename [startup-config]?
Building configuration...
[OK]
Office-SW1#

# ✅ Configuration is now saved — safe from restarts!
```

---

## 9. Quick Revision Glossary

| Term | Definition |
|---|---|
| **CLI** | Text-based command interface for configuring devices |
| **IOS** | Cisco's operating system for routers and switches |
| **Console Connection** | Direct physical cable connection from PC to device |
| **Terminal Emulator** | PC software to access device CLI (e.g., PuTTY) |
| **User EXEC Mode** | Default login mode — monitoring only (`Switch>`) |
| **Privileged EXEC Mode** | Full access mode — enabled with `enable` (`Switch#`) |
| **Global Config Mode** | Change-making mode — entered with `conf t` (`Switch(config)#`) |
| **Running Config** | Active config in RAM — lost on restart if not saved |
| **Startup Config** | Saved config in NVRAM — survives restarts |
| **Hostname** | Device name shown in the CLI prompt |
| **`enable`** | Command to enter Privileged EXEC mode |
| **`configure terminal`** | Command to enter Global Configuration mode |
| **`hostname`** | Command to change the device name |
| **`copy run start`** | Command to save running config to startup config |
| **`show running-config`** | Displays the current active configuration |
| **`show startup-config`** | Displays the saved startup configuration |
| **`?`** | Help command — lists available commands in current mode |
| **Config Tab** | PT-only GUI tab — shows equivalent IOS commands |
| **RAM** | Temporary memory — stores running config |
| **NVRAM** | Permanent memory — stores startup config |

---

## 10. Key Points to Remember

> ✅ The **Config tab only exists in Packet Tracer** — on real hardware, CLI is mandatory
> ✅ When you change settings in the Config tab, the **equivalent IOS commands** appear in the window — use this to learn CLI syntax!
> ✅ IOS has **3 main modes:** User EXEC (`>`) → Privileged EXEC (`#`) → Global Config (`(config)#`)
> ✅ **`Press Return to Get Started`** means the device has fully loaded IOS and is ready
> ✅ Use **`?`** anytime to see available commands in the current mode
> ✅ Changes in CLI take effect **immediately** in running-config (RAM)
> ✅ Running config is stored in **RAM** → **LOST on restart** if not saved
> ✅ **ALWAYS save** with `copy running-config startup-config` after making changes
> ✅ Startup config is stored in **NVRAM** → survives restarts
> ✅ **Hostname change** is visible immediately in the prompt → `Switch(config)#` becomes `Office-SW1(config)#`
> ✅ To access CLI on **real equipment** → connect PC via Console cable → open Terminal app
> ✅ In Packet Tracer → access terminal via **PC → Desktop → Terminal**

---

*📝 Notes by: Noor Ul Nisa | Cisco NetAcad | June 2026*
