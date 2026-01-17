# 🎨 Performance Overlay Color Indicators (Red / White / Green)

This document explains the **color changes** observed in the emulator performance overlay (AetherSX2 / NetherSX2-style HUD) and how they relate to **timing behavior**, not raw frame rate.

These indicators are intended as **real-time diagnostics**, not absolute measures of accuracy. They should be understood as *signals of internal timing state* rather than judgments of playability or correctness.

---

## 🟢 Green — Stable Timing State

**Green text indicates:**
- Emulated timing is **within expected tolerance**
- Frame pacing is currently stable
- No immediate synchronization warnings are detected

### What Green means
- The emulator considers the current workload **well-balanced**
- EE, VU, and GS workloads are being serviced without visible overruns
- Audio and video timing are aligned at that moment
- CPU scheduling and thermal conditions are not currently limiting execution

### What Green does *not* guarantee
- Full cycle-accurate emulation
- Long-session determinism
- Absence of rare logic or physics drift

Green reflects a **momentary stable state**, not a permanent guarantee of correctness.

> **Important clarification:**  
> Green does *not* mean “exactly 100% speed.”  
> It means the emulator currently has **timing headroom** and is not missing deadlines.  
> That headroom can allow the reported speed to temporarily exceed 100% (for example, 120–130%) without indicating improved accuracy.

---

## ⚪ White — Neutral / Acceptable Timing State

**White text indicates:**
- Timing is **within acceptable limits**, but not ideal
- Minor execution or pacing fluctuations are occurring
- The emulator has **not crossed warning thresholds**

### Why White appears
- Natural scene-to-scene workload variation
- Short EE or VU execution spikes
- Streaming assets or scripted camera transitions
- Mild thermal throttling or OS scheduling variance (common on Android)

White is the **most common real-world state** during normal gameplay.

### Key clarification
White does **not** mean “nothing is happening” or “perfect accuracy.”  
It means **the emulator is tolerating current variance without flagging stress**.

---

## 🔴 Red — Timing Stress / Warning State

**Red text indicates:**
- One or more internal timing thresholds have been exceeded
- Frame pacing instability has been detected
- Emulator workload is temporarily unsustainable

### Common causes
- Heavy EE or VU microcode bursts
- Cutscenes, streaming-heavy sections, or scripted events
- Thermal throttling reducing sustained clocks
- Aggressive speedhack settings (EE Cycle Rate / Cycle Skip)
- CPU contention or background load on mobile devices

### Important clarification
Red does **not always mean low FPS**.

A game may:
- Appear visually smooth
- Maintain near-100% reported speed
- Still trigger red due to **timing deviation or missed scheduling windows**

Red is a **timing warning**, not a failure indicator.

---

## 🎯 Why Colors Change During Gameplay

Color changes are **dynamic and expected** because:
- PS2 engines are highly burst-driven
- Different subsystems (EE, VU0, VU1, GS) are stressed unevenly
- Emulated workloads are non-uniform by design
- Modern mobile SoCs constantly adjust clocks and scheduling

This is why **short benchmarks are misleading** and **long-session testing is required** to understand real behavior.

---

## 🧠 Accuracy-First Interpretation

Overlay colors should be interpreted as:

- **Green** → Stable at this moment  
- **White** → Acceptable, fluctuating  
- **Red** → Timing stress detected  

They reflect **observable emulator timing behavior**, not correctness guarantees.

---

## ❓ FAQ — Performance Overlay Color Indicators

### Does green mean the emulator is fully accurate?
No. Green only indicates that current timing is within tolerance. Accuracy requires sustained validation over time, not a single stable moment.

### Does red mean the game is broken or unplayable?
No. Red highlights timing stress. Many games continue to function correctly despite transient red states, especially during heavy scenes.

### Why does the color change even when FPS looks stable?
Because FPS measures output frames, not internal timing. The overlay reacts to execution variance, synchronization, and pacing, which FPS alone cannot reveal.

### Why is white so common?
White reflects realistic execution variance. Real PS2 workloads are not uniform, and emulation on modern systems introduces additional scheduling noise.

### Can overlay colors be used as proof of correctness?
No. They are **diagnostic tools**, not validation metrics. Correctness must be evaluated through behavior, timing consistency, and long-session testing.

---

## 📚 Supporting References & Rationale

The interpretation of overlay color indicators aligns with established emulator and real-time system principles:

- **PCSX2 Development Team** — Official documentation and developer guidance emphasize that reported speed and FPS do not equate to correct timing or synchronization.  
  https://pcsx2.net

- **Copetti, R.** — *PlayStation 2 Architecture: A Practical Analysis*  
  Explains the burst-driven, multi-unit nature of PS2 workloads and why timing variance is intrinsic to the system.  
  https://www.copetti.org/writings/consoles/playstation-2/

- **Bridges, P. G., et al. (2012).** *Virtual-machine-based emulation of future generation high-performance computing systems.*  
  Demonstrates how emulation often trades strict timing accuracy for practicality, even when output appears correct.  
  https://doi.org/10.1177/1094342012436619

- **Staelens, N., et al. (2012).** *Assessing the importance of audio/video synchronization for video sequences.*  
  Establishes perceptual and technical thresholds for A/V sync independent of frame rate.  
  https://doi.org/10.1007/s00530-012-0262-4

---

## 📌 Summary

- Overlay colors represent **timing state**, not FPS
- Color changes are **expected and normal**
- White is the most common real-world condition
- Red indicates stress, not automatic failure
- Only **extended, behavior-based testing** reveals true stability

**FPS ≠ accuracy  
Color ≠ correctness  
Behavior defines reality**
