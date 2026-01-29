# Open Source Magnetic Generator Research Platform (v3.9.2)

Zenodo Archive https://doi.org/10.5281/zenodo.18370596

Project Status Update (v3.9.2 and Forward)

After running more rigorous simulations and completing a deeper engineering audit, we identified limitations in the v3.9.2 architecture that made it unsuitable for the level of validation and measurement rigor we are aiming for. Rather than continuing forward with known gaps, we made a deliberate decision to pivot the electronics and control architecture. The revised direction is inspired by Joule Thief–style regenerative behavior, but is implemented in a fundamentally different and more controlled way, suitable for scalable testing and proper energy accounting.

What remains valid in v3: The mechanical design and STL files remain valid and may be freely used to print and assemble the physical generator. The v3 repository is retained as a historical and mechanical reference.

What is changing: The electronics, control logic, and power architecture beyond v3.9.2 are under active redesign. The newer architecture is not represented in the v3 branch and should not be considered an incremental update to it. 

Current architecture (in development): Uses ferrite-core bifilar coils, replicated across the full matrix (55 coils total). Each physical coil contains two electrically independent windings. Regenerative behavior is actively coordinated by a microcontroller, rather than relying on purely passive oscillation. The goal is to study whether JT-like flyback recovery can be synchronized, gated, and measured safely at scale, with explicit current limiting, protection, and instrumentation.

Current focus: Empirical validation at low voltage (24 V) and modest power levels (tens of watts up to ~100 W). Verifying switching behavior, timing, thermal limits, and measurement methodology before any higher-voltage or higher-power work is considered. Future updates will be published as the redesigned electronics and control system mature. Please continue to check the repository for new releases and documentation.

## Project Overview
This repository contains the complete design files and engineering documentation for a 55-coil drum-style electromechanical test platform. The system is designed as an educational tool to rigorously investigate control strategies for pulsed magnetic interaction, specifically exploring the angle-timed impulse ("timed push") mechanical oscillator concept (evaluated experimentally).

## Purpose
The goal of this project is to provide a standardized, reproducible hardware platform for researchers to:
1. Study the effects of precise pulse timing on rotor momentum.
2. Evaluate the efficiency of series-aiding bifilar coil geometries.
3. Perform honest, measurement-based energy accounting (input versus harvest).

**Disclaimer:** This project is strictly educational. No claims are made regarding net-energy gain or sustained operation. Any conclusions drawn from this hardware must be based on verifiable metrology.

## Contents
* **Documentation:** Full Student Build Guide including wiring diagrams, theory of operation, and safety protocols.
* **CAD:** Complete FreeCAD source files and print-ready STL files for the 96 mm rotor / 160 mm stator architecture.
* **Code:** Reserved directory for future reference firmware related to timing control and experimental evaluation.

## License
* **Hardware:** CERN Open Hardware Licence v2 – Weakly Reciprocal (CERN-OHL-W)
* **Documentation:** Creative Commons Attribution-ShareAlike 4.0 (CC BY-SA 4.0)

## Dedication
Dedicated to the memory of Andrei Slobodian and the preservation of his electromechanical concepts for public study.
