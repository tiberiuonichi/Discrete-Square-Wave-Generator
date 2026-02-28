# Discrete Transistor-Level Square Wave Generator

## Project Description
This project focuses on the design, simulation, and physical layout of a relaxation oscillator configured as a square wave generator. The core of the circuit is a Schmitt Trigger implemented through a custom-designed Operational Amplifier (Op-Amp) built entirely from discrete bipolar junction transistors (BJT). 

The implementation demonstrates a deep understanding of analog integrated circuit architecture, featuring a multi-stage amplifier design rather than relying on off-the-shelf integrated circuits. The project was developed using the Cadence OrCAD suite, including Capture for schematics, PSpice for analog analysis, and PCB Editor for the physical board design.

The design includes a complete manufacturing package (Drill Charts, Solder Mask, and Silk Screen layers) optimized for SMD assembly.

## Technical Specifications
- Topology: Relaxation Oscillator using a Discrete Op-Amp Schmitt Trigger
- Frequency Range: Adjustable from 38 kHz to 76 kHz
- Output Voltage (Vpp): 0 V to 4.75 V
- Load Impedance (RL): 19 kΩ
- Power Supply: Dual Rail ±9V DC
- Technology: Surface Mount Devices (SMD) and Through-Hole (THT) components

## Circuit Architecture
The discrete operational amplifier is composed of several fundamental stages:
1. Input Stage: Differential pair utilizing Q3 and Q4 (QBC846B) with an active load current mirror (Q1, Q2) to maximize open-loop gain and CMRR.
2. Intermediate Gain Stage: High-gain common emitter amplifier (Q8).
3. Output Stage: Complementary push-pull configuration (Q9, Q10) providing low output impedance and sufficient current drive for the feedback network.
4. Bias Circuitry: Transistor-based current sources (Q5, Q6) to ensure stable operating points across the entire operating range.

## Simulation and Performance Analysis
Extensive PSpice simulations were performed to validate the design across various conditions:
- Transient Analysis: Verification of the RC time constants and the switching thresholds.
- Power Analysis: Calculation of static and dynamic power dissipation to ensure thermal stability (Power_Dissipation_Map).
- Parametric Sweeps: Evaluation of the output frequency and amplitude stability relative to component tolerances.
- Bias Point Analysis: Validation of the DC operating points for all discrete stages (DC_Voltage_Bias_Points and DC_Current_Bias_Points).

## Project Structure
- /Design_Files: OrCAD Capture source files (.DSN, .OPJ).
- /Simulation: PSpice simulation profiles, waveforms, and analysis results.
- /Layout: PCB design files including the board file (.BRD) and manufacturing data.
- /BOM: Detailed Bill of Materials including manufacturer part numbers.
- /Docs: Technical reports, block diagrams, and manufacturing tables.
- /Datasheets: Technical specifications for the discrete components used in the design.

## Visual Documentation
The following results were captured during the PSpice simulation phase:
- Output Waveforms: [Maximum Peak-to-Peak Voltage](Simulation/Maximum_Peak-to-Peak_Voltage.jpg), [Minimum Peak-to-Peak Voltage](Simulation/Minimum_Peak-to-Peak_Voltage.jpg).
- Analysis: [Thermal_Analysis_Sweep](Simulation/Thermal_Analysis_Sweep.jpg), [Power Dissipation Map](Simulation/Power_Dissipation_Map.jpg).
- DC Verification: [Voltage Bias Points](Simulation/DC_Voltage_Bias_Points.jpg), [Current Bias Points](Simulation/DC_Current_Bias_Points.jpg).

## Documentation
The detailed technical report, including analytical calculations for the Op-Amp stages and PSpice simulation results, is available in the following document:
- [Technical_Report_RO.pdf](Docs/Technical_Report_RO.pdf) (Language: Romanian)

---
- **Author:** Onichi Ionut-Tiberiu
- **Academic Context:** CEF PR 2025-2026