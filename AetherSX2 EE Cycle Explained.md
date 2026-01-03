# AetherSX2 — EE Cycle Rate Explained  
**Deep Technical Reference**  
*Darkelf Retro Lounge Documentation Series*

**Scope:** Advanced / Maintainer-Level  
**Applies to:** AetherSX2 (Android)  
**Audience:** Power users, emulator tuners, documentation maintainers

---

## Overview

The **EE Cycle Rate** controls how many **Emotion Engine (EE) CPU cycles** AetherSX2 allows to execute per emulated frame.

It is one of the **most powerful — and most dangerous — tuning options** in the emulator.

This is **not** a traditional overclock or underclock.  
It is a **scheduler timing adjustment** that changes how the emulator balances CPU, VU, and GPU workloads. :contentReference[oaicite:0]{index=0}

---

## What the EE Cycle Rate Actually Does

The EE Cycle Rate:

- Adjusts the instruction budget per frame
- Directly impacts:
  - CPU load
  - Frame pacing
  - Audio stability
  - Synchronization accuracy
- Does **not** change real hardware frequency

**Reference:**  
Real PlayStation 2 EE clock ≈ **294 MHz → represented as 100%**

---

## EE Cycle Rate = 100%  
### (Default / Accurate)

**Behavior**
- Executes the correct number of EE instructions per frame
- Matches real PlayStation 2 timing behavior

**Recommended For**
- Most games
- Accuracy-critical titles
- Rhythm and timing-sensitive games

**Risk Level**
- None

---

## EE Cycle Rate = –1  
### (Light Underclock)

**Internal Effect**
- Slight reduction in EE instruction execution
- Reduces CPU pressure without breaking timing assumptions

**Benefits**
- Smooths micro-stutter
- Fixes minor audio crackle
- Improves frame pacing on mobile CPUs

**Recommended Usage**
- First performance tweak to try
- Safe for the majority of titles

**Risk Level**
- Very Low

---

## EE Cycle Rate = –2  
### (Moderate Underclock)

**Internal Effect**
- Noticeable reduction in EE workload
- Frees execution time for:
  - VU0 / VU1
  - Graphics Synthesizer (GS)

**Benefits**
- Improves performance on:
  - Mid-range devices
  - CPU-bound open-world games
  - AI-heavy titles

**Trade-Offs**
- Slower physics updates
- Delayed animation ticks
- Potential cutscene timing issues

**Recommended Usage**
- Per-game override only

**Risk Level**
- Medium

---

## EE Cycle Rate = –3  
### (Heavy Underclock)

**Internal Effect**
- Aggressively limits EE execution
- Maximum CPU relief at the cost of accuracy

**Benefits**
- Last-resort option for:
  - Extremely demanding games
  - Very weak hardware

**Severe Trade-Offs**
- Broken physics
- Game logic errors
- Animation desynchronization
- AI instability

**Recommended Usage**
- Only if –1 and –2 fail
- Never as a global setting

**Risk Level**
- High

---

## EE Cycle Rate > 100%  
### (Overclock)

**Internal Effect**
- Increases EE instruction budget per frame
- Speeds up CPU-side logic execution

### Why This Is Dangerous

Many PlayStation 2 games:
- Tie gameplay speed to CPU loops
- Assume fixed EE timing
- Use busy-wait logic instead of timers

**Common Failures**
- Physics running too fast
- Accelerated animations
- AI misbehavior
- Audio/video desynchronization

**Recommended Usage**
- Almost never
- Only for very specific, logic-bound titles

**Risk Level**
- Very High

---

## Why Underclocking Works Better Than Overclocking

Mobile emulation is usually **GPU- or VU-bound**, not CPU-bound.

**Underclocking**
- Prevents EE from overwhelming slower components
- Improves overall pipeline balance

**Overclocking**
- Exacerbates synchronization problems

---

## Games That Commonly Benefit from Underclocking

- Open-world titles
- Streaming-heavy games
- AI-dense systems
- Games with:
  - Audio crackle
  - Uneven frame pacing

---

## Games That Dislike Underclocking

- Rhythm games
- Timing-critical combat systems
- Fixed-timestep physics engines

---

## Best Practices (Highly Recommended)

- Start at **100%**
- Try **–1** first
- Increase only if necessary
- Always use **per-game overrides**
- Never globally underclock
- Avoid combining aggressive underclock with:
  - Instant VU1
  - Frame skipping

---

## Summary Table

| EE Cycle Rate | Description | Accuracy Risk |
|--------------|------------|---------------|
| 100% | Hardware-accurate | None |
| –1 | Light underclock | Very Low |
| –2 | Moderate underclock | Medium |
| –3 | Heavy underclock | High |
| >100% | Overclock | Very High |

---

## Key Takeaway

> **EE Cycle Rate is a load-balancing tool, not a speed hack.**  
> Used correctly, it restores synchronization.  
> Used incorrectly, it breaks games.

---

**Darkelf Retro Lounge**  
*Preserving accuracy • Tuning performance • Respecting original hardware*
