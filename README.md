# Compact Varactor-Controlled 2-Bit RIS Based on an ELC Resonator

A compact, ultrathin, varactor-controlled 2-bit Reconfigurable Intelligent Surface (RIS) built on an electric-inductor-capacitor (ELC) resonator unit cell. The design achieves a thickness below λ₀/20 at 5 GHz, an operating bandwidth of approximately 250 MHz, and an average reflection amplitude of about −3 dB, with all unit cells electrically interconnected to remove the need for a separate biasing layer.

## Overview

Reconfigurable Intelligent Surfaces enable programmable control over how electromagnetic waves are reflected, transforming the wireless propagation environment into a controllable medium rather than treating it as fixed and unpredictable. This work targets two persistent limitations in RIS design: the added thickness from separate biasing layers, and the narrow bandwidth typical of varactor-tuned multi-bit surfaces caused by a steep phase-vs-frequency slope.

The proposed unit cell integrates a split-ring structure with an ELC resonator and a single varactor diode (SMV2019-040LF) placed across the capacitive gap, where the electric field is most concentrated and phase tunability is most sensitive. Widening the top and bottom arms flattens the phase slope for bandwidth, and an air-gapped ground plane (0.9 mm below the substrate) further extends it. Extended horizontal arms allow adjacent unit cells to share a continuous biasing path, eliminating the need for a dedicated bias network layer.

## Design Objectives

- 2-bit phase quantization (four states, ~90° apart) at 5 GHz
- Overall thickness below λ₀/20
- Bandwidth wider than typical varactor-based multi-bit RIS designs
- No additional biasing layer

## Key Results

- **Phase range:** 270°, achieved across four bias states (00, 01, 10, 11)
- **Bandwidth:** ~250 MHz (4.75–5 GHz), roughly 5% fractional bandwidth
- **Reflection amplitude:** ~−3 dB average across operating states
- **Thickness:** λ₀/20.8 at 5 GHz (unit cell 0.1λ₀ × 0.1λ₀)
- **Biasing:** Fully interconnected unit cells; no separate bias layer required
- **Validation:** Equivalent circuit model (ECM) shows good agreement with full-wave HFSS simulation

### Functional States

| Bias Voltage | Varactor Capacitance | ∠(S₁₁) | Code |
|---|---|---|---|
| 20 V | 0.3 pF | −123° | 00 |
| 4.67 V | 0.7 pF | −213° | 01 |
| 5 V | 0.66 pF | −300° | 10 |
| 0 V | 2.22 pF | −392° | 11 |

## Structure

- **Metal layers:** Copper (σ = 5.8 × 10⁷ S/m), 0.035 mm thick
- **Substrate:** FR4 (εᵣ = 4.4, tan δ = 0.02), height = 1.6 mm
- **Air gap:** h₂ = 0.9 mm between substrate and ground plane, for bandwidth enhancement
- **Tuning element:** Varactor diode SMV2019-040LF (Lᵥ = 0.45 nH, Rᵥ = 4.8 Ω, Cᵥ = 0.3–2.22 pF)
- **Biasing chokes:** 3.5 nH inductors (LQP03HQ3N5C02D) to block high-frequency currents from entering bias lines


## Applications

Vehicular communication links, satellite platforms, and other high-mobility wireless scenarios where compact, low-profile beam control is needed.
