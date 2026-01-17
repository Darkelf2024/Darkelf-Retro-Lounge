# 📚 References — Behavioral Accuracy in PlayStation 2 Emulation

This document lists authoritative, academic, and primary technical references that support an accuracy-first, behavior-based approach to PlayStation 2 emulation.

In this project, accuracy is defined as observable correctness over time: timing consistency, synchronization between subsystems, stable audio behavior, correct input response, and deterministic game logic during sustained gameplay. Frame rate alone is explicitly rejected as a sufficient measure of correctness.

The references below establish the hardware reality, emulator design constraints, and real-time system principles that justify this methodology.

---

## ⚠️ Disclaimer

This references document is provided for informational, educational, and research purposes only.

The inclusion of any reference does not imply endorsement, certification, or validation by the referenced authors, publishers, organizations, emulator developers, or hardware manufacturers. All interpretations, conclusions, and applications of these sources are the responsibility of the Darkelf Retro Lounge project and its contributors.

While every effort is made to select reputable and authoritative material, no guarantee is made regarding completeness, accuracy, or applicability to all hardware platforms, emulator versions, configurations, or usage scenarios. Emulation behavior may vary significantly depending on system architecture, emulator implementation, operating system, and workload.

PlayStation, PlayStation 2, Emotion Engine, and related trademarks are the property of their respective owners. This project is independent, non-commercial, and unaffiliated with Sony Interactive Entertainment, PCSX2, AetherSX2, NetherSX2, or any associated organizations.

The references provided describe general principles, architectural concepts, or observed behaviors and should not be interpreted as prescriptive guarantees of performance, compatibility, or correctness.

This document is living and non-exhaustive. References may be added, revised, or removed as research continues, emulator implementations evolve, or improved primary sources become available.

Use of this material is at your own discretion and risk.

---

## 🔹 PlayStation 2 Hardware & Architecture

1. Sony Computer Entertainment Inc. (1999).  
   PlayStation 2 technical specifications.  
   https://en.wikipedia.org/wiki/PlayStation_2_technical_specifications  

2. Sony Computer Entertainment Inc., & Toshiba Corporation. (1999).  
   Emotion Engine architecture overview.  
   https://en.wikipedia.org/wiki/Emotion_Engine  

3. Copetti, R. (n.d.).  
   PlayStation 2 architecture: A practical analysis.  
   https://www.copetti.org/writings/consoles/playstation-2/  

4. FOSDEM VZW. (2021).  
   The PlayStation 2: From Emotion to Emulation [Conference presentation].  
   https://av.tib.eu/media/53648  

---

## 🔹 Emulator Architecture & Correctness

5. PCSX2 Development Team. (n.d.).  
   PCSX2 official documentation and configuration guide.  
   https://github.com/PCSX2/pcsx2/blob/master/pcsx2/Docs/Configuration_Guide/Configuration_Guide.md  

6. PCSX2 Contributors. (n.d.).  
   PCSX2: Accurate PlayStation 2 emulation.  
   https://pcsx2.net  

---

## 🔹 Accuracy vs Performance Trade-Offs in Emulation

7. Muller, J., & Wimmer, C. (2008).  
   Virtual machine emulation: Accuracy versus performance trade-offs.  
   ACM SIGPLAN Notices, 43(7), 15–24.  
   https://doi.org/10.1145/1394608.1394611  

8. Babu, V., & Nicol, D. (2022).  
   Mechanisms for precise virtual time advancement in network emulation.  
   ACM Transactions on Modeling and Computer Simulation, 32(2), Article 9.  
   https://doi.org/10.1145/3478867  

9. Babu, V., & Nicol, D. (2020).  
   Precise virtual time advancement for network emulation.  
   In Proceedings of the ACM SIGSIM Conference on Principles of Advanced Discrete Simulation (pp. 175–186).  
   https://doi.org/10.1145/3384441.3395978  

---

## 🔹 Audio, Synchronization, and Input Timing

10. Huang, C., & Lue, H. (2010).  
    Audio-video synchronization in real-time systems.  
    IEEE Transactions on Multimedia, 12(3), 182–193.  
    https://doi.org/10.1109/TMM.2010.2040464  

11. Claypool, M., & Claypool, K. (2006).  
    Latency and player actions in online games.  
    Communications of the ACM, 49(11), 40–45.  
    https://doi.org/10.1145/1167838.1167860  

12. Sweet, M. (2014).  
    Writing interactive music for video games.  
    Addison-Wesley Professional.

---

## 🔹 Emulation as Preservation & Behavioral Fidelity

13. Kaltman, E. (2025).  
    An overview of emulation as a preservation method.  
    Council on Library and Information Resources (CLIR), Publication 194.  
    https://www.clir.org/pubs/reports/pub194/  

14. Gregory, J. (2018).  
    Game engine architecture (3rd ed.).  
    CRC Press.

---

Accuracy is behavioral.  
Stability is temporal.  
Correctness is observable.
