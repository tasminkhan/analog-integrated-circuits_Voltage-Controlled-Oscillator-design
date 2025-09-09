# Analog Integrated Circuit Design Exercises

This collection showcases progressive analog IC design exercises, from fundamental device characterization to complex circuit implementations using Cadence Virtuoso and standard design methodologies.

## 01: MOSFET Characteristics Study
**Focus**: Single-stage common source CMOS amplifier analysis  
**Key Topics**: I-V characteristics, threshold voltage extraction, transconductance analysis, mobility comparison between NMOS/PMOS  
**Tools**: Cadence Virtuoso, gpdk090 PDK  

Analysis includes device parameter extraction across different process corners (TT, SS, FF) and performance trade-offs in amplifier configurations.

## 02: Common Source Amplifier Topologies
**Focus**: Five different CS amplifier load configurations  
**Key Topics**: Resistive, diode-connected, current-source, active, and triode loads  
**Analysis**: Gain-bandwidth trade-offs, output swing limitations, power consumption  

Systematic comparison of amplifier topologies examining voltage gain, linearity, and design constraints for each configuration.

## 03: Layout Design and Verification
**Focus**: Physical implementation of CS amplifier with current source load  
**Key Topics**: Layout design rules, DRC verification, LVS checking  
**Tools**: Virtuoso Layout Suite, PVS verification, gpdk045 PDK  

Hands-on experience with IC layout design including minimum geometry calculations, design rule compliance, and schematic-layout correlation.

## 04: Bandgap Reference Circuit
**Focus**: Temperature-compensated voltage reference design  
**Key Topics**: Temperature coefficient analysis, supply voltage regulation, bipolar device integration  
**Specifications**: 1.2V output with zero temperature coefficient at room temperature  

Implementation of classical bandgap architecture using CMOS and bipolar devices for precision voltage generation.

## 05: Two-Stage Operational Amplifier
**Focus**: Complete op-amp design with compensation  
**Key Topics**: AC/DC analysis, frequency response, CMRR, PSRR measurements  
**Specifications**: >5000 V/V gain, 5MHz GBW, 10V/μs slew rate  

Comprehensive op-amp design covering stability analysis, common-mode rejection, power supply rejection, and performance optimization across process corners.
