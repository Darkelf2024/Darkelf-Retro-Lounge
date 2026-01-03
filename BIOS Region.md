# AetherSX2 — BIOS Region Documentation  
**PAL, NTSC-U Compatibility & Testing Policy**  
*Darkelf Retro Lounge Documentation Series*

---

## Overview

PlayStation 2 emulation traditionally recommends matching the **BIOS region** to the **game region** for historical hardware accuracy.  
Modern emulation, including **AetherSX2**, relaxes these constraints to allow greater flexibility **without sacrificing stability**.

---

## BIOS Configuration Used for Testing

All testing performed by **Darkelf Retro Lounge** uses a **standardized BIOS configuration** to ensure consistency across titles and test sessions.

| Setting | Configuration |
|------|---------------|
| **BIOS Region** | European (PAL) |
| **Game Regions Tested** | PAL, NTSC-U (USA) |
| **Emulator** | AetherSX2 |

---

## Observed Behavior in AetherSX2

- Both **PAL** and **NTSC-U** game images **boot, run, and save correctly** when using a **European (PAL) BIOS**.
- No region-related **crashes, hangs, or regressions** were observed during extended testing.
- **AetherSX2 does not strictly enforce BIOS–ROM region matching**, allowing a single BIOS to support mixed-region libraries reliably.

---

## Accuracy vs Practical Emulation

On original PlayStation 2 hardware, **BIOS and game region matching was mandatory** to ensure proper video timing and system behavior.

In emulation:
- Region checks are **virtualized**
- Broader compatibility is enabled
- Core emulation accuracy is **not compromised**

This allows modern emulators like AetherSX2 to balance **historical accuracy** with **real-world usability**.

---

## Testing Policy Statement

Darkelf Retro Lounge testing uses a **European (PAL) PlayStation 2 BIOS** as a standardized baseline.

- **PAL and NTSC-U titles** are considered **valid and compatible** under this configuration
- Unless a title demonstrates **documented region-specific issues**
- Any such issues are recorded **on a per-game basis**

---

## When BIOS Region Matching May Still Matter

BIOS region matching may still be relevant for:

- Debugging and emulator development
- Preservation and hardware-accurate comparisons
- Titles with **hardcoded video timing assumptions**

Any region-specific behavior is explicitly documented when encountered.

---

## Key Takeaway

> **BIOS region matching is recommended for historical accuracy, but is *not required* for functional gameplay in AetherSX2.**

---

**Darkelf Retro Lounge**  
*Preserving Accuracy • Testing Limits • Respecting Original Hardware*
