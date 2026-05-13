# batteries - 3 voltage-capacity

## Understanding Battery Voltage and Capacity

Voltage and capacity are the two most important specifications of any battery. Voltage determines the electrical "pressure" and compatibility with devices, while capacity determines how long a battery will last between charges or replacements.

This document explains these fundamental concepts in detail, including how to measure them, what affects them, and how to interpret battery specifications.

## Battery Voltage

### What is Voltage in a Battery?

Voltage is the electrical potential difference between the positive and negative terminals of a battery. It represents the "pressure" that pushes electrons through a circuit.

```
VOLTAGE ANALOGY

    Water System                      Electrical System
    ──────────────────────────────────────────────────────────────
    Water pressure (PSI)          =    Voltage (Volts)
    Water flow (gallons/minute)   =    Current (Amperes)
    Pipe restriction              =    Resistance (Ohms)
    Water wheel                   =    Motor / Load


    VISUAL REPRESENTATION:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Low Voltage (1.5V)         High Voltage (12V)             │
    │                                                             │
    │   ┌─────┐                    ┌─────┐                        │
    │   │ 1.5V│                    │ 12V │                        │
    │   └──┬──┘                    └──┬──┘                        │
    │      │                          │                           │
    │      ▼                          ▼                           │
    │    (trickle)             (strong flow)                      │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

### Nominal vs Actual Voltage

Battery voltage is not constant throughout its life.

```
NOMINAL VOLTAGE

    The "advertised" voltage printed on the battery

    Examples:
    ├── Alkaline AA:  1.5V nominal
    ├── NiMH AA:      1.2V nominal
    ├── Li-ion 18650: 3.7V nominal
    └── Car battery:  12V nominal (6 cells × 2.1V)


    ACTUAL VOLTAGE VARIES:

    Condition           Alkaline AA    NiMH AA      Li-ion 18650
    ──────────────────────────────────────────────────────────────
    Brand new (OCV)     1.60-1.65V     1.40-1.45V   3.60-3.70V
    Under load (fresh)  1.50-1.55V     1.30-1.35V   3.50-3.60V
    During use          1.0-1.5V       1.1-1.3V     3.0-3.6V
    Cutoff (device stops) 0.8-1.0V     1.0V         2.8-3.0V
    Fully discharged    0.8-1.0V       1.0V         2.5-3.0V
    Over-discharged     <0.8V          <0.8V        <2.5V (damage!)
```

### Open Circuit Voltage (OCV)

Voltage measured with no load connected.

```
OPEN CIRCUIT VOLTAGE

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Voltmeter                                                 │
    │   ┌─────┐                                                   │
    │   │  V  │                                                   │
    │   └──┬──┘                                                   │
    │      │                                                      │
    │    ┌─┴─┐ ┌─┴─┐                                              │
    │    │ + │ │ - │                                              │
    │    └───┘ └───┘                                              │
    │      │     │                                                │
    │   ┌──┴─────┴──┐                                             │
    │   │  BATTERY  │  (no load connected)                        │
    │   └───────────┘                                             │
    │                                                             │
    │   OCV = Highest possible voltage from battery               │
    │   OCV decreases as battery discharges                       │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    OCV vs STATE OF CHARGE (resting, 25°C)

    Alkaline (1.5V nominal):
    SoC (%)    OCV (V)
    ──────────────────
    100        1.60-1.65
    90         1.55-1.60
    75         1.50-1.55
    50         1.45-1.50
    25         1.35-1.45
    10         1.25-1.35
    5          1.15-1.25
    0          <1.10

    NiMH (1.2V nominal):
    SoC (%)    OCV (V)
    ──────────────────
    100        1.40-1.45
    90         1.38-1.42
    75         1.35-1.40
    50         1.28-1.32
    25         1.20-1.25
    10         1.15-1.20
    5          1.10-1.15
    0          <1.00

    Li-ion (3.7V nominal):
    SoC (%)    OCV (V)
    ──────────────────
    100        4.15-4.20
    90         4.05-4.10
    75         3.95-4.00
    50         3.72-3.78
    25         3.58-3.63
    10         3.40-3.45
    5          3.30-3.35
    0          2.50-3.00
```

### Voltage Under Load

Voltage drops when current flows due to internal resistance.

```
VOLTAGE UNDER LOAD

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Voltmeter           Load (e.g., light bulb)               │
    │   ┌─────┐            ┌─────┐                                │
    │   │  V  │            │     │                                │
    │   └──┬──┘            └──┬──┘                                │
    │      │                  │                                   │
    │    ┌─┴─┐ ┌─┴─┐        ┌─┴─┐                                 │
    │    │ + │ │ - │        │   │                                 │
    │    └───┘ └───┘        └───┘                                 │
    │      │     │            │                                   │
    │   ┌──┴─────┴──┐         │                                   │
    │   │  BATTERY  ├─────────┘                                   │
    │   └───────────┘                                             │
    │                                                             │
    │   V_load = V_OCV - I × R_int                                │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    VOLTAGE DROP EXAMPLE:

    Alkaline AA battery:
    ├── OCV = 1.60V
    ├── Internal resistance = 0.2Ω (200mΩ)
    ├── Load current = 500mA (0.5A)
    │
    └── V_load = 1.60V - (0.5A × 0.2Ω) = 1.60V - 0.10V = 1.50V


    LOAD VOLTAGE BY DISCHARGE RATE (AA alkaline)

    Current    V_load (fresh)    V_load (50% discharged)
    ──────────────────────────────────────────────────────
    10mA       1.55V             1.45V
    100mA      1.50V             1.35V
    500mA      1.40V             1.20V
    1000mA     1.30V             1.00V (device cutoff)
    2000mA     1.10V             0.80V (severely sagged)
```

### Cutoff Voltage

The minimum voltage a device needs to operate.

```
CUTOFF VOLTAGE EXPLANATION

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Device stops working when voltage drops below cutoff      │
    │                                                             │
    │   Voltage                                                   │
    │        │                                                    │
    │    1.6 ┼●                                                   │
    │        │ ╲                                                  │
    │    1.4 ┼  ╲                                                 │
    │        │   ╲                                                │
    │    1.2 ┼    ╲                                               │
    │        │     ╲                                              │
    │    1.0 ┼      ●────────────────────────────────────────     │
    │        │      │                                             │
    │        │      │ (device stops - battery still has           │
    │    0.8 ┼      │  capacity left!)                            │
    │        │      │                                             │
    │        └──────┴────────────────────────────────────► Time   │
    │            │                                                │
    │            ▼                                                │
    │         Cutoff Voltage (device dependent)                   │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    TYPICAL CUTOFF VOLTAGES:

    Device Type                 Cutoff Voltage (per cell)    Notes
    ──────────────────────────────────────────────────────────────
    TV remote                   1.0-1.1V                    Works well with alkaline
    LED flashlight              0.9-1.0V                    Some work with NiMH
    Digital camera              1.0-1.1V                    NiMH recommended
    Motorized toy               0.8-1.0V                    May work with NiMH
    Wall clock                  1.2-1.3V                    Needs alkaline (1.5V)
    Smoke detector              1.2-1.3V                    Use alkaline only
    Arduino / microcontroller   3.0-3.3V (for 3.3V logic)   Needs boost converter for 1.5V


    PROBLEM WITH HIGH CUTOFF DEVICES:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Alkaline battery in a device with 1.2V cutoff:           │
    │   ├── Battery still has 30-40% capacity                    │
    │   ├── But voltage dropped to 1.2V                          │
    │   ├── Device thinks battery is dead                        │
    │   └── Battery discarded with usable energy remaining!      │
    │                                                             │
    │   Solution: Use NiMH (holds 1.2V for most of discharge)    │
    │   or use device with lower cutoff.                         │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

### Voltage by Chemistry

```
NOMINAL VOLTAGES COMPARISON

    Chemistry               Nominal V    Full V    Cutoff V    Notes
    ──────────────────────────────────────────────────────────────
    Alkaline                1.5V         1.65V     0.8-1.0V    Primary
    Zinc-carbon             1.5V         1.60V     0.8-0.9V    Primary (obsolete)
    Lithium primary (1.5V)  1.5V         1.80V     0.8-1.0V    Primary
    Lithium primary (3V)    3.0V         3.30V     2.0V        Coin cells (CR2032)
    NiCd                    1.2V         1.45V     1.0V        Rechargeable
    NiMH                    1.2V         1.45V     1.0V        Rechargeable
    Lead-acid (per cell)    2.1V         2.45V     1.75V       Rechargeable
    Lead-acid (12V)         12.6V        14.4V     10.5V       Car battery
    Li-ion (NMC)            3.7V         4.20V     2.8-3.0V    Rechargeable
    LiFePO₄                 3.2V         3.65V     2.5V        Rechargeable
    LiPo                    3.7V         4.20V     3.0V        Rechargeable
    LTO                     2.4V         2.80V     1.5V        Rechargeable


    SERIES VOLTAGES (common battery packs):

    Cells in series    Alkaline    NiMH/NiCd    Li-ion    Lead-acid
    ──────────────────────────────────────────────────────────────
    1                  1.5V        1.2V         3.7V      2.1V
    2                  3.0V        2.4V         7.4V      4.2V
    3                  4.5V        3.6V         11.1V     6.3V
    4                  6.0V        4.8V         14.8V     8.4V
    5                  7.5V        6.0V         18.5V     10.5V
    6                  9.0V        7.2V         22.2V     12.6V (car)
    10                 15.0V       12.0V        37.0V     21.0V
    20                 30.0V       24.0V        74.0V     42.0V
```

## Battery Capacity

### What is Capacity?

Capacity is the amount of charge a battery can store, measured in ampere-hours (Ah) or milliampere-hours (mAh).

```
CAPACITY DEFINITION

    1 Ah = 1 ampere of current for 1 hour
    1 Ah = 1000 mAh


    VISUAL REPRESENTATION (2000mAh battery):

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   2000mA (2A) ─────────────────────────────────► 1 hour    │
    │                                                             │
    │   1000mA (1A) ──────────────────────────► 2 hours          │
    │                                                             │
    │   500mA ────────────────────► 4 hours                      │
    │                                                             │
    │   250mA ──────────► 8 hours                               │
    │                                                             │
    │   125mA ────► 16 hours                                    │
    │                                                             │
    │   62mA ─► 32 hours                                        │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    CAPACITY FORMULA:

    Capacity (Ah) = Current (A) × Time (hours)

    Examples:
    ├── 2000mAh = 2A × 1 hour = 1A × 2 hours = 0.5A × 4 hours
    └── 500mAh = 0.5A × 1 hour = 0.25A × 2 hours = 0.1A × 5 hours
```

### Ampere-hour (Ah) vs Watt-hour (Wh)

Understanding the difference between charge capacity and energy capacity.

```
Ah vs Wh EXPLANATION

    Ampere-hour (Ah):
    ├── Measures charge (number of electrons)
    ├── Does NOT account for voltage
    └── Good for comparing same voltage batteries

    Watt-hour (Wh):
    ├── Measures energy (actual work capability)
    ├── Accounts for voltage: Wh = Ah × V
    └── Better for comparing different battery types


    EXAMPLE COMPARISON:

    Battery A: 2000mAh, 1.2V (NiMH)
    Battery B: 2000mAh, 3.7V (Li-ion)

    Both have SAME charge capacity (2000mAh)
    But DIFFERENT energy capacity:

    Battery A energy = 2.0Ah × 1.2V = 2.4Wh
    Battery B energy = 2.0Ah × 3.7V = 7.4Wh

    Li-ion stores 3× more energy! (runs device 3× longer)


    WHY THIS MATTERS:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Comparing a 2500mAh NiMH (1.2V) with a 2000mAh Li-ion    │
    │   (3.7V):                                                  │
    │                                                             │
    │   NiMH energy = 2.5Ah × 1.2V = 3.0Wh                       │
    │   Li-ion energy = 2.0Ah × 3.7V = 7.4Wh                     │
    │                                                             │
    │   Li-ion has LOWER mAh rating but HIGHER energy!           │
    │   Li-ion will run device 2.5× longer!                      │
    │                                                             │
    │   Always compare Wh for true capacity comparison.         │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

### How Capacity is Measured

Standard methods for determining battery capacity.

```
CAPACITY TESTING

    Standard test conditions (IEC):
    ├── Temperature: 20-25°C (68-77°F)
    ├── Discharge rate: 0.2C (5-hour rate)
    ├── Cutoff voltage: 1.0V per cell (primary)
    └── Rest period before test


    TEST PROCEDURE:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   1. Fully charge battery (if rechargeable)                │
    │   2. Let rest for 1-2 hours                                │
    │   3. Connect constant current load                         │
    │   4. Discharge at 0.2C until cutoff voltage                │
    │   5. Measure time to cutoff                                │
    │   6. Calculate capacity = I × t                            │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    EXAMPLE:

    2000mAh rated battery:
    ├── Test current = 0.2 × 2000 = 400mA
    ├── Time to cutoff = 5 hours
    └── Measured capacity = 0.4A × 5h = 2000mAh ✓


    WHY 0.2C IS STANDARD:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Lower discharge rates = higher measured capacity         │
    │   Higher discharge rates = lower measured capacity         │
    │                                                             │
    │   0.2C gives consistent, comparable measurements           │
    │   across different battery types                           │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

### Factors Affecting Capacity

```
TEMPERATURE EFFECTS

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Relative Capacity vs Temperature                         │
    │                                                             │
    │   Capacity (% of 20°C rating)                              │
    │        │                                                  │
    │    120 ┼                              ●                    │
    │        │                           ╱                       │
    │    110 ┼                         ╱                         │
    │        │                       ╱                           │
    │    100 ┼─────────────────────●                             │
    │        │                    ╱                              │
    │     90 ┼                  ╱                                │
    │        │                ╱                                  │
    │     80 ┼              ╱                                    │
    │        │            ╱                                      │
    │     70 ┼          ╱                                        │
    │        │        ╱                                          │
    │     60 ┼      ●                                            │
    │        │                                                  │
    │        └────────────────────────────────────────► Temp    │
    │        -20°C  0°C   20°C   40°C   60°C                    │
    │                                                             │
    │   Li-ion: -20°C = 70-80%, 0°C = 90-95%, 40°C = 105-110%   │
    │   Alkaline: -20°C = 20-40%, 0°C = 60-80%, 40°C = 105%     │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    DISCHARGE RATE EFFECTS (Peukert)

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Higher current = Lower effective capacity                │
    │                                                             │
    │   Capacity (AA alkaline) vs Discharge Rate:                │
    │                                                             │
    │   10mA   :  3000mAh (100%)                                 │
    │   100mA  :  2700mAh (90%)                                  │
    │   500mA  :  1800mAh (60%)                                  │
    │   1000mA :  1000mAh (33%)                                  │
    │   2000mA :   400mAh (13%)                                  │
    │                                                             │
    │   Peukert's Law: Iⁿ × t = constant                         │
    │   n (Peukert exponent): Alkaline = 1.1-1.4, Lead-acid = 1.2│
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    AGE EFFECTS

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Capacity decreases with age and cycles                    │
    │                                                             │
    │   Rechargeable battery capacity vs cycles:                  │
    │                                                             │
    │   0 cycles:  100% (2000mAh)                                │
    │   100 cycles: 95% (1900mAh)                                │
    │   300 cycles: 85% (1700mAh)                                │
    │   500 cycles: 75% (1500mAh) - end of useful life           │
    │                                                             │
    │   Primary battery capacity vs storage time:                 │
    │                                                             │
    │   New:        100%                                         │
    │   1 year:     95-97%                                       │
    │   3 years:    85-90%                                       │
    │   5 years:    75-85%                                       │
    │   10 years:   50-60%                                       │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

### Typical Capacities by Battery Size

```
PRIMARY BATTERIES (Alkaline, 25°C, low drain)

    Size          Capacity (mAh)    Energy (Wh)    Equivalent
    ──────────────────────────────────────────────────────────────
    AAA           1000-1200         1.5-1.8        -
    AA            2500-3000         3.8-4.5        -
    C             7000-8000         10.5-12.0      -
    D             15000-20000       22.5-30.0      -
    9V            400-600           3.6-5.4        -
    CR2032        220-240           0.66-0.72      -
    CR123A        1400-1600         4.2-4.8        -


    RECHARGEABLE BATTERIES

    Size/Type                NiMH            Li-ion (3.7V)
    ──────────────────────────────────────────────────────────────
    AAA (NiMH)               800-1100 mAh     -
    AA (NiMH standard)       2000-2500 mAh    -
    AA (NiMH LSD/Eneloop)    1900-2000 mAh    -
    AA (NiMH high capacity)  2700-2800 mAh    -
    18650 Li-ion              -               2000-3500 mAh
    21700 Li-ion              -               4000-5000 mAh
    26650 Li-ion              -               5000-6000 mAh
    LiPo pouch (500mAh)       -               500 mAh
    LiPo pouch (2000mAh)      -               2000 mAh


    LEAD-ACID BATTERIES (Ah, not mAh!)

    Type                      Capacity (Ah)    Energy (Wh)
    ──────────────────────────────────────────────────────────────
    Motorcycle (12V)          5-15             60-180
    Small car (12V)           40-60            480-720
    Standard car (12V)        60-80            720-960
    Large car/SUV (12V)       80-100           960-1200
    Deep cycle (12V)          100-250          1200-3000
    Golf cart (6V)            200-250          1200-1500
    Industrial (2V cell)      500-5000         1000-10000
```

## State of Charge (SoC)

### Estimating SoC from Voltage

How to tell how much charge is left.

```
SoC vs OCV (Resting, 25°C)

    ALKALINE (1.5V):

    SoC (%)    Voltage     Action
    ──────────────────────────────
    100        1.60-1.65   Fresh
    90         1.55-1.60   Good
    75         1.50-1.55   Good
    50         1.45-1.50   Half used
    25         1.35-1.45   Replace soon
    10         1.25-1.35   Weak
    5          1.15-1.25   Replace
    0          <1.10       Dead


    NiMH (1.2V):

    SoC (%)    Voltage     Action
    ──────────────────────────────
    100        1.40-1.45   Fresh charge
    90         1.38-1.42   Good
    75         1.35-1.40   Good
    50         1.28-1.32   Half used
    25         1.20-1.25   Recharge soon
    10         1.15-1.20   Recharge
    5          1.10-1.15   Recharge immediately
    0          <1.00       Over-discharged (damage risk)


    Li-ion (3.7V):

    SoC (%)    Voltage     Action
    ──────────────────────────────
    100        4.15-4.20   Full (disconnect charger)
    90         4.05-4.10   Good
    75         3.95-4.00   Good
    50         3.72-3.78   Storage voltage (ideal)
    25         3.58-3.63   Recharge soon
    10         3.40-3.45   Recharge immediately
    5          3.30-3.35   Danger zone
    0          2.50-3.00   Damaged (if <2.5V)


    IMPORTANT NOTES:

    ├── Voltage must be measured after 30+ minutes rest
    ├── Surface charge affects readings (use load briefly)
    ├── Temperature affects voltage (colder = lower voltage)
    └── Different chemistries have different curves
```

### Battery Capacity vs Device Runtime

```
RUNTIME CALCULATION

    Runtime (hours) = Battery Capacity (Ah) / Device Current (A)


    EXAMPLES:

    1. AA alkaline (2000mAh) in TV remote (50mA average):
       Runtime = 2000mAh / 50mA = 40 hours of use
       (but 40 hours = ~1 year of typical use)

    2. 18650 Li-ion (2500mAh) in flashlight (500mA):
       Runtime = 2500mAh / 500mA = 5 hours

    3. Car battery (60Ah) with headlights (5A):
       Runtime = 60Ah / 5A = 12 hours (before dead)

    4. Laptop battery (50Wh) with 20W power consumption:
       Runtime = 50Wh / 20W = 2.5 hours


    REALITY CHECK:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Actual runtime is ALWAYS less than calculated:           │
    │                                                             │
    │   ├── Voltage drops (lower voltage = less power)          │
    │   ├── Temperature effects (cold reduces capacity)          │
    │   ├── Peukert effect (high current = lower capacity)       │
    │   ├── Age (old batteries have less capacity)               │
    │   ├── Device cutoff (voltage too low, battery remains)     │
    │   └── Self-discharge (idle loss)                          │
    │                                                             │
    │   Safety margin: Calculate 60-80% of theoretical          │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

## Quick Reference Table

| Parameter | Symbol | Unit | Formula | Typical Range |
|-----------|--------|------|---------|---------------|
| Nominal voltage | V_nom | Volt | - | 1.2V to 3.7V (cell) |
| Open circuit voltage | V_OCV | Volt | - | 1.2V to 4.2V |
| Cutoff voltage | V_cut | Volt | - | 0.8V to 3.0V |
| Capacity (charge) | C | Ah, mAh | C = I × t | 50mAh to 5000Ah |
| Energy capacity | E | Wh, kWh | E = C × V | 0.1Wh to 100kWh |
| C-rate | C | - | I / C_nom | 0.1C to 120C |
| Peukert exponent | n | - | Iⁿ × t = constant | 1.05 to 1.5 |
| Self-discharge | - | %/month | - | 1% to 30% |

## Summary

1. **Voltage** is electrical pressure that pushes current (measured in Volts)

2. **Nominal voltage** is the advertised value; actual voltage varies during use

3. **Open circuit voltage (OCV)** is measured with no load (highest voltage)

4. **Voltage under load** is always lower due to internal resistance: V_load = V_OCV - I × R_int

5. **Cutoff voltage** is where device stops working (different for each device)

6. **Capacity** is charge stored, measured in ampere-hours (Ah) or mAh

7. **Energy capacity** (Wh = Ah × V) is better for comparing different chemistries

8. **Higher voltage batteries** store more energy for same mAh rating

9. **Temperature affects capacity:** cold = less capacity, hot = more (but shorter life)

10. **High discharge rates** reduce effective capacity (Peukert effect)

11. **Alkaline** loses capacity rapidly at high current (2000mA = 13% of rating)

12. **NiMH and Li-ion** handle high current much better (maintain 80-95% at 1C)

13. **Capacity decreases with age:** 500 cycles = ~75% for Li-ion

14. **SoC estimation** from voltage requires resting, temperature compensation

15. **Runtime calculation:** hours = Ah / A (but actual will be 60-80% of theoretical)

16. **Compare batteries by Wh,** not mAh, for true energy comparison

*This documentation belongs to https://github.com/InterCentury*