# 🎮 Darkelf Retro Lounge  
## AetherSX2 Accuracy-First Documentation & Compatibility Project

**Darkelf Retro Lounge** is an accuracy-focused PlayStation 2 emulation research and documentation project dedicated to **AetherSX2 on Android**.

This project exists to document **how AetherSX2 actually behaves** on real hardware — not myths, unsafe “FPS boost” settings, or short benchmark runs. Every conclusion is grounded in sustained testing, emulator internals, and behavior validation.

> **FPS ≠ accuracy. Behavior defines correctness.**

---

## 🎯 Project Goals

Darkelf Retro Lounge prioritizes:

- ✅ Correct emulation behavior  
- ✅ Long-session stability  
- ✅ Safe, explainable configuration choices  
- ✅ Transparent testing methodology  
- ❌ No unsafe speed-hack myths  
- ❌ No “one-size-fits-all” settings  

---

## 📚 AetherSX2 Documentation Series  
### (Darkelf Retro Lounge)

The **AetherSX2 Documentation Series** is a structured, multi-part technical reference that explains *why* emulator settings exist, *when* they should be used, and *how* they affect correctness.

Each document builds on the previous one, forming a complete understanding of AetherSX2 behavior.

---

### 1️⃣ BIOS & Region Behavior  
Explains:
- BIOS region differences  
- Boot behavior and timing  
- When region choice impacts compatibility  

---

### 2️⃣ CPU vs GPU Responsibilities  
Covers:
- Emotion Engine (EE) behavior  
- Vector Unit (VU) workload  
- Graphics Synthesizer (GS) responsibilities  

Clarifies why GPU power alone does **not** guarantee performance or accuracy.

---

### 3️⃣ EE Cycle Rate, Cycle Skip, MTVU & Instant VU1  
A deep technical breakdown of:
- EE Cycle Rate  
- EE Cycle Skip  
- MTVU threading  
- Instant VU1  

Explains when these settings help performance — and when they silently break logic, physics, or timing.

---

### 4️⃣ Software vs Hardware Renderer  
Details:
- When software rendering is required  
- Why hardware rendering can break effects  
- How to safely choose a renderer per game  

---

### 5️⃣ Thermals & Sustained Performance  
Focuses on real Android behavior:
- Thermal throttling  
- Sustained clocks vs burst performance  
- Why short tests are misleading  

---

### 6️⃣ Testing Methodology & Validation  
Defines how Darkelf Retro Lounge evaluates games:
- Long play sessions  
- Multiple gameplay scenarios  
- Stability over time  
- Behavior consistency  

This methodology underpins all compatibility claims.

---

### 7️⃣ Game Engine Stress Patterns  
Classifies PS2 engines based on:
- CPU load  
- VU stress  
- GS behavior  
- Streaming demands  

Explains why different games require different configuration strategies.

---

### 8️⃣ Known Broken Combinations & Emulator Myths  
Documents unsafe myths such as:
- “Universal best settings”  
- Aggressive cycle skipping  
- Stacked speed hacks that break gameplay  

---

### 9️⃣ Android SoC Behavior  
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
- Analyzes ROM filenames and load patterns  
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

---

**FPS ≠ accuracy.  
Behavior defines correctness.**
