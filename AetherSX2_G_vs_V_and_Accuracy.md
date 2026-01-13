# Understanding AetherSX2 Performance Metrics and Accuracy

## 📊 G vs V — What the Metrics Mean in AetherSX2

AetherSX2 exposes two performance metrics that are often misunderstood: **G** and **V**. These values measure different parts of the emulation pipeline and should not be interpreted the same way.

### **G — Internal Game Rate**
**G** represents the **internal PlayStation 2 game update rate**.  
This reflects how fast the emulated PS2’s game logic is running, including:
- Game logic and timing
- Physics and animations
- AI behavior
- Input processing

G is the most direct indicator of **internal emulation speed**. On original hardware, PAL titles target ~50 updates per second and NTSC titles target ~60.

On low-power Android hardware, G may run **below native targets** even when the game remains playable and correctly paced.

---

### **V — Video Output Rate**
**V** represents the **video output frame rate** — the frames actually presented to the display.

V is influenced by:
- Display refresh rate
- PAL vs NTSC timing
- Frame pacing and duplication
- Renderer behavior

For PAL titles, V typically sits near **50 FPS**, even when internal G is lower.

---

### **Why G and V Can Differ**
On constrained hardware, AetherSX2 prioritizes **stable output pacing and audio sync**. As a result:
- V may remain near target refresh
- G may fluctuate or remain below native speed
- Frames may be duplicated or reused visually

This can produce gameplay that **looks smooth** while internal simulation runs below full speed.

---

### **How These Metrics Are Used in This Project**
This project considers **G** as an indicator of internal load and accuracy, while **V** reflects visual smoothness.

Playability assessments are based on:
- Stability of G over time
- Consistency of pacing
- Correct gameplay behavior
- Audio and input sync

Raw FPS alone is not used as a measure of correctness.

---

## 🎯 Cycle Accuracy vs Behavioral Accuracy

Accuracy in emulation can be measured in different ways. This project distinguishes between **cycle accuracy** and **behavioral accuracy**, especially when evaluating emulation on low-power devices.

---

### **Cycle Accuracy**
Cycle accuracy refers to emulation that:
- Matches original hardware timing cycle-for-cycle
- Achieves native internal update rates (50/60 Hz)
- Preserves exact instruction timing and latency

Cycle-accurate emulation is the ideal goal but typically requires **desktop-class hardware** and is rarely achievable on low-power Android devices.

---

### **Behavioral Accuracy**
Behavioral accuracy focuses on **how the game behaves**, rather than matching every hardware cycle.

A behaviorally accurate game:
- Progresses at the correct pace
- Maintains correct logic and physics
- Keeps audio synchronized
- Responds to input correctly
- Avoids timing-related bugs or logic errors

Even when internal G is below native targets, behavior can remain correct if pacing and synchronization are preserved.

---

### **Why This Project Focuses on Behavioral Accuracy**
On constrained hardware, insisting on full cycle accuracy would exclude nearly all playable results and fail to reflect real-world emulator behavior.

This project therefore prioritizes **behavioral accuracy on real devices**, documenting:
- What works reliably
- What requires configuration changes
- What fails due to hardware limits

This approach provides **useful, honest data** without overstating hardware capability.

---

### **Key Takeaway**
**FPS does not define accuracy. Behavior does.**

Cycle accuracy is the ideal.  
Behavioral accuracy is the practical reality on mobile hardware.

Both matter — but they are not the same thing.
