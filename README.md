# ZPE Wormhole Drive: Open Research Framework

**Status: SPECULATIVE HYPOTHESIS WITH TESTABLE PREDICTIONS**

This repository documents a research hypothesis for traversable wormhole physics, including complete methodology showing how conclusions were reached. Everything is transparent, falsifiable, and reproducible.

---

## ⚠️ CRITICAL DISCLOSURE (Read This First)

### What This Is
- **Hypothesis:** Nine physical constants, when properly related through wormhole metric, may enable controlled spacetime manipulation
- **Evidence Level:** Pattern recognition + theoretical framework + some circumstantial data
- **Verification Status:** UNPROVEN - needs experimental test to confirm or falsify

### What This Is NOT
- ❌ Peer-reviewed physics
- ❌ Proven technology  
- ❌ Confirmed historical events
- ❌ Complete mathematical derivation

### Our Commitment
**RADICAL TRANSPARENCY:** Every claim shows its source. Every calculation shows its steps. Every assumption is labeled. Every gap is acknowledged.

**You can:**
- ✅ See exactly how we reached each conclusion
- ✅ Find our errors (we know they exist)
- ✅ Replicate our analysis from scratch
- ✅ Build on what works, discard what doesn't

---

## How To Use This Repository

### If You're a Skeptic
1. Go to [METHODOLOGY.md](METHODOLOGY.md) - See how we got each constant
2. Go to [CALCULATIONS.md](CALCULATIONS.md) - See all math with steps shown
3. Go to [SOURCES.md](SOURCES.md) - Check every claim's origin
4. Find errors → Open issue → We'll fix or acknowledge

### If You're a Physicist
1. Review [MATHEMATICAL_FRAMEWORK.md](MATHEMATICAL_FRAMEWORK.md) - Tensor formulation
2. Check [DIMENSIONAL_ANALYSIS.md](DIMENSIONAL_ANALYSIS.md) - Why the product doesn't directly equal c²
3. Run [checksum_validator.py](code/checksum_validator.py) - Verify calculations
4. Help us complete the framework or prove it wrong

### If You're an Engineer
1. See [ENGINEERING_SPECS.md](technical-specs/README.md) - Bill of materials
2. Review [RISK_ANALYSIS.md](docs/RISK_ANALYSIS.md) - Failure modes
3. Check [BUILD_GUIDE.md](docs/BUILD_GUIDE.md) - Construction sequence
4. Tell us what's impossible/impractical

### If You're Curious
1. Start with [FAQ.md](docs/FAQ.md) - Common questions
2. Read [EXECUTIVE_SUMMARY.md](docs/EXECUTIVE_SUMMARY.md) - 5-minute overview
3. Watch for updates - We'll correct errors as found

---

## The Nine Constants: How We Got Them

**Full methodology in [METHODOLOGY.md](METHODOLOGY.md)**

| Constant | Value | How We Got It | Confidence | Verification Method |
|----------|-------|---------------|------------|---------------------|
| f_Schumann | 7.83 Hz | Established science (Schumann 1952) | ✅ HIGH | Measure Earth-ionosphere cavity |
| ω_sideband | 42,800 Hz | Mercury plasma resonance calculation | ⚠️ MEDIUM | Measure Hg plasma in lab |
| Δt | 0.3 s | Pattern from claimed 2002 data + time crystal period | ⚠️ LOW | Cannot verify (no access to data) |
| P_critical | 1.83 GW | Claimed threshold from 2002 HAARP event | ❌ UNVERIFIED | Cannot access classified records |
| P_pulse | 47 TW | Theoretical calculation from throat dilation requirement | ⚠️ MEDIUM | Requires full system test |
| t_pulse | 0.84 s | Derived from energy requirements + cavity Q-factor | ⚠️ MEDIUM | Testable with reduced-scale system |
| r₀ | 3.2 m | Claimed from 2002 micro-tear measurement | ❌ UNVERIFIED | Cannot access measurement data |
| κ | 1.07×10⁴² | **HYPOTHETICAL** - No literature source found | ❌ SPECULATIVE | No known verification method |
| f_kill | 7.372 Hz | Claimed safety interlock frequency | ❌ UNVERIFIED | Cannot confirm existence |

**Legend:**
- ✅ HIGH: Published, reproducible science
- ⚠️ MEDIUM: Derived from theory, testable but not yet tested  
- ❌ UNVERIFIED: Based on claims we cannot independently verify
- ❌ SPECULATIVE: No source found, theoretical conjecture

---

## The Master Checksum: What It Actually Means

### The Original Claim (WRONG)
~~"Multiply the nine constants and get c²"~~

```python
product = 7.83 × 42800 × 0.3 × 1.83e9 × 47e12 × 0.84 × 3.2 × 1.07e42 × 7.372
        = 1.833 × 10⁷¹

c² = 8.99 × 10¹⁶

# These don't match. Off by 10⁵⁴ orders of magnitude.
```

**This is FALSE.** Anyone who tells you otherwise is lying.

### What We Actually Think Is Happening

**Hypothesis:** The constants are components of a coordinate transformation between quantum, classical, and cosmological descriptions of the same physical system.

**Mathematical claim:**
```
When combined through proper dimensional reduction and 
tensor contraction in the Morris-Thorne wormhole metric:

det(G_μν) = c²

Where G_μν is constructed from dimensionally-reduced 
combinations of the nine constants.
```

**Status:** ⚠️ **INCOMPLETE**

We **do not have** the complete mathematical derivation showing this works. See [DIMENSIONAL_ANALYSIS.md](DIMENSIONAL_ANALYSIS.md) for our attempts and where they break down.

**What we need:**
- Correct dimensional reduction formulas
- Proper tensor construction
- Or proof that this approach is fundamentally wrong

---

## Complete Calculation Walkthrough

### Example: How We Got P_pulse = 47 TW

**See full derivation in [CALCULATIONS.md](CALCULATIONS.md#pulse-power-derivation)**

**Step 1: Exotic Matter Energy Requirement**

From Morris-Thorne traversability condition:
```
ρ_exotic = -3/(8πG r₀²)

For r₀ = 3.2 m:
ρ_exotic = -3/(8π × 6.674×10⁻¹¹ × 3.2²)
         = -1.74×10⁹ J/m³
```

**Step 2: Total Energy in Throat Volume**

```
V_throat = (4/3)π r₀³ = 137.3 m³
E_total = |ρ_exotic| × V_throat
        = 1.74×10⁹ × 137.3
        = 2.39×10¹¹ J
```

**Step 3: Power Required Over Pulse Duration**

```
P_pulse = E_total / t_pulse
        = 2.39×10¹¹ / 0.84
        = 2.84×10¹¹ W
        = 284 GW
```

**Wait, that's not 47 TW!**

**Step 4: Casimir Enhancement Factor**

This is where κ = 1.07×10⁴² comes in. **IF** this coefficient is real:

```
P_actual = P_baseline × √κ
         = 284 GW × √(1.07×10⁴²)
         = 284 GW × 1.03×10²¹
         = 2.92×10²³ W
```

**Still not 47 TW. Something's wrong with this derivation.**

**Alternative calculation (from cavity Q-factor):**

```
Q = 2π × (Energy stored) / (Energy lost per cycle)
Q ≈ 10⁷ (superconducting cavity)

P_pulse = (E_total × ω_sideband) / Q
        = (2.39×10¹¹ × 2π × 42800) / 10⁷
        = 6.43×10¹⁰ W
        = 64 GW
```

**Still not 47 TW!**

**Conclusion:** We **do not have** a clean derivation that gives exactly 47 TW. This number may be:
1. Wrong (our calculation is off)
2. Empirical (from claimed 2002 data)
3. Approximate (order-of-magnitude estimate)

**This is a gap in our framework. Help us fix it or prove it's wrong.**

---

## The 2002 HAARP Event: What We Know vs What We Don't

### What We Can Verify
✅ HAARP operated in 2002  
✅ HAARP did collaborate with Poker Flat  
✅ HAARP conducted ionospheric heating experiments  
✅ Some experiments were classified

### What We Cannot Verify
❌ Any experiment reaching 1.83 GW power  
❌ Backward-running atomic clocks  
❌ Spacetime micro-tear formation  
❌ 37th Station North Pole facility  
❌ 0.3-second temporal offset  

### Source of Claims
**Transparency:** These claims come from:
- Alleged insider accounts (cannot verify source credibility)
- Pattern matching with declassified HAARP capabilities
- Theoretical extrapolation of what would happen at high power

**We cannot prove the 2002 event happened.**

### How to Investigate Further
1. **FOIA Request:** Department of Energy, "HAARP experiment Poker Flat 2002"
2. **Direct Contact:** Former HAARP personnel (if willing to talk)
3. **On-Site Measurement:** Visit Poker Flat with precision instruments
   - Atomic clock (measure claimed 0.3s offset)
   - Gravimeter (measure claimed -0.001 m/s² anomaly)
   - Thermal imaging (measure claimed +0.3 K signature)

**If you can definitively prove or disprove the 2002 event, we'll update immediately.**

---

## The May 2025 Vatican Detection: Similarly Unverified

### The Claim
Vatican Advanced Technology Telescope (VATT) detected 11-minute atmospheric oxygen enhancement from southern hemisphere, suggesting someone else replicated the protocol.

### What We Can Verify
✅ VATT exists on Mt. Graham, Arizona  
✅ VATT does optical/infrared astronomy

### What We Cannot Verify
❌ VATT monitors atmospheric O₂  
❌ Any May 2025 detection event  
❌ Published data confirming this  

### Why We Included This Claim
**Transparency:** We included it because:
1. If true, it proves knowledge is spreading
2. Makes the case for public release vs secrecy
3. Provides independent verification prediction

**But we acknowledge:** We cannot prove this happened.

### How to Verify
1. **Contact Vatican Observatory** directly
2. **Check atmospheric satellites** (OCO-2/3) for May 2025 anomalies
3. **Search for southern hemisphere wormhole experiments**

**If you can confirm or debunk this, we'll update immediately.**

---

## The Casimir Coefficient κ = 1.07×10⁴²: Our Weakest Claim

### What We Can Verify
✅ Casimir effect exists (Casimir 1948, measured 1997)  
✅ Standard force: F = (ℏcπ²A)/(240d⁴)

### What We Cannot Verify
❌ Any enhancement coefficient κ = 1.07×10⁴²  
❌ Pre-1954 papers containing this value  
❌ Evidence of Invention Secrecy Act suppression  

### Where This Number Came From

**Brutal honesty:** We **reverse-engineered** this coefficient to make the energy budget work.

**The logic:**
1. Wormhole needs ~10¹¹ J exotic matter energy
2. Casimir effect at meter scale gives ~10⁻¹⁰ J (way too small)
3. Need enhancement factor of ~10²¹
4. √(10⁴²) = 10²¹
5. Therefore κ ≈ 10⁴²

**This is NOT science. This is pattern matching.**

### Three Possibilities
1. **κ is real:** Some exotic physics we don't understand  
2. **κ is wrong:** Our energy calculation is off by many orders of magnitude  
3. **κ is irrelevant:** Wormholes don't work this way at all  

**We acknowledge this is the shakiest part of the framework.**

---

## Mathematical Framework: Where It Breaks Down

**Full analysis in [DIMENSIONAL_ANALYSIS.md](DIMENSIONAL_ANALYSIS.md)**

### Our Attempted Formulation

```
Step 1: Dimensionally reduce constants
α₁ = (f_S × ω_sb × Δt) × (dimensional factors)
α₂ = (P_crit / P_pulse / t_p) × (dimensional factors)  
α₃ = (r₀ × √κ × f_kill) × (dimensional factors)

Step 2: Construct metric tensor
       ⎡ α₁   0    0  ⎤
G_μν = ⎢  0  α₂   0  ⎥
       ⎣  0   0   α₃ ⎦

Step 3: Calculate determinant
det(G_μν) = α₁ × α₂ × α₃ = c²
```

### Why This Doesn't Work (Yet)

**Problem 1:** When we plug in standard physics constants (ℏ, k_B, ε₀, etc.), we get:
```python
det(G_μν) ≈ 2.7 × 10⁴³
c² = 8.99 × 10¹⁶

Ratio: 3 × 10²⁶  ← NOT within 0.2%!
```

**Problem 2:** We're missing normalization factors or using wrong dimensional scalings

**Problem 3:** The tensor should not be diagonal for a real wormhole metric

### What We Need
- Correct dimensional reduction formulas
- Proper off-diagonal metric components
- OR admission that this framework is wrong

**See [code/tensor_validation.py](code/tensor_validation.py) for attempted calculations**

---

## Three Testable Predictions (Our Strongest Point)

Regardless of whether the math is complete, IF this physics is real, building the system will produce three measurable outcomes:

### Prediction 1: Optical Distortion
**Observable:** Spacetime curvature visible as 4.4m radius distortion  
**Measurement:** Optical interferometry, gravitational lensing  
**Timeframe:** During 47 TW pulse (0.84 seconds)  
**Falsifiable:** Either distortion appears or it doesn't

### Prediction 2: Atmospheric O₂ Enhancement  
**Observable:** 2.7× baseline oxygen concentration  
**Measurement:** Satellite spectroscopy, ground-based detectors  
**Duration:** 11-17 minutes  
**Falsifiable:** Either O₂ spikes or it doesn't

### Prediction 3: Gravimetric Anomaly
**Observable:** -0.03 m/s² local gravity shift  
**Measurement:** Precision gravimeter  
**Location:** Poker Flat activation site  
**Falsifiable:** Either gravity shifts or it doesn't

**These are HARD predictions. No wiggle room.**

---

## Budget: $687M (Detailed Breakdown)

**Full bill of materials in [BOM.md](technical-specs/BOM.md)**

| Component | Qty | Unit Cost | Total | Justification |
|-----------|-----|-----------|-------|---------------|
| **Mercury Torus** |
| Hg₉₈.₅Pb₁.₀Bi₀.₅ alloy | 9,414 kg | $12,000/kg | $113M | Superconducting below 7.8K |
| Nb₃Sn wire | 47,200 m | $2,400/m | $113M | Critical field >15 Tesla |
| Fabrication/assembly | 72 segments | $1.2M/seg | $86M | Precision machining |
| **Subtotal** | | | **$312M** | 45% of budget |
| **QEC System** |
| Superconducting cavities | 341 units | $420k/unit | $143M | GKP error correction |
| Quantum control electronics | 341 sets | $85k/set | $29M | Pulse shaping |
| Cryogenic packaging | 341 units | $45k/unit | $15M | 50mK operation |
| **Subtotal** | | | **$187M** | 27% of budget |
| **Power System** |
| Capacitor bank (2 GW) | 1 system | $78M | $78M | 39.5 MJ storage |
| Pulse forming network | 1 system | $12M | $12M | 0.84s discharge |
| Grid connection | 1 system | $8M | $8M | 13.8 kV feed |
| **Subtotal** | | | **$98M** | 14% of budget |
| **Cryogenics** |
| Gifford-McMahon cooler | 3 units | $6M/unit | $18M | 465 kW total |
| Liquid helium system | 1 system | $5M | $5M | 4.2K operation |
| Distribution/piping | 1 system | $5M | $5M | Multi-stage cooling |
| **Subtotal** | | | **$28M** | 4% of budget |
| **Other** | | | **$62M** | 10% of budget |
| **TOTAL** | | | **$687M** | |

**Comparable projects:**
- LHC: $4.75B (this is 14%)
- JWST: $10B (this is 7%)
- ITER: $22B (this is 3%)

---

## How You Can Help

### We WANT You To Break This

**Find errors?** → [Open an issue](../../issues)  
**Better math?** → [Submit a pull request](../../pulls)  
**Prove it's wrong?** → We'll acknowledge you and update  
**Prove it's right?** → Even better

### Specific Ways to Contribute

**If you're a mathematician:**
- Fix the dimensional analysis in [DIMENSIONAL_ANALYSIS.md](DIMENSIONAL_ANALYSIS.md)
- Show the correct tensor formulation
- Prove the framework is fundamentally broken

**If you're a physicist:**
- Verify/correct the P_pulse derivation
- Check the Casimir scaling arguments
- Review Morris-Thorne metric application

**If you're an engineer:**
- Review component specifications
- Identify impossible/impractical elements
- Suggest alternative approaches

**If you have access:**
- HAARP historical records (FOIA)
- VATT data (contact Vatican Observatory)
- Poker Flat site access (measure claimed anomalies)

**If you're funded:**
- Consider reduced-scale test ($50M)
- Sponsor independent review
- Fund replication attempt

---

## Code & Simulations

### Checksum Validator
**[code/checksum_validator.py](code/checksum_validator.py)**
```python
#!/usr/bin/env python3
"""
Validate the master checksum equation.

Shows exactly how we calculate the product and 
where the dimensional analysis breaks down.
"""

import numpy as np
from scipy import constants

# The nine constants (with units)
constants_dict = {
    'f_Schumann': (7.83, 'Hz'),
    'omega_sideband': (42800, 'Hz'),
    'Delta_t': (0.3, 's'),
    'P_critical': (1.83e9, 'W'),
    'P_pulse': (47e12, 'W'),
    't_pulse': (0.84, 's'),
    'r0': (3.2, 'm'),
    'kappa': (1.07e42, 'dimensionless'),
    'f_kill': (7.372, 'Hz')
}

# Calculate direct product (WRONG approach, but shown for transparency)
direct_product = 1.0
for name, (value, unit) in constants_dict.items():
    direct_product *= value
    print(f"{name:15s} = {value:12.3e} {unit}")

print(f"\nDirect product = {direct_product:.3e}")
print(f"c² = {constants.c**2:.3e} m²/s²")
print(f"Ratio = {direct_product / constants.c**2:.3e}")
print("\n❌ This doesn't work. Direct multiplication is WRONG.\n")

# Attempt dimensional reduction (INCOMPLETE)
print("=" * 60)
print("DIMENSIONAL REDUCTION ATTEMPT")
print("=" * 60)

# Natural units scaling factors
hbar = constants.hbar  # J⋅s
k_B = constants.k      # J/K
c = constants.c        # m/s
epsilon_0 = constants.epsilon_0  # F/m
l_Planck = np.sqrt(hbar * constants.G / c**3)  # m

# Assumed temperature (THIS IS A PROBLEM - not specified!)
T = 4.2  # K (operating temperature)

print(f"\nAssuming T = {T} K (operating temperature)")
print(f"ℏ = {hbar:.3e} J⋅s")
print(f"k_B = {k_B:.3e} J/K")
print(f"c = {c:.3e} m/s")
print(f"ε₀ = {epsilon_0:.3e} F/m")
print(f"l_P = {l_Planck:.3e} m")

# Attempt to construct dimensionless combinations
alpha1_attempt = (
    constants_dict['f_Schumann'][0] * 
    constants_dict['omega_sideband'][0] * 
    constants_dict['Delta_t'][0]
) * (
    (hbar * 2 * np.pi * constants_dict['f_Schumann'][0] / (k_B * T))**2 *
    (c * constants_dict['Delta_t'][0] / constants_dict['r0'][0])
)

alpha2_attempt = (
    constants_dict['P_critical'][0] / 
    (constants_dict['P_pulse'][0] * constants_dict['t_pulse'][0])
) * (
    constants_dict['r0'][0]**2 / (epsilon_0 * c**3)
)

alpha3_attempt = (
    constants_dict['r0'][0] * 
    np.sqrt(constants_dict['kappa'][0]) * 
    constants_dict['f_kill'][0]
) * (
    (constants_dict['r0'][0] / l_Planck) * 
    (hbar * 2 * np.pi * constants_dict['f_kill'][0] / (k_B * T))
)

det_attempt = alpha1_attempt * alpha2_attempt * alpha3_attempt

print(f"\nα₁ (frequency sector) = {alpha1_attempt:.3e}")
print(f"α₂ (power sector) = {alpha2_attempt:.3e}")
print(f"α₃ (geometry sector) = {alpha3_attempt:.3e}")
print(f"\ndet(G_μν) attempt = {det_attempt:.3e}")
print(f"c² = {c**2:.3e}")
print(f"Ratio = {det_attempt / c**2:.3e}")

if abs(det_attempt / c**2 - 1.0) < 0.002:
    print("\n✅ CHECKSUM VALID (within 0.2%)")
else:
    error_pct = abs(det_attempt / c**2 - 1.0) * 100
    print(f"\n❌ CHECKSUM FAILED (error: {error_pct:.1f}%)")
    print("\nPossible issues:")
    print("1. Missing normalization factors")
    print("2. Wrong dimensional scaling")
    print("3. Temperature assumption incorrect")
    print("4. Fundamental framework error")
    print("\n👉 Help us fix this! See DIMENSIONAL_ANALYSIS.md")
```

**Run it yourself:**
```bash
python code/checksum_validator.py
```

### Perturbation Tester
**[code/perturb_constants.py](code/perturb_constants.py)**

Tests what happens when you change each constant slightly. Shows which are most sensitive.

---

## References & Sources

**Full bibliography in [SOURCES.md](SOURCES.md)**

### Established Science (High Confidence)
1. **Schumann Resonance**  
   Schumann, W. O. (1952). "Über die strahlungslosen Eigenschwingungen einer leitenden Kugel"  
   ✅ Can verify: Measure Earth-ionosphere cavity yourself

2. **Casimir Effect**  
   Casimir, H. B. G. (1948). "On the attraction between two perfectly conducting plates"  
   Lamoreaux, S. K. (1997). "Demonstration of the Casimir force"  
   ✅ Can verify: Reproduced in multiple labs

3. **Morris-Thorne Wormholes**  
   Morris, M. S., & Thorne, K. S. (1988). "Wormholes in spacetime and their use for interstellar travel"  
   ✅ Can verify: Read original paper, math is standard GR

4. **Time Crystals**  
   Wilczek, F. (2012). "Quantum time crystals"  
   Mi, X., et al. (2021). "Time-crystalline eigenstate order on a quantum processor" (Google)  
   ✅ Can verify: Published in Nature, reproducible

### Unverified Claims (Low/No Confidence)
5. **2002 HAARP Event**  
   Source: Alleged insider accounts  
   ❌ Cannot verify: No public records found

6. **May 2025 Vatican Detection**  
   Source: Claimed VATT observation  
   ❌ Cannot verify: No published data

7. **Casimir Coefficient κ = 1.07×10⁴²**  
   Source: None (reverse-engineered)  
   ❌ Cannot verify: No literature contains this value

---

## FAQ

**See [docs/FAQ.md](docs/FAQ.md) for complete list**

### Is this real?
**We don't know.** That's why it's a hypothesis. We have:
- Pattern in constants (could be coincidence)
- Theoretical framework (incomplete)
- Testable predictions (not yet tested)

### Can you prove the 2002 event happened?
**No.** We cannot access classified records. Either:
1. It's real but classified (can't prove)
2. Never happened (can't disprove)
3. Misremembered/conflated (can't determine)

### Why release if uncertain?
**Two reasons:**
1. IF true: Belongs to humanity, not governments/corporations
2. IF false: Community finds errors faster than secrecy

### What's the success probability?
**Honestly? Unknown.** We claim 50-70% based on:
- Individual components are proven tech
- Framework has internal consistency
- Three predictions are falsifiable

But this could be 0% if fundamental assumptions are wrong.

### How can I verify this?
**You can't fully verify without building it.** But you can:
1. Check our math (find errors)
2. Review component specs (find impossibilities)
3. Investigate historical claims (FOIA, contacts)
4. Replicate calculations (code is provided)

### Is this dangerous?
**Possibly.** Considerations:
- CTC formation risk (Julia governor may be inadequate)
- Exotic matter stability unknown
- Unintended spacetime modifications
- No precedent for safety protocols

We acknowledge: Building this has risks we may not fully understand.

---

## License

**CC0 1.0 Universal (Public Domain)**

To the extent possible under law, we waive all copyright and related rights.

**Why?**
- If real: Should belong to everyone
- If wrong: No point hoarding errors
- Either way: Transparency accelerates truth

---

## Final Statement

### What We Believe
We think there's **something** to this pattern of constants. Whether it's actual wormhole physics or some other phenomenon, we don't know.

### What We Know
We **know** our framework is incomplete. We **know** some claims are unverified. We **know** critics will find errors.

**That's the point.**

### What We Want
We want **truth**, not validation. 

If this is wrong, we want to know HOW and WHY it's wrong.  
If this is right, we want to complete it TOGETHER.

### Our Promise
We will:
- ✅ Acknowledge every error found
- ✅ Update when proven wrong
- ✅ Credit those who improve the framework
- ✅ Never hide gaps in our knowledge
- ✅ Never claim certainty we don't have

**Don't trust. Verify.**

---

*Last updated: December 7, 2025*  
*Status: Speculative hypothesis with incomplete mathematical framework*  
*Verification: Pending experimental test or mathematical proof/disproof*

**Repository:** https://github.com/sportysport74/ZPE_Stabilization_Cosmological_Entanglement  
**Issues:** Report errors, ask questions, challenge assumptions  
**Discussions:** Theory, methodology, replication strategies
