# Mercury Torus Assembly - Technical Specifications

## Overview

The mercury torus is the primary containment vessel for plasma generation and exotic matter production. It consists of 7 nested spherical shells with golden ratio scaling, operating at 4.2 K.

## Geometric Specifications

| Parameter | Value |
|-----------|-------|
| Major radius (R_major) | 11.0 m (36 ft) |
| Minor radius (r_minor) | 0.8 m (2.6 ft) |
| Volume | 138.5 m³ |
| Surface area | 347.7 m² |
| Wall thickness | 25 mm |
| Number of segments | 72 |

## Materials

### Structural Layer
- **Material:** 316L stainless steel
- **Function:** Structural support, vacuum containment
- **Thickness:** 20 mm

### Superconducting Layer  
- **Material:** Nb₃Sn (niobium-tin)
- **Critical temperature:** 18.3 K
- **Thickness:** 3 mm
- **Function:** RF cavity, magnetic shielding

### Topological Superconductor Coating
- **Composition:** Hg₉₈.₅Pb₁.₀Bi₀.₅
- **Critical temperature:** 7.8 K
- **Thickness:** 2 mm
- **Function:** Majorana zero mode generation (topological protection)

## Deposition Protocol

```
1. Substrate preparation
   - Surface cleaning: Ar ion sputtering, 500 eV, 30 min
   - Base pressure: < 10⁻¹⁰ Torr
   
2. Co-sputtering deposition
   - Hg target: 98.5% power
   - Pb target: 1.0% power  
   - Bi target: 0.5% power
   - Substrate temperature: 100 K
   - Deposition rate: 0.5 nm/s
   - Total time: 67 minutes (for 2 mm)
   
3. Quality control
   - STM verification of Majorana signatures
   - Zero-bias conductance peak FWHM < 100 μeV
   - Acceptance criteria: > 95% surface coverage
```

## Mercury Fill System

| Parameter | Value |
|-----------|-------|
| Mercury mass | 13,124 kg (13.1 tons) |
| Vapor pressure | 10 Pa at 300 K |
| Ionization fraction | 0.7% |
| Electron density | 7 × 10²² m⁻³ |
| Purity | 99.9999% (6N) |

### Handling & Safety

- Closed-loop recirculation (zero environmental release)
- EPA compliance for industrial mercury use
- Emergency containment: Activated carbon absorption
- Personnel protection: Full HAZMAT suits, respirators

## Cost Breakdown

| Item | Cost |
|------|------|
| Nb₃Sn fabrication | $87.3M |
| Hg-Pb-Bi coating | $184.6M |
| Mercury (13.1 tons @ $50/kg) | $0.7M |
| Purification | $17.5M |
| Cryostat | $22.3M |
| **Total** | **$312.4M** |

## Procurement

- **Nb₃Sn supplier:** ATI Specialty Materials or Western Superconducting
- **Mercury source:** Bethlehem Apparatus or Alfa Aesar (distilled under vacuum)
- **Cryostat:** Cryomech or Sumitomo (SHI) custom build
- **Lead time:** 18-24 months (Hg-Pb-Bi coating is critical path)

## References

See main operational manual Section 5.2 for complete derivations.
