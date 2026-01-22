<p align="center">
  <img src="assets/darkelf-retro-lounge-banner.png" alt="Darkelf Retro Lounge" width="900">
</p>

# **Darkelf Retro Lounge**

**Darkelf Retro Lounge** is a PlayStation 2 emulation research and documentation project focused on **behavioral accuracy**, **timing consistency**, and **long-session stability** on real Android hardware.

The project centers on **AetherSX2** and **NetherSX2**, documenting how these emulators *actually behave during sustained gameplay* rather than relying on short benchmarks, unsafe “FPS boost” configurations, or unverifiable performance claims.

Testing emphasizes:

* Real-device behavior
* Long play sessions
* Explainable emulator configuration choices
* Observable correctness in timing, logic, audio, and input

> **FPS ≠ accuracy.
> Behavior defines correctness.**

---

## 📌 Project Scope

This repository documents:

* Testing data for **200+ PS2 games** on AetherSX2 / NetherSX2
  👉 [PS2 Game Lists](https://github.com/Darkelf2024/PS2-Playable-Lists-for-AetherSX2-NetherSX2/tree/main)
* Emulator behavior comparisons across AetherSX2, NetherSX2, and related builds
* Technical documentation explaining *why* emulator settings exist and *how* they affect correctness

### Current Status

* Active testing in progress
* Documentation and lists are continuously refined
* Corrections are ongoing as new behavior is validated
* No executable code yet (documentation-first project)

### Notes

* No copyrighted game files are shared
* All documentation is publicly available
* Discussion, contributions, and updates are coordinated via Discord

---

## 📑 Table of Contents

* [🎯 Project Goals](#-project-goals)
* [📚 AetherSX2 Documentation Series](#-aethersx2-documentation-series)
* [📱 PS2 Compatibility & Playability Lists](#-ps2-compatibility--playability-lists)
* [🛠️ Companion Tool — Darkelf ROM Detector](#️-companion-tool--darkelf-rom-detector)
* [📖 Additional Technical References](#-additional-technical-references)
* [📝 Darkelf Retro Blog](https://github.com/Darkelf2024/Darkelf-Retro-Lounge/wiki)
* [🧠 Darkelf Philosophy](#-darkelf-philosophy)
* [📌 About Darkelf Retro Lounge](#-about-darkelf-retro-lounge)
* [👤 About the Author](About.md)
* [🧩 Version Comparison](Version%20Comparison.md)
* [📘 Darkelf Lounge Definitions List](Darkelf%20Lounge%20Definitions%20List.md)
* [🌍 Notice for Non-Native English Speakers](Notice%20Non-Native%20English%20Speakers.md)
* [📚 References](https://github.com/Darkelf2024/Darkelf-Retro-Lounge/blob/main/REFERENCES.md)
* [🎨 Performance Overlay Color Indicators](https://github.com/Darkelf2024/Darkelf-Retro-Lounge/blob/main/Overlay_Color_Indicators_with_FAQ_and_References.md)

---

## 🎯 Project Goals

Darkelf Retro Lounge prioritizes:

* ✅ Correct emulation behavior
* ✅ Long-session stability
* ✅ Safe, explainable configuration choices
* ✅ Transparent and repeatable testing methodology

And explicitly rejects:

* ❌ FPS-only compatibility claims
* ❌ Unsafe speed-hack myths
* ❌ One-size-fits-all configuration advice

---

## 📚 AetherSX2 Documentation Series

The **AetherSX2 Documentation Series** is a structured technical reference explaining:

* **Why** emulator settings exist
* **When** they should be used
* **How** they affect correctness, timing, and stability

Each document builds on the previous one to form a complete understanding of emulator behavior.

### 1️⃣ BIOS & Region Behavior

👉 [AetherSX2 BIOS Region](https://github.com/Darkelf2024/Darkelf-Retro-Lounge/blob/main/BIOS%20Region.md)

Explains BIOS region differences, boot behavior, and compatibility impact.

---

### 2️⃣ CPU vs GPU Responsibilities

👉 [AetherSX2 CPU vs GPU](https://github.com/Darkelf2024/Darkelf-Retro-Lounge/blob/main/AetherSX2%20CPU%20VS%20GPU.md)

Details EE, VU, and GS responsibilities and why GPU power alone does not ensure accuracy.

---

### 3️⃣ EE Cycle Rate, Cycle Skip, MTVU & Instant VU1

👉 [AetherSX2 EE Cycle Explained](https://github.com/Darkelf2024/Darkelf-Retro-Lounge/blob/main/AetherSX2%20EE%20Cycle%20Explained.md)

Explains when performance options help — and when they silently break timing, logic, or physics.

---

### 4️⃣ Software vs Hardware Renderer

👉 [AetherSX2 Software vs Hardware Renderer](https://github.com/Darkelf2024/Darkelf-Retro-Lounge/blob/main/AetherSX2%20Software%20vs%20Hardware%20Render.md)

Covers renderer selection and common accuracy pitfalls.

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

Classifies PS2 engines by CPU, VU, GS, and streaming stress characteristics.

---

### 8️⃣ Known Broken Combinations & Emulator Myths

👉 [AetherSX2 Known Broken Combinations](https://github.com/Darkelf2024/Darkelf-Retro-Lounge/blob/main/AetherSX2%20Known%20Broken%20Combinations.md)

Documents unsafe configuration myths and broken setting combinations.

---

### 9️⃣ Android SoC Behavior

👉 [AetherSX2 Android SoC Behavior](https://github.com/Darkelf2024/Darkelf-Retro-Lounge/blob/main/AetherSX2%20Android%20SoC%20Behavior.md)

Explains sustained performance limits beyond synthetic benchmarks.

---

## 📱 PS2 Compatibility & Playability Lists

Compatibility and playability lists are based on:

* Real hardware testing
* Long-session validation
* Accuracy-first configuration

Individual game titles are intentionally excluded from this README and maintained in dedicated repositories.

---

## 🛠️ Companion Tool — Darkelf ROM Detector

**Darkelf ROM Detector** is a companion analysis tool that:

* Analyzes ROM metadata and engine characteristics
* Suggests *safe* EE Cycle Rate and Cycle Skip ranges
* Accounts for device class and sustained performance limits

The tool **supports** testing — it does not replace per-game validation.

---

## 📖 Additional Technical References

These documents expand on real-world behavior, configuration tradeoffs, and commonly misunderstood emulator features. They complement — but do not replace — the core documentation series.

### 🔹 NetherSX2 Black — Real-World Results

👉 [NetherSX2 Black Real World Results](https://github.com/Darkelf2024/Darkelf-Retro-Lounge/blob/main/NetherSX2%20Black%20Real%20World%20Results.md)

Documents sustained gameplay behavior, stability, and accuracy observations specific to NetherSX2 Black builds.

---

### 🔹 Blending Accuracy vs Performance

👉 [Blending Accuracy vs Performance](https://github.com/Darkelf2024/Darkelf-Retro-Lounge/blob/main/Blending_Accuracy_vs_Performance.md)

Explains why performance tuning must remain constrained by behavioral correctness, not FPS targets.

---

### 🔹 Audio Async Mix vs TimeStretch

👉 [Audio Async Mix vs TimeStretch](https://github.com/Darkelf2024/Darkelf-Retro-Lounge/blob/main/Audio_Async_Mix_vs_TimeStretch.md)

Details how audio synchronization strategies affect timing stability, pitch behavior, and long-session correctness.

---

### 🔹 Affinity Control — Disabled vs Performance

👉 [Affinity Control Disabled vs Performance](https://github.com/Darkelf2024/Darkelf-Retro-Lounge/blob/main/Affinity_Control_Disabled_vs_Performance.md)

Explains why CPU affinity controls may improve short-term metrics while degrading sustained stability.

---

### 🔹 AetherSX2 & NetherSX2 — Theory vs Real World

👉 [AetherSX2 NetherSX2 Theory vs Real World](https://github.com/Darkelf2024/Darkelf-Retro-Lounge/blob/main/AetherSX2_NetherSX2_Theory_vs_Real_World.md)

Contrasts emulator theory, assumptions, and online advice with observed behavior on real Android hardware.

---

## 🧠 Darkelf Philosophy

Darkelf Retro Lounge promotes:

* Emulator correctness over perceived speed
* Stability over time
* Per-game understanding
* Transparent, explainable documentation

It explicitly rejects copy-paste settings, FPS-only claims, and short-form benchmark testing.

---

## 📌 About Darkelf Retro Lounge

Darkelf Retro Lounge is a long-term documentation and testing effort for:

* Emulator users who value correctness
* Developers and testers
* Retro gaming enthusiasts seeking stable, explainable emulation

If you care about **how emulation actually works**, you’re in the right place.

**Accuracy is not a checkbox.
Stability is not a benchmark.
Behavior is the metric.**

## License

All original documentation and writing in this repository is licensed under
the Creative Commons Attribution 4.0 International License (CC BY 4.0),
unless otherwise noted.

