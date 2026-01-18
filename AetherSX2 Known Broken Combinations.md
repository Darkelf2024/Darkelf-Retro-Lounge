# AetherSX2 — Known Broken Combinations & Emulator Myths  
### Part 8 · Darkelf Retro Lounge Documentation Series

## What *Not* to Enable Together — and Why

This document catalogs **commonly reported “fixes”** that actually introduce **instability, accuracy loss, or broken gameplay** in AetherSX2.  
It also addresses **persistent emulator myths** that continue to circulate despite repeated testing evidence.

The goal is simple:  
**preserve correctness, timing, and long-session stability** over misleading short-term gains.

---

## 1. Broken or Risky Setting Combinations

Certain emulator settings interact in ways that **compound inaccuracies** instead of solving performance problems.  
While some combinations may temporarily raise FPS, they often **silently break game logic**.

### ⚠️ Known Problematic Combinations

| Combination | Why It Breaks |
|------------|--------------|
| **Instant VU1 + EE Cycle Skip** | Destroys timing determinism and breaks logic execution |
| **EE Cycle Rate -3 + Frame Skipping** | Breaks physics, cutscenes, and scripted events |
| **Global Software Renderer** | Global Software Renderer — Causes severe CPU overload on most Android devices; intended only for specific titles that require exact GS behavior |
| **Overclock + Speed Hacks** | Accelerates game logic unpredictably |
| **MTVU + Aggressive EE Undercycle** | Causes thread desynchronization in timing-sensitive titles |

**Key takeaway:**  
> Instant gains without trade-off analysis usually indicate correctness loss — unless validated through consistency tests.

---

## 2. Common Emulator Myths

Many configuration myths persist due to **misunderstanding emulator internals**, or by applying **desktop PCSX2 advice directly to Android**.

### ❌ Common False Assumptions

- “Overclocking always improves performance”
- “Vulkan automatically fixes accuracy issues”
- “Higher FPS means better emulation”
- “Speed hacks are safe if the game looks fine”
- “Global settings work for all games”

These assumptions are **frequently disproven** during extended play sessions.

---

## 3. Why These Myths Persist

Several factors contribute to ongoing misinformation:

- Short benchmark testing instead of full playthroughs
- Settings copied from outdated guides or PC configurations
- FPS-focused videos without logic or stability validation
- Lack of understanding of EE/VU timing dependencies

Emulation correctness cannot be evaluated in **five-minute test runs**.

---

## 4. Safe Configuration Philosophy

Stable emulation comes from **minimal, targeted changes**, not stacked hacks.

### ✅ Best Practices

- Avoid global speed hacks
- Tune **per-game**, not per-emulator
- Prefer default timing unless instability is proven
- Validate through **long-session gameplay**
- Prioritize logic correctness over raw FPS

> **Higher FPS does not equal correct emulation.**

---

## Final Takeaway

**Accuracy is cumulative.**  
Stacking hacks, skips, and overrides may appear beneficial at first — but they almost always introduce subtle or catastrophic failures later.

**Trust long-session stability over short-term gains.**

---

### Darkelf Retro Lounge  
*Preserving Accuracy · Testing Limits · Respecting Original Hardware*
