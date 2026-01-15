## Darkelf Retro Lounge 

This is a PlayStation 2 emulation research and documentation project focused on cycle-level considerations and behavioral accuracy, with specific emphasis on AetherSX2 and NetherSX2 on Android.

The project documents how AetherSX2 and NetherSX2 behave on real Android hardware through sustained play testing and behavior-based validation—not short benchmarks, unsafe “FPS boost” configurations, or unverified performance claims. Findings prioritize correctness, long-session stability, and explainable configuration choices grounded in emulator internals.

In this project, accuracy refers to correct observed emulator behavior: timing consistency, game logic, audio synchronization, and input response as experienced during extended gameplay on real devices. It does not claim or imply full cycle-accurate PS2 hardware emulation, nor does it guarantee full-speed or universally stable performance on constrained hardware.

The project is informed by decades of hands-on testing experience, including professional beta testing and firmware evaluation for retro gaming platforms. This background underpins a strict testing methodology and a deliberate rejection of unsafe, misleading, or performance-only emulator practices.

FPS ≠ accuracy. Behavior defines correctness.

---

## 📌 Project Scope

This repository will hold:
- Testing data for 200+ PS2 games on AetherSX2\NetherSX2  [PS2 GAME LISTS HERE](https://github.com/Darkelf2024/PS2-Playable-Lists-for-AetherSX2-NetherSX2/tree/main)
- Compatibility comparisons with NetherSX and related builds  
- Documentation explaining emulator behavior and testing metrics  

**Current Status:**  
🔧 Testing in progress on AetherSX2/NetherSX2
🧠 Results and documentation evolving - work in progress & corrections being made!
📌 No executable code yet  

**Notes:**  
- No copyrighted game files are shared  
- All releases are published publicly  

Contributing, discussions, and updates are tracked in the Discord server.

---

## 📑 Table of Contents

- [🎯 Project Goals](#-project-goals)
- [📚 AetherSX2 Documentation Series](#-aethersx2-documentation-series)
- [📱 PS2 Compatibility & Playability Lists](#-ps2-compatibility--playability-lists)
- [🛠️ Companion Tool — Darkelf ROM Detector](#️-companion-tool--darkelf-rom-detector)
- [🧠 Darkelf Philosophy](#-darkelf-philosophy)
- [📌 About Darkelf Retro Lounge](#-about-darkelf-retro-lounge)
- [👤 About the Author](About.md)
- [🧩 Version Comparison](Version%20Comparison.md)


---

## 🎯 Project Goals

Darkelf Retro Lounge prioritizes:

- ✅ Correct emulation behavior  
- ✅ Long-session stability  
- ✅ Safe, explainable configuration choices  
- ✅ Transparent testing methodology  

And explicitly rejects:

- ❌ FPS-only compatibility claims  
- ❌ Unsafe speed-hack myths  
- ❌ One-size-fits-all settings  

---

## 📚 AetherSX2 Documentation Series

The **AetherSX2 Documentation Series** is a structured technical reference explaining *why* emulator settings exist, *when* they should be used, and *how* they affect correctness.

Each document builds on the previous one to form a complete understanding of AetherSX2 behavior.

### 1️⃣ BIOS & Region Behavior  
👉 [AetherSX2 BIOS Region](https://github.com/Darkelf2024/Darkelf-Retro-Lounge/blob/main/BIOS%20Region.md)

Covers BIOS region differences, boot behavior, and compatibility impact.

---

### 2️⃣ CPU vs GPU Responsibilities  
👉 [AetherSX2 CPU vs GPU](https://github.com/Darkelf2024/Darkelf-Retro-Lounge/blob/main/AetherSX2%20CPU%20VS%20GPU.md)

Explains EE, VU, and GS responsibilities and why GPU power alone does not guarantee accuracy.

---

### 3️⃣ EE Cycle Rate, Cycle Skip, MTVU & Instant VU1  
👉 [AetherSX2 EE Cycle Explained](https://github.com/Darkelf2024/Darkelf-Retro-Lounge/blob/main/AetherSX2%20EE%20Cycle%20Explained.md)

Details when performance settings help — and when they silently break timing, logic, or physics.

---

### 4️⃣ Software vs Hardware Renderer  
👉 [AetherSX2 Software vs Hardware Renderer](https://github.com/Darkelf2024/Darkelf-Retro-Lounge/blob/main/AetherSX2%20Software%20vs%20Hardware%20Render.md)

Explains renderer selection and common accuracy pitfalls.

---

### 5️⃣ Thermals & Sustained Performance  
👉 [AetherSX2 Thermals and Performance](https://github.com/Darkelf2024/Darkelf-Retro-Lounge/blob/main/AetherSX2%20Thermals%20and%20Performance.md)

Focuses on real-world Android behavior, sustained clocks, and thermal throttling.

---

### 6️⃣ Testing Methodology & Validation  
👉 [AetherSX2 Testing Methodology](https://github.com/Darkelf2024/Darkelf-Retro-Lounge/blob/main/AetherSX2%20Testing%20Methodology.md)

Defines long-session testing, scenario coverage, and validation standards.

---

### 7️⃣ Game Engine Stress Patterns  
👉 [AetherSX2 Game Engine Categories](https://github.com/Darkelf2024/Darkelf-Retro-Lounge/blob/main/AetherSX2%20Game%20Engine%20Categories.md)

Classifies PS2 engines by CPU, VU, GS, and streaming stress patterns.

---

### 8️⃣ Known Broken Combinations & Emulator Myths  
👉 [AetherSX2 Known Broken Combinations](https://github.com/Darkelf2024/Darkelf-Retro-Lounge/blob/main/AetherSX2%20Known%20Broken%20Combinations.md)

Documents unsafe configuration myths and broken setting combinations.

---

### 9️⃣ Android SoC Behavior  
👉 [AetherSX2 Android SoC Behavior](https://github.com/Darkelf2024/Darkelf-Retro-Lounge/blob/main/AetherSX2%20Android%20SoC%20Behavior.md)

Explains sustained performance limits and SoC-specific behavior beyond synthetic benchmarks.

---

## 📱 PS2 Compatibility & Playability Lists

Compatibility and playability lists are maintained separately and are based on:
- Real hardware testing  
- Long-session validation  
- Accuracy-first configuration  

Individual game titles are intentionally excluded from this README.

---

## 🛠️ Companion Tool — Darkelf ROM Detector

**Darkelf ROM Detector** is a companion analysis tool that:
- Analyzes ROM metadata and engine patterns  
- Suggests safe EE Cycle Rate and Cycle Skip values  
- Accounts for device class and sustained performance  

The tool complements — but does not replace — per-game validation.

---

## 🧠 Darkelf Philosophy

Darkelf Retro Lounge promotes:
- Emulator correctness  
- Stability over time  
- Per-game understanding  
- Explainable documentation  

And rejects copy-paste settings, FPS-only claims, and short benchmark testing.

---

## 📌 About Darkelf Retro Lounge

Darkelf Retro Lounge is a long-term documentation and testing effort for:
- Emulator users who value correctness  
- Developers and testers  
- Retro gaming enthusiasts seeking stable, accurate emulation  

If you care about **how emulation actually works**, you’re in the right place.

> **FPS ≠ accuracy. Behavior defines correctness.**
