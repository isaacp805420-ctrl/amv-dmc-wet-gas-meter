
# AMV-DMC: Adaptive Multi-Variable System for High-Accuracy Wet Gas Measurement

## Overview
The **Adaptive Multi-Variable Differential and Mass Compensation (AMV-DMC)** system is a pre-assembled spool skid designed to meet strict industrial wet gas measurement requirements. Built for upstream lines from oil treatment to compression plants, it achieves expanded uncertainty within $\pm3\%$ (targeting $\pm2\%$ to $\pm2.5\%$ at $90\%$ to $99\%$ GVF) through dynamic sensor fusion.

## Operating Envelope
* **Line Size:** 4" pilot spool (scalable to 2"–6")
* **Operating Pressure:** 30 to 70 bar
* **Temperature:** Up to 80°C
* **Target Uncertainty:** $\pm2.0\%$ to $\pm2.5\%$ expanded uncertainty (95% confidence level) at $90\%$ to $99\%$ GVF.

---

## Technical Approach & Sensor Train
The spool maintains minimum straight runs of **10D upstream** and **5D downstream** of the Venturi element:

1. **Capacitance Ring Sensor (Upstream):** Measures dielectric permittivity to derive liquid volume fraction. Water cut is supplied via periodic lab updates or operator input.
2. **Modified Venturi ($\Delta P$):** Provides primary gas flow measurement. Wet gas over-reading is corrected using established correlations (e.g., de Leeuw model), mapping liquid loading from the capacitance sensor to estimate the Lockhart-Martinelli parameter ($\le 0.3$).
3. **Coriolis Meter (Optional):** Used purely as a density cross-check to flag inconsistencies between capacitance and $\Delta P$ readings (excluded from fallback mode).
4. **Signal Fusion & Dynamic Compensation:** Integrates capacitance, $\Delta P$, and Coriolis density in a real-time compensation matrix.
5. **Robust Fallback Strategy:** If signal fusion drifts under severe slugging, the system automatically defaults to a reliable Venturi-plus-capacitance correction mode.

---

## Validation Roadmap (12-Week MVP)
* **Weeks 1–4 (Algorithm Tuning):** Ingest historical GVF datasets, finalize correction matrix, and run parallel safety/permit reviews.
* **Weeks 5–8 (Flow-Loop Test):** 5-day campaign at a partner facility matching line gas density ratios to validate core accuracy claims.
* **Weeks 9–12 (Field Pilot):** 30-day trial on an active line, benchmarking against existing facility allocation meters (Success Criterion: sustained mean deviation within $\pm3.0\%$).

---

## Minimum Viable Budget ($25,000 Scope)
* **Hardware ($10,000):** Machined Venturi insert, pressure transducers, capacitance ring assembly.
* **Flow-Loop Testing ($10,000):** 5-day facility window.
* **Field Integration & Reporting ($5,000):** Data logging hardware, firmware flashing, and technical reporting.

---

## Governing Standards & Compliance
* Aligned with **ISO/TR 11583** (Wet gas flow measurement with pressure differential devices).
* Draws on guidance from **ISO/TR 12748** (Natural gas operations).
* Hazardous-area compliance via certified ATEX/IECEx Zone 1 components and standard safety barriers.

