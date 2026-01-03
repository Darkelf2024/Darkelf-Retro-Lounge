# AetherSX2 — Software vs Hardware Renderer (Part 4)  
## Accuracy, Compatibility, and When Software Is Required  
*Darkelf Retro Lounge Documentation Series*

---

## Overview

This document explains the **critical differences between Software and Hardware rendering** in **AetherSX2**.

While **hardware rendering** provides higher performance and visual enhancements, **software rendering** exists to deliver **pixel-accurate output** required by certain PlayStation 2 titles. :contentReference[oaicite:0]{index=0}

---

## 1. Hardware Rendering Overview

Hardware renderers (**Vulkan** and **OpenGL**) offload rendering tasks to the GPU.

They enable:
- Resolution scaling
- Texture filtering
- Post-processing effects

However, hardware renderers must **approximate the behavior of the original PlayStation 2 Graphics Synthesizer (GS)**.

Due to architectural differences between modern GPUs and the PS2 GS, certain effects may render incorrectly, including:
- Blending operations
- Depth priority
- Sprite ordering

---

## 2. Software Rendering Overview

The **Software Renderer** emulates the Graphics Synthesizer **entirely on the CPU**.

Characteristics:
- Prioritizes correctness over performance
- Produces output closest to real PlayStation 2 hardware
- Ignores resolution scaling and visual enhancements

Software rendering correctly handles GS edge cases that hardware renderers cannot accurately reproduce.

---

## 3. Why Some Games Require Software Rendering

Certain PlayStation 2 titles rely on:
- Non-standard GS behavior
- Heavy sprite usage
- Precise blending and transparency operations

When these titles are rendered using hardware renderers, issues may occur such as:
- Missing effects
- Broken transparency
- Incorrect layering or draw order

These problems are not emulator bugs but **limitations of hardware GS approximation**.

---

## 4. Performance Trade-Offs

| Renderer Type | Accuracy | Performance | Typical Use Case |
|--------------|----------|-------------|------------------|
| Hardware (Vulkan / OpenGL) | Medium–High | High | Most 3D titles |
| Software Renderer | Very High | Very Low | Accuracy-critical titles |

Hardware rendering is suitable for the majority of games.  
Software rendering is **extremely CPU-intensive** and often impractical for real-time play on mobile devices.

---

## 5. Best Practices

- Use **hardware rendering by default**
- Switch to **software rendering only when visual correctness is broken**
- Attempt hardware accuracy settings or per-game fixes before using software rendering
- Always apply software rendering through **per-game overrides**
- Never enable software rendering globally

---

## Key Takeaway

> **Hardware rendering delivers speed and enhancements, but software rendering exists to preserve correctness when approximation fails.**

---

**Darkelf Retro Lounge**  
*Preserving Accuracy • Testing Limits • Respecting Original Hardware*
