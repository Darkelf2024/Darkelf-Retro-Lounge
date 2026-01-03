# AetherSX2 — Testing Methodology & Validation (Part 6)  
## How Games Are Evaluated, Verified, and Classified  
*Darkelf Retro Lounge Documentation Series*

---

## Overview

This document describes the **testing methodology** used by **Darkelf Retro Lounge** when evaluating PlayStation 2 titles under **AetherSX2**.

The goal is **repeatability, transparency, and accuracy-focused validation**, rather than subjective performance impressions or short benchmark testing. :contentReference[oaicite:0]{index=0}

---

## 1. Testing Philosophy

Testing prioritizes:

- Correctness
- Stability
- Determinism

over peak performance.

Games are evaluated as **interactive systems over time**, not as isolated benchmark runs.

A title is **not considered working** unless it remains stable during **extended gameplay sessions**.

---

## 2. Baseline Configuration

Each game begins testing using a **standardized baseline configuration**, including:

- Hardware renderer enabled
- Default EE timing
- MTVU enabled on supported devices
- No aggressive speed hacks

This baseline ensures results are comparable across devices and test sessions.

---

## 3. Test Duration & Scenarios

Games are tested across **multiple gameplay scenarios**, including:

- Menus
- Active gameplay
- Combat encounters
- Cutscenes
- Loading transitions

Test sessions are long enough to expose:

- Thermal throttling
- Timing drift
- Accumulated instability

---

## 4. Validation Criteria

Validation focuses on the following criteria:

| Category | Criteria |
|--------|----------|
| Stability | No crashes or lockups |
| Timing | Consistent frame pacing |
| Audio | No persistent crackle or desynchronization |
| Visuals | Correct layering, blending, and effects |
| Gameplay | Physics and logic behave correctly |

All criteria must be met for a title to be considered stable.

---

## 5. Classification Outcomes

Titles are classified based on **observed behavior**, not theoretical performance:

- **Fully Playable**
- **Playable with Tweaks**
- **Accuracy Issues Present**
- **Unsupported**

Classifications may change as **emulator versions evolve**.

Documentation is **version-aware** and avoids permanent judgments.

---

## Key Takeaway

> **Reproducible testing and transparency matter more than raw performance claims.**

---

**Darkelf Retro Lounge**  
*Preserving Accuracy • Testing Limits • Respecting Original Hardware*
