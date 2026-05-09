# Types - 02: Lithium-Ion Battery

## What is a Lithium-Ion Battery?

The lithium-ion (Li-ion) battery is a rechargeable battery technology that uses lithium ions as the primary charge carriers. It has become the dominant battery technology for portable electronics, electric vehicles, and grid storage due to its high energy density, low self-discharge, and lack of memory effect.

Lithium-ion batteries were first proposed in the 1970s, with the first commercial version released by Sony in 1991. Since then, Li-ion technology has evolved dramatically, with numerous chemistries optimized for energy density, power output, safety, or cost. The 2019 Nobel Prize in Chemistry was awarded to John Goodenough, M. Stanley Whittingham, and Akira Yoshino for their work developing lithium-ion batteries.

## Basic Chemistry and Construction

### How Lithium-Ion Batteries Work

Li-ion batteries store energy by moving lithium ions between positive and negative electrodes.

```
LITHIUM-ION BATTERY CHEMISTRY (Generic)

    DISCHARGE REACTION:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   LiC₆ (anode) + CoO₂ (cathode) → LiCoO₂ + C₆               │
    │                                                             │
    │   Lithium ions move from ANODE (negative) to CATHODE (+)    │  
    │   Electrons flow through external circuit                   │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    CHARGE REACTION (reverse):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   LiCoO₂ + C₆ → LiC₆ (anode) + CoO₂ (cathode)               │
    │                                                             │
    │   Lithium ions move from CATHODE (+) to ANODE (negative)    │
    │   (electrons pushed by charger)                             │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    SIMPLIFIED ANALOGY:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Li-ions = Swing (rocking chair battery)                   │
    │   Anode = Negative terminal (graphite)                      │
    │   Cathode = Positive terminal (lithium metal oxide)         │
    │   Electrolyte = Swimming pool (lithium salt in solvent)     │
    │                                                             │
    │   Ions "swing" back and forth between electrodes            │
    │   Hence nickname: "Rocking chair battery"                   │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

### Physical Construction

```
LI-ION BATTERY CROSS-SECTION (Cylindrical 18650)

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ┌─────────────────────────────────────────────────────┐   │
    │   │  ┌────────────────────────────────────────────────┐ │   │
    │   │  │                                                │ │   │
    │   │  │   Positive terminal (+)                        │ │   │
    │   │  │   (PTC + CID safety devices)                   │ │   │
    │   │  └────────────────────────────────────────────────┘ │   │
    │   │                                                     │   │
    │   │  ┌────────────────────────────────────────────────┐ │   │
    │   │  │  ████████████████████████████████████████████  │ │   │
    │   │  │  ██  Safety vent (bursts at high pressure) ██  │ │   │
    │   │  │  ████████████████████████████████████████████  │ │   │
    │   │  └────────────────────────────────────────────────┘ │   │
    │   │                                                     │   │
    │   │  ┌────────────────────────────────────────────────┐ │   │
    │   │  │  ████████████████████████████████████████████  │ │   │
    │   │  │  ██         Separator (porous polymer)     ██  │ │   │
    │   │  │  ██      (prevents short circuit)          ██  │ │   │
    │   │  │  ████████████████████████████████████████████  │ │   │
    │   │  └────────────────────────────────────────────────┘ │   │
    │   │                                                     │   │
    │   │  ┌────────────────────────────────────────────────┐ │   │
    │   │  │  ████████████████████████████████████████████  │ │   │
    │   │  │  ██             Cathode (positive)         ██  │ │   │
    │   │  │  ██        (lithium metal oxide)           ██  │ │   │
    │   │  │  ██        coated on aluminum foil         ██  │ │   │
    │   │  │  ████████████████████████████████████████████  │ │   │
    │   │  └────────────────────────────────────────────────┘ │   │
    │   │                                                     │   │
    │   │  ┌────────────────────────────────────────────────┐ │   │
    │   │  │  ████████████████████████████████████████████  │ │   │
    │   │  │  ██         Electrolyte (liquid)           ██  │ │   │
    │   │  │  ██    (lithium salt in organic solvent)   ██  │ │   │
    │   │  │  ████████████████████████████████████████████  │ │   │
    │   │  └────────────────────────────────────────────────┘ │   │
    │   │                                                     │   │
    │   │  ┌────────────────────────────────────────────────┐ │   │
    │   │  │  ████████████████████████████████████████████  │ │   │
    │   │  │  ██             Anode (negative)           ██  │ │   │
    │   │  │  ██        (graphite / carbon)             ██  │ │   │
    │   │  │  ██        coated on copper foil           ██  │ │   │
    │   │  │  ████████████████████████████████████████████  │ │   │
    │   │  └────────────────────────────────────────────────┘ │   │
    │   │                                                     │   │
    │   │  ┌─────────────────────────────────────────────┐    │   │
    │   │  │                                             │    │   │
    │   │  │   Negative terminal (-)                     │    │   │
    │   │  │   (case / can)                              │    │   │
    │   │  └─────────────────────────────────────────────┘    │   │
    │   │                                                     │   │
    │   └─────────────────────────────────────────────────────┘   │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    COMPONENT FUNCTIONS:

    Component               Function
    ──────────────────────────────────────────────────────────────
    Anode (graphite)        Stores Li-ions during charge
    Cathode (Li-metal oxide) Stores Li-ions during discharge
    Separator               Prevents short circuit, allows Li-ion flow
    Electrolyte             Conductive medium for Li-ions
    Current collectors      Aluminum (cathode), Copper (anode)
    PTC (Positive Temp Coeff) Limits current if overheated
    CID (Current Interrupt) Permanently disconnects if pressure high
    Safety vent             Releases gas at extreme pressure
```

## Lithium-Ion Form Factors

### Cylindrical Cells

The most common format (18650, 21700, etc.)

```
CYLINDRICAL CELL FORMATS

    18650 (18mm diameter × 65mm length):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ┌─────────────────────────────────────────────────────┐   │
    │   │  ████████████████████████████████████████████████   │   │
    │   │  ██                  18650                     ██   │   │
    │   │  ██               Li-ion Cell                  ██   │   │
    │   │  ██               (18×65mm)                    ██   │   │
    │   │  ████████████████████████████████████████████████   │   │
    │   │      │                                   │          │   │
    │   │      │                                   │          │   │
    │   │    ┌─┴─┐                               ┌─┴────┐     │   │
    │   │    │ + │                               │ -    │     │   │
    │   │    │top│                               │bottom│     │   │
    │   │    └───┘                               └──────┘     │   │
    │   └─────────────────────────────────────────────────────┘   │
    │                                                             │
    │   Capacity: 2000-3500mAh                                    │
    │   Voltage: 3.6V-3.7V nominal, 4.2V full                     │
    │   Use: Laptops, power tools, flashlights, vapes             │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    COMMON CYLINDRICAL SIZES:

    Size        Diameter    Length    Typical Capacity    Common Use
    ──────────────────────────────────────────────────────────────
    14500       14mm        50mm      600-900mAh          AA replacement
    14650       14mm        65mm      1000-1400mAh        Medical
    16650       16mm        65mm      1600-2000mAh        Flashlights
    17670       17mm        67mm      1300-1800mAh        Old laptops
    18500       18mm        50mm      1400-2000mAh        Power tools
    18650       18mm        65mm      2000-3500mAh        MOST COMMON
    20700       20mm        70mm      3000-4000mAh        E-bikes, vapes
    21700       21mm        70mm      4000-5000mAh        Tesla, power tools
    26650       26mm        65mm      4000-5500mAh        Flashlights, e-bikes
    32650       32mm        65mm      5000-6000mAh        Large packs
    4680        46mm        80mm      9000-10000mAh       Tesla (new)


    SAFETY FEATURES (Cylindrical):

    ├── PTC (Positive Temperature Coefficient) – Resettable fuse
    ├── CID (Current Interrupt Device) – Permanent disconnect (pressure)
    ├── Safety vent – Releases gas (prevents explosion)
    └── Steel case – Very robust, crush-resistant
```

### Prismatic Cells

Rectangular, space-efficient cells.

```
PRISMATIC CELL

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ┌─────────────────────────────────────────────────────┐   │
    │   │  ████████████████████████████████████████████████   │   │
    │   │  ██               Prismatic Cell               ██   │   │
    │   │  ██              (rectangular)                 ██   │   │
    │   │  ████████████████████████████████████████████████   │   │
    │   │                                                     │   │
    │   │   ┌─────────────────────────────────────────────┐   │   │
    │   │   │                                             │   │   │
    │   │   │          Stacked layers                     │   │   │
    │   │   │      (or wound flat oval)                   │   │   │
    │   │   │                                             │   │   │
    │   │   └─────────────────────────────────────────────┘   │   │
    │   │                                                     │   │
    │   │   Terminals on top (often screw or nut)             │   │
    │   │    Aluminum or steel case                           │   │
    │   │                                                     │   │
    │   └─────────────────────────────────────────────────────┘   │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘

    Advantages:
    ├── Higher space efficiency (no wasted space between cylinders)
    ├── Better for thin devices (phones, tablets)
    ├── Lower cost per Wh (for large format)
    └── Easier thermal management (flat surfaces)

    Disadvantages:
    ├── Less robust case (can swell)
    ├── Lower energy density than cylindrical (by volume)
    └── Can bulge with age (normal, but dangerous)

    Use: Smartphones, tablets, laptops (older), power banks, EVs
```

### Pouch Cells (LiPo)

Lightweight, flexible cells in foil pouches.

```
POUCH CELL (LiPo / Lithium Polymer)

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ┌─────────────────────────────────────────────────────┐   │
    │   │  ████████████████████████████████████████████████   │   │
    │   │  ██              Pouch Cell                    ██   │   │
    │   │  ██         (Lithium Polymer)                  ██   │   │
    │   │  ████████████████████████████████████████████████   │   │
    │   │                                                     │   │
    │   │   ┌─────────────────────────────────────────────┐   │   │
    │   │   │                                             │   │   │
    │   │   │   Flexible aluminum laminate pouch          │   │   │
    │   │   │                                             │   │   │
    │   │   │   ┌─────┐                                   │   │   │
    │   │   │   │     │  Tab (+)                          │   │   │
    │   │   │   └──┬──┘                                   │   │   │
    │   │   │      │                                      │   │   │
    │   │   │   ┌──┴──┐                                   │   │   │
    │   │   │   │     │  Tab (-)                          │   │   │
    │   │   │   └─────┘                                   │   │   │
    │   │   │                                             │   │   │
    │   │   └─────────────────────────────────────────────┘   │   │
    │   │                                                     │   │
    │   └─────────────────────────────────────────────────────┘   │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘

    Advantages:
    ├── Lightest weight (no metal case)
    ├── Can be very thin (<1mm)
    ├── Can be made in custom shapes
    ├── Highest energy density (by weight)
    └── Low cost for high volume

    Disadvantages:
    ├── Most delicate (pouch easily damaged)
    ├── Swells when damaged or aged (normal but dangerous)
    ├── Requires rigid support (no structural strength)
    ├── No built-in pressure vent (pouch just ruptures)
    └── More prone to fire when damaged

    Use: Drones, RC hobby, smartphones (current), tablets, wearables

    WARNING: Pouch cells are the most dangerous Li-ion format!
    Punctured pouch = immediate fire (vent with flame)
    Always handle with care, never crush or bend
```

## Lithium-Ion Chemistries

### NMC (Lithium Nickel Manganese Cobalt Oxide)

The most common consumer Li-ion chemistry.

```
NMC CHARACTERISTICS

    Composition: LiNiMnCoO₂ (various ratios: 111, 523, 622, 811)
    
    Typical voltage: 3.6-3.7V nominal
    Full charge: 4.2V
    Discharge cutoff: 2.5-3.0V

    Advantages:
    ├── High energy density (150-220 Wh/kg)
    ├── Good power output (high C-rate capability)
    ├── Balanced performance (energy + power)
    ├── Long cycle life (500-2000 cycles)
    ├── Most common in consumer products
    └── Lower cobalt content than LCO (cheaper)

    Disadvantages:
    ├── Contains cobalt (expensive, ethical concerns)
    ├── Thermal runaway at ~210°C
    └── Less energy dense than NCA

    Use: Power tools, e-bikes, laptops, EVs (Tesla, many others)
    Cobalt ratios: 111, 523, 622, 811 (less cobalt = cheaper, shorter life)
```

### LCO (Lithium Cobalt Oxide) - Original Li-ion

The original commercial Li-ion chemistry.

```
LCO CHARACTERISTICS

    Composition: LiCoO₂
    
    Typical voltage: 3.6-3.7V nominal
    Full charge: 4.2V (some 4.35V, 4.4V high-voltage variants)
    Discharge cutoff: 2.5-3.0V

    Advantages:
    ├── High energy density (160-200 Wh/kg)
    ├── Very smooth voltage curve
    ├── Stable performance
    └── Mature technology

    Disadvantages:
    ├── Expensive (cobalt is costly)
    ├── Lower power output (low C-rate)
    ├── Shorter cycle life (300-500 cycles)
    ├── Thermal runaway at ~150°C (less stable)
    ├── Cobalt mining ethical concerns
    └── Declining in popularity (replaced by NMC)

    Use: Smartphones (older), laptops (older), cameras
```

### LFP (Lithium Iron Phosphate) - Safest Chemistry

The safest and longest-lasting Li-ion chemistry.

```
LFP CHARACTERISTICS

    Composition: LiFePO₄
    
    Typical voltage: 3.2-3.3V nominal
    Full charge: 3.6-3.65V
    Discharge cutoff: 2.5V

    Advantages:
    ├── Excellent safety (no thermal runaway below ~270°C)
    ├── Very long cycle life (2000-5000+ cycles)
    ├── No cobalt (cheaper, ethical)
    ├── Flat voltage curve (stable output)
    ├── High power output (high C-rate)
    ├── Environmentally friendly
    └── Can be discharged to 0V (less damage)

    Disadvantages:
    ├── Lower energy density (90-140 Wh/kg)
    ├── Lower nominal voltage (3.2V vs 3.6-3.7V)
    ├── Higher self-discharge than NMC
    └── Poor cold temperature performance

    Use: Solar storage, golf carts, RVs, marine, power tools, EV buses
```

### NCA (Lithium Nickel Cobalt Aluminum Oxide)

High-energy chemistry used by Tesla.

```
NCA CHARACTERISTICS

    Composition: LiNiCoAlO₂
    
    Typical voltage: 3.6-3.7V nominal
    Full charge: 4.2V
    Discharge cutoff: 2.5-3.0V

    Advantages:
    ├── Very high energy density (200-260 Wh/kg)
    ├── High power capability
    ├── Lower cobalt content than LCO
    └── Good cycle life (500-1000 cycles)

    Disadvantages:
    ├── Contains cobalt (expensive)
    ├── Less stable than LFP (thermal runaway ~200°C)
    ├── Special handling required
    └── Limited suppliers

    Use: Tesla EVs (older models), high-energy applications
```

### LTO (Lithium Titanate) - Fastest Charging

Ultra-fast charging, extremely long life.

```
LTO CHARACTERISTICS

    Composition: Li₂TiO₃ (titanate anode)
    
    Typical voltage: 2.3-2.4V nominal (lower voltage!)
    Full charge: 2.8V
    Discharge cutoff: 1.5V

    Advantages:
    ├── Extremely long life (10,000-20,000+ cycles)
    ├── Very fast charging (5-10 minutes possible)
    ├── Excellent safety (no thermal runaway)
    ├── Wide temperature range (-50°C to +60°C)
    ├── High power output (very high C-rate)
    └── Zero-strain material (no expansion/contraction)

    Disadvantages:
    ├── Low energy density (50-80 Wh/kg) – lowest Li-ion!
    ├── Low voltage (2.4V vs 3.6V)
    ├── Expensive (titanium is costly)
    └── Larger for same energy

    Use: Electric buses, grid storage, industrial, UPS
```

### Chemistry Comparison Table

| Chemistry | Voltage | Energy Density (Wh/kg) | Cycle Life | Safety | Cobalt? | Cost | Best For |
|-----------|---------|------------------------|------------|--------|---------|------|----------|
| NMC | 3.6-3.7V | 150-220 | 500-2000 | Good | Yes | Medium | General, EVs |
| LCO | 3.6-3.7V | 160-200 | 300-500 | Poor | Yes | High | Phones (old) |
| LFP | 3.2-3.3V | 90-140 | 2000-5000+ | Excellent | No | Low | Solar, storage |
| NCA | 3.6-3.7V | 200-260 | 500-1000 | Fair | Yes | High | High-energy EVs |
| LTO | 2.3-2.4V | 50-80 | 10,000-20,000+ | Excellent | No | High | Fast charge |

## Key Specifications

### Voltage

```
LI-ION VOLTAGE RANGES (by cathode chemistry)

    PARAMETER               NMC/LCO      LFP          LTO
    ──────────────────────────────────────────────────────────
    Nominal voltage         3.6-3.7V     3.2-3.3V     2.3-2.4V
    Maximum charge          4.2V         3.65V        2.8V
    Minimum discharge       2.5-3.0V     2.5V         1.5V
    Storage (long-term)     3.7-3.8V     3.3V         2.3V
    Overcharge limit        4.25V        3.70V        2.9V
    Over-discharge limit    2.0V         2.0V         1.2V


    STATE OF CHARGE (NMC/LCO 4.2V cell):

    SoC (%)    Voltage (resting)    Notes
    ──────────────────────────────────────────────────────────
    100%       4.15-4.20V           Full charge
    90%        4.05-4.10V           Good
    80%        3.95-4.00V           Ideal storage?
    70%        3.87-3.92V           
    60%        3.80-3.85V
    50%        3.72-3.78V           Ideal long-term storage
    40%        3.65-3.70V
    30%        3.58-3.63V
    20%        3.50-3.55V           Recharge soon
    10%        3.40-3.45V           Danger zone
    0%         2.50-3.00V           Damaged (if <2.5V)

    WARNING: Voltage below 2.5V = irreversible damage!
    Do NOT attempt to charge deeply discharged Li-ion.
```

### Capacity

```
CAPACITY RATINGS

    TYPICAL CAPACITIES BY CELL SIZE:

    Cell Format    Capacity Range    Typical     Common Use
    ──────────────────────────────────────────────────────────
    18650          1500-3500mAh      2500mAh     Laptops, vapes
    21700          3000-5000mAh      4000mAh     Power tools, Tesla
    26650          4000-5500mAh      5000mAh     Flashlights
    32650          5000-6000mAh      5500mAh     E-bikes
    Prismatic      1000-5000mAh      3000mAh     Phones, tablets
    Pouch (LiPo)   200-5000+Ah       2000mAh     Drones, RC


    ENERGY DENSITY BY CHEMISTRY:

    Chemistry     Wh/kg (cell)    Wh/L (cell)    Wh/kg (pack)
    ──────────────────────────────────────────────────────────
    NMC (811)     220-260         550-650        150-180
    NMC (622)     200-230         500-600        140-170
    LCO           160-200         400-500        120-150
    LFP           90-140          220-280        80-120
    NCA           200-260         550-700        150-180
    LTO           50-80           100-150        40-70
```

### C-Rate Capability

How quickly a battery can charge or discharge.

```
C-RATE DEFINITION

    1C = Current equal to rated capacity in 1 hour
    
    Example: 2000mAh battery
    1C = 2.0A discharge (full discharge in 1 hour)
    2C = 4.0A discharge (30 minutes)
    0.5C = 1.0A discharge (2 hours)


    TYPICAL C-RATES:

    Chemistry     Max Charge     Max Discharge    Continuous
    ──────────────────────────────────────────────────────────
    NMC           1-2C           3-5C             1-2C
    LCO           0.7-1C         1-2C             0.5-1C
    LFP           1-3C           5-10C            1-2C
    NCA           1-2C           3-5C             1-2C
    LTO           5-10C          10-30C           2-5C
    Power cells   3-5C           10-20C           2-3C
    Energy cells  0.5-1C         1-3C             0.5-1C


    CAPACITY vs DISCHARGE RATE (NMC example, 2000mAh rated at 0.2C):

    Discharge Rate    Actual Capacity    Runtime
    ──────────────────────────────────────────────────────────
    0.2C (0.4A)       2000mAh (100%)     5 hours
    0.5C (1.0A)       1950mAh (97.5%)    1.95 hours
    1C (2.0A)         1900mAh (95%)      57 minutes
    2C (4.0A)         1750mAh (87.5%)    26 minutes
    3C (6.0A)         1550mAh (77.5%)    15.5 minutes
    5C (10A)          1300mAh (65%)      7.8 minutes
```

## Safety and Protection

### Built-in Safety Features

Li-ion cells have multiple safety mechanisms.

```
SAFETY DEVICES IN CYLINDRICAL CELLS

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   PTC (Positive Temperature Coefficient)                    │
    │   ├── Resettable fuse                                       │
    │   ├── Resistance increases with temperature                 │
    │   ├── Limits current during overheat                        │
    │   └── Resets when cooled                                    │
    │                                                             │
    │   CID (Current Interrupt Device)                            │
    │   ├── One-time permanent disconnect                         │
    │   ├── Activates at high internal pressure                   │
    │   ├── Physically breaks connection                          │
    │   └── Cannot be reset (battery is dead)                     │
    │                                                             │
    │   Safety Vent                                               │
    │   ├── Last resort protection                                │
    │   ├── Ruptures at extreme pressure                          │
    │   ├── Releases gas (may be flammable)                       │
    │   ├── Prevents explosion                                    │
    │   └── Battery destroyed                                     │
    │                                                             │
    │   Separator                                                 │
    │   ├── Shuts down at high temperature (shutdown separator)   │
    │   ├── Pores close when hot (stops ion flow)                 │
    │   └── Prevents thermal runaway propagation                  │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    POUCH CELL SAFETY:

    ├── NO PTC or CID (pouch is too thin)
    ├── Relies on external protection circuit (BMS)
    ├── Pouch swells before venting (warning sign!)
    ├── Ruptures with flame (very dangerous)
    └── Requires mechanical support (battery compartment)
```

### Battery Management System (BMS)

Multi-cell Li-ion packs require a BMS.

```
BMS PROTECTION FUNCTIONS

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   PROTECTION              TRIGGER           ACTION          │
    │   ──────────────────────────────────────────────────────────│
    │   Over-voltage            Cell >4.25V       Stop charge     │
    │   Under-voltage           Cell <2.5V        Stop discharge  │
    │   Over-current (charge)   >1-2C             Stop charge     │
    │   Over-current (discharge)>3-5C             Stop discharge  │
    │   Short circuit           Instant >100A     Instant cutoff  │
    │   Over-temperature        >65°C             Stop both       │
    │   Under-temperature       <0°C              Stop charge     │
    │   Cell imbalance          ΔV >0.3V          Balance charge  │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    BALANCE CHARGING:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Without balancing (dangerous!):                           │
    │   ┌─────────────────────────────────────────────────────┐   │
    │   │  Cell1: 4.20V  ✓                                    │   │
    │   │  Cell2: 4.20V  ✓                                    │   │
    │   │  Cell3: 4.15V  (undercharged)                       │   │
    │   └─────────────────────────────────────────────────────┘   │
    │   Charger sees 4.18V average → continues charging           │
    │   Cell3 reaches 4.20V, Cell1/Cell2 OVERCHARGE to 4.30V+     │
    │   Result: Fire/explosion!                                   │
    │                                                             │
    │   With balancing (safe):                                    │
    │   ┌─────────────────────────────────────────────────────┐   │
    │   │  Cell1: 4.18V  (balancing resistor on)              │   │
    │   │  Cell2: 4.18V  (balancing resistor on)              │   │
    │   │  Cell3: 4.15V  (no balancing)                       │   │
    │   └─────────────────────────────────────────────────────┘   │
    │   BMS bleeds excess charge from Cell1/Cell2                 │
    │   All cells reach 4.20V together → safe!                    │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘

    WARNING: NEVER charge multi-cell Li-ion without BMS!
    Unbalanced cells = overcharge = fire.
```

## Common Applications

### Electric Vehicles (EVs)

```
EV BATTERY REQUIREMENTS

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Tesla Model 3 (Long Range):                               │
    │   ├── Chemistry: NCA or NMC (varies by year)                │
    │   ├── Cells: 4416 x 21700 (or 4680 for newer)               │
    │   ├── Voltage: 350-400V (nominal)                           │
    │   ├── Capacity: 75-82 kWh                                   │
    │   ├── Weight: 480 kg (~1060 lbs)                            │
    │   ├── Range: 350+ miles                                     │
    │   ├── Fast charge: 15-30 minutes (250kW)                    │
    │   └── Life: 300-500 cycles (150,000+ miles)                 │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    EV BATTERY CHEMISTRY TRENDS:

    Manufacturer     Historical          Current              Future
    ──────────────────────────────────────────────────────────────
    Tesla           18650 NCA           21700 NCA/NMC        4680 NMC
    GM              LFP (Bolt)          NCMA                 LFP
    Ford            NMC (earlier)       NCM (Mustang)        LFP
    VW Group        NMC                 NMC/SSB              SSB
    BYD             LFP (Blade)         LFP (Blade)          LFP

    LFP gaining popularity (cheaper, safer, no cobalt)
```

### Consumer Electronics

```
CONSUMER ELECTRONICS REQUIREMENTS

    Device              Cell Format    Typical Capacity    Voltage
    ──────────────────────────────────────────────────────────────
    Smartphone          Pouch (LiPo)   3000-5000mAh        3.85V
    Tablet              Pouch          5000-10000mAh       3.85V
    Laptop              Pouch/Prismatic 40-99Wh (2-3S)     7.4-11.4V
    Power bank          18650/Pouch     5000-30000mAh       3.6-3.7V
    Wireless earbuds    Pouch (tiny)    30-50mAh            3.7V
    Smartwatch          Pouch (curved)  200-400mAh          3.85V
    E-cigarette / vape  18650           2500-3000mAh        3.6-3.7V


    VOLTAGE NOTES:

    Standard Li-ion: 3.6-3.7V nominal, 4.2V full
    High-voltage Li-ion: 3.85V nominal, 4.35V/4.4V full (smartphones)
    Requires special charger (not interchangeable!)
```

### Power Tools

```
POWER TOOL BATTERY REQUIREMENTS

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Common power tool voltages:                              │
    │   ├── 12V: 3 cells in series (3S) – 10.8-12.6V            │
    │   ├── 18V: 5 cells in series (5S) – 18-21V                │
    │   ├── 20V: 5 cells in series (5S) – 18-21V (marketing)    │
    │   ├── 24V: 6 cells in series (6S) – 21.6-25.2V            │
    │   ├── 36V: 10 cells in series (10S) – 36-42V              │
    │   └── 40V: 10 cells in series (10S) – 36-42V (marketing)  │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    Tool Type          Typical Battery    Cells    Capacity
    ──────────────────────────────────────────────────────────────
    Drill/driver       12V-18V            3-5S     1.5-5Ah
    Impact driver      18V-20V            5S       2-5Ah
    Circular saw       18V-36V            5-10S    4-8Ah
    Lawn mower         36V-40V            10S      4-10Ah
    Chainsaw           36V-80V            10-20S   4-8Ah

    Cells: Usually 18650 or 21700 high-power (30A+ capable)
    Chemistry: NMC or LFP (some)
```

## Common Problems and Troubleshooting

### Problem 1: Battery Won't Charge

```
SYMPTOMS:
├── Charger doesn't recognize battery
├── Battery voltage 0V or very low (<0.5V)
├── Battery shows no signs of life
├── Charger flashes error code

CAUSES:
├── Over-discharge (cell voltage <2.0V)
├── Charger not compatible (wrong voltage/chemistry)
├── BMS tripped (CID activated)
├── Internal short circuit
├── Bad connection or broken tab

DIAGNOSIS:
├── Measure cell voltage (if accessible)
├── Try "waking" deeply discharged cell (with caution!)
├── Check charger output voltage
├── Inspect for physical damage (swelling, dents)
├── Test with known good charger

SOLUTIONS:
├── Battery <2.0V: Attempt recovery (with caution, outside!)
│   └── Charge at VERY low current (0.05C) until 2.5V
├── Battery 0V: Internal CID tripped = REPLACE (dangerous)
├── Swollen battery: STOP, REPLACE, DISPOSE
├── Use correct charger (Li-ion ONLY, not NiMH or lead-acid)

WARNING: Attempting to charge a deeply discharged Li-ion is DANGEROUS!
Only attempt if you understand the risks and have appropriate safety equipment.
Damaged or 0V Li-ion = FIRE RISK – replace immediately!
```

### Problem 2: Rapid Self-Discharge

```
SYMPTOMS:
├── Battery loses charge overnight (without use)
├── Voltage drops quickly when idle
├── Battery gets warm even when not in use
├── Capacity significantly reduced

CAUSES:
├── Internal short circuit (dendrites, separator damage)
├── Damaged separator (from over-discharge or overcharge)
├── Contamination inside cell
├── High temperature (accelerates self-discharge)
├── Old age (normal end-of-life)

DIAGNOSIS:
├── Measure voltage daily (should drop <0.05V per week)
├── Check temperature (warm idle = internal short)
├── Compare to known good battery
├── Discharge test vs spec

SOLUTIONS:
├── If warm when idle: REPLACE IMMEDIATELY (fire risk!)
├── If self-discharge >5% per day: REPLACE
├── Store in cool location if mild self-discharge
├── For old batteries: Recycle (reached end of life)

WARNING: Lithium-ion batteries that self-discharge rapidly are dangerous!
Internal short = thermal runaway risk = replace now!
```

### Problem 3: Swollen Battery (Pouch/Pouch LiPo)

```
SYMPTOMS:
├── Battery case visibly puffed or bloated
├── Device case bulging or separating
├── Battery no longer fits in compartment
├── Reduced capacity (swelling from gas)

CAUSES:
├── Gas generation from electrolyte decomposition
├── Overcharging (voltage too high)
├── Overheating (during use or charging)
├── Manufacturing defect
├── End of normal life (gas accumulates with age)
├── Mechanical damage (pouch punctured)

DIAGNOSIS:
├── Remove battery and place on flat surface
├── Rotate battery – if spins easily, it's swollen
├── Compare thickness to new/newer battery
├── Check for hot spots (internal short)

SOLUTIONS:
├── STOP USING IMMEDIATELY – swollen Li-ion is DANGEROUS!
├── DO NOT CHARGE (fire risk)
├── DO NOT PUNCTURE (fire/explosion)
├── Place in fireproof container (sand, metal box)
├── Dispose at hazardous waste facility ASAP
├── Do NOT store indoors

WARNING: Swollen Li-ion pouch cells are EXTREMELY DANGEROUS!
They can catch fire spontaneously or when punctured.
Handle with extreme care, keep away from flammables.
```

### Problem 4: Overheating During Charge/Discharge

```
SYMPTOMS:
├── Battery too hot to touch (>50°C)
├── Charger stops prematurely (thermal protection)
├── Equipment reduces performance (throttling)
├── Burning smell

CAUSES:
├── Charging/discharging at excessive C-rate
├── High internal resistance (old/damaged battery)
├── Poor ventilation (battery enclosed)
├── Ambient temperature too high
├── Internal short (self-heating)
├── Mismatched charger (wrong voltage/current)

DIAGNOSIS:
├── Measure temperature with IR thermometer
├── Compare to normal operation (warm = OK, hot = problem)
├── Check charge/discharge current vs rating
├── Inspect for swelling (internal short)

SOLUTIONS:
├── Stop charging/discharging immediately if >50°C
├── Allow to cool before further use
├── Reduce charge/discharge current (lower C-rate)
├── Improve ventilation (add airflow)
├── Move battery to cooler environment
├── If internal short suspected: REPLACE

NORMAL TEMPERATURES (under 1C rate):
├── 20-35°C (68-95°F): Normal
├── 35-45°C (95-113°F): Warm (acceptable)
├── 45-50°C (113-122°F): Hot (reduce load)
├── 50-60°C (122-140°F): Very hot (stop!)
├── >60°C (>140°F): Danger (thermal runaway risk)

Permanent damage occurs above 60°C!
```

## Charging Best Practices

```
LI-ION CHARGING RULES

    DO:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ✓ Use Li-ion charger ONLY (not NiMH, lead-acid, etc.)    │
    │   ✓ Set charger to correct cell count (1S, 2S, 3S, etc.)  │
    │   ✓ Use balance charger for multi-cell packs               │
    │   ✓ Charge on non-flammable surface (concrete, ceramic)    │
    │   ✓ Use LiPo safety bag for pouch/LiPo cells               │
    │   ✓ Charge at 0.5-1C rate for longest life                 │
    │   ✓ Monitor temperature (stop if >45°C)                    │
    │   ✓ Disconnect when fully charged                          │
    │   ✓ Store at 50% charge (3.7-3.8V)                        │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    DON'T:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ✗ Never leave charging unattended (especially LiPo)      │
    │   ✗ Never charge below 0°C (irreversible damage)           │
    │   ✗ Never charge swollen or damaged battery                │
    │   ✗ Never exceed 4.20V per cell (4.2V for standard)        │
    │   ✗ Never charge at >1C unless battery is rated for it     │
    │   ✗ Never use "car charger" or "dumb" chargers             │
    │   ✗ Never charge on flammable surface (wood, carpet)       │
    │   ✗ Never charge in sealed container                       │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    OPTIMAL CHARGE PROFILE (NMC/LCO):

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Current (A)    Voltage (V)                               │
    │        │               │                                   │
    │    1C ┼●             4.2 ┼                     ●            │
    │        │ ╲                 │                   ╱│            │
    │    0.8C┼  ╲               4.0 ┼                 ╱             │
    │        │   ╲                 │               ╱               │
    │    0.6C┼    ╲               3.8 ┼           ╱                 │
    │        │     ╲               │         ╱                     │
    │    0.4C┼      ╲             3.6 ┼     ╱                       │
    │        │       ╲             │   ╱                           │
    │    0.2C┼        ╲           3.4 ┼●                            │
    │        │         ╲           │                               │
    │    0.0C┼──────────●──────────3.2 ┼────────────────► Time     │
    │                                                             │
    │          CC phase          CV phase                         │
    │      (Constant Current)  (Constant Voltage)                │
    │                                   │                         │
    │                                   ▼                         │
    │                          Stop when current drops to C/10    │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

## Storage and Disposal

### Long-term Storage

```
STORAGE BEST PRACTICES

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Ideal storage: 3.7-3.8V (50-60% charge)                 │
    │   Temperature: 5-15°C (41-59°F) for best life              │
    │   Acceptable: 0-25°C (32-77°F)                             │
    │   Avoid: >30°C (>86°F) – accelerates aging                │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    STORAGE LIFE (NMC, 50% charge):

    Temperature     Capacity loss/year    Notes
    ──────────────────────────────────────────────────────────────
    0°C (32°F)      2-4%                  Excellent (freezer not needed)
    25°C (77°F)     10-20%                Normal storage
    40°C (104°F)    25-35%                Reduced life
    60°C (140°F)    40-50%                Severe damage


    LONG-TERM STORAGE GUIDELINES:

    ├── Charge to 50-60% (3.7-3.8V per cell) – NOT fully charged!
    ├── Store in cool, dry place
    ├── Check voltage every 6 months
    ├── Recharge to 3.7-3.8V if voltage drops below 3.3V
    ├── Never store fully discharged (<2.5V) – permanent damage
    └── Never store in hot car or direct sunlight
```

### Disposal and Recycling

```
END-OF-LIFE INDICATORS

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ☑ Swollen or puffed (pouch cells) – IMMEDIATE disposal  │
    │   ☑ Cracked or leaking case – DANGER – dispose immediately│
    │   ☑ Capacity <60-70% of original – recycle                 │
    │   ☑ Won't hold charge overnight – recycle                   │
    │   ☑ Visible corrosion or rust – recycle                     │
    │   ☑ Age >5 years (consumer) or >10 years (EV) – recycle    │
    │   ☑ Physical damage (dents, punctures) – recycle           │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    RECYCLING LOCATIONS:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   US:                                                        │
    │   ├── Call2Recycle (call2recycle.org) – (800) 822-8837     │
    │   ├── Best Buy                                             │
    │   ├── Home Depot                                           │
    │   ├── Lowe's                                               │
    │   ├── Staples                                              │
    │   ├── Local hazardous waste facility                       │
    │   └── Battery specialty stores (Batteries Plus)           │
    │                                                             │
    │   WARNING: DO NOT throw Li-ion batteries in trash!        │
    │   They can catch fire in garbage trucks or landfills!      │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    PREPARING FOR DISPOSAL:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ✓ Discharge to <1V (if safe) using resistor              │
    │     (Skip if battery is swollen or damaged)                │
    │   ✓ Tape terminals with electrical tape                    │
    │   ✓ Place each battery in separate plastic bag             │
    │   ✓ Store in cool, dry location until recycling            │
    │   ✓ Do NOT store for extended periods                      │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

## Quick Reference Table

| Parameter | NMC/LCO | LFP | LTO |
|-----------|---------|-----|-----|
| Nominal voltage | 3.6-3.7V | 3.2-3.3V | 2.3-2.4V |
| Full charge | 4.2V | 3.65V | 2.8V |
| Discharge cutoff | 2.5-3.0V | 2.5V | 1.5V |
| Energy density (Wh/kg) | 150-260 | 90-140 | 50-80 |
| Cycle life (100% DoD) | 300-500 | 1500-2000 | 3000-5000+ |
| Max charge C-rate | 1-2C | 1-3C | 5-10C |
| Max discharge C-rate | 3-5C | 5-10C | 10-30C |
| Thermal runaway temp | ~150-210°C | ~270°C+ | None |
| Safety | Moderate | Excellent | Excellent |
| Cobalt content | Yes (some) | No | No |
| Relative cost | $$ | $ | $$$ |
| Best for | General, EVs | Storage, safety | Fast charge |

## Summary

1. **Lithium-ion battery** uses Li-ions moving between electrodes (rocking chair battery)

2. **Invented:** 1970s research, commercialized by Sony in 1991

3. **Nominal voltages:** NMC/LCO (3.6-3.7V), LFP (3.2-3.3V), LTO (2.3-2.4V)

4. **Full charge voltages:** 4.2V (NMC/LCO), 3.65V (LFP), 2.8V (LTO)

5. **Minimum discharge:** 2.5-3.0V – below 2.5V = permanent damage

6. **Form factors:** Cylindrical (18650, 21700), Prismatic (rectangular), Pouch (LiPo)

7. **NMC** – Most common, balanced performance (power tools, EVs, laptops)

8. **LCO** – Original chemistry, high energy, lower safety (phones – older)

9. **LFP** – Safest, longest life, no cobalt (solar, storage, EV buses)

10. **NCA** – Highest energy density (Tesla older models)

11. **LTO** – Fastest charging, longest cycle life (10,000-20,000 cycles)

12. **Pouch cells (LiPo)** – Lightest, most dangerous – handle with care

13. **BMS mandatory for multi-cell packs** – prevents overcharge, over-discharge, balancing

14. **Never overcharge** (>4.25V) – causes fire/explosion (thermal runaway)

15. **Never over-discharge** (<2.5V) – causes permanent damage, dendrites

16. **Swollen Li-ion = DANGER** – stop using, dispose immediately (fire risk)

17. **Storage at 50% charge** (3.7-3.8V) – cool location (5-25°C)

18. **Recycle all Li-ion batteries** – never in trash (fire hazard)

*This documentation belongs to https://github.com/InterCentury*