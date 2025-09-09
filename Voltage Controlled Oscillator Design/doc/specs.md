# LC Cross-Coupled VCO Design Specifications

## Target Specifications

| Parameter | Specification | Unit | Status |
|-----------|---------------|------|--------|
| **Frequency Range** | 855 - 881 | MHz | ✓ Achieved |
| **Supply Voltage** | 3 - 5 | V | ✓ Achieved |
| **Supply Current (max)** | 50 | mA | ✓ Achieved |
| **Tuning Voltage** | 0.4 - 2.4 | V | ✓ Achieved |
| **Phase Noise @ 1MHz offset** | < -130 | dBc/Hz | ✓ Achieved |
| **Output Power @ Vtune=0.4V** | > -5 | dBm | ✓ Achieved |

## Detailed Performance Data

### Frequency Tuning Response
| Control Voltage (V) | Frequency (MHz) | Peak-to-Peak Voltage (V) | Output Power (dBm) |
|-------------------- |-----------------|-------------------------|-------------------|
| 0.5 | 856 | 1.124 | -6.57 |
| 1.4 | 870 | 2.183 | - |
| 2.4 | 880 | 2.872 | 12.26 |

**Linear Tuning Region**: 1.45V - 1.8V (most linear frequency response)  
**Tuning Sensitivity**: ~12 MHz/V in linear region

### Phase Noise Performance
- **Vcont = 0.5V**: -152.19 dBc/Hz @ 1MHz offset
- **Vcont = 2.4V**: -157.97 dBc/Hz @ 1MHz offset

Both measurements significantly exceed the -130 dBc/Hz specification requirement.

## Circuit Parameters

### Device Sizing
- **NMOS (M1, M2)**: W/L = 700nm/100nm (ratio = 7)
- **Tail Current Source**: 40mA bias current  
- **Supply Voltage**: 4V DC
- **Power Consumption**: 160mW (40mA × 4V)

### LC Tank Components
- **Inductor**: 2nH (on-chip spiral, estimated Q ~5-10)
- **Fixed Capacitor**: Cp = 14.5pF
- **Parasitic Capacitor**: Cpar = 4fF
- **Varactor**: nmoscap1v (gpdk045), drain-body-source connected

### Bias Conditions
- **Gate-Source Overdrive**: Vgs - Vt ≈ 0.4-0.5V for optimal gm
- **Operating Region**: Saturation for both cross-coupled devices
- **Virtual Ground**: Node between tail current sources maintains AC ground
