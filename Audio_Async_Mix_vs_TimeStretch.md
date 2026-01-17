# Audio Sync (Mix) vs TimeStretch

## Audio Sync (Mix)
- Locks audio to the emulator's internal game clock
- Preserves correct cadence and timing
- No pitch warping or time stretching
- Best when frame pacing is stable (even if under full speed)

**Pros**
- More behaviorally accurate
- Cleaner audio over long sessions
- Reflects real PS2 hardware behavior

**Cons**
- Audible slowdown if emulation speed drops significantly

## TimeStretch
- Dynamically stretches or compresses audio to mask speed changes
- Prioritizes continuous sound output

**Pros**
- Masks instability on weaker hardware
- Reduces dropouts during heavy slowdown

**Cons**
- Can introduce warbling or pitch artifacts
- Alters perceived game behavior

## Practical Guidance
- Stable pacing → Audio Sync (Mix)
- Unstable pacing → TimeStretch

## Theory vs Real-World
- Experiences may differ with certain conditions
