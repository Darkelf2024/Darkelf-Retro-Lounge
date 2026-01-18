# AetherSX2 — Android SoC Behavior & Sustained Clocks (Part 9)  
## Why Chipset Design Matters More Than Raw Specs  
*Darkelf Retro Lounge Documentation Series*

---

## Overview

This document examines how different **Android System-on-Chip (SoC) designs** affect **AetherSX2 performance**.

Rather than focusing on benchmark numbers, this guide explains **architectural differences**, **scheduler behavior**, and **sustained clock characteristics** that determine real-world emulation stability. 

---

## 1. Why SoC Design Matters in Emulation

PlayStation 2 emulation on mobile devices is highly sensitive to:

- CPU latency
- Cache behavior
- Sustained clock speeds

Two devices with similar benchmark scores can perform very differently during extended gameplay sessions due to differences in SoC design and thermal management.

---

## 2. Snapdragon (Qualcomm)

Snapdragon SoCs typically offer:

- Strong single-core performance
- Large CPU caches
- Mature GPU driver stacks

These characteristics make Snapdragon-based devices the **most consistent choice** for AetherSX2 across a wide range of hardware.

Snapdragon devices often sustain performance better under **Vulkan**, due to stable and well-optimized drivers.

---

## 3. Exynos (Samsung)

Exynos SoCs vary widely by generation.

Common characteristics include:

- Good peak performance
- Aggressive thermal throttling on some models
- Less predictable GPU driver behavior

These factors can negatively impact **long-session emulation stability**.

---

## 4. MediaTek (Dimensity)

Modern Dimensity chips provide:

- Competitive multi-core performance
- Improved efficiency over older generations

However, they may suffer from:

- Weaker single-core throughput
- Inconsistent GPU driver behavior in emulation workloads

Dimensity-based devices can perform well but often require **more conservative emulator settings**.

---

## 5. Scheduler & Power Management Differences

Android emulation performance is strongly influenced by factors outside emulator control, including:

- Android scheduler behavior
- CPU governor tuning
- OEM thermal policies

These elements directly determine how long a device can maintain high clock speeds under sustained load.

---

## SoC Family Comparison

| SoC Family | Strengths | Common Limitations |
|-----------|----------|-------------------|
| Snapdragon | Strong single-core, stable drivers | Device-dependent thermals |
| Exynos | Good peak performance | Aggressive throttling, GPU quirks |
| MediaTek | High multi-core throughput | Lower single-core consistency |

---

## Key Takeaway

> **Emulation performance depends on sustained clocks, scheduler behavior, and driver maturity — not just advertised specifications.**

---

**Darkelf Retro Lounge**  
*Preserving Accuracy • Testing Limits • Respecting Original Hardware*
