# 🎮 Darkelf Retro Lounge  
## AetherSX2 Accuracy-First Documentation & Compatibility Project

**Darkelf Retro Lounge** is an accuracy-first PlayStation 2 emulation research and documentation project created by **Dr. Kevin Moore**, dedicated to **AetherSX2 on Android**.

This project documents **how AetherSX2 actually behaves on real hardware** — not myths, unsafe “FPS boost” settings, or short benchmark runs. All findings are grounded in sustained testing, emulator internals, and behavior-based validation, with a focus on correctness, long-session stability, and explainable configuration choices.

Dr. Moore brings decades of hands-on testing experience, including work as a **hired beta tester for the MMORPG *Neocron* (2001–2002)** and as a **beta tester for *MuOS* custom firmware for retro gaming devices**. This background informs Darkelf Retro Lounge’s strict testing methodology and rejection of unsafe emulator myths.

> **FPS ≠ accuracy. Behavior defines correctness.**

**Retro emulation testing and compatibility research**

This repository will hold:
- Testing data for ~200 PS2 games on AetherSX2
- Compatibility comparisons vs NetherSX and other builds
- Documentation and explanations of testing metrics

**Current Status:**  
🔧 Testing in progress on AetherSX2  
🧠 Results and documentation pending  
📌 No executable code yet

**Purpose:**  
Provide structured, transparent emulation research and compatibility insights.

**Notes:**  
- No copyrighted game files are shared here  
- All releases will be published publicly

Contributing, discussions, and updates are tracked in the Discord server.

---

## 📑 Table of Contents

- [🎯 Project Goals](#-project-goals)
- [📚 AetherSX2 Documentation Series](#-aethersx2-documentation-series)
  - [1️⃣ BIOS & Region Behavior](#1️⃣-bios--region-behavior)
  - [2️⃣ CPU vs GPU Responsibilities](#2️⃣-cpu-vs-gpu-responsibilities)
  - [3️⃣ EE Cycle Rate, Cycle Skip, MTVU & Instant VU1](#3️⃣-ee-cycle-rate-cycle-skip-mtvu--instant-vu1)
  - [4️⃣ Software vs Hardware Renderer](#4️⃣-software-vs-hardware-renderer)
  - [5️⃣ Thermals & Sustained Performance](#5️⃣-thermals--sustained-performance)
  - [6️⃣ Testing Methodology & Validation](#6️⃣-testing-methodology--validation)
  - [7️⃣ Game Engine Stress Patterns](#7️⃣-game-engine-stress-patterns)
  - [8️⃣ Known Broken Combinations & Emulator Myths](#8️⃣-known-broken-combinations--emulator-myths)
  - [9️⃣ Android SoC Behavior](#9️⃣-android-soc-behavior)
- [📱 PS2 Compatibility & Playability Lists](#-ps2-compatibility--playability-lists)
- [🛠️ Companion Tool — Darkelf ROM Detector](#️-companion-tool--darkelf-rom-detector)
- [🧠 Darkelf Philosophy](#-darkelf-philosophy)
- [📌 About Darkelf Retro Lounge](#-about-darkelf-retro-lounge)

---

## 🎯 Project Goals

Darkelf Retro Lounge prioritizes:

- ✅ Correct emulation behavior  
- ✅ Long-session stability  
- ✅ Safe, explainable configuration choices  
- ✅ Transparent testing methodology  

And explicitly rejects:

- ❌ Unsafe speed-hack myths  
- ❌ FPS-only compatibility claims  
- ❌ “One-size-fits-all” settings  

---

## 📚 AetherSX2 Documentation Series  
### (Darkelf Retro Lounge)

The **AetherSX2 Documentation Series** is a structured, multi-part technical reference explaining *why* emulator settings exist, *when* they should be used, and *how* they affect correctness.

Each document builds on the previous one, forming a complete understanding of AetherSX2 behavior.

---

### 1️⃣ BIOS & Region Behavior

**Documentation:**  
👉 [AetherSX2 BIOS Region](https://github.com/Darkelf2024/Darkelf-Retro-Lounge/blob/main/BIOS%20Region.md)

Explains:
- BIOS region differences  
- Boot behavior and timing  
- When region choice impacts compatibility  

---

### 2️⃣ CPU vs GPU Responsibilities

**Documentation:**  
👉 [AetherSX2 CPU vs GPU](https://github.com/Darkelf2024/Darkelf-Retro-Lounge/blob/main/AetherSX2%20CPU%20VS%20GPU.md)

Covers:
- Emotion Engine (EE) behavior  
- Vector Unit (VU) workload  
- Graphics Synthesizer (GS) responsibilities  

Clarifies why GPU power alone does **not** guarantee performance or accuracy.

---

### 3️⃣ EE Cycle Rate, Cycle Skip, MTVU & Instant VU1

**Documentation:**  
👉 [AetherSX2 EE Cycle Explained](https://github.com/Darkelf2024/Darkelf-Retro-Lounge/blob/main/AetherSX2%20EE%20Cycle%20Explained.md)

A deep technical breakdown of:
- EE Cycle Rate  
- EE Cycle Skip  
- MTVU threading  
- Instant VU1  

Explains when these settings help performance — and when they silently break logic, physics, or timing.

---

### 4️⃣ Software vs Hardware Renderer

**Documentation:**  
👉 [AetherSX2 Software vs Hardware Renderer](https://github.com/Darkelf2024/Darkelf-Retro-Lounge/blob/main/AetherSX2%20Software%20vs%20Hardware%20Render.md)

Explains:
- When software rendering is required  
- Why hardware rendering can break effects  
- How to safely choose a renderer per game  

---

### 5️⃣ Thermals & Sustained Performance

**Documentation:**  
👉 [AetherSX2 Thermals Sustained Performance](https://github.com/Darkelf2024/Darkelf-Retro-Lounge/blob/main/AetherSX2%20Thermals%20Sustained%20Performance.md)

Focuses on real Android behavior:
- Thermal throttling  
- Sustained clocks vs burst performance  
- Why short tests are misleading  

---

### 6️⃣ Testing Methodology & Validation

**Documentation:**  
👉 [AetherSX2 Testing Methodology](https://github.com/Darkelf2024/Darkelf-Retro-Lounge/blob/main/AetherSX2%20Testing%20Methodology%20Validation.md)

Defines how Darkelf Retro Lounge evaluates games:
- Long play sessions  
- Multiple gameplay scenarios  
- Stability over time  
- Behavior consistency  

This methodology underpins all compatibility claims.

---

### 7️⃣ Game Engine Stress Patterns

**Documentation:**  
👉 [AetherSX2 Game Engine Categories](https://github.com/Darkelf2024/Darkelf-Retro-Lounge/blob/main/AetherSX2%20Game%20Engine%20Categories.md)

Classifies PS2 engines based on:
- CPU load  
- VU stress  
- GS behavior  
- Streaming demands  

Explains why different games require different configuration strategies.

---

### 8️⃣ Known Broken Combinations & Emulator Myths

**Documentation:**  
👉 [AetherSX2 Known Broken Combinations](https://github.com/Darkelf2024/Darkelf-Retro-Lounge/blob/main/AetherSX2%20Known%20Broken%20Combinations%20Myths.md)

Documents unsafe myths such as:
- “Universal best settings”  
- Aggressive cycle skipping  
- Stacked speed hacks that break gameplay  

---

### 9️⃣ Android SoC Behavior

**Documentation:**  
👉 [AetherSX2 Android SoC Behavior](https://github.com/Darkelf2024/Darkelf-Retro-Lounge/blob/main/AetherSX2%20Android%20SoC%20Behavior.md)

Explains how Android SoCs behave under AetherSX2, focusing on:
- Sustained performance  
- CPU architecture limits  
- GPU driver behavior  

Rather than synthetic benchmarks.

---

## 📱 PS2 Compatibility & Playability Lists

Darkelf Retro Lounge maintains **separate PS2 compatibility and playability lists** for AetherSX2.

📄 **Important:**
- Individual game lists are maintained in a **separate file**
- This README intentionally does **not** list individual titles  

Compatibility is determined by:
- Real hardware testing  
- Long-session validation  
- Accuracy-first configuration choices  

Games are evaluated on **correctness and stability**, not raw FPS.

---

## 🛠️ Companion Tool — Darkelf ROM Detector

**Darkelf ROM Detector** is an accuracy-first analysis tool designed to complement this documentation.

It:
- Analyzes ROM filenames and engine load patterns  
- Suggests safe EE Cycle Rate and Cycle Skip values  
- Accounts for device class and sustained performance  
- Avoids dangerous configuration recommendations  

The tool follows the same philosophy as this project.

---

## 🧠 Darkelf Philosophy

Darkelf Retro Lounge rejects:
- Copy-paste “best settings”  
- FPS-only compatibility claims  
- Unsafe emulator myths  
- Short benchmark testing  

Instead, it promotes:
- Emulator correctness  
- Stability over time  
- Per-game understanding  
- Clear, explainable documentation  

---

## 📌 About Darkelf Retro Lounge

Darkelf Retro Lounge is a long-term documentation and testing effort built for:
- Emulator users who value correctness  
- Developers and testers  
- Retro gaming enthusiasts who want stable, accurate emulation  

If you care about **how emulation actually works**, you’re in the right place.

> **FPS ≠ accuracy. Behavior defines correctness.**
