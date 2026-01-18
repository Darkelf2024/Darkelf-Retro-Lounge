# AetherSX2 — Game Engine Categories & Stress Patterns (Part 7)  
## Why Different Games Stress the Emulator Differently  
*Darkelf Retro Lounge Documentation Series*

---

## Overview

This document categorizes common **PlayStation 2 game engine designs** and explains how each type stresses different subsystems within **AetherSX2**.

Understanding these stress patterns helps explain why certain games require **specific settings, renderers, or timing adjustments**, rather than assuming emulator-wide issues.

---

## 1. CPU-Heavy Logic Engines

These engines emphasize:

- Complex AI systems  
- Physics simulations  
- Extensive scripting logic  

They heavily tax the **Emotion Engine (EE)** and often benefit from:

- EE Cycle underclocking  
- MTVU when supported  

---

## 2. VU-Heavy Geometry Engines

These engines offload significant work to **VU1**, including:

- Geometry processing  
- Animation workloads  

They stress **vector processing and synchronization** and may exhibit instability when **Instant VU1** is enabled.

---

## 3. GS-Heavy Rendering Engines

These engines rely on:

- Heavy blending  
- Post-processing effects  
- High fill-rate usage  

They stress the **Graphics Synthesizer (GS)** and may expose **hardware renderer inaccuracies**.

---

## 4. Sprite-Based and 2D Engines

Sprite-based engines depend on:

- Strict draw ordering  
- Precise blending correctness  

They often require the software renderer to maintain correct draw ordering and blending accuracy.

---

## 5. Streaming Open-World Engines

Open-world engines continuously stream assets and rely on:

- Tight timing between subsystems  
- Stable performance over long sessions  

They are sensitive to:

- EE Cycle adjustments  
- Thermal throttling  

---

## Engine Stress Summary

| Engine Type | Primary Stress | Common Fixes |
|------------|--------------|--------------|
| Logic-Heavy | EE / CPU | EE Cycle -1, MTVU |
| VU-Heavy | VU1 Sync | Disable Instant VU1 |
| GS-Heavy | GPU / GS | Higher blending accuracy |
| Sprite / 2D | GS Ordering | Software Renderer |
| Open-World | Timing & Streaming | Balanced EE settings |

---

## Key Takeaway

> **Performance issues are often engine-specific rather than emulator-wide.**

Understanding engine stress patterns allows for **targeted, safer fixes** instead of blanket configuration changes.

---

**Darkelf Retro Lounge**  
*Preserving Accuracy • Testing Limits • Respecting Original Hardware*
