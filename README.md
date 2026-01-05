# 🚅 System Hazard Analysis: High Speed Railway (ERTMS/ETCS L2)

**Course:** Safety in Automation Systems (Politecnico di Milano)  
**Context:** Rome-Naples High-Speed/High-Capacity (HS/HC) Line

This project delivers a complete safety and hazard analysis for the Rome-Naples railway section, which was the first in Europe to operate under the **ERTMS/ETCS Level 2** standard. The goal was to identify critical vulnerabilities in the signaling system and calculate the probability of catastrophic failure using industry-standard methods. [file:13]

## 📝 Project Overview

We analyzed the interaction between the **Ground Subsystem** (RBC, Interlocking) and the **On-Board Subsystem** (EVC, DMI, Odometer) to understand how failures propagate in a system that relies entirely on digital radio communication rather than physical trackside signals.

### The System
*   **Line:** 205 km, double track, max speed 300 km/h.
*   **Standard:** ETCS Level 2 (GSM-R for data, Eurobalises for positioning).
*   **Operating Modes:** Full Supervision (nominal) vs. Partial Supervision (degraded).

## 🛠️ Analysis Performed

We followed the standard safety lifecycle to break down the system:

### 1. Functional & Architectural Analysis
Mapped out the logical architecture, focusing on the data flow between the **Radio Block Center (RBC)** and the train's **European Vital Computer (EVC)**.

### 2. Preliminary Hazard Analysis (PHA)
Identified high-level risks using severity/probability matrices.
*   *Key Hazards:* Train collision, Derailment (overspeed), Stop failure.
*   *Outcome:* Classified risks for passengers, infrastructure, and rolling stock.

### 3. FMEA (Failure Mode and Effect Analysis)
Bottom-up analysis of specific component failures. We looked at what happens when:
*   The **Odometer** drifts or loses calibration.
*   The **GSM-R** connection drops.
*   The **Balise Reader** fails to detect a location reference.

### 4. FTA (Fault Tree Analysis)
We built a quantitative fault tree to calculate the probability of the top event: **"Train Crash"**.
*   **Top Event Probability:** Estimated at $3.1 \times 10^{-6}$ (over a 10-year interval).
*   **Critical Path:** The analysis showed that the EVC and RBC electronics are the single most critical points of failure (~20% importance ranking each).

### 5. Event Trees (ET) & Cause-Consequence
Modeled specific scenarios, such as a **DMI (Screen) Malfunction** or an **EVC Error**, to see if the emergency braking system would correctly intervene to prevent an accident. [file:13]

## 📄 Report
The full analysis, including the detailed probability calculations and risk matrices, is available here:
[**Download Full Report (PDF)**](./SHA-of-a-HSHC-Railway-Safety-in-Automation-Systems-Project-a.y.-2019-2020-Franco-Luna-Savino-2.pdf)

## 👥 Contributors
*   Alex Miguel Franco Martínez
*   David Estebán Luna Sanchez
*   Giuseppe Matteo Daniele Savino
