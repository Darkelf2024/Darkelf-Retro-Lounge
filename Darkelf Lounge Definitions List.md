# Darkelf Retro Lounge — Definitions & Terminology

> **Disclaimer**
>  
> This documentation reflects observed emulator behavior under controlled testing conditions.
> Results may vary by device, Android version, emulator build, game revision, and workload.
> No configuration, definition, or classification in this repository guarantees performance,
> accuracy, or stability across all hardware.

---

## Core Emulation Concepts

### Emulation Accuracy
The degree to which emulator behavior matches original PlayStation 2 hardware behavior, including timing, logic execution, physics, rendering, and synchronization.

Accuracy does **not** imply visual fidelity alone and does **not** guarantee high performance.

### Performance
The ability to maintain playable frame pacing and responsiveness.
Performance is evaluated over sustained gameplay, not short benchmark runs.

### Stability
The emulator’s ability to run without crashes, lockups, timing drift, or accumulating errors during extended play sessions.

A game that runs briefly but degrades over time is **not considered stable**.

### Determinism
Consistent and predictable behavior across frames and sessions.
Loss of determinism often manifests as broken physics, inconsistent AI behavior, or desynchronized audio/animation.

---

## Playability & Accuracy Classifications

### Behaviorally Playable
A classification indicating that a game:
- runs to completion
- maintains acceptable performance
- does not exhibit major logic or progression blockers

Behaviorally playable does **not** imply full accuracy.
Minor timing deviations, physics inaccuracies, or visual inconsistencies may still exist.

### Cycle-Aware Accuracy
A strict accuracy standard evaluating whether a game remains correct when emulator cycle timing is altered or stressed.

Cycle-aware accuracy focuses on:
- EE instruction pacing
- EE–VU synchronization
- logic and physics consistency under timing pressure
- long-session stability

A title that only behaves correctly under ideal timing conditions is **not cycle-aware accurate**.

### Playable vs Accurate
- Playable: runs acceptably without major visible issues
- Behaviorally Playable: completes correctly with minor inaccuracies
- Accurate: matches expected hardware behavior under normal conditions
- Cycle-Aware Accurate: remains correct under timing stress and long sessions

Playable does **not** imply accurate.

---

## CPU / EE / VU Terminology

### Emotion Engine (EE)
The PlayStation 2 CPU responsible for game logic, AI, physics, and scripting.
In emulation, EE behavior is governed by timing budgets, not real clock frequency.

### Vector Units (VU0 / VU1)
PS2 coprocessors used for geometry, animation, and vector math.
VU1 is frequently a synchronization bottleneck.

### MTVU (Multithreaded VU1)
A load-balancing option that executes VU1 on a separate CPU thread.
MTVU behavior varies by game, SoC, and Android scheduler.

### Instant VU1
A timing shortcut that bypasses EE–VU synchronization.
Often breaks physics and logic; not accuracy-safe.

### EE Cycle Rate
A scheduler timing control that limits EE instructions per frame.
It is a load-balancing tool, not a speed hack.

### EE Cycle Skip
Discards EE execution to maintain frame rate.
Inherently inaccurate.

---

## Rendering Terminology

### Graphics Synthesizer (GS)
The PS2 graphics processor with behavior fundamentally different from modern GPUs.

### Hardware Renderer
GPU-based rendering (Vulkan/OpenGL) that approximates GS behavior.
Fast but not perfectly accurate.

### Software Renderer
CPU-based GS emulation.
Highest accuracy, extremely CPU-intensive, intended only for specific titles.

### Blending Accuracy
Controls how closely transparency and blending match PS2 behavior.
Higher accuracy increases GPU load and does not guarantee performance changes.

---

## Platform & Hardware Terms

### SoC (System-on-Chip)
Integrated CPU, GPU, memory controller, and power management.
Emulation depends on sustained clocks, cache behavior, scheduler decisions, and thermals.

### Scheduler Behavior
How Android assigns threads to cores.
Can override emulator intent and vary widely between devices.

### Sustained Performance
Performance after thermal equilibrium is reached.
More meaningful than peak benchmarks.

### Thermal Throttling
Clock reduction to prevent overheating.
Causes audio crackle, slowdowns, and pacing instability.

---

## Configuration Philosophy

### Baseline Configuration
A controlled starting point for testing.
Not an optimized preset.

### Per-Game Override
Settings applied only to a specific title.
Aggressive options should never be global.

### Speed Hacks
Options that trade correctness for apparent performance.

---

## Testing & Documentation Terms

### Long-Session Testing
Extended gameplay used to expose thermal, timing, and stability issues.

### Engine-Specific Behavior
Different game engines stress different subsystems.
Issues are often engine-specific, not emulator-wide.

### Global Settings
Settings applied to all games.
Global aggressive changes are discouraged.

---

**Darkelf Retro Lounge**  
Preserving Accuracy • Testing Limits • Respecting Original Hardware
