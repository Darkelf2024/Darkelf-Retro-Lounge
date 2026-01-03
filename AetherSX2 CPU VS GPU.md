# AetherSX2 — CPU vs GPU Usage (Part 2)  
**Darkelf Retro Lounge Documentation Series**

---

## Overview

This document explains how **CPU and GPU resources** are utilized during **PlayStation 2 emulation in AetherSX2**.

It demonstrates why **CPU performance remains the dominant factor** in emulation accuracy and stability, while **GPU performance primarily affects visual fidelity**.

:contentReference[oaicite:0]{index=0}

---

## 1. Why PlayStation 2 Emulation Is CPU-Centric

The original PlayStation 2 relied on **tight parallel execution** between:

- Emotion Engine (EE)
- Vector Units (VU0 / VU1)
- Graphics Synthesizer (GS)

In emulation, this behavior must be reconstructed in software with **precise synchronization**, placing significant demands on the CPU.

---

## 2. CPU Responsibilities in AetherSX2

The CPU is responsible for emulating:

- Game logic
- Physics calculations
- Artificial intelligence
- Audio timing
- DMA transfers
- Inter-processor synchronization

**Single-core performance and instruction throughput** are more important than raw core count.

Many problems commonly blamed on GPU limitations are actually **CPU scheduling or synchronization bottlenecks**.

---

## 3. GPU Responsibilities in AetherSX2

The GPU handles rendering-related tasks, including:

- Resolution scaling
- Texture filtering
- Blending accuracy
- Post-processing effects

A stronger GPU allows higher resolutions and better visual output, but **cannot compensate for insufficient CPU performance**.

---

## 4. Common Bottleneck Scenarios

| Hardware Balance | Result |
|-----------------|--------|
| Strong CPU + Weak GPU | Stable gameplay at lower resolution |
| Weak CPU + Strong GPU | High resolution, unstable gameplay |
| Balanced CPU + GPU | Best overall accuracy and stability |

---

## 5. Emulator Settings as Load Balancers

Settings such as:

- EE Cycle Rate  
- EE Cycle Skip  
- MTVU  
- Instant VU1  

exist to manage **CPU load and synchronization**.

These options are **not graphical enhancements**.  
They are tools to **rebalance execution across emulator subsystems**.

---

## 6. Thermal & Sustained Performance

On mobile devices, sustained emulation performance is constrained by:

- Thermal throttling
- Power limits
- Long-duration clock stability

Emulation tuning must account for **long-term stability**, not short benchmark peaks.

---

## Key Takeaway

> **CPU performance determines whether a game runs correctly.  
> GPU performance determines how good it looks.**

---

**Darkelf Retro Lounge**  
*Preserving Accuracy • Testing Limits • Respecting Original Hardware*
