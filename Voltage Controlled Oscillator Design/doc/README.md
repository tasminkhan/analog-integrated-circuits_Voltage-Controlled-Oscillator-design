# LC Cross-Coupled Voltage Controlled Oscillator

## Overview
This project presents the design and implementation of an LC tank voltage controlled oscillator using cross-coupled NMOS differential pair topology. The VCO targets wireless communication applications requiring low phase noise and stable oscillation characteristics in the 855-881 MHz frequency range.

## Design Tools
- **Cadence Virtuoso**: Schematic capture, simulation, and layout design
- **Process Design Kit**: gpdk045 (45nm CMOS technology)
- **Device Libraries**: nmos1v, nmoscap1v for varactor implementation
- **Simulation Engine**: Spectre for AC, DC, transient, and noise analysis
- **Layout Verification**: Implementation with generic inductor and capacitor cells and DRC and LVS check

## Design Methodology

### Circuit Architecture Selection
The project evaluates two primary VCO topologies:
- **Ring VCO**: High integration, low power, wide tuning range but poor phase noise at high frequencies
- **LC VCO**: Superior phase noise performance, narrow tuning range, higher power consumption

**Selected: LC VCO** for optimal phase noise performance required in RF applications despite area and power trade-offs.

### Design Approach
1. **Tank Design**: 2nH inductor with variable capacitor network using varactors
2. **Active Circuit**: Cross-coupled NMOS differential pair for negative resistance generation
3. **Bias Network**: 40mA tail current source for stable operation
4. **Frequency Control**: Dual varactor configuration with center-tap tuning voltage

### Key Consideration

- Active circuit must provide sufficient negative conductance to overcome tank losses
- Transconductance requirement: gm ≥ 2/RT where RT represents total tank resistance
- Bias current optimization balancing noise performance vs. power consumption
- Varactor capacitance variation: Ctank_min to Ctank_max determines tuning range
- Decrese in tank's capacitance to mitigate the effect of parasitic capacitance on frequency and phase noise

## Applications
- Wireless communication systems (GSM, WiFi frequency bands)
- Phase-locked loops for frequency synthesis
- Clock generation for high-speed digital systems
- RF front-end local oscillator applications
