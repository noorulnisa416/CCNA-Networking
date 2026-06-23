# 📁 Cisco Packet Tracer — File Types Notes

> **Topic:** Cisco Packet Tracer File Types  
> **Course:** Getting Started with Cisco Packet Tracer  
> **Student:** Noor Ul Nisa  

---

## 📋 Overview

Cisco Packet Tracer can create **four different types of files**, each used for a different purpose.

| File Type | Full Name | Purpose |
|---|---|---|
| `.pka` | Packet Tracer Activity | Scored activities with instructions |
| `.pkt` | Packet Tracer Network | Saved network simulations |
| `.pksz` | Packet Tracer Tutored Activity | Guided activities with hints |
| `.pkz` | Packet Tracer Zipped *(deprecated)* | Old format for embedding images |

---

## 1️⃣ .pka — Packet Tracer Activity File

> 💡 **Memory Tip:** Think of the **"a"** in `.pka` as **"activity"**

### Definition:
The `.pka` file is the **most common file type** you will use in Cisco Packet Tracer. It is a **Packet Tracer Activity file** that includes an instructions window and is usually scored.

### Key Features:
- ✅ Has an **Instructions Window** (shows what to do step by step)
- ✅ **Scored** — tracks your progress and gives points
- ✅ Contains **TWO networks** inside:
  - 🔵 **Initial Network** — opens when you launch the activity (what you work on)
  - 🔴 **Answer Network** — runs in the background (used for scoring/feedback)
- ✅ Shows **Completion Percentage** to track progress
- ✅ Has **Check Results** feature for instant feedback
- ❌ Learners **cannot access** the answer network

### When you see it:
Used in **labs, assignments, and assessments** on Cisco NetAcad.

### Example:
The **"Build a Small Network"** project was a `.pka` file — it had instructions on the left panel and gave a score of 4/4.

---

## 2️⃣ .pkt — Packet Tracer Network File

### Definition:
The `.pkt` file is created when you **build a simulated network in Packet Tracer and save it**. It is a plain network file with no scoring or instructions.

### Key Features:
- ✅ Saves your **network topology** (all devices and connections)
- ✅ Can have **graphic background images** embedded within it
- ❌ **No instructions window**
- ❌ **No activity scoring**
- ❌ No answer network

### When you use it:
- When you **create your own network from scratch**
- When you want to **save your practice work**
- For **personal projects and experiments**

### Example:
If you design a home network with a router, switch, and 3 PCs and save it — that saved file is a `.pkt` file.

---

## 3️⃣ .pksz — Packet Tracer Tutored Activity File

### Definition:
The `.pksz` file is specific to **Packet Tracer Tutored Activities (PTTA)**. It is a bundle that includes multiple components to provide a guided, hint-based learning experience.

### What it bundles:
| Component | Purpose |
|---|---|
| `.pka` file | The actual activity |
| Media assets | Images, icons, visual content |
| Scripting file | Powers the hinting system |

### Key Features:
- ✅ Provides **contextualized hints** to help students
- ✅ Designed to **support and guide** students through activities
- ✅ Includes the full `.pka` activity inside
- ✅ Best for **beginners** who need extra guidance

### When you see it:
Used in **Tutored Activities (PTTA)** — like the one in the previous module where you navigated the logical/physical interface.

### Key Difference from .pka:
| Feature | .pka | .pksz |
|---|---|---|
| Instructions | ✅ Yes | ✅ Yes |
| Scoring | ✅ Yes | ✅ Yes |
| Hints System | ❌ No | ✅ Yes |
| Media Assets | ❌ No | ✅ Yes |

---

## 4️⃣ .pkz — Deprecated File Type

### Definition:
The `.pkz` file type was **previously used** to embed images and other files inside a Packet Tracer file. It is now considered **deprecated** (outdated/no longer needed).

### Why it's deprecated:
> Images and files are now **embedded directly** within regular `.pkt` or `.pka` files by default — so `.pkz` is no longer necessary.

### Where you might still see it:
- In the **File menu → "Save As PKZ..."** option
- In very **old Packet Tracer files** from earlier versions

### Status: ⚠️ Deprecated — Avoid using this format

---

## 📊 Full Comparison Table

| Feature | .pka | .pkt | .pksz | .pkz |
|---|---|---|---|---|
| Instructions Window | ✅ Yes | ❌ No | ✅ Yes | ❌ No |
| Scoring / Graded | ✅ Yes | ❌ No | ✅ Yes | ❌ No |
| Answer Network | ✅ Yes (hidden) | ❌ No | ✅ Yes (hidden) | ❌ No |
| Hint System | ❌ No | ❌ No | ✅ Yes | ❌ No |
| Background Images | ✅ Yes | ✅ Yes | ✅ Yes | ✅ Yes |
| Media Assets | ❌ No | ❌ No | ✅ Yes | ❌ No |
| Current / Active | ✅ Yes | ✅ Yes | ✅ Yes | ⚠️ Deprecated |
| Best Used For | Activities & labs | Practice networks | Tutored activities | Old files only |

---

## 🧠 Quick Revision

| Question | Answer |
|---|---|
| Most common file type? | `.pka` |
| Which file has hints? | `.pksz` |
| Which file has NO instructions or scoring? | `.pkt` |
| Which file type is deprecated? | `.pkz` |
| What does "a" in .pka stand for? | Activity |
| How many networks does .pka contain? | 2 (initial + answer) |
| Can students see the answer network in .pka? | ❌ No |
| What does .pksz bundle? | .pka + media assets + scripting file |
| Why is .pkz deprecated? | Images now embed directly in .pkt/.pka |
| What is PTTA? | Packet Tracer Tutored Activity |

---

## 📌 Key Points to Remember

> ✅ `.pka` = most common — has instructions + scoring + 2 networks  
> ✅ `.pkt` = plain saved network — no instructions, no scoring  
> ✅ `.pksz` = tutored activity — includes hints to help learners  
> ✅ `.pkz` = old/deprecated — no longer needed  
> ✅ The **answer network** in `.pka` runs in the background — learners can't access it  
> ✅ **Completion percentage** is shown in `.pka` activity instructions window  
> ✅ `.pksz` is used for **PTTA** (Packet Tracer Tutored Activities)  

---

*📝 Notes by: Noor Ul Nisa | Cisco NetAcad | June 2026*
