# Version Comparison  
## AetherSX2 1.5-3668 vs AetherSX2 1.5-4248 vs NetherSX2

This document explains the **practical differences, advantages, and trade-offs** between the three most commonly used Android PS2 emulator builds. Comparisons are based on **real-world behavior, defaults, long-session stability, and configuration discipline**, not short benchmark runs or FPS-only claims.

---

## Overview

All three builds share the same core emulation lineage, but differ significantly in:

- default configuration philosophy  
- exposed tuning options  
- performance vs accuracy priorities  

None of these builds are inherently “bad.” They simply serve **different goals**.

---

## AetherSX2 v1.5-3668

### Summary
**AetherSX2 v1.5-3668** is a stable, conservative Android build that **plays PS2 games well out of the box** while prioritizing correct behavior and predictable timing.

### Strengths
- Strong real-world performance despite conservative defaults
- Excellent long-session stability
- Minimal tuning required for correct behavior
- Clean, repeatable baseline for testing and documentation
- Defaults discourage unsafe speed hacks

### Why it feels plug-and-play
- Normal Speed fixed at 100%
- EE Cycle Skip disabled by default
- Fewer risky or misleading options exposed
- Results reflect emulator behavior rather than configuration artifacts

### Trade-offs
- Slightly less peak performance headroom than aggressive presets
- Requires EE underclocking (`-1 / -2`) instead of shortcuts on CPU-bound titles
- Fewer advanced knobs for users chasing maximum FPS at any cost

### Best use
**Primary baseline for gameplay, compatibility testing, and documentation**

> Conservative does not mean slow.  
> v1.5-3668 plays many PS2 titles smoothly and reliably, often with fewer issues than more aggressive builds.

---

## AetherSX2 v1.5-4248

### Summary
**AetherSX2 v1.5-4248** is a later Android build that introduces additional compatibility fixes and exposes more configuration options.

### Strengths
- Includes fixes beyond 3668
- Greater flexibility for advanced users
- Can outperform 3668 in select edge cases
- Useful for renderer-specific or driver-specific investigation

### Trade-offs
- Defaults are less conservative
- Higher risk of accidental timing or behavior changes
- Requires stronger user discipline to maintain accuracy
- Results are more configuration-dependent

### Best use
**Secondary validation and comparison build**

Recommended when:
- a title behaves unexpectedly on 3668
- testing regressions or compatibility changes
- verifying whether an issue is version-specific

---

## NetherSX2

### Summary
**NetherSX2** is a fork of AetherSX2 (commonly based on 4248-era code) with performance-oriented defaults and convenience-focused changes.

### Strengths
- Higher apparent performance out of the box
- Easier to achieve smooth FPS on weaker hardware
- Popular on handheld devices and mid-range SoCs
- Convenient for casual play

### Trade-offs
- Often relies on EE Cycle Skip or aggressive tuning
- Timing correctness is not guaranteed
- Behavior varies by preset and build
- Not suitable as a clean accuracy reference

### Best use
**Performance-assisted or casual play**

Results should be clearly labeled as:
> *Performance-tuned / speed-hack-assisted*

---

## Direct Comparison Table

| Build | Accuracy | Performance | Defaults | Recommended Role |
|------|---------|-------------|----------|------------------|
| AetherSX2 3668 | High | High (consistent) | Conservative | Primary baseline |
| AetherSX2 4248 | Medium–High | Medium–High | Mixed | Secondary validation |
| NetherSX2 | Variable | High | Aggressive | Casual / performance |

---

## Which Version Should I Use?

### If you want correct behavior with minimal tuning
➡ **Use AetherSX2 v1.5-3668**

This is the recommended choice for:
- accuracy-first testing
- documentation
- long play sessions
- consistent results across devices

---

### If a game has known issues on 3668
➡ **Test with AetherSX2 v1.5-4248**

Use it to:
- check for fixes or regressions
- compare behavior across versions
- isolate renderer or driver-specific problems

---

### If your priority is smoothness over strict accuracy
➡ **Use NetherSX2**

Best for:
- casual play
- weaker hardware
- “can this be made playable?” scenarios

Accuracy trade-offs should be assumed unless proven otherwise.

---

## OS Considerations: StockOS vs GammaOS

### Mangmi StockOS
- More background services
- Less aggressive CPU governor behavior
- Earlier thermal throttling
- Tighter performance headroom

**Implication:**  
StockOS benefits most from **conservative defaults**.  
AetherSX2 3668 is typically the most stable and predictable choice.

---

### GammaOS
- Improved CPU governor tuning
- Better sustained clocks
- Reduced background overhead

**Implication:**  
GammaOS allows more headroom:
- EE underclocking is often sufficient
- 4248 may perform better in some cases
- Still benefits from avoiding EE Cycle Skip

---

## Project Stance (Important)

For accuracy-first research and compatibility documentation:

- **AetherSX2 v1.5-3668** is used as the primary reference
- **AetherSX2 v1.5-4248** is used for secondary validation
- **NetherSX2** results are documented separately with context

This approach prioritizes:
- behavior correctness
- long-session stability
- reproducibility
- transparency

Over raw FPS or short benchmark results.

---

## Final Takeaway

- **AetherSX2 3668**  
  Stable, capable, and reliable. Conservative defaults that still deliver strong real-world performance.

- **AetherSX2 4248**  
  Flexible and sometimes more compatible, but requires discipline.

- **NetherSX2**  
  Optimized for convenience and smoothness, not strict correctness.

> **FPS is a metric. Behavior defines correctness.**
