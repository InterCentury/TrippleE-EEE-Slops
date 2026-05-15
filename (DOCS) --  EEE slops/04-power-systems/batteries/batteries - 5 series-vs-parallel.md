# batteries - 5 series-vs-parallel

## Series vs Parallel Battery Configurations

Batteries can be connected together in different ways to achieve different voltage and capacity combinations. The two fundamental configurations are series and parallel, which can also be combined to create series-parallel banks.

Understanding these configurations is essential for designing battery packs for anything from a simple flashlight to an electric vehicle battery system. This document explains how each configuration works, when to use which, and critical safety considerations.

## Series Configuration

### How Series Works

Connecting batteries end-to-end increases voltage while keeping capacity the same.

```
SERIES CONNECTION DIAGRAM

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Battery 1      Battery 2      Battery 3                   │
    │   ┌─────┐        ┌─────┐        ┌─────┐                     │
    │   │  +  │        │  +  │        │  +  │                     │
    │   │     │        │     │        │     │                     │
    │   │  -  │────────│  +  │────────│  -  │                     │
    │   └──┬──┘        └──┬──┘        └──┬──┘                     │
    │      │              │              │                        │
    │      │              │              │                        │
    │   ┌──┴──┐        ┌──┴──┐        ┌──┴──┐                     │
    │   │  -  │        │  +  │        │  -  │                     │
    │   └─────┘        └─────┘        └─────┘                     │
    │                                                             │
    │   Negative output ───┘        └─── Positive output          │
    │                                                             │
    │   Total Voltage = V₁ + V₂ + V₃                              │
    │   Total Capacity = Same as single battery                   │
    │   Total Current = Same as single battery                    │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    EXAMPLE (3 × 1.2V NiMH, 2000mAh):

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Battery 1    Battery 2    Battery 3      Output           │
    │   1.2V         1.2V         1.2V           3.6V             │
    │   2000mAh      2000mAh      2000mAh        2000mAh          │
    │                                                             │
    │   3.6V × 2000mAh = 7.2Wh                                    │
    │   (Same Wh as 3 batteries individually)                     │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    RULES FOR SERIES CONNECTION:

    ├── Voltages ADD (V_total = V₁ + V₂ + V₃)
    ├── Capacity (Ah) remains SAME as single cell
    ├── Current capability SAME as single cell
    ├── Watt-hours ADD (Wh_total = Wh₁ + Wh₂ + Wh₃)
    └── All batteries must have SAME capacity and chemistry!
```

### Why Use Series?

```
ADVANTAGES OF SERIES:

    ┌───────────────────────────────────────────────────────────────────┐
    │                                                                   │
    │   1. HIGHER VOLTAGE for devices requiring more power              │
    │                                                                   │
    │   2. LOWER CURRENT for same power (P = V × I)                     │
    │      └── Less I²R loss = more efficient                           │
    │                                                                   │
    │   3. THINNER WIRES possible (lower current = smaller gauge)       │
    │                                                                   │
    │   4. STANDARD VOLTAGES achieved                                   │
    │      ├── 2 cells (1.2V) = 2.4V (older electronics)                │
    │      ├── 3 cells (1.2V) = 3.6V (early electronics)                │
    │      ├── 4 cells (1.2V) = 4.8V (some power tools)                 │
    │      ├── 6 cells (1.2V) = 7.2V (cordless tools)                   │
    │      ├── 10 cells (3.7V) = 37V (e-bikes)                          │
    │      └── 96 cells (3.7V) = 355V (EV batteries)                    │
    │                                                                   │
    └───────────────────────────────────────────────────────────────────┘


    DISADVANTAGES OF SERIES:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   1. WEAKEST CELL limits the entire pack                    │
    │      └── One bad cell = entire pack fails                   │
    │                                                             │
    │   2. IMBALANCE is dangerous (Li-ion)                        │
    │      └── One cell overcharges while others are charging     │
    │                                                             │
    │   3. CELL MATCHING critical                                 │
    │      └── Same capacity, age, internal resistance            │
    │                                                             │
    │   4. BMS REQUIRED for multi-cell Li-ion                     │
    │      └── Balancing and protection circuit necessary         │
    │                                                             │
    │   5. ONE OPEN CELL kills entire pack                        │
    │      └── Series = single point of failure                   │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

## Parallel Configuration

### How Parallel Works

Connecting batteries side-by-side increases capacity while keeping voltage the same.

```
PARALLEL CONNECTION DIAGRAM

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │                       Positive output (+)                   │
    │                              │                              │
    │              ┌───────────────┼───────────────┐              │
    │              │               │               │              │
    │              ▼               ▼               ▼              │
    │         ┌────┴────┐     ┌────┴────┐     ┌────┴────┐         │
    │         │  +      │     │  +      │     │  +      │         │
    │         │Battery1 │     │Battery2 │     │Battery3 │         │
    │         │  -      │     │  -      │     │  -      │         │
    │         └────┬────┘     └────┬────┘     └────┬────┘         │
    │              │               │               │              │
    │              └───────────────┼───────────────┘              │
    │                              │                              │
    │                       Negative output (-)                   │
    │                                                             │
    │   Total Voltage = Same as single battery                    │
    │   Total Capacity = C₁ + C₂ + C₃                             │
    │   Total Current = I₁ + I₂ + I₃ (device dependent)           │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    EXAMPLE (3 × 1.2V NiMH, 2000mAh):

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Battery 1    Battery 2    Battery 3      Output           │
    │   1.2V         1.2V         1.2V           1.2V             │
    │   2000mAh      2000mAh      2000mAh        6000mAh          │
    │                                                             │
    │   1.2V × 6000mAh = 7.2Wh                                    │
    │   (Same Wh as 3 batteries individually)                     │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    RULES FOR PARALLEL CONNECTION:

    ├── Voltages SAME (V_total = V₁ = V₂ = V₃)
    ├── Capacity (Ah) ADDS (C_total = C₁ + C₂ + C₃)
    ├── Current capability ADDS (can supply more current)
    ├── Watt-hours ADD (Wh_total = Wh₁ + Wh₂ + Wh₃)
    └── All batteries must have SAME voltage (both type and charge state!)
```

### Why Use Parallel?

```
ADVANTAGES OF PARALLEL:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   1. HIGHER CAPACITY for longer runtime                     │
    │                                                             │
    │   2. HIGHER CURRENT CAPABILITY                              │
    │      └── More cells in parallel = can supply more current   │
    │                                                             │
    │   3. REDUNDANCY (one cell can fail, pack still works)       │
    │      └── If one cell opens, others continue                 │
    │                                                             │
    │   4. LOWER INTERNAL RESISTANCE                              │
    │      └── Parallel reduces overall resistance                │
    │      └── I/R_total = 1/R₁ + 1/R₂ + 1/R₃                     │
    │                                                             │
    │   5. BALANCING OCCURS NATURALLY (for same chemistry)        │
    │      └── Cells self-balance if connected directly           │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    DISADVANTAGES OF PARALLEL:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   1. VOLTAGE SAME as single cell (no increase)              │
    │                                                             │
    │   2. CELL MATCHING still important                          │
    │      └── Different voltages cause high circulating current  │
    │                                                             │
    │   3. HIGH CIRCULATING CURRENT if cells at different SoC     │
    │      └── Can damage cells or cause fire (Li-ion)            │
    │                                                             │
    │   4. SHORTED CELL drags down entire pack                    │
    │      └── One shorted cell = all cells discharge into it     │
    │                                                             │
    │   5. MORE COMPLEX WIRING (multiple connections)             │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

## Series-Parallel Configuration

### Combining Both

For applications requiring both higher voltage AND higher capacity.

```
SERIES-PARALLEL (2S2P) DIAGRAM

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │                     Positive output (+)                     │
    │                            │                                │
    │            ┌───────────────┴───────────────┐                │
    │            │                               │                │
    │            ▼                               ▼                │
    │      ┌─────┴─────┐                   ┌─────┴─────┐          │
    │      │  SERIES   │                   │  SERIES   │          │
    │      │  STRING 1 │                   │  STRING 2 │          │
    │      │           │                   │           │          │
    │      │  ┌─────┐  │                   │  ┌─────┐  │          │
    │      │  │Cell1│  │                   │  │Cell3│  │          │
    │      │  │ (+) │  │                   │  │ (+) │  │          │
    │      │  └──┬──┘  │                   │  └──┬──┘  │          │
    │      │     │     │                   │     │     │          │
    │      │  ┌──┴──┐  │                   │  ┌──┴──┐  │          │
    │      │  │Cell2│  │                   │  │Cell4│  │          │
    │      │  │ (-) │  │                   │  │ (-) │  │          │
    │      │  └──┬──┘  │                   │  └──┬──┘  │          │
    │      │     │     │                   │     │     │          │
    │      └─────┴─────┘                   └─────┴─────┘          │
    │            │                               │                │
    │            └───────────────┬───────────────┘                │
    │                            │                                │
    │                     Negative output (-)                     │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    SPECIFICATIONS (2S2P, 3.7V Li-ion, 2000mAh cells):

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Series strings: 2 cells in series (2S)                    │
    │   Parallel strings: 2 strings (2P)                          │
    │                                                             │
    │   Voltage = 2 × 3.7V = 7.4V                                 │
    │   Capacity = 2 × 2000mAh = 4000mAh (4Ah)                    │
    │   Energy = 7.4V × 4Ah = 29.6Wh                              │
    │                                                             │
    │   Total cells = 2S × 2P = 4 cells                           │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    COMMON SERIES-PARALLEL CONFIGURATIONS:

    Configuration       Voltage*       Capacity*       Cells
    ──────────────────────────────────────────────────────────────
    2S2P (4 cells)      7.4V           4.0Ah           4
    3S2P (6 cells)      11.1V          4.0Ah           6
    4S2P (8 cells)      14.8V          4.0Ah           8
    4S3P (12 cells)     14.8V          6.0Ah           12
    5S2P (10 cells)     18.5V          4.0Ah           10
    6S2P (12 cells)     22.2V          4.0Ah           12
    10S4P (40 cells)    37.0V          8.0Ah           40
    96S2P (192 cells)   355V           5.0Ah           192 (EV)

    *Based on 3.7V Li-ion, 2000mAh cells
```

## Cell Matching

### Why Matching Matters

Connecting mismatched cells can cause serious problems.

```
CELL MATCHING REQUIREMENTS

    FOR SERIES CONNECTION (critical!):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   MUST match:                                               │
    │   ├── Capacity (Ah / mAh)                                   │
    │   ├── Chemistry (same type)                                 │
    │   ├── Brand and model (ideally)                             │
    │   ├── Age (same batch/cycles)                               │
    │   ├── Internal resistance                                   │
    │   └── State of charge (before connecting)                   │
    │                                                             │
    │   Why: Weakest cell limits entire pack                      │
    │         Imbalance leads to overcharge/over-discharge        │
    │         Li-ion: OVERCHARGE = FIRE                           │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    FOR PARALLEL CONNECTION (still important):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   MUST match:                                               │
    │   ├── Chemistry (same type)                                 │
    │   ├── Voltage BEFORE connecting (within 0.05V)              │
    │   └── Capacity (similar preferred)                          │
    │                                                             │
    │   Why: Different voltages = high circulating current        │
    │         Can damage cells, cause overheating, fire           │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    MISMATCHED CELL EXAMPLE:

    2000mAh cell in series with 1000mAh cell:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   During discharge:                                         │
    │   ├── 1000mAh cell empties FIRST                            │
    │   ├── 2000mAh cell still has 1000mAh left                   │
    │   ├── 1000mAh cell gets reverse charged                     │
    │   └── Damage or explosion!                                  │
    │                                                             │
    │   During charge (Li-ion):                                   │
    │   ├── 1000mAh cell fills FIRST                              │
    │   ├── 2000mAh cell still charging                           │
    │   ├── 1000mAh cell OVERCHARGES (>4.2V)                      │
    │   └── FIRE / EXPLOSION!                                     │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

## Balancing (For Series Packs)

### Why Balancing is Required

Multi-cell Li-ion packs must have balanced cells.

```
BALANCING EXPLANATION

    WITHOUT BALANCING (Dangerous):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   3S Li-ion pack (12.6V full):                              │
    │                                                             │
    │   Cell 1: 4.20V (full)                                      │
    │   Cell 2: 4.15V (90%)                                       │
    │   Cell 3: 4.05V (80%)                                       │
    │                                                             │
    │   Charger sees 12.40V (not yet 12.6V)                       │
    │   Charger continues charging!                               │
    │                                                             │
    │   Cell 1 overcharges: 4.20 → 4.30 → 4.40V                   │
    │                                                             │
    │   RESULT: FIRE or EXPLOSION!                                │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘

   WITH BALANCING (Safe):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Balance charger or BMS:                                   │
    │                                                             │
    │   Cell 1: 4.20V → Bleed resistor turns on (shunt)           │
    │   Cell 2: 4.15V → No bleeding                               │
    │   Cell 3: 4.05V → No bleeding                               │
    │                                                             │
    │   Cell 1 voltage held at 4.20V while others catch up        │
    │   All cells reach 4.20V together                            │
    │                                                             │
    │   RESULT: Safe, balanced pack                               │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
  
   BALANCING METHODS:
   ────────────────────────────────────────────────────────────────────────
   │Method             │ Description                    │ Best For        │  
   │───────────────────│────────────────────────────────│─────────────────│ 
   │Passive balancing  │ Bleed resistors burn excess    │ Low-cost BMS    │ 
   │                   │ energy as heat                 │                 │                      
   │                   │                                │                 │ 
   │Active balancing   │ Transfers energy from high to  │ High-end BMS    │       
   │                   │ low cells (efficient)          │                 │ 
   │                   │                                │                 │ 
   │Top balancing      │ Balances at full charge        │ Consumer packs  │          
   │                   │ (most common)                  │                 │    
   │                   │                                │                 │ 
   │Bottom balancing   │ Balances near empty            │ Industrial      │
   ────────────────────────────────────────────────────────────────────────
```

## Practical Applications

### Common Battery Configurations

```
DEVICE-SPECIFIC CONFIGURATIONS

    DEVICE                  CONFIGURATION          REASON
    ──────────────────────────────────────────────────────────────
    TV Remote               2S alkaline (3V)       2 cells in series
    LED flashlight          1S or 2S Li-ion        Voltage depends on LED
    Cordless drill (12V)    5S Li-ion (18V)        5 cells in series
    Cordless drill (18V)    5S Li-ion (18V)        5 cells in series
    Cordless drill (20V)    5S Li-ion (18V)        5 cells (marketing)
    Laptop battery          3S or 4S Li-ion        11.1V or 14.8V
    Power tool pack         5S2P Li-ion (18V, 4Ah) 10 cells
    E-bike battery          10S4P Li-ion (36V, 8Ah) 40 cells
    Car battery             6S lead-acid (12V)      6 cells in series
    Golf cart (36V)         18S lead-acid (36V)     18 cells (6V×6)
    Solar storage           4S LiFePO₄ (12.8V)      4 cells in series
    Tesla Model 3           96S46P (355V, 217Ah)    4416 cells!
```

### Designing a Battery Pack

```
EXAMPLE: 12V, 100Ah LiFePO₄ battery pack

    Step 1: Choose cells
    ├── LiFePO₄ cells: 3.2V, 50Ah each
    └── Need 12V and 100Ah

    Step 2: Series for voltage
    ├── 12V / 3.2V = 3.75 → 4 cells in series (4S)
    ├── 4S voltage = 4 × 3.2V = 12.8V (perfect for 12V system)
    └── 4S capacity = 50Ah (same as single cell)

    Step 3: Parallel for capacity
    ├── Need 100Ah, have 50Ah
    ├── 100Ah / 50Ah = 2 parallel strings (2P)
    └── Total capacity = 2 × 50Ah = 100Ah

    Step 4: Series-parallel
    ├── 4 cells in series × 2 parallel strings
    ├── Total cells = 4S × 2P = 8 cells
    └── Configuration: 4S2P

    Step 5: BMS requirements
    ├── BMS must support 4S LiFePO₄
    ├── Balance leads: 5 pins (4 cells + ground)
    └── Current rating: 100A minimum (for 1C discharge)

    Result: 12.8V, 100Ah, 1280Wh battery pack
```

## Current and Power Calculations

### How Configuration Affects Performance

```
SERIES CALCULATIONS

    Given: 3 × 3.7V Li-ion, 2000mAh cells

    V_total = 3.7V + 3.7V + 3.7V = 11.1V
    C_total = 2000mAh (same)
    I_max = 5A (same as single cell - example)
    P_max = V_total × I_max = 11.1V × 5A = 55.5W
    E_total = 11.1V × 2Ah = 22.2Wh


    PARALLEL CALCULATIONS

    Given: 3 × 3.7V Li-ion, 2000mAh cells

    V_total = 3.7V (same)
    C_total = 2000mAh + 2000mAh + 2000mAh = 6000mAh (6Ah)
    I_max = 5A + 5A + 5A = 15A (current adds!)
    P_max = 3.7V × 15A = 55.5W
    E_total = 3.7V × 6Ah = 22.2Wh


    SERIES-PARALLEL (2S3P) CALCULATIONS

    Given: 6 × 3.7V Li-ion, 2000mAh cells (2S × 3P)

    V_total = 2 × 3.7V = 7.4V
    C_total = 3 × 2000mAh = 6000mAh (6Ah)
    I_max = 3 × 5A = 15A (current adds from parallel)
    P_max = 7.4V × 15A = 111W
    E_total = 7.4V × 6Ah = 44.4Wh

    Total cells = 6 (2 series × 3 parallel)
```

## Safety Considerations

### Series Safety (Li-ion)

```
SERIES CONNECTION SAFETY RULES

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ☐ ALWAYS use Battery Management System (BMS)             │
    │   ☐ Use balance charger for charging                       │
    │   ☐ Monitor individual cell voltages                       │
    │   ☐ Match cells carefully (same capacity, age, IR)        │
    │   ☐ Never mix different chemistries                       │
    │   ☐ Never mix different capacities                        │
    │   ☐ Never mix old and new cells                           │
    │   ☐ Check cell balance regularly                          │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    CONSEQUENCES OF NO BMS (multi-cell Li-ion):

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Over-discharge:      Cell reversed polarity (damage)     │
    │   Overcharge:          FIRE or EXPLOSION!                  │
    │   Imbalance:           Overcharge of strong cell → FIRE    │
    │   Over-current:        Overheating, thermal runaway        │
    │   Short circuit:       Fire, explosion                     │
    │                                                             │
    │   BMS is NOT optional for multi-cell Li-ion!              │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

### Parallel Safety

```
PARALLEL CONNECTION SAFETY RULES

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ☐ Voltage must be equal BEFORE connecting                │
    │      (within 0.05V for Li-ion, 0.1V for NiMH)              │
    │                                                             │
    │   ☐ Use pre-charge resistor if voltages differ            │
    │      (prevents high inrush current)                        │
    │                                                             │
    │   ☐ Use fuses on each parallel string                     │
    │      (prevents catastrophic failure if one string shorts)  │
    │                                                             │
    │   ☐ Same chemistry only                                   │
    │                                                             │
    │   ☐ Similar capacity recommended                          │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    RISK: CONNECTING UNEQUAL VOLTAGES

    Example: 3.7V Li-ion in parallel with 4.0V Li-ion

    Voltage difference = 0.3V
    Internal resistance (each) = 0.05Ω
    Loop resistance = 0.05Ω + 0.05Ω = 0.1Ω
    Circulating current = 0.3V / 0.1Ω = 3A (significant!)

    Can cause: heating, reduced life, fire in extreme cases
```

## Quick Reference Table

| Configuration | Voltage | Capacity | Current Capability | Energy | Use Case |
|---------------|---------|----------|--------------------|--------|----------|
| Single cell | V | C | I | V × C | Low power devices |
| Series (2S) | 2V | C | I | 2V × C | Higher voltage devices |
| Series (3S) | 3V | C | I | 3V × C | Power tools |
| Parallel (2P) | V | 2C | 2I | V × 2C | Extended runtime |
| Parallel (3P) | V | 3C | 3I | V × 3C | High current devices |
| 2S2P | 2V | 2C | 2I | 4V × C | Balanced power + runtime |
| 3S2P | 3V | 2C | 2I | 6V × C | EV, e-bike packs |

## Summary

1. **Series connection** increases voltage (V_total = V₁ + V₂ + V₃)

2. **Series capacity** stays the same (C_total = C_cell)

3. **Parallel connection** increases capacity (C_total = C₁ + C₂ + C₃)

4. **Parallel voltage** stays the same (V_total = V_cell)

5. **Watt-hours add** regardless of configuration (Wh_total = Wh₁ + Wh₂)

6. **Series-parallel** combines both: series for voltage, parallel for capacity/runtime

7. **Cell matching** is critical for series (same capacity, age, chemistry, IR)

8. **Mismatched series cells** cause overcharge/over-discharge (fire risk for Li-ion)

9. **Parallel cells** must have same voltage BEFORE connecting (within 0.05V for Li-ion)

10. **BMS mandatory** for multi-cell Li-ion packs (prevents overcharge, over-discharge, imbalance)

11. **Passive balancing** uses bleed resistors (most common, wastes energy as heat)

12. **Active balancing** transfers energy (more efficient, higher cost)

13. **Weakest cell limits the entire pack** in series configuration

14. **One shorted cell in parallel** can discharge entire pack (use fuses per string)

15. **Higher current capability** in parallel: I_max = I_cell × number_of_strings

16. **Power (watts)** = V × I; series increases voltage, parallel increases current

17. **EV batteries** use series-parallel: Tesla Model 3 = 96S46P (4416 cells)

18. **Series configuration** is single point of failure: one open cell kills the pack

*This documentation belongs to https://github.com/InterCentury*