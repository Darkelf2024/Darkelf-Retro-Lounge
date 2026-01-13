# Interpreting NetherSX2 Performance Metrics (Real-World Example)

**Game Tested:** Black (PlayStation 2, PAL)  
**Emulator:** NetherSX2 (Android)

This document provides a practical interpretation of real NetherSX2 performance metrics captured during sustained gameplay of *Black* on low-power Android hardware.

---

## Captured Metrics

```
G: 25.17 (PAL)
V: 50.34
Speed: 101% (100%)

Frame Times:
34.52 ms
39.73 ms
45.59 ms

VE: 18.50 ms
GPU: 61.0% (24.24 ms)

Spike:
62.2 ms

Recovery:
21.0 ms
```

---

## What These Numbers Mean

### G — Internal Game Rate
- **G ≈ 25 Hz**
- Represents the internal PS2 game logic update rate
- Below native PAL target (50 Hz), which is expected on low-power SoCs
- Does *not* automatically indicate poor gameplay

### V — Video Output Rate
- **V ≈ 50 FPS**
- Matches PAL video timing
- Reflects what is actually displayed on screen

### Emulation Speed
- **~100%**
- Indicates real-time pacing with no global slowdown

---

## Frame Time Analysis

### Typical Frame Times
- **~34–45 ms** most of the time
- Indicates stable pacing with frame reuse / duplication
- Acceptable for PAL output on constrained hardware

### VE (Video Engine)
- **~18.5 ms**
- Confirms stable video delivery and smooth presentation

### GPU Load
- **~61%**
- GPU is not saturated
- No GPU bottleneck observed

### Spikes
- **~62 ms occasional**
- Typical during:
  - Texture uploads
  - Scene transitions
  - Asset streaming
- These spikes are brief and recover quickly

### Recovery
- **~21 ms**
- System returns to normal pacing rapidly

---

## Is This Bad Frame Pacing?

**No.**

Bad frame pacing would involve:
- Constant, repeated spikes
- Large frame time swings every frame
- Visible stutter during normal traversal
- Audio desynchronization

None of those behaviors are present here.

---

## What This Demonstrates (Black – PS2, NetherSX2)

- Stable PAL video output (~50 FPS)
- Lower internal game rate compensated by pacing
- Correct audio and input behavior
- Expected transient spikes under load in a heavy FPS title

This is an example of **behavioral accuracy** rather than cycle-accurate emulation.

---

## Key Takeaway

> FPS alone does not define correctness.  
> Frame pacing and behavior over time matter more.

These results reflect normal, acceptable behavior for *Black* running under **NetherSX2** on low-power Android handhelds.