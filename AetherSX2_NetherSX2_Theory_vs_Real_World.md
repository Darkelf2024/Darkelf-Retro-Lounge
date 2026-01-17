
# AetherSX2 / NetherSX2 – Practical Emulation Settings Guide
## Theory vs Real‑World Behavior on Android Hardware

This document consolidates practical findings from sustained testing on low‑power Android devices using **AetherSX2** and **NetherSX2**.  
It focuses on *behavioral accuracy*, real gameplay usability, and measured performance — not just theoretical best‑practice defaults.

---

## 1. Audio: Async Mix vs TimeStretch

### Async Mix
**Theory**
- Mixes audio asynchronously from emulation timing
- Designed to preserve audio continuity when emulation speed fluctuates

**Real‑World Behavior**
- Works well when emulation speed is near target (≈95–100%)
- Reduces audio crackle during brief stalls
- Can introduce subtle desync if emulation speed drops for extended periods

**Performance Impact**
- Low
- Preferred on constrained hardware when pacing is stable

### TimeStretch
**Theory**
- Dynamically stretches/compresses audio to match emulation speed
- Keeps audio synced to game logic

**Real‑World Behavior**
- Most reliable when emulation speed fluctuates frequently
- Can sound unnatural or “warbly” during heavy load
- More forgiving when internal game rate (G) is unstable

**Performance Impact**
- Moderate CPU overhead
- Safer default for unstable titles

**Practical Takeaway**
- Async Mix is viable for near‑target speed gameplay
- TimeStretch is safer when speed varies significantly

---

## 2. CPU Affinity Control – Disabled vs Enabled

### Disabled (Default / Recommended)
**Theory**
- OS scheduler dynamically assigns threads

**Real‑World Behavior**
- Better thermal distribution
- Fewer sustained throttling events
- More consistent long‑session performance

**Performance Impact**
- Neutral to positive

### Enabled
**Theory**
- Pins emulator threads to specific cores

**Real‑World Behavior**
- Can improve short‑term benchmarks
- Often worsens sustained emulation due to thermal saturation
- Increased stutter under long loads

**Performance Impact**
- Often negative over time

**Practical Takeaway**
- Leave affinity control disabled on mobile devices unless a game requires it - Some games depend on it
- Can alter the behavior regarding G/V stability
- CPU affinity doesn’t just affect raw performance; it can materially change emulation behavior by stabilizing scheduling, which in turn improves G/V consistency, pacing, and perceived playability on mobile hardware.
- Some PS2 titles benefit from Performance affinity because they’re CPU-bound and sensitive to scheduling jitter, while others run better with default affinity to avoid thermal or stability issues. It’s workload-dependent, not universal.

---

## 3. Blending Accuracy vs Performance

Blending affects how the PS2 GS handles framebuffer effects such as motion blur, shadows, and transparency.

### Blending Modes

#### Basic / Minimum
- Lowest GPU cost
- Visual artifacts common
- Useful only for extreme low‑end devices

#### Medium
- Balanced option
- Minor visual compromises
- Often acceptable for many titles

#### Full
- Near‑accurate blending behavior
- Moderate GPU cost
- Recommended baseline for most devices

#### Ultra
- Highest accuracy
- Corrects effects relied on by many PS2 titles
- Heavier GPU load

**Real‑World Observation**
- Ultra blending often improves *behavioral correctness* even when FPS is unchanged
- Some games rely on blending behavior for proper visual logic

**Practical Takeaway**
- Use Full or Ultra where thermals allow
- Visual correctness often matters more than raw FPS

---

## Summary: Theory vs Real‑World Emulation

### Theory‑Driven Expectations
- Perfect cycle accuracy
- Locked 50/60 FPS
- Strict frametime targets

### Real‑World Mobile Reality
- Thermal limits dominate
- Stable pacing matters more than raw FPS
- Behavioral correctness is achievable even below native internal rates

### Key Insight
**FPS ≠ Accuracy**  
On Android hardware, *behavioral accuracy* — correct pacing, logic, audio sync, and input response — is the most meaningful metric.

AetherSX2 and NetherSX2 can deliver highly playable PS2 experiences when configured with real hardware constraints in mind.

---

## Final Note

These findings are based on sustained, real‑device testing and will continue to evolve.  
Settings that work in theory may not hold under long‑session mobile thermal limits.

Documentation will be updated as new data is gathered.
