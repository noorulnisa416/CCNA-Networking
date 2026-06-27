# 💻 Packet Tracer — Explore Device Configuration Using the CLI (Console)

> **Activity Type:** Packet Tracer Hands-On Lab (1.1.8)
> **Course:** Exploring Networking with Cisco Packet Tracer | Cisco NetAcad
> **Student:** Noor Ul Nisa | Virtual University of Pakistan
> **Date:** June 2026
> **Final Score:** ✅ 100% Complete

---

## 📋 Table of Contents

1. [Key Definitions](#1-key-definitions)
2. [Objectives & Background](#2-objectives--background)
3. [Part 1 — Connect to the Device Using a Console Connection](#3-part-1--connect-to-the-device-using-a-console-connection)
4. [Part 2 — Copy Configuration Information to the Device](#4-part-2--copy-configuration-information-to-the-device)
5. [Part 3 — Save the Updated Configuration to the Device](#5-part-3--save-the-updated-configuration-to-the-device)
6. [Complete CLI Session — All Commands](#6-complete-cli-session--all-commands)
7. [IOS Modes Summary](#7-ios-modes-summary)
8. [Running Config vs Startup Config](#8-running-config-vs-startup-config)
9. [Quick Revision Glossary](#9-quick-revision-glossary)
10. [Key Points to Remember](#10-key-points-to-remember)

---

## 1. Key Definitions

### 🔹 Console Connection
**Definition:** A **direct physical cable connection** between a laptop/PC and a networking device (switch or router) used for **initial configuration** — even before the device is on an active network.

- In Packet Tracer → identified as the **Console cable** (shown as a **light blue cable**)
- Does NOT require any network connectivity — works on a standalone device
- Used for new devices, password recovery, and troubleshooting

---

### 🔹 Terminal Emulation Application
**Definition:** A **software program on a PC or laptop** that simulates a text-based terminal to allow you to communicate with and configure a network device through the console connection.

- **In Packet Tracer:** Laptop → Desktop tab → **Terminal** application
- **Real-world equivalents:** PuTTY, Tera Term, SecureCRT, HyperTerminal
- The Terminal Configuration window has settings for communication → accept defaults → click **OK**

---

### 🔹 hostname Command
**Definition:** The IOS command used to **assign a name to a networking device**. The name appears in the CLI prompt immediately after the command is entered.

```bash
Switch(config)# hostname Office-SW2
Office-SW2(config)#   ← Name changes immediately!
```

---

### 🔹 line con 0
**Definition:** The IOS command to **enter Console Line Configuration Mode** — used to configure settings for the console port (port 0 is always the first console port).

```bash
Switch(config)# line con 0
Switch(config-line)#
```

---

### 🔹 password Command
**Definition:** Sets a **password on a line** (console, VTY, etc.) to restrict access. Must be followed by the `login` command to enforce the password.

```bash
Office-SW2(config-line)# password Cisco123
Office-SW2(config-line)# login
```

---

### 🔹 login Command
**Definition:** Enables **password checking** on a line. Without `login`, the password is set but not enforced — anyone can access the device without a password.

---

### 🔹 show running-config
**Definition:** Displays the **current active configuration** stored in the device's RAM. Shows everything currently configured on the device.

```bash
Switch# show running-config
```
> Press **CTRL-C** to return to the switch prompt if the output is long.
> Press **Spacebar** to advance to the next screen if `--More--` appears.

---

### 🔹 copy running-config startup-config
**Definition:** The command that **saves the running configuration from RAM to NVRAM** (permanent storage). This ensures configuration survives a device restart.

```bash
Office-SW2# copy running-config startup-config
Destination filename [startup-config]?   ← Press ENTER to confirm
Building configuration...
[OK]
```

---

### 🔹 reload Command
**Definition:** **Reboots the device** — reloads the IOS software and startup configuration. Used to test whether configuration was saved properly.

```bash
Office-SW2# reload
Proceed with reload? [confirm]   ← Press ENTER to confirm
```

> After reload, if the password was saved correctly → device will ask for password = **`Cisco123`**

---

### 🔹 User Access Verification
**Definition:** The **password prompt message** shown on the console after the device reboots, when a console password has been set and saved. It confirms the password protection is active.

```
User Access Verification
Password:
```
> ⚠️ **Note:** Passwords do NOT display on the screen as you type — this is normal security behavior!

---

### 🔹 %SYS-5-CONFIG_I Message
**Definition:** A Cisco IOS **system message** that appears automatically when configuration changes are made through the console. It confirms that the configuration was applied from the console.

```
%SYS-5-CONFIG_I: Configured from console by console
```

---

## 2. Objectives & Background

### 🎯 Objectives
| Part | Task |
|---|---|
| **Part 1** | Connect to the switch **Office-SW2** using a console connection and Terminal app |
| **Part 2** | Copy configuration commands to the device: set hostname + set console password |
| **Part 3** | Save the updated configuration and verify it persists after a reload |

### 📖 Background / Scenario
A **new switch (Office-SW2)** is being added to the office network. Before placing a networking device into a network:

- It must be **configured and tested** first
- New switches and routers may **NOT be pre-configured** with enough information to be accessible via Ethernet or wireless
- A **console connection + terminal emulation app** provides a way to configure the device without needing an active network
- Changes made in CLI take effect immediately as part of the **running configuration**
- Configuration **must be saved** to survive a restart

---

## 3. Part 1 — Connect to the Device Using a Console Connection

### 🔧 Step 1: Access the CLI Using Terminal Emulation

| Step | Action |
|---|---|
| **a** | Click **Laptop0** on the table in the **Physical Workspace** |
| **b** | Click the **Desktop** tab in the configuration window |
| **c** | Open the **Terminal** application → the Terminal Configuration window appears → accept defaults → click **OK** |
| **d** | A terminal window opens showing the switch console → wait for scrolling to stop → **"Press RETURN to get started!"** appears → press **ENTER** |

> 💡 **What is the Console cable?** In Packet Tracer, the Console cable is the **light blue cable** connecting Laptop0 to Office-SW2's console port.

**What you see when connected:**
```
Press RETURN to get started!

Switch>
```

---

### 🔧 Step 2: Access Privileged EXEC Mode

**a. Explore User EXEC Mode commands:**
```bash
Switch> ?
```
> A list of commands available in User EXEC mode is displayed.
> ❓ **Question asked:** What is the last command displayed in the list?

**b. Enter Privileged EXEC Mode:**
```bash
Switch> enable
Switch#
```
> ✅ Notice the prompt changed from `Switch>` to `Switch#` — this confirms Privileged EXEC mode!

**c. Explore Privileged EXEC Mode commands:**
```bash
Switch# ?
```
> If **`--More--`** appears at the bottom → press **Spacebar** to see the next screen.
> ❓ **Question asked:** What is the last command in the list for Privileged EXEC mode?

**d. View the Running Configuration:**
```bash
Switch# show running-config
```
> Displays the current default (minimal) configuration on the new switch.
> Press **CTRL-C** to return to the switch prompt.

---

## 4. Part 2 — Copy Configuration Information to the Device

### 🔧 Step 1: Enter Global Configuration Mode

```bash
Switch# configure terminal
Enter configuration commands, one per line.  End with CNTL/Z.
Switch(config)#
```
> ✅ Prompt changes to `Switch(config)#` — confirms Global Configuration mode!

---

### 🔧 Step 2: Copy and Paste Configuration Commands

**a. The commands to copy into the switch:**

```bash
hostname Office-SW2
line con 0
password Cisco123
login
end
```

**b. Right-click at the switch prompt → select Paste → commands are applied:**

```bash
Switch(config)# hostname Office-SW2
Office-SW2(config)# line con 0
Office-SW2(config-line)# password Cisco123
Office-SW2(config-line)# login
Office-SW2(config-line)# end
Office-SW2#
%SYS-5-CONFIG_I: Configured from console by console
```

> ✅ **What happened line by line:**
> - `hostname Office-SW2` → device name changed → prompt now shows **Office-SW2**
> - `line con 0` → entered Console Line mode → prompt changes to `(config-line)#`
> - `password Cisco123` → set console password to **Cisco123**
> - `login` → enabled password enforcement on the console port
> - `end` → returned to Privileged EXEC mode

---

### 🔧 Step 3: Test the New Configuration

**a. Type `exit` to test the console password:**
```bash
Office-SW2# exit
```
> Screen refreshes → **"Press RETURN to get started!"** message appears

**b. Press ENTER.**
> ❓ **Question asked:** What message is shown on the console?
> ✅ **Answer:** `User Access Verification` — password prompt appears!

**c. Enter the password:**
```
Password: Cisco123
```
> ⚠️ Password does **NOT display** on screen — this is normal!
> ✅ **User EXEC prompt appears** → password is working!

> 🏁 **Completion at this point: 75%**

---

## 5. Part 3 — Save the Updated Configuration to the Device

> **Why save?** If the device loses power or is restarted, all configuration changes are **lost** unless saved. The startup configuration (NVRAM) loads when the device starts — we must copy running config to startup config.

---

### 🔧 Step 1: Enter Privileged EXEC Mode

```bash
Office-SW2> enable
Office-SW2#
```

---

### 🔧 Step 2: Save Running Config to Startup Config

```bash
Office-SW2# copy running-config startup-config
Destination filename [startup-config]?
Building configuration...
[OK]
```

> ✅ Press **ENTER** to accept the default filename `startup-config`
> ✅ **[OK]** confirms the configuration was saved successfully to NVRAM!

---

### 🔧 Step 3: Verify the Save with reload

**a. Reload (reboot) the device:**
```bash
Office-SW2# reload
Proceed with reload? [confirm]
```
> Press **ENTER** to confirm the reload.
> IOS software reloads and reads the **startup configuration from NVRAM**.

**b. Press ENTER when "Press RETURN to get started!" appears.**
> If the configuration was saved correctly → `User Access Verification` password prompt appears ✅

**c. Enter password:**
```
Password: Cisco123
```
> ✅ User EXEC prompt appears → confirms configuration was saved and loaded correctly!

> 🏁 **Completion at this point: 100%** 🎉

---

## 6. Complete CLI Session — All Commands

```bash
# ─────────────────────────────────────────
# PART 1 — Connect and Explore
# ─────────────────────────────────────────

# Default prompt after connection
Switch>

# Explore User EXEC commands
Switch> ?

# Enter Privileged EXEC mode
Switch> enable
Switch#

# Explore Privileged EXEC commands
Switch# ?

# View running configuration
Switch# show running-config


# ─────────────────────────────────────────
# PART 2 — Configure the Device
# ─────────────────────────────────────────

# Enter Global Configuration mode
Switch# configure terminal
Switch(config)#

# Set hostname
Switch(config)# hostname Office-SW2
Office-SW2(config)#

# Enter Console Line config mode
Office-SW2(config)# line con 0
Office-SW2(config-line)#

# Set console password
Office-SW2(config-line)# password Cisco123

# Enable password checking
Office-SW2(config-line)# login

# Exit back to Privileged EXEC
Office-SW2(config-line)# end
Office-SW2#

# Test the password
Office-SW2# exit
# → Press ENTER → enter "Cisco123" → User EXEC prompt appears ✅


# ─────────────────────────────────────────
# PART 3 — Save the Configuration
# ─────────────────────────────────────────

# Enter Privileged EXEC
Office-SW2> enable
Office-SW2#

# Save configuration to NVRAM
Office-SW2# copy running-config startup-config
# → Press ENTER → [OK] ✅

# Reload to verify
Office-SW2# reload
# → Press ENTER → "Press RETURN to get started!" → Enter "Cisco123" → ✅ 100% Complete!
```

---

## 7. IOS Modes Summary

| Mode | Prompt | How to Enter | What You Can Do |
|---|---|---|---|
| User EXEC | `Switch>` | Default on login | View basic info, limited monitoring |
| Privileged EXEC | `Switch#` | `enable` | Full monitoring, save/reload, view all |
| Global Config | `Switch(config)#` | `configure terminal` | Change device-wide settings |
| Console Line Config | `Switch(config-line)#` | `line con 0` | Set console password, login |

**Mode Navigation:**
```
Switch>
  │ enable
  ▼
Switch#
  │ configure terminal
  ▼
Switch(config)#
  │ line con 0
  ▼
Switch(config-line)#
  │ end / Ctrl+Z
  ▼
Switch#
  │ exit
  ▼
Switch>  ← Password prompt appears if login is set
```

---

## 8. Running Config vs Startup Config

```
┌──────────────────────────────────────────────────────┐
│                  DEVICE MEMORY                       │
│                                                      │
│  ┌──────────────────────────────┐                    │
│  │     RAM — Temporary          │                    │
│  │   running-config             │◄── All CLI changes │
│  │   (active, lost on restart)  │    take effect here│
│  └──────────────┬───────────────┘                    │
│                 │  copy running-config startup-config │
│                 ▼                                    │
│  ┌──────────────────────────────┐                    │
│  │     NVRAM — Permanent        │                    │
│  │   startup-config             │◄── Loaded on boot  │
│  │   (survives restart)         │                    │
│  └──────────────────────────────┘                    │
└──────────────────────────────────────────────────────┘
```

| | Running Config | Startup Config |
|---|---|---|
| **Location** | RAM | NVRAM |
| **Temporary?** | ✅ Yes — lost on restart | ❌ No — permanent |
| **Updated by** | Every CLI change | `copy running-config startup-config` |
| **Loaded when** | Device is running | Device boots up |
| **View command** | `show running-config` | `show startup-config` |

---

## 9. Quick Revision Glossary

| Term | Definition |
|---|---|
| **Console Connection** | Direct cable connection from PC to network device for initial config |
| **Console Cable** | Light blue cable in PT connecting laptop to switch console port |
| **Terminal Application** | Software (in PT: Desktop → Terminal) to access device CLI |
| **User EXEC Mode** | Default mode — monitoring only (`Switch>`) |
| **Privileged EXEC Mode** | Full access mode — entered with `enable` (`Switch#`) |
| **Global Config Mode** | Change-making mode — entered with `configure terminal` (`Switch(config)#`) |
| **Line Con 0** | Console Line Config mode — configure console port settings |
| **hostname** | Command to set the device name |
| **password** | Command to set a password on a line |
| **login** | Command to enforce password checking on a line |
| **running-config** | Active config in RAM — lost if not saved |
| **startup-config** | Saved config in NVRAM — survives restarts |
| **show running-config** | View the current active configuration |
| **copy run start** | Save running config to startup config |
| **reload** | Reboot the device — reloads IOS and startup config |
| **User Access Verification** | Password prompt after reboot if console password is set |
| **%SYS-5-CONFIG_I** | System message confirming config was applied from console |
| **--More--** | Pause indicator — press Spacebar to see next screen |
| **CTRL-C** | Stops output and returns to prompt |
| **Cisco123** | Console password used in this activity |

---

## 10. Key Points to Remember

> ✅ A **console connection** allows device configuration without any network being active
> ✅ Console cable in Packet Tracer = **light blue cable**
> ✅ Access CLI via: **Laptop → Desktop tab → Terminal app → accept defaults → OK**
> ✅ Wait for **"Press RETURN to get started!"** before typing commands
> ✅ `Switch>` = User EXEC mode → type `enable` → enter Privileged EXEC `Switch#`
> ✅ Use `?` **anytime** to see available commands in the current mode
> ✅ If `--More--` appears → press **Spacebar** to advance | **CTRL-C** to exit
> ✅ `configure terminal` → enters Global Config mode `Switch(config)#`
> ✅ `hostname Office-SW2` → changes device name → **prompt changes immediately**
> ✅ `line con 0` → enters Console Line mode `(config-line)#`
> ✅ `password Cisco123` + `login` → sets and enforces console password
> ✅ `end` → returns directly to Privileged EXEC from any config mode
> ✅ `exit` → from Privileged EXEC → returns to User EXEC (triggers password prompt)
> ✅ Passwords **do NOT display** on screen when typed — this is normal security behavior
> ✅ **ALWAYS SAVE:** `copy running-config startup-config` → writes to NVRAM
> ✅ `reload` → reboots device → loads startup config → tests if save was successful
> ✅ After reload with saved password → **User Access Verification** prompt confirms success ✅
> ✅ Configuration changes are **only made to running-config** — must copy to startup-config to persist
> ✅ Activity completion: **75% after Part 2** | **100% after Part 3** 🎉

---

*📝 Notes by: Noor Ul Nisa | Cisco NetAcad | June 2026*
*© 2017–2022 Cisco and/or its affiliates. All rights reserved. Cisco Public.*
