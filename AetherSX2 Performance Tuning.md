# AetherSX2 Performance Tuning — Part 3  
## MTVU, Instant VU1 & EE Cycle Skip Explained  
*Darkelf Retro Lounge Documentation Series*

---

## Overview

This document explains three of the **most misunderstood performance-related options** in **AetherSX2**:

- Multithreaded VU (MTVU)
- Instant VU1
- EE Cycle Skip

These settings are often described as “speed hacks,” but are more accurately understood as **load-balancing and scheduling shortcuts** that trade accuracy for performance. 

---

## 1. Multithreaded VU (MTVU)

**MTVU** offloads **Vector Unit 1 (VU1)** execution to a **separate CPU thread**.

### How It Works
- Allows VU1 to execute in parallel with the Emotion Engine (EE)
- Takes advantage of multi-core CPUs common in modern devices

### Benefits
- Significant performance improvements on multi-core hardware
- Reduced CPU contention between EE and VU workloads

### Risks
- Slight reduction in determinism
- Possible timing-related bugs in games that rely on strict EE–VU synchronization

### Recommended Usage
- Generally safe on modern devices
- Should be the **first performance-related option enabled**

---

## 2. Instant VU1

**Instant VU1** bypasses synchronization checks between the EE and VU1 microprograms.

### How It Works
- Skips waiting for proper EE–VU1 coordination
- Forces immediate VU1 execution

### Benefits
- Large and immediate performance gains

### Accuracy Trade-Offs
Instant VU1 commonly causes:
- Broken physics
- Animation glitches
- Missing or incorrect effects
- Collision detection errors

### Recommended Usage
- Only as a **last-resort, per-game override**
- Never recommended as a global setting

---

## 3. EE Cycle Skip

**EE Cycle Skip** instructs the emulator to **skip Emotion Engine cycles** when it detects that execution is falling behind real-time.

### How It Works
- Discards CPU execution to maintain frame rate
- Differs fundamentally from EE Cycle Rate

### Key Difference from EE Cycle Rate
- **EE Cycle Rate** rebalances workload
- **EE Cycle Skip** actively throws away execution

### Benefits
- Preserves apparent speed
- Prevents extreme slowdowns

### Accuracy Trade-Offs
- Logic errors
- Animation desynchronization
- Unreliable game behavior

---

## Summary of Effects

| Setting | Primary Benefit | Primary Risk |
|-------|----------------|-------------|
| MTVU | Parallel VU execution | Timing instability |
| Instant VU1 | Large speed increase | Broken physics & visuals |
| EE Cycle Skip | Maintains frame rate | Logic & animation errors |

---

## Best Practices & Usage Guidelines

- Enable **MTVU first**
- Use **Instant VU1** and **EE Cycle Skip** only as **last-resort, per-game options**
- Never combine:
  - Aggressive EE underclocking
  - Instant VU1
  - EE Cycle Skip  
  as global settings

This combination almost guarantees instability.

---

## Key Takeaway

> **These settings trade accuracy for speed.**  
> Use them deliberately, sparingly, and only when CPU limitations demand it.

---

**Darkelf Retro Lounge**  
*Preserving Accuracy • Testing Limits • Respecting Original Hardware*
