# what-is-battery ?

A battery is a device that converts chemical energy directly into electrical energy through an electrochemical reaction. It consists of one or more electrochemical cells, each containing two electrodes (anode and cathode) and an electrolyte. When connected to an external circuit, chemical reactions inside the battery produce a flow of electrons — electricity.

The word "battery" was first used by Benjamin Franklin in 1749 to describe a set of linked capacitors (Leyden jars) "for the purpose of discharging more power at once" — like a battery of cannons. The first true electrochemical battery, the Voltaic Pile, was invented by Alessandro Volta in 1800, consisting of alternating discs of zinc and copper separated by brine-soaked cardboard.

## Basic Principles

### The Electrochemical Cell

All batteries are built from fundamental units called cells.

```
SIMPLE ELECTROCHEMICAL CELL

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ┌─────────────────────────────────────────────────────┐   │
    │   │                                                     │   │
    │   │   Electron flow (through external circuit)          │   │
    │   │   ──────────────────────────────────────────────►   │   │
    │   │                                                     │   │
    │   │   ┌─────────┐                        ┌─────────┐    │   │
    │   │   │         │                        │         │    │   │
    │   │   │  ANODE  │                        │ CATHODE │    │   │
    │   │   │   (-)   │                        │   (+)   │    │   │
    │   │   │         │                        │         │    │   │
    │   │   │  Zinc   │     ◄── IONS ───►      │ Copper  │    │   │
    │   │   │   Zn    │                        │   Cu    │    │   │
    │   │   │         │                        │         │    │   │
    │   │   └────┬────┘                        └────┬────┘    │   │
    │   │        │                                  │         │   │
    │   │        │         ┌──────────────────┐     │         │   │
    │   │        └─────────┤  ELECTROLYTE     ├─────┘         │   │
    │   │                  │  (salt solution) │               │   │
    │   │                  └──────────────────┘               │   │
    │   │                                                     │   │
    │   │   Ion flow (through electrolyte)                    │   │
    │   │   ◄────────────────────────────────────────────────►│   │
    │   │                                                     │   │
    │   └─────────────────────────────────────────────────────┘   │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    KEY COMPONENTS:

    Component           Function
    ──────────────────────────────────────────────────────────────
    Anode (-)           Electrode where oxidation occurs
                        (loses electrons)
    
    Cathode (+)         Electrode where reduction occurs
                        (gains electrons)
    
    Electrolyte         Conductive medium that allows ion flow
                        between electrodes
    
    Separator           Prevents physical contact between electrodes
                        (allows ions to pass)
    
    External circuit    Path for electrons to do work
                        (light bulb, motor, etc.)
```

### How a Battery Works

The fundamental process that makes a battery work.

```
BATTERY OPERATION PRINCIPLE

    DISCHARGE (battery powering a device):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Anode reaction (oxidation):                               │
    │   Zn → Zn²⁺ + 2e⁻                                           │
    │   (zinc loses electrons, becomes positive ion)              │
    │                                                             │
    │   Cathode reaction (reduction):                             │
    │   2MnO₂ + 2H⁺ + 2e⁻ → Mn₂O₃ + H₂O                           │
    │   (manganese dioxide gains electrons)                       │
    │                                                             │
    │   Electrolyte: Allows Zn²⁺ and OH⁻ ions to move             │
    │                                                             │
    │   Net effect:                                               │
    │   ├── Electrons flow through external circuit (current)     │
    │   ├── Ions flow through electrolyte (completes circuit)     │
    │   └── Chemical energy → Electrical energy                   │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    CHARGE (rechargeable battery only):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   External power forces electrons back to anode             │
    │   Chemical reactions reverse                                │
    │   Electrical energy → Chemical energy (stored)              │
    │                                                             │
    │   Anode: Zn²⁺ + 2e⁻ → Zn                                    │
    │   Cathode: Mn₂O₃ + H₂O → 2MnO₂ + 2H⁺ + 2e⁻                  │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

## Battery vs Cell

### Distinguishing the Terms

```
BATTERY vs CELL

    CELL:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   A single electrochemical unit                             │
    │                                                             │
    │   ┌─────────────────────────────────────────────────────┐   │
    │   │                                                     │   │
    │   │   ┌───┬───────────┬───┐                             │   │
    │   │   │ - │  ANODE    │ + │  1.5V                       │   │
    │   │   │   │  │ 1.2V   │   │                             │   │
    │   │   └───┴───────────┴───┘                             │   │
    │   │                                                     │   │
    │   └─────────────────────────────────────────────────────┘   │
    │                                                             │
    │   Examples: AA battery, single Li-ion 18650                 │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    BATTERY:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Two or more cells connected together                      │
    │                                                             │
    │   ┌─────────────────────────────────────────────────────┐   │
    │   │                                                     │   │
    │   │   ┌───┬───────────┬───┐  ┌───┬───────────┬───┐      │   │
    │   │   │ - │  CELL 1   │ + │──│ - │  CELL 2   │ + │      │   │
    │   │   │   │  1.5V     │   │  │   │  1.5V     │   │      │   │
    │   │   └───┴───────────┴───┘  └───┴───────────┴───┘      │   │
    │   │                            │                        │   │
    │   │                            ▼                        │   │
    │   │                       Output: 3.0V                  │   │
    │   │                                                     │   │
    │   └─────────────────────────────────────────────────────┘   │
    │                                                             │
    │   Examples: 9V battery (6 cells in series), car battery     │
    │             (6 cells in series, 12V), laptop battery pack   │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    USAGE IN COMMON LANGUAGE:

    ├── "AA battery" is actually a single CELL (but called battery)
    ├── "Car battery" is truly a BATTERY (6 cells)
    ├── "9V battery" is truly a BATTERY (6 cells)
    └── In common usage, "battery" is used for both
```

## Primary vs Secondary Batteries

### The Fundamental Classification

```
PRIMARY BATTERIES (Non-rechargeable)

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Characteristics:                                          │
    │   ├── Cannot be recharged (chemical reaction irreversible)  │
    │   ├── Lower initial cost                                    │
    │   ├── Higher energy density (Wh/kg)                         │
    │   ├── Longer shelf life                                     │
    │   ├── Lower self-discharge                                  │
    │   └── Disposal after single use                             │
    │                                                             │
    │   Examples:                                                 │
    │   ├── Alkaline (AA, AAA, C, D, 9V)                          │
    │   ├── Zinc-carbon (old, cheap)                              │
    │   ├── Lithium primary (CR2032, Energizer Ultimate)          │
    │   ├── Silver oxide (watches, hearing aids)                  │
    │   └── Zinc-air (hearing aids)                               │
    │                                                             │
    │   Best for:                                                 │
    │   ├── Low-drain devices (remotes, clocks)                   │
    │   ├── Emergency equipment (must work after years)           │
    │   ├── Devices with infrequent use                           │
    │   └── Where recharging isn't practical                      │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    SECONDARY BATTERIES (Rechargeable)

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Characteristics:                                          │
    │   ├── Can be recharged hundreds/thousands of times          │
    │   ├── Higher initial cost                                   │
    │   ├── Lower energy density (Wh/kg)                          │
    │   ├── Shorter shelf life (higher self-discharge)            │
    │   ├── Requires charger                                      │
    │   └── Lower cost per use (over lifetime)                    │
    │                                                             │
    │   Examples:                                                 │
    │   ├── Lead-acid (car battery, UPS)                          │
    │   ├── NiCd (power tools, aviation)                          │
    │   ├── NiMH (AA/AAA rechargeable, hybrid cars)               │
    │   ├── Li-ion (phones, laptops, EVs)                         │
    │   ├── LiFePO₄ (solar storage, golf carts)                   │
    │   └── LiPo (drones, RC)                                     │
    │                                                             │
    │   Best for:                                                 │
    │   ├── High-drain devices (cameras, tools)                   │
    │   ├── Frequently used devices (phones, laptops)             │
    │   ├── High power applications (EVs)                         │
    │   └── Where cost per use matters                            │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    COMPARISON TABLE:

    Feature                 Primary                 Secondary
    ──────────────────────────────────────────────────────────────
    Rechargeable            No                      Yes
    Initial cost            Low                     High
    Cost per cycle          High                    Very low
    Energy density          Higher                  Lower
    Self-discharge          <2%/year                2-30%/month*
    Shelf life              5-20 years              1-10 years
    Voltage (AA size)       1.5V                    1.2V (NiMH)
    Typical use             Remotes, clocks         Phones, tools
    
    *LSD NiMH has low self-discharge (comparable to primary)
```

## Battery Parameters

### Voltage (V)

The electrical potential difference between terminals.

```
VOLTAGE BY CHEMISTRY

    Primary Batteries:

    Chemistry               Nominal Voltage    Full (fresh)    Cutoff
    ────────────────────────────────────────────────────────────────────
    Alkaline                1.5V               1.60-1.65V      0.8-1.0V
    Zinc-carbon             1.5V               1.55-1.60V      0.8-0.9V
    Lithium (Li-FeS₂)       1.5V               1.80V           0.8-1.0V
    Lithium (Li-MnO₂)       3.0V               3.2-3.3V        2.0V
    Lithium (Li-SOCl₂)      3.6V               3.65-3.70V      2.5V
    Silver oxide            1.55V              1.60V           1.2V
    Zinc-air                1.4V               1.45V           1.0V

    Secondary Batteries:

    Chemistry               Nominal Voltage    Full (charged)  Cutoff
    ────────────────────────────────────────────────────────────────────
    Lead-acid (per cell)    2.0-2.1V           2.40-2.45V      1.75V
    Lead-acid (12V)         12.0-12.6V         13.8-14.4V      10.5V
    NiCd                    1.2V               1.40-1.45V      1.0V
    NiMH                    1.2V               1.40-1.45V      1.0V
    Li-ion (NMC)            3.6-3.7V           4.20V           2.5-3.0V
    LiFePO₄                 3.2-3.3V           3.60-3.65V      2.5V
    LiPo                    3.7V               4.20V           3.0V
    LTO                     2.3-2.4V           2.80V           1.5V
```

### Capacity (Ah / mAh / Wh)

The amount of charge or energy a battery can store.

```
CAPACITY EXPLANATION

    Ampere-hour (Ah) = Current × Time

    1 Ah = 1 ampere for 1 hour
    1 Ah = 1000 mAh (milliampere-hours)


    EXAMPLE:

    A 2000mAh (2Ah) battery can theoretically provide:
    ├── 2000mA for 1 hour
    ├── 1000mA for 2 hours
    ├── 500mA for 4 hours
    ├── 200mA for 10 hours
    └── 20mA for 100 hours


    ENERGY (Watt-hour):

    Wh = Ah × V
    Wh is a more accurate measure of stored energy

    Example: 2000mAh AA alkaline (1.5V)
    Energy = 2Ah × 1.5V = 3Wh

    Example: 2000mAh Li-ion 18650 (3.7V)
    Energy = 2Ah × 3.7V = 7.4Wh

    Same capacity (mAh) but 2.5× more energy!


    TYPICAL CAPACITIES BY SIZE:

    Size/Format             Alkaline        NiMH            Li-ion
    ──────────────────────────────────────────────────────────────────────
    AAA                     1000-1200 mAh   800-1100 mAh    -
    AA                      2500-3000 mAh   2000-2800 mAh   -
    C                       7000-8000 mAh   4500-6000 mAh   -
    D                       15000-20000 mAh 8000-12000 mAh  -
    9V                      400-600 mAh     200-300 mAh     -
    18650                   -               -               2000-3500 mAh
    21700                   -               -               4000-5000 mAh
    CR2032                  240 mAh         -               -
```

### C-Rate (Discharge Rate)

How quickly a battery can be charged or discharged.

```
C-RATE DEFINITION

    1C = The current that would fully discharge the battery in 1 hour

    For a 2000mAh battery:
     -> 0.5C = 1000mA  (discharge in 2 hours)
     -> 1C   = 2000mA  (discharge in 1 hour)
     -> 2C   = 4000mA  (discharge in 30 minutes)
     -> 5C   = 10000mA (discharge in 12 minutes)


    TYPICAL C-RATES BY CHEMISTRY:

    Chemistry               Max Charge C    Max Discharge C     Notes
    ────────────────────────────────────────────────────────────────────────────
    Alkaline                N/A             0.2-0.5C            Poor high rate
    Lead-acid               0.3C            3-5C (CCA)          Starting only
    NiCd                    1C              10-20C              Very good
    NiMH (standard)         1C              3-5C                Good
    NiMH (high power)       2-3C            10-15C              Power tools
    Li-ion (energy)         1C              2-3C                Phones, laptops
    Li-ion (power)          2-3C            10-30C              Power tools
    LiFePO₄                 1-3C            5-10C               Good power
    LiPo (RC)               5C              30-120C!            Extreme power
    LTO                     5-10C           10-30C              Fast charge


    PRACTICAL EFFECTS OF C-RATE:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Higher C-rate → Higher current → More heat                │
    │   More heat → Reduced efficiency → More losses              │
    │                                                             │
    │   Example (2000mAh Li-ion at 25°C):                         │
    │   0.2C (400mA):   2000mAh (100%) efficiency                 │
    │   1C (2000mA):    1950mAh (97.5%)                           │
    │   2C (4000mA):    1800mAh (90%)                             │
    │   5C (10000mA):   1500mAh (75%)                             │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

### Cycle Life

The number of charge/discharge cycles before capacity degrades.

```
CYCLE LIFE DEFINITION

    Number of cycles until capacity drops below 80% of original


    TYPICAL CYCLE LIFE BY CHEMISTRY (100% depth of discharge)

    Chemistry               Cycle Life (80% DoD)    Notes
    ──────────────────────────────────────────────────────────────────────
    Lead-acid (starting)    50-100                   Not for deep cycle
    Lead-acid (deep cycle)  200-500                  Better
    NiCd                    500-1000                 Excellent
    NiMH                    300-500                  Good
    Li-ion (NMC)            300-500                  Good
    LiFePO₄                 2000-5000+               Excellent
    LTO                     10000-20000+             Best
    (Alkaline primary)      N/A (single use)         -


    DEPTH OF DISCHARGE (DoD) EFFECT:

    Depth of Discharge      Cycles (LiFePO₄)
    ──────────────────────────────────────────
    100% (full discharge)   2000
    80%                     3000
    50%                     5000
    30%                     8000
    10%                     15000+


    CYCLE LIFE DEFINED:

    End of life = capacity <80% of original
    Battery may still work (shorter runtime)
```

### Internal Resistance

The inherent resistance inside the battery that causes voltage drop and heating.

```
INTERNAL RESISTANCE (IR)

    Effects:
    ├── Voltage drop under load: V_drop = I × R_internal
    ├── Heat generation: P_heat = I² × R_internal
    ├── Reduced power delivery at high current
    └── Increases with age (end-of-life indicator)


    TYPICAL IR VALUES (new, at 25°C)

    Chemistry / Size        IR (mΩ)         Notes
    ──────────────────────────────────────────────────────────────
    Alkaline AA             150-300         High
    NiMH AA                 20-50           Lower
    NiCd AA                 15-30           Lower
    Li-ion 18650            20-80           Depends on type
    Li-ion 18650 (high power) 10-30         Very low
    LiFePO₄ 18650           10-40           Low
    Lead-acid 12V (car)     5-15            Very low
    LTO                     1-5             Extremely low


    IR INCREASE WITH AGE:

    New battery:            IR = 20mΩ
    After 100 cycles:       IR = 25-30mΩ
    After 300 cycles:       IR = 40-60mΩ
    End of life:            IR = 80-100mΩ+ (poor performance)
```

## Battery Configurations

### Series Connection

Connecting cells end-to-end to increase voltage.

```
SERIES CONFIGURATION

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   -││+   -││+   -││+                                        │
    │   Cell 1  Cell 2  Cell 3                                    │
    │                        │                                    │
    │                        ▼                                    │
    │   Total voltage = V₁ + V₂ + V₃                              │
    │   Total capacity = Same as single cell                      │
    │   (current same through all cells)                          │
    │                                                             │
    │   Example: 3 × 1.2V NiMH cells → 3.6V                       │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘

    Use: Higher voltage devices
    Caution: Cells must be same type, age, charge state
```

### Parallel Connection

Connecting cells side-by-side to increase capacity.

```
PARALLEL CONFIGURATION

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   -││+                                                      │
    │   Cell 1  ─┐                                                │
    │            │                                                │
    │   -││+     │                                                │
    │   Cell 2  ─┤                                                │
    │            │                                                │
    │   -││+     │                                                │
    │   Cell 3  ─┘                                                │
    │                                                             │
    │   Total voltage = Same as single cell                       │
    │   Total capacity = C₁ + C₂ + C₃                             │
    │   (current divides among cells)                             │
    │                                                             │
    │   Example: 3 × 2000mAh Li-ion → 6000mAh, 3.7V               │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘

    Use: Higher capacity, longer runtime
    Caution: Cells must be matched (voltage, capacity, IR)
    Never parallel different chemistries!
```

### Series-Parallel Combination

Both series and parallel for high voltage AND high capacity.

```
SERIES-PARALLEL (4S2P example)

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   -││+   -││+   -││+   -││+                                 │
    │   Cell1   Cell2   Cell3   Cell4                             │
    │       │       │     │      │                                │
    │       │       │     │      │                                │
    │   -││+   -││+   -││+   -││+                                 │
    │    Cell5  Cell6  Cell7  Cell8                               │
    │                                                             │
    │   Configuration: 4 cells in series (4S)                     │
    │                 2 parallel strings (2P)                     │
    │                                                             │
    │   Voltage = 4 × V_cell                                      │
    │   Capacity = 2 × C_cell                                     │
    │                                                             │
    │   Example: 4S2P Li-ion (2000mAh cells)                      │
    │   Voltage = 4 × 3.7V = 14.8V                                │
    │   Capacity = 2 × 2000 = 4000mAh (4Ah)                       │
    │   Energy = 14.8V × 4Ah = 59.2Wh                             │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘

    Use: EV batteries, power tool packs, large solar storage
    Requires BMS with balancing!
```

## Historical Development

### Timeline of Battery Technology

```
BATTERY HISTORY TIMELINE

    1800 ─── Voltaic Pile (Volta) - First true battery
           Zinc and copper discs with brine electrolyte
    
    1836 ─── Daniell Cell - Improved, more stable voltage
    
    1859 ─── Lead-acid battery (Planté) - First rechargeable
           Still used today in cars!
    
    1866 ─── Leclanché cell - Precursor to zinc-carbon
    
    1888 ─── Dry cell (Gassner) - Leak-proof, portable
    
    1899 ─── NiCd battery (Jungner) - First practical<br>rechargeable portable
    
    1949 ─── Alkaline battery (Urry) - Higher capacity,<br>longer life
    
    1970 ─── Primary lithium battery (first commercial)
    
    1980 ─── Li-ion prototype (Goodenough)
    
    1991 ─── Commercial Li-ion (Sony)
    
    1995 ─── NiMH commercialized
    
    2005 ─── LSD NiMH (Eneloop) - Low self-discharge
    
    2009 ─── LiFePO₄ popularized for EVs
    
    2010+ ─── LTO, solid-state, advanced Li-ion
```

## Applications by Battery Type

```
APPLICATION MATRIX

    Application                 Typical Battery          Why
    ──────────────────────────────────────────────────────────────────────────────────
    Remote control              Alkaline                Long shelf life
    Wall clock                  Alkaline                Long life, cheap
    Smoke detector              Alkaline / Lithium      Reliability, long life
    Digital camera              NiMH (Eneloop)          High current, rechargeable
    Smartphone                  Li-ion (pouch)          High energy density
    Laptop                      Li-ion (18650/pouch)    Energy density
    Cordless drill              Li-ion (18650)          High power, lightweight
    Car starting                Lead-acid (AGM)         High CCA, cheap
    EV (electric car)           Li-ion (NMC/LFP)        Energy + Power
    Solar storage               LiFePO₄                 Long cycle life, safe
    UPS (backup)                Lead-acid (SLA)         Float charge capable
    Hearing aid                 Zinc-air / Silver oxide High energy density small
    Watch                       Silver oxide            Stable voltage
    Medical implant             Lithium primary         Very long life (10+ years)
    Drone / RC                  LiPo                    High power, lightweight
    Power tool (old)            NiCd (sub-C)            High current, robust
    E-bike                      Li-ion (18650/21700)    Good balance
    Golf cart                   Lead-acid deep cycle    Cheap, available
    Emergency light             NiCd / Lead-acid        Float charge
```

## Battery Terms Glossary

```
COMMON BATTERY TERMS

    Term                    Meaning
    ─────────────────────────────────────────────────────────────────────────────
    Ah (Ampere-hour)        Unit of charge capacity
    Anode                   Negative electrode (where oxidation occurs)
    BMS                     Battery Management System (protects Li-ion)
    C-rate                  Discharge/charge rate relative to capacity
    Capacity                Amount of charge a battery can store
    Cathode                 Positive electrode (where reduction occurs)
    Cell                    Single electrochemical unit
    CCA                     Cold Cranking Amps (lead-acid starting power)
    Cycle                   One complete discharge and recharge
    Cycle life              Number of cycles before 80% capacity
    Depth of Discharge (DoD) Percentage of capacity used per cycle
    Dendrite                Crystal growth that can cause internal shorts
    Electrolyte             Conductive medium between electrodes
    Energy density          Energy per unit weight or volume (Wh/kg, Wh/L)
    Float charge            Maintenance charge (full voltage, low current)
    Internal resistance (IR) Resistance inside battery (causes voltage drop)
    Li-ion                  Lithium-ion (rechargeable)
    LiFePO₄                 Lithium Iron Phosphate (safe Li-ion)
    LiPo                    Lithium Polymer (pouch cell)
    LSD                     Low Self-Discharge (Eneloop-type NiMH)
    Memory effect           Voltage depression in NiCd from shallow cycles
    NiCd                    Nickel-Cadmium (rechargeable, toxic)
    NiMH                    Nickel-Metal Hydride (rechargeable)
    Open circuit voltage    Voltage with no load
    Primary battery         Non-rechargeable
    Secondary battery       Rechargeable
    Self-discharge          Capacity loss when not in use
    Separator               Prevents short between electrodes
    Series                  Cells connected + to - (voltage adds)
    Parallel                Cells connected + to +, - to - (capacity adds)
    SLA                     Sealed Lead-Acid (maintenance-free)
    SoC                     State of Charge (percentage full)
    Thermal runaway         Self-heating leading to fire/explosion (Li-ion)
    Trickle charge          Very low rate continuous charge
```

## Quick Reference Table

| Parameter | Symbol | Unit | Typical Range |
|-----------|--------|------|---------------|
| Voltage (cell) | V | Volt | 1.2V to 3.7V |
| Voltage (battery) | V | Volt | 1.5V to 800V+ |
| Capacity | C | Ah (mAh) | 50mAh to 5000Ah |
| Energy | E | Wh (kWh) | 0.1Wh to 100kWh |
| Power | P | W (kW) | 0.1W to 1000kW+ |
| C-rate | C | - | 0.1C to 120C |
| Cycle life | - | cycles | 1 to 20000+ |
| Self-discharge | - | %/month | 1% to 30% |
| Internal resistance | R_int | mΩ | 1mΩ to 500mΩ |

## Summary

1. **Battery** converts chemical energy to electrical energy via electrochemical reactions

2. **Cell** is a single unit; **battery** is multiple cells connected together

3. **Primary batteries** are non-rechargeable (alkaline, lithium primary)

4. **Secondary batteries** are rechargeable (Li-ion, NiMH, lead-acid)

5. **Anode (-)** loses electrons (oxidation); **Cathode (+)** gains electrons (reduction)

6. **Electrolyte** allows ion flow between electrodes

7. **Separator** prevents physical contact while allowing ion flow

8. **Voltage** is electrical potential difference (1.2V to 3.7V per cell typical)

9. **Capacity (Ah)** is charge stored (1Ah = 1 ampere for 1 hour)

10. **Energy (Wh)** = Ah × V (better measure of actual energy stored)

11. **C-rate** indicates charge/discharge speed relative to capacity

12. **Cycle life** is number of cycles before capacity drops to 80%

13. **Internal resistance** causes voltage drop and heating (I²R)

14. **Series connection** increases voltage (capacity unchanged)

15. **Parallel connection** increases capacity (voltage unchanged)

16. **Depth of Discharge (DoD)** affects cycle life (shallower = longer life)

17. **Self-discharge** is capacity loss when idle (varies by chemistry)

18. **Battery invented 1800 by Volta; rechargeable developed 1859 (Planté)**

*This documentation belongs to https://github.com/InterCentury*