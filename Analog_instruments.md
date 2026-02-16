# Analog Instruments
## Complete Study Guide for AP ECET

![Topic](https://img.shields.io/badge/Topic-Analog%20Instruments-blue)
![Weightage](https://img.shields.io/badge/Weightage-25%25-orange)
![Questions](https://img.shields.io/badge/Expected%20Questions-4--5-green)

---

## 📚 Table of Contents

1. [Topic Overview](#topic-overview)
2. [Extension of Range of Ammeter](#1-extension-of-range-of-ammeter)
3. [Extension of Range of Voltmeter](#2-extension-of-range-of-voltmeter)
4. [Extension of Range of Ohmmeter](#3-extension-of-range-of-ohmmeter)
5. [FET Voltmeter](#4-fet-voltmeter)
6. [Differential Voltmeter](#5-differential-voltmeter)
7. [Practice Questions with Explanations](#practice-questions-with-explanations)

---

## Topic Overview

### What are Analog Instruments?

Analog instruments display measurements using a continuous scale with a moving pointer. Unlike digital instruments that show discrete numerical values, analog instruments provide readings through the physical deflection of a pointer across a calibrated scale.

### Sub-topics Covered

| Sub-topic | Weightage | Priority |
|-----------|-----------|----------|
| Extension of Ammeter Range | 20% | HIGH |
| Extension of Voltmeter Range | 25% | HIGH |
| Extension of Ohmmeter Range | 15% | MEDIUM |
| FET Voltmeter | 25% | HIGH |
| Differential Voltmeter | 15% | MEDIUM |

---

## 1. Extension of Range of Ammeter

### Basic Concept

An ammeter measures electric current flowing through a circuit. Every ammeter has a maximum current capacity called **full-scale deflection current (Im)**. When circuit current exceeds this value, the meter can be damaged.

**Problem:** How to measure currents larger than the meter's capacity?

**Solution:** Use a **shunt resistor** connected in **parallel** with the ammeter.

---

### Why Parallel Connection?

```
Current Flow Understanding:

When a low resistance (shunt) is connected in parallel:
- Current divides between shunt and meter
- Most current flows through shunt (low resistance path)
- Only small, safe current flows through meter
- Total current can be calculated from meter reading
```

### Circuit Diagram

```
                    I (Total Current to measure)
                           │
           ┌───────────────┼───────────────┐
           │               │               │
           │          ┌────┴────┐          │
           │          │         │          │
          Ish         │   Im    │          │
           │          │   ↓     │          │
           ↓          │  ┌───┐  │          │
       ┌───────┐      │  │   │  │          │
       │ Rsh   │      │  │ Rm│  │          │
       │(Shunt)│      │  │   │  │          │
       └───┬───┘      │  └───┘  │          │
           │          │  Meter  │          │
           │          └────┬────┘          │
           │               │               │
           └───────────────┼───────────────┘
                           │
                           ↓
                      To Circuit

Where:
- I = Total current to be measured
- Im = Current through meter (full-scale deflection current)
- Ish = Current through shunt
- Rm = Meter resistance
- Rsh = Shunt resistance
```

---

### Working Principle

**Step 1:** Total current (I) enters the parallel combination

**Step 2:** Current divides based on resistance values
- Lower resistance → More current
- Higher resistance → Less current

**Step 3:** Current division follows the rule:
- Ish × Rsh = Im × Rm (Voltage across parallel elements is equal)

**Step 4:** Total current I = Im + Ish

---

### Derivation of Formulas

**Starting Point:**
Since shunt and meter are in parallel, voltage across both is equal.

```
Voltage across meter = Voltage across shunt
Im × Rm = Ish × Rsh

Also, total current:
I = Im + Ish
Therefore: Ish = I - Im

Substituting:
Im × Rm = (I - Im) × Rsh

Solving for Rsh:
Rsh = (Im × Rm) / (I - Im)
```

**Introducing Multiplying Factor (n):**
```
n = I / Im = Total current / Meter current

This represents how many times the range is extended.

Substituting in the formula:
Rsh = (Im × Rm) / (I - Im)
Rsh = (Im × Rm) / (n×Im - Im)
Rsh = (Im × Rm) / (Im × (n - 1))
Rsh = Rm / (n - 1)
```

---

### Final Formulas

| Formula | Description |
|---------|-------------|
| **n = I / Im** | Multiplying factor |
| **Rsh = Rm / (n - 1)** | Shunt resistance (using n) |
| **Rsh = (Im × Rm) / (I - Im)** | Shunt resistance (direct) |

---

### Key Points to Remember

```
✓ Shunt is connected in PARALLEL
✓ Shunt has LOW resistance
✓ Most current bypasses through shunt
✓ Shunt protects the meter from excess current
✓ Higher the range extension → Lower the shunt resistance
✓ Shunt material: Manganin or Constantan (low temperature coefficient)
```

---

### Practical Considerations

**Shunt Requirements:**
- Very low resistance (milliohms to few ohms)
- Low temperature coefficient of resistance
- High current carrying capacity
- Stable over time

**Common Shunt Materials:**
- Manganin (copper-manganese-nickel alloy)
- Constantan (copper-nickel alloy)

---

## 2. Extension of Range of Voltmeter

### Basic Concept

A voltmeter measures potential difference (voltage) across a component. Every voltmeter has a maximum voltage capacity. When circuit voltage exceeds this value, the meter can be damaged.

**Problem:** How to measure voltages larger than the meter's capacity?

**Solution:** Use a **multiplier resistor** connected in **series** with the voltmeter.

---

### Why Series Connection?

```
Voltage Division Understanding:

When a high resistance (multiplier) is connected in series:
- Total voltage divides between multiplier and meter
- Most voltage drops across multiplier
- Only small, safe voltage appears across meter
- Total voltage can be calculated from meter reading
```

### Circuit Diagram

```
        ←───────────── V (Total Voltage) ─────────────→
        
        +                                              -
        │                                              │
        │     Rs (Multiplier)              Rm          │
        ├────────/\/\/\/\/───────────────/\/\/\/───────┤
        │                                              │
        │     ←─── Vs ───→            ←─── Vm ───→     │
        │                                              │
        │                    Meter                     │
        │                                              │
        
Where:
- V = Total voltage to be measured
- Vm = Voltage across meter (full-scale deflection voltage)
- Vs = Voltage across multiplier (series resistor)
- Rm = Meter resistance
- Rs = Multiplier (series) resistance
```

---

### Working Principle

**Step 1:** Total voltage (V) appears across the series combination

**Step 2:** Voltage divides based on resistance values
- Higher resistance → More voltage drop
- Lower resistance → Less voltage drop

**Step 3:** Same current flows through both (series connection):
- Im = V / (Rs + Rm)

**Step 4:** Voltage division:
- Vm = Im × Rm
- Vs = Im × Rs
- V = Vm + Vs

---

### Derivation of Formulas

**Starting Point:**
Current through series combination is same.

```
Total voltage:
V = Vm + Vs
V = Im × Rm + Im × Rs
V = Im × (Rm + Rs)

For original meter (without multiplier):
Vm = Im × Rm

Dividing:
V / Vm = (Rm + Rs) / Rm
```

**Introducing Multiplying Factor (n):**
```
n = V / Vm = New range / Original range

Therefore:
n = (Rm + Rs) / Rm
n × Rm = Rm + Rs
Rs = Rm × (n - 1)

Also, Total Resistance:
Rtotal = Rm + Rs = n × Rm
```

---

### Final Formulas

| Formula | Description |
|---------|-------------|
| **n = V / Vm** | Multiplying factor |
| **Rs = Rm × (n - 1)** | Multiplier resistance |
| **Rtotal = n × Rm** | Total voltmeter resistance |

---

### Key Points to Remember

```
✓ Multiplier is connected in SERIES
✓ Multiplier has HIGH resistance
✓ Most voltage drops across multiplier
✓ Multiplier protects meter from excess voltage
✓ Higher the range extension → Higher the multiplier resistance
✓ Multiplier material: Usually carbon or wire-wound resistors
```

---

### Comparison: Ammeter vs Voltmeter Extension

| Parameter | Ammeter | Voltmeter |
|-----------|---------|-----------|
| Element used | Shunt | Multiplier |
| Connection | Parallel | Series |
| Resistance value | Low | High |
| Purpose | Bypass excess current | Drop excess voltage |
| Formula | Rsh = Rm/(n-1) | Rs = Rm×(n-1) |

---

## 3. Extension of Range of Ohmmeter

### Basic Concept

An ohmmeter measures resistance by passing a known current through the unknown resistor and measuring the resulting voltage drop, or vice versa.

**Key Feature:** Ohmmeter contains an internal battery that depletes over time, affecting accuracy.

---

### Types of Ohmmeters

**1. Series Type Ohmmeter:**
- Unknown resistance connected in series
- Zero on right side of scale
- Infinity on left side

**2. Shunt Type Ohmmeter:**
- Unknown resistance connected in parallel
- Zero on left side of scale
- Infinity on right side

---

### Series Type Ohmmeter Circuit

```
    ┌────────────────────────────────────────┐
    │                                        │
    │   ┌───┐    R1 (Zero Adj)    Rx        │
    ├───┤ E ├───/\/\/\/\/───┬───/\/\/\/─────┤
    │   └───┘               │               │
    │   Battery        ┌────┴────┐          │
    │                  │  Meter  │          │
    │                  │  (Rm)   │          │
    │                  └────┬────┘          │
    │                       │               │
    └───────────────────────┴───────────────┘

Where:
- E = Internal battery
- R1 = Zero adjustment resistor
- Rm = Meter resistance
- Rx = Unknown resistance to be measured
```

---

### Working Principle

**When Rx = 0 (Short Circuit):**
- Maximum current flows
- Pointer shows ZERO resistance (full-scale deflection)

**When Rx = ∞ (Open Circuit):**
- No current flows
- Pointer shows INFINITY resistance (no deflection)

**For any Rx:**
- Current is inversely related to Rx
- Scale is NON-LINEAR

---

### Zero Adjustment

**Why Zero Adjustment is Needed:**
```
As battery ages:
- Battery voltage decreases
- Current through circuit decreases
- Full-scale deflection not achieved when Rx = 0
- Readings become inaccurate

Zero adjustment compensates for:
- Battery voltage changes
- Ensures accurate zero reading
- Must be done before each measurement
```

**Procedure:**
1. Short circuit the terminals (Rx = 0)
2. Adjust R1 until pointer reads exactly zero
3. Now the meter is calibrated for current battery voltage

---

### Scale Characteristics

```
Ohmmeter Scale (Non-Linear):

    ∞    50   20   10   5    2    1    0
    ├────┼────┼────┼────┼────┼────┼────┤
    │    │    │    │         │         │
    ↑                                  ↑
    No                              Full
    deflection                   deflection

Key Points:
- Scale is REVERSED (zero on right)
- Scale is NON-LINEAR (cramped at high values)
- Mid-scale resistance = Internal resistance (half-scale reading)
```

---

### Key Points to Remember

```
✓ Zero adjustment compensates for BATTERY AGING
✓ Scale is NON-LINEAR
✓ Scale is REVERSED compared to ammeter/voltmeter
✓ Must calibrate before each use
✓ Internal resistance affects accuracy
✓ Mid-scale reading = Internal resistance
```

---

## 4. FET Voltmeter

### Basic Concept

FET (Field Effect Transistor) voltmeter uses a FET at its input stage to achieve extremely high input impedance, minimizing the loading effect on the circuit being measured.

---

### Why High Input Impedance is Important?

**Loading Effect Problem:**

```
When measuring voltage in a circuit:

Original Circuit:           With Conventional Voltmeter:
                            
    R1                          R1
    ┌─/\/\/─┬─                  ┌─/\/\/─┬─
    │       │                   │       │
   Vs      R2   Actual         Vs    R2 ║ Rm   Measured
    │       │   Voltage             │   │      Voltage
    └───────┴─                  └───────┴─

Problem:
- Voltmeter resistance (Rm) parallels R2
- Effective resistance decreases
- Measured voltage differs from actual voltage
- This error is called LOADING EFFECT
```

---

### How FET Voltmeter Solves This

**FET Input Characteristics:**
- Gate draws almost zero current
- Input impedance: 10^12 Ω or higher
- Negligible loading effect
- Accurate measurement of high-impedance circuits

---

### Block Diagram

```
    ┌─────────────────────────────────────────────────────┐
    │                  FET VOLTMETER                       │
    │                                                      │
    │   Input          FET           DC              PMMC  │
    │    ○────┬────┤ Input ├────► Amplifier ────► Meter   │
    │         │    │ Stage │                              │
    │         │    └───────┘                              │
    │        ═╧═                                          │
    │      (Very high                                     │
    │       input Z)                                      │
    │                                                      │
    └─────────────────────────────────────────────────────┘

Signal Flow:
1. Input voltage applied to FET gate
2. FET provides impedance transformation
3. DC amplifier increases signal level
4. PMMC meter displays reading
```

---

### FET Input Stage Circuit

```
                        +Vdd
                          │
                          RL
                          │
    Input ────┬──────────┤├── Output
              │          │
              │         FET
             Rin        │
        (10^12 Ω)       │
              │         Rs
              │          │
             ═╧═        ═╧═
             GND        GND

Characteristics:
- Gate current ≈ 0 (only leakage)
- Input impedance = Very High
- No loading on measured circuit
```

---

### Comparison: Conventional vs FET Voltmeter

| Parameter | Conventional Voltmeter | FET Voltmeter |
|-----------|----------------------|---------------|
| Input Impedance | 10-20 kΩ/V | 10^10 to 10^12 Ω |
| Loading Effect | Significant | Negligible |
| Accuracy in High-Z circuits | Poor | Excellent |
| Cost | Lower | Higher |
| Complexity | Simple | More complex |
| Power requirement | Self-powered | Needs power supply |

---

### Advantages of FET Voltmeter

```
1. Very high input impedance (10^12 Ω)
2. Negligible loading effect
3. Can measure in high-impedance circuits
4. Accurate measurement of sensitive circuits
5. Wide frequency range
6. High sensitivity
```

### Disadvantages of FET Voltmeter

```
1. Requires external power supply
2. More expensive than conventional meters
3. More complex circuitry
4. Temperature sensitivity of FET
5. Requires careful handling
```

---

### Applications

```
✓ Measuring voltage in high-impedance circuits
✓ pH meter measurements
✓ Biological signal measurements
✓ Vacuum tube circuit measurements
✓ Capacitor voltage measurements
✓ Any application where loading must be minimized
```

---

### Key Points to Remember

```
✓ Main advantage: HIGH INPUT IMPEDANCE
✓ Minimizes LOADING EFFECT
✓ Uses FET at input stage
✓ Input impedance: 10^10 to 10^12 Ω
✓ Essential for high-impedance circuit measurements
✓ Requires external power supply
```

---

## 5. Differential Voltmeter

### Basic Concept

A differential voltmeter measures voltage by comparing the unknown voltage with a known reference voltage using the **null balance** technique. At balance, the difference between two voltages is zero.

---

### Principle of Operation

**Null Balance Method:**
```
Unknown Voltage (Vx) is compared with Reference Voltage (Vr)

At null (balance):
Vx = Vr

The null detector shows ZERO when both voltages are equal.
Reference voltage is read from calibrated dial.
```

---

### Block Diagram

```
    ┌─────────────────────────────────────────────────────┐
    │              DIFFERENTIAL VOLTMETER                 │
    │                                                      │
    │                        ┌──────────────┐              │
    │    Vx ────────────────┤              │              │
    │    (Unknown)          │     NULL     │              │
    │                       │   DETECTOR   ├───► Display  │
    │    Vr ────────────────┤              │   (Zero at   │
    │    (Reference)        │              │    balance)  │
    │        ↑              └──────────────┘              │
    │        │                                            │
    │   ┌────┴─────┐                                      │
    │   │ Precision │                                      │
    │   │ Reference │                                      │
    │   │ Source    │                                      │
    │   └──────────┘                                      │
    │                                                      │
    └─────────────────────────────────────────────────────┘

Operation:
1. Apply unknown voltage Vx
2. Adjust reference voltage Vr
3. When null detector shows zero, Vx = Vr
4. Read Vr from calibrated dial = measured voltage
```

---

### Working Principle

**Step 1:** Unknown voltage Vx applied to one input

**Step 2:** Reference voltage Vr adjusted using precision potentiometer

**Step 3:** Null detector compares both voltages

**Step 4:** When Vx = Vr:
- Difference = 0
- Null detector shows zero deflection
- This is the BALANCE condition

**Step 5:** At balance, Vx equals the dial reading of Vr

---

### Key Features

**At Null Balance:**
```
When Vx = Vr:
- No current flows through null detector
- Input impedance becomes INFINITE
- No loading effect whatsoever
- Maximum accuracy achieved
```

---

### Advantages

```
1. Very HIGH ACCURACY (0.001% possible)
2. No loading effect at balance
3. High resolution (can detect µV differences)
4. Excellent for calibration purposes
5. Independent of null detector sensitivity at balance
6. Can measure very small voltages accurately
```

### Disadvantages

```
1. Manual balancing required (slower)
2. More complex than direct reading meters
3. Requires precision reference source
4. Higher cost
5. Not suitable for rapidly changing voltages
```

---

### Applications

```
✓ Calibration of other voltmeters
✓ Precision voltage measurements
✓ Standards laboratory measurements
✓ Measurement of small DC voltages
✓ Thermocouple measurements
✓ Potentiometer calibration
```

---

### Key Points to Remember

```
✓ Works on NULL BALANCE principle
✓ Compares unknown with reference voltage
✓ At balance: Vx = Vr
✓ Very HIGH ACCURACY measurement
✓ No loading effect at null
✓ Used for precision and calibration work
✓ Measures very small voltages accurately
```

---

## Practice Questions with Explanations

### Question 1

**The range of an ammeter can be extended by connecting a:**
- A) High resistance in series
- B) Low resistance in parallel
- C) High resistance in parallel
- D) Low resistance in series

**Correct Answer: B**

**Explanation:**

To extend ammeter range, we need to bypass excess current around the meter. This requires:

**Why Parallel?**
- Ammeter must remain in series with the circuit to measure current
- A parallel path allows excess current to bypass the meter
- Current divides between meter and bypass path

**Why Low Resistance?**
- Lower resistance provides easier path for current
- Most current flows through low resistance path (shunt)
- Only safe amount passes through meter

**Why Not Other Options?**

| Option | Why Incorrect |
|--------|---------------|
| A) High R in series | Would reduce total current, not extend range |
| C) High R in parallel | Very little current would bypass meter |
| D) Low R in series | Would affect circuit operation, not protect meter |

---

### Question 2

**A voltmeter has resistance of 10 kΩ and reads up to 10V. To extend its range to 100V, the multiplier resistance required is:**
- A) 80 kΩ
- B) 90 kΩ
- C) 100 kΩ
- D) 110 kΩ

**Correct Answer: B**

**Explanation:**

**Given:**
- Meter resistance (Rm) = 10 kΩ
- Original range (Vm) = 10 V
- New range (V) = 100 V

**Step 1:** Calculate multiplying factor
```
n = V / Vm
n = 100 / 10
n = 10
```

**Step 2:** Apply multiplier resistance formula
```
Rs = Rm × (n - 1)
Rs = 10 kΩ × (10 - 1)
Rs = 10 kΩ × 9
Rs = 90 kΩ
```

**Verification:**
```
Total resistance = Rm + Rs = 10 kΩ + 90 kΩ = 100 kΩ
Current at full scale = 100V / 100kΩ = 1 mA
Voltage across meter = 1 mA × 10 kΩ = 10V ✓
```

---

### Question 3

**The main advantage of FET voltmeter over conventional voltmeter is:**
- A) Low input impedance
- B) High input impedance
- C) Low cost
- D) Simple construction

**Correct Answer: B**

**Explanation:**

**Why High Input Impedance is the Main Advantage:**

FET voltmeter has input impedance of 10^10 to 10^12 Ω compared to conventional voltmeter's 10-20 kΩ/V.

**Impact of High Input Impedance:**

```
High Input Impedance Results In:
├── Negligible loading effect
├── Accurate measurements in high-Z circuits
├── Minimal current drawn from circuit
└── True voltage reading without disturbance
```

**Why Other Options are Incorrect:**

| Option | Why Incorrect |
|--------|---------------|
| A) Low input impedance | FET voltmeter has HIGH impedance, not low |
| C) Low cost | FET voltmeters are MORE expensive |
| D) Simple construction | FET voltmeters are MORE complex |

---

### Question 4

**In an ohmmeter, zero adjustment is done to compensate for:**
- A) Change in temperature
- B) Change in battery voltage
- C) Change in external resistance
- D) Change in meter sensitivity

**Correct Answer: B**

**Explanation:**

**Why Battery Voltage Compensation?**

```
Ohmmeter Operation:
├── Internal battery provides current
├── Current creates deflection proportional to resistance
└── Full-scale deflection = Zero resistance

When Battery Ages:
├── Voltage decreases
├── Current decreases (for same circuit)
├── Full-scale deflection NOT achieved at Rx = 0
└── All readings become INACCURATE
```

**Zero Adjustment Process:**
1. Short circuit terminals (Rx = 0)
2. Adjust zero adjust resistor
3. Set pointer to exactly zero ohms
4. This compensates for reduced battery voltage

**Why Other Options are Incorrect:**

| Option | Why Incorrect |
|--------|---------------|
| A) Temperature | Not primary purpose of zero adjustment |
| C) External resistance | Zero adjustment is internal calibration |
| D) Meter sensitivity | Sensitivity is fixed characteristic |

---

### Question 5

**Differential voltmeter is used for measuring:**
- A) Very high voltages
- B) Very low voltages with high accuracy
- C) AC voltages only
- D) Current

**Correct Answer: B**

**Explanation:**

**Why High Accuracy for Low Voltages?**

```
Differential Voltmeter Characteristics:
├── Null balance principle
├── Compares unknown with precision reference
├── At balance: Zero current through detector
├── No loading effect at null
└── Extremely high accuracy achievable
```

**Accuracy Capability:**
- Resolution: Can detect microvolt differences
- Accuracy: 0.001% or better possible
- Ideal for precision measurements

**Why Other Options are Incorrect:**

| Option | Why Incorrect |
|--------|---------------|
| A) Very high voltages | Not primary application |
| C) AC voltages only | Primarily used for DC measurements |
| D) Current | It measures voltage, not current |

---

### Question 6

**To measure a current of 100 mA using an ammeter with full-scale deflection of 10 mA and internal resistance of 5 Ω, the shunt resistance required is:**
- A) 0.45 Ω
- B) 0.50 Ω
- C) 0.55 Ω
- D) 0.60 Ω

**Correct Answer: C**

**Explanation:**

**Given:**
- Total current (I) = 100 mA
- Meter current (Im) = 10 mA
- Meter resistance (Rm) = 5 Ω

**Method 1: Using Multiplying Factor**
```
Step 1: Calculate n
n = I / Im = 100 / 10 = 10

Step 2: Calculate Rsh
Rsh = Rm / (n - 1)
Rsh = 5 / (10 - 1)
Rsh = 5 / 9
Rsh = 0.555 Ω ≈ 0.55 Ω
```

**Method 2: Direct Formula**
```
Rsh = (Im × Rm) / (I - Im)
Rsh = (10 mA × 5 Ω) / (100 mA - 10 mA)
Rsh = 50 mV / 90 mA
Rsh = 0.555 Ω ≈ 0.55 Ω
```

**Verification:**
```
Voltage across parallel combination:
V = Im × Rm = 10 mA × 5 Ω = 50 mV

Current through shunt:
Ish = V / Rsh = 50 mV / 0.555 Ω = 90 mA

Total current:
I = Im + Ish = 10 mA + 90 mA = 100 mA ✓
```

---

### Question 7

**A 0-10V voltmeter has a resistance of 1000 ohms. The resistance required to convert it to 0-50V range is:**
- A) 4000 Ω in series
- B) 4000 Ω in parallel
- C) 5000 Ω in series
- D) 5000 Ω in parallel

**Correct Answer: A**

**Explanation:**

**Given:**
- Original range = 10 V
- New range = 50 V
- Meter resistance (Rm) = 1000 Ω

**Step 1:** Calculate multiplying factor
```
n = V2 / V1 = 50 / 10 = 5
```

**Step 2:** Calculate multiplier resistance
```
Rs = Rm × (n - 1)
Rs = 1000 × (5 - 1)
Rs = 1000 × 4
Rs = 4000 Ω
```

**Step 3:** Connection type
- Voltmeter range extension uses SERIES connection
- Therefore: **4000 Ω in series**

**Why Not Parallel?**
- Parallel connection is for ammeter range extension
- Voltmeter needs series multiplier to drop excess voltage

---

### Question 8

**FET voltmeter is preferred for measuring voltage across:**
- A) Low impedance circuits
- B) High impedance circuits
- C) Only resistive circuits
- D) Only reactive circuits

**Correct Answer: B**

**Explanation:**

**Why High Impedance Circuits?**

```
Loading Effect Analysis:

In High-Z Circuit:
├── Circuit resistance is high
├── Conventional meter's resistance comparable to circuit
├── Significant loading effect occurs
├── Measured voltage ≠ Actual voltage
└── FET voltmeter's very high input Z → No loading

In Low-Z Circuit:
├── Circuit resistance is low
├── Any meter's resistance >> circuit resistance
├── Loading effect minimal anyway
├── Conventional meter works fine
└── FET voltmeter not specifically needed
```

**Practical Example:**
```
Measuring in 1 MΩ circuit:
- Conventional (20 kΩ/V × 10V = 200 kΩ): Significant loading
- FET voltmeter (10^12 Ω): Negligible loading
```

---

### Question 9

**The shunt resistance of an ammeter should be:**
- A) Very high
- B) Very low
- C) Equal to meter resistance
- D) Infinite

**Correct Answer: B**

**Explanation:**

**Why Very Low Resistance?**

```
Purpose of Shunt:
├── Bypass most of the current around meter
├── Only allow safe current through meter
└── Protect meter from excessive current

Current Division Principle:
├── Current prefers low resistance path
├── If Rsh is low → Most current through shunt
├── If Rsh is high → Most current through meter (dangerous!)
└── Therefore, Rsh must be VERY LOW
```

**Mathematical Proof:**
```
For range extension of 10x (n = 10):
Rsh = Rm / (n - 1) = Rm / 9

If Rm = 9 Ω, then Rsh = 1 Ω
Shunt is 9 times smaller than meter resistance
```

**Why Other Options are Incorrect:**

| Option | Why Incorrect |
|--------|---------------|
| A) Very high | Would not bypass current effectively |
| C) Equal to Rm | Would only double the range |
| D) Infinite | No current bypass, no range extension |

---

### Question 10

**In a differential voltmeter, at null balance:**
- A) Maximum current flows through detector
- B) No current flows through detector
- C) Current oscillates
- D) Detector shows maximum deflection

**Correct Answer: B**

**Explanation:**

**Null Balance Condition:**

```
At Balance:
├── Unknown voltage (Vx) = Reference voltage (Vr)
├── Potential difference across detector = 0
├── No driving force for current
└── Current through detector = ZERO

Physical Understanding:
├── Detector connected between Vx and Vr points
├── When Vx = Vr, both points at same potential
├── No potential difference = No current flow
└── Detector shows ZERO (null) reading
```

**Why This is Important:**
```
At Null Balance:
├── Zero current means infinite input impedance
├── No loading effect on measured circuit
├── Maximum accuracy achieved
└── Reading depends only on reference source accuracy
```

---

### Question 11

**The sensitivity of a voltmeter is expressed in:**
- A) Ohms
- B) Amperes
- C) Ohms per volt
- D) Volts per ohm

**Correct Answer: C**

**Explanation:**

**Voltmeter Sensitivity Definition:**

```
Sensitivity (S) = Total Resistance / Voltage Range
                = Rtotal / V
                = Ohms / Volt
                = Ω/V

Alternatively:
S = 1 / Im
Where Im = Full-scale deflection current
```

**Practical Meaning:**
```
If sensitivity = 20,000 Ω/V:
├── For 10V range: Input resistance = 20,000 × 10 = 200 kΩ
├── For 50V range: Input resistance = 20,000 × 50 = 1 MΩ
└── Higher sensitivity = Higher input resistance = Less loading
```

**Why Other Options are Incorrect:**

| Option | Why Incorrect |
|--------|---------------|
| A) Ohms | This is resistance, not sensitivity |
| B) Amperes | This is current unit |
| D) Volts per ohm | Inverted, incorrect unit |

---

### Question 12

**When measuring resistance with an ohmmeter, the pointer indicates:**
- A) Linear scale reading
- B) Non-linear scale reading
- C) Exponential reading
- D) Logarithmic reading

**Correct Answer: B**

**Explanation:**

**Why Non-Linear Scale?**

```
Ohmmeter Current Equation:
I = E / (R + Rx)

Where:
├── E = Battery voltage (constant)
├── R = Internal resistance (constant)
└── Rx = Unknown resistance (variable)

Current vs Resistance Relationship:
├── When Rx = 0: I = E/R (maximum current)
├── When Rx = R: I = E/2R (half current)
├── When Rx = ∞: I = 0 (zero current)

This relationship is HYPERBOLIC, not linear.
Therefore, scale is NON-LINEAR.
```

**Scale Characteristics:**
```
Ohmmeter Scale:
├── Compressed at high resistance end
├── Expanded at low resistance end
├── Zero on right (full-scale deflection)
├── Infinity on left (no deflection)
└── Most accurate readings near mid-scale
```

---

### Question 13

**A multiplier is connected in _____ with the voltmeter to extend its range:**
- A) Series
- B) Parallel
- C) Series-parallel
- D) None of these

**Correct Answer: A**

**Explanation:**

**Why Series Connection?**

```
Voltage Division Requirement:
├── Total voltage must divide between multiplier and meter
├── Series connection creates voltage divider
├── Multiplier drops excess voltage
└── Safe voltage appears across meter

Series Connection Properties:
├── Same current through both components
├── Voltage divides proportionally to resistance
├── Higher resistance → Higher voltage drop
└── Multiplier (high R) → Drops most voltage
```

**Circuit Analysis:**
```
        ←─────────── V (Total) ──────────→
        
        Rs (Multiplier)         Rm (Meter)
        ───/\/\/\/\/───────────/\/\/\/───
        
        ←── Vs (dropped) ──→←── Vm (safe) ──→

For proper operation:
├── Rs >> Rm (for large range extension)
├── Most voltage drops across Rs
└── Only rated voltage appears across Rm
```

---

### Question 14

**The input impedance of FET voltmeter is in the range of:**
- A) Few ohms
- B) Few kilo ohms
- C) Few mega ohms
- D) 10^10 to 10^12 ohms

**Correct Answer: D**

**Explanation:**

**FET Input Characteristics:**

```
FET Gate Properties:
├── Gate is insulated from channel
├── Only leakage current flows (pA range)
├── Input appears as very high resistance
└── Typical values: 10^10 to 10^14 Ω

For FET Voltmeter:
├── FET at input stage
├── Input impedance: 10^10 to 10^12 Ω
├── Much higher than conventional meters
└── Enables measurement without loading
```

**Comparison:**
```
┌─────────────────────┬────────────────────┐
│ Meter Type          │ Input Impedance    │
├─────────────────────┼────────────────────┤
│ PMMC (moving coil)  │ Few Ω to kΩ       │
│ Conventional VOM    │ 10-50 kΩ          │
│ VTVM (vacuum tube)  │ 1-10 MΩ           │
│ FET Voltmeter       │ 10^10 - 10^12 Ω   │
└─────────────────────┴────────────────────┘
```

---

### Question 15

**Zero adjustment in an ohmmeter is required because:**
- A) To set the pointer to zero position initially
- B) To compensate for battery voltage reduction
- C) To increase the range
- D) To decrease sensitivity

**Correct Answer: B**

**Explanation:**

**Battery Aging Effect:**

```
Fresh Battery Condition:
├── Battery voltage = Rated value
├── At Rx = 0: Full current flows
├── Pointer reaches zero ohms mark
└── Accurate readings obtained

Aged Battery Condition:
├── Battery voltage decreased
├── At Rx = 0: Less current flows
├── Pointer does NOT reach zero mark
├── All readings are WRONG
└── Zero adjustment compensates for this

Zero Adjustment Mechanism:
├── Adjustable resistor in circuit
├── Compensates for reduced battery voltage
├── Restores full-scale deflection at Rx = 0
└── Must be done before each measurement session
```

**Why Not Other Options:**

| Option | Why Incorrect |
|--------|---------------|
| A) Initial position | Pointer naturally rests at infinity, not zero |
| C) Increase range | Zero adjustment doesn't change range |
| D) Decrease sensitivity | Not related to sensitivity |

---

## Quick Revision Summary

### Ammeter Range Extension
```
- Shunt in PARALLEL
- LOW resistance
- Rsh = Rm / (n - 1)
- Bypasses excess current
```

### Voltmeter Range Extension
```
- Multiplier in SERIES
- HIGH resistance
- Rs = Rm × (n - 1)
- Drops excess voltage
```

### Ohmmeter
```
- Zero adjustment for battery compensation
- Non-linear scale
- Scale is reversed (zero on right)
```

### FET Voltmeter
```
- HIGH input impedance (10^10 - 10^12 Ω)
- Negligible loading effect
- For high-impedance circuit measurement
```

### Differential Voltmeter
```
- Null balance principle
- Very HIGH ACCURACY
- No loading at balance
- Vx = Vr at null
```

---

## Formula Quick Reference

| Application | Formula |
|-------------|---------|
| Multiplying factor (Ammeter) | n = I / Im |
| Shunt resistance | Rsh = Rm / (n - 1) |
| Multiplying factor (Voltmeter) | n = V / Vm |
| Multiplier resistance | Rs = Rm × (n - 1) |
| Total voltmeter resistance | Rtotal = n × Rm |
| Voltmeter sensitivity | S = 1 / Im = Ω/V |

---

*End of Analog Instruments Study Guide*
