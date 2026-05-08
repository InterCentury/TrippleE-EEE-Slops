# Types - 03: Lithium Polymer (LiPo) Battery

## What is a Lithium Polymer Battery?

Lithium Polymer (LiPo) is a rechargeable battery that uses a polymer electrolyte instead of a liquid electrolyte. The term "LiPo" most commonly refers to pouch cell batteries with a flexible, foil-based enclosure, which are the dominant format for drones, RC vehicles, smartphones, and wearable devices.

The key distinction of LiPo batteries is their solid or gel-like polymer electrolyte, which eliminates the need for a rigid metal case. This allows them to be manufactured in very thin, flexible, lightweight formats that can be customized to fit almost any shape. The first commercial LiPo batteries appeared in the 1990s and have since become ubiquitous in portable electronics.

## LiPo vs Standard Li-ion

### Key Differences

Understanding the difference between "LiPo" (chemistry) and "LiPo" (format).

```
LITHIUM POLYMER CLARIFICATION

    TRUE LITHIUM POLYMER (Chemistry):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Uses solid or gel polymer electrolyte                     │
    │   No liquid electrolyte                                     │
    │   More stable than liquid Li-ion                            │
    │   Lower ionic conductivity (historically)                   │
    │   True LiPo is rare today                                   │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    MODERN "LiPo" (Pouch Cell Format):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   What is commonly sold as "LiPo" is actually:             │
    │   ├── Standard Li-ion chemistry (NMC, LCO, LFP)            │
    │   ├── Liquid or gel electrolyte                            │
    │   ├── Pouch cell format (flexible foil)                    │
    │   └── Marketing term "LiPo" = pouch cell                  │
    │                                                             │
    │   True polymer electrolyte is uncommon in consumer products│
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    PRACTICAL DEFINITION (Consumer Use):

    "LiPo" = Pouch cell lithium-ion battery in flexible packaging

    Characteristics:
    ├── Flexible aluminum-laminated foil pouch
    ├── No rigid metal case
    ├── Very lightweight
    ├── Can be made in thin, custom shapes
    ├── Higher energy density by weight
    └── More susceptible to damage (punctures, swelling)
```

### Comparison: Cylindrical Li-ion vs Pouch LiPo

```
COMPARISON CHART

    Feature                 Cylindrical 18650    Pouch Cell ("LiPo")
    ──────────────────────────────────────────────────────────────
    Case                    Rigid steel         Flexible foil pouch
    Weight                  Heavier             Lighter (20-30% less)
    Energy density (Wh/kg)  200-250             230-280
    Energy density (Wh/L)   600-700             500-600 (typically)
    Shape                   Round only          Custom (any shape)
    Thickness               Minimum 18mm        Down to 0.5mm
    Mechanical strength     Very strong         Delicate
    Crush resistance        Excellent           Poor
    Puncture resistance     Good                Poor (fire risk!)
    Swelling                Very rare           Common (normal with age)
    Safety vent             Yes (built-in)      No (pouch ruptures)
    PTC / CID               Yes                 No (external BMS only)
    Cost per Wh             Lower               Higher
    Manufacturing           Very automated      Less automated
    Cooling                 Internal (center)   External (surface only)
    Vibration resistance    Excellent           Good

    WARNING: Pouch cells are more dangerous when damaged!
    Puncture = immediate fire (jet flame), no safety vent.
```

## LiPo Form Factors

### Pouch Cell Construction

How pouch cells are made.

```
POUCH CELL CROSS-SECTION

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ┌─────────────────────────────────────────────────────┐   │
    │   │  Aluminum laminate foil pouch                       │   │
    │   │  ┌─────────────────────────────────────────────┐    │   │
    │   │  │                                             │    │   │
    │   │  │  ┌─────────────────────────────────────┐   │    │   │
    │   │  │  │  Tab (+) (aluminum)                 │   │    │   │
    │   │  │  └─────────────────────────────────────┘   │    │   │
    │   │  │                                             │    │   │
    │   │  │  Stacked layers:                           │    │   │
    │   │  │                                             │    │   │
    │   │  │  ████████████████████████████████████████  │    │   │
    │   │  │  ██      Cathode (positive)          ██   │    │   │
    │   │  │  ██      (aluminum foil)             ██   │    │   │
    │   │  │  ████████████████████████████████████████  │    │   │
    │   │  │  ██      Separator (polymer)         ██   │    │   │
    │   │  │  ████████████████████████████████████████  │    │   │
    │   │  │  ██      Anode (negative)            ██   │    │   │
    │   │  │  ██      (copper foil)               ██   │    │   │
    │   │  │  ████████████████████████████████████████  │    │   │
    │   │  │  ██      Separator                   ██   │    │   │
    │   │  │  ████████████████████████████████████████  │    │   │
    │   │  │  ██      Cathode                     ██   │    │   │
    │   │  │  ████████████████████████████████████████  │    │   │
    │   │  │      (multiple layers stacked)              │    │   │
    │   │  │                                             │    │   │
    │   │  │  ┌─────────────────────────────────────┐   │    │   │
    │   │  │  │  Tab (-) (copper/nickel)            │   │    │   │
    │   │  │  └─────────────────────────────────────┘   │    │   │
    │   │  │                                             │    │   │
    │   │  └─────────────────────────────────────────────┘    │   │
    │   │                                                     │   │
    │   └─────────────────────────────────────────────────────┘   │
    │                                                             │
    │   Pouch layers (outside to inside):                         │
    │   ├── Outer: Nylon (protection)                            │
    │   ├── Middle: Aluminum (moisture barrier)                  │
    │   ├── Inner: Polypropylene (heat seal, chemical resistance)│
    │   └── Total thickness: 100-150µm                           │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    SEAL AREAS:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ┌─────────────────────────────────────────────────────┐   │
    │   │  ████████████████████████████████████████████████   │   │
    │   │  ██             Top seal                     ██   │   │
    │   │  ██     (positive and negative tabs)         ██   │   │
    │   │  ██     (sealed around tabs)                 ██   │   │
    │   │  ██                                       ██   │   │
    │   │  ██         ┌─────────────────────┐       ██   │   │
    │   │  ██         │                     │       ██   │   │
    │   │  ██         │   Cell body         │       ██   │   │
    │   │  ██         │   (active area)     │       ██   │   │
    │   │  ██         │                     │       ██   │   │
    │   │  ██         └─────────────────────┘       ██   │   │
    │   │  ██                                       ██   │   │
    │   │  ██             Bottom seal              ██   │   │
    │   │  ██                                       ██   │   │
    │   │  ██            Side seals                ██   │   │
    │   │  ████████████████████████████████████████████   │   │
    │   └─────────────────────────────────────────────────────┘   │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

### Common Pouch Cell Sizes

```
POUCH CELL DIMENSIONS

    Naming convention: Thickness × Width × Length (mm)
    
    Example: 504060 = 5.0mm thick, 40mm wide, 60mm long

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Small (phone-sized):                                      │
    │   ├── 303030: 3.0 × 30 × 30 mm (150-200mAh)               │
    │   ├── 354040: 3.5 × 40 × 40 mm (300-400mAh)               │
    │   ├── 404060: 4.0 × 40 × 60 mm (500-700mAh)               │
    │   └── 505070: 5.0 × 50 × 70 mm (1000-1200mAh)             │
    │                                                             │
    │   Medium (RC/drone sized):                                 │
    │   ├── 503040: 5.0 × 30 × 40 mm (400-500mAh)               │
    │   ├── 653450: 6.5 × 34 × 50 mm (800-1000mAh)              │
    │   ├── 803850: 8.0 × 38 × 50 mm (1200-1500mAh)             │
    │   └── 904560: 9.0 × 45 × 60 mm (1800-2200mAh)             │
    │                                                             │
    │   Large (tablet/power bank sized):                         │
    │   ├── 105070: 10 × 50 × 70 mm (3000-3500mAh)              │
    │   ├── 125080: 12 × 50 × 80 mm (4000-5000mAh)              │
    │   ├── 1550100: 15 × 50 × 100 mm (6000-8000mAh)            │
    │   └── 2060130: 20 × 60 × 130 mm (10000-12000mAh)          │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    TYPICAL CAPACITY BY SIZE (3.7V LiPo):

    Size (mm)           Typical Capacity (mAh)    Application
    ──────────────────────────────────────────────────────────────
    3×20×25             120-150                  Hearing aid
    4×30×40             350-450                  Fitness tracker
    5×30×50             600-800                  Smartwatch
    5×40×60             1000-1200                Smartphone (small)
    6×40×70             1500-1800                Smartphone
    8×50×80             2500-3000                Smartphone (large)
    10×60×80            4000-5000                Tablet
    12×60×120           6000-8000                Power bank
    15×60×130           9000-11000               Large power bank
    20×80×150           15000-20000              Laptop (external)
```

### Custom Shapes

LiPo cells can be manufactured in almost any shape.

```
CUSTOM SHAPE CAPABILITIES

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Possible shapes:                                          │
    │                                                             │
    │   Rectangular:    ┌─────┐  Most common                     │
    │                   │     │                                  │
    │                   └─────┘                                  │
    │                                                             │
    │   Notched:        ┌─────┐                                  │
    │                   │  ┌──┘  Fits around components          │
    │                   │  │                                     │
    │                   └──┘                                     │
    │                                                             │
    │   Tapered:        ┌─────┐                                  │
    │                   │    \  Wedge shape                      │
    │                   │     \                                  │
    │                   └──────┘                                 │
    │                                                             │
    │   Curved:         (     )  Radiused for curved devices     │
    │                   (     )                                  │
    │                    ‾‾‾‾‾                                   │
    │                                                             │
    │   Folded:         ┌───┐                                    │
    │                   │   ├──┐  L-shape (fit in corners)       │
    │                   └───┘  │                                 │
    │                        ┌─┘                                 │
    │                        │                                   │
    │                        └───┘                               │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘

    Minimum thickness: ~0.5mm (500µm)
    Maximum thickness: ~20mm (limited by heat dissipation)
    Custom shapes require high minimum order quantities (10k-100k units)
```

## LiPo Specifications

### Voltage

```
LIPO VOLTAGE BY CELL COUNT

    Cell Count (S)    Nominal V    Full Charge    Empty (cutoff)
    ──────────────────────────────────────────────────────────────
    1S (single)       3.7V         4.2V           3.0-3.3V
    2S (2 cells)      7.4V         8.4V           6.0-6.6V
    3S (3 cells)      11.1V        12.6V          9.0-9.9V
    4S (4 cells)      14.8V        16.8V          12.0-13.2V
    5S (5 cells)      18.5V        21.0V          15.0-16.5V
    6S (6 cells)      22.2V        25.2V          18.0-19.8V
    8S (8 cells)      29.6V        33.6V          24.0-26.4V
    10S (10 cells)    37.0V        42.0V          30.0-33.0V
    12S (12 cells)    44.4V        50.4V          36.0-39.6V

    NOTES:
    ├── 1S = 1 cell in series (most common for single-cell devices)
    ├── 2S-6S common for RC/drones
    ├── 3S = "11.1V LiPo" (standard RC pack)
    ├── 6S = "22.2V LiPo" (larger drones, RC helicopters)
    └── "S" count = cells in series (voltage adds)


    VOLTAGE vs STATE OF CHARGE (1S LiPo)

    SoC (%)    Voltage (resting)    Notes
    ──────────────────────────────────────────────────────────────
    100%       4.18-4.20V           Full charge – ready to fly/fly
    90%        4.05-4.10V           Stop charging (storage for long)
    80%        3.95-4.00V           
    70%        3.87-3.92V
    60%        3.80-3.85V
    50%        3.72-3.78V           IDEAL LONG-TERM STORAGE
    40%        3.65-3.70V
    30%        3.58-3.63V
    20%        3.50-3.55V           Land/RECHARGE SOON!
    15%        3.45-3.50V           Low voltage warning
    10%        3.40-3.45V           Danger zone (damage)
    5%         3.30-3.35V           SEVERE DAMAGE
    0%         <3.00V               Likely ruined

    DRONE/POWER TOOL CUTOFFS:
    ├── Soft cutoff (warning): 3.3-3.5V per cell
    ├── Hard cutoff (shutdown): 3.0-3.3V per cell
    └── NEVER discharge below 3.0V!
```

### Capacity and C-Rating

LiPo batteries are known for high discharge rates (C-ratings).

```
C-RATING EXPLANATION

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   C-Rating = Maximum safe continuous discharge rate        │
    │                                                             │
    │   2000mAh battery:                                         │
    │   1C = 2.0A                                                │
    │   20C = 40A (continuous)                                  │
    │   40C = 80A (burst, 5-10 seconds)                         │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    TYPICAL LIPO C-RATINGS:

    Application              Continuous C    Burst C       Discharge A (2Ah)
    ──────────────────────────────────────────────────────────────
    Smartphone              1-2C            N/A           2-4A
    Power bank              1-2C            N/A           2-4A
    Laptop                  2-3C            N/A           4-6A
    RC car (basher)         20-40C          40-80C        40-80A
    RC drone (racing)       70-120C         100-150C      140-240A
    RC plane                30-50C          50-70C        60-100A
    E-bike                  10-20C          20-30C        20-40A
    Power tool              10-15C          20-30C        20-50A
    FPV goggles             5-10C           N/A           10-20A


    WHAT C-RATING MEANS:

    C-Rating    Max Safe Current (2Ah)    Runtime (full discharge)
    ──────────────────────────────────────────────────────────────
    1C          2.0A                       60 minutes
    5C          10A                        12 minutes
    10C         20A                        6 minutes
    20C         40A                        3 minutes
    30C         60A                        2 minutes
    50C         100A                       1.2 minutes
    100C        200A                       36 seconds

    WARNING: Exceeding C-rating causes:
    ├── Extreme heat (battery can exceed 80°C)
    ├── Voltage sag (shuts down device)
    ├── Reduced capacity (permanent)
    ├── Swelling (gas generation)
    └── FIRE (thermal runaway)
```

### Internal Resistance

Internal resistance (IR) is critical for LiPo performance.

```
INTERNAL RESISTANCE (IR)

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Typical IR per cell (new, at 25°C):                      │
    │                                                             │
    │   Cell Size     High C (racing)    Mid C (sport)    Low C   │
    │   ──────────────────────────────────────────────────────────│
    │   1S 150mAh     30-50mΩ            50-80mΩ          80-120mΩ│
    │   1S 500mAh     15-25mΩ            25-40mΩ          40-60mΩ │
    │   2S 1000mAh    8-15mΩ             15-25mΩ          25-35mΩ │
    │   3S 1300mAh    6-12mΩ             12-20mΩ          20-30mΩ │
    │   3S 2200mAh    5-8mΩ              8-15mΩ           15-22mΩ │
    │   4S 1500mAh    5-10mΩ             10-18mΩ          18-25mΩ │
    │   6S 5000mAh    2-4mΩ              4-7mΩ            7-12mΩ  │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    WHAT IR AFFECTS:

    Low IR (good):
    ├── Higher voltage under load (less sag)
    ├── More power output (W = V × I)
    ├── Less heat generated (P = I²R)
    ├── Longer cycle life
    └── Better performance in cold weather

    High IR (bad/aging):
    ├── Voltage sag under load (loss of power)
    ├── Overheating (wasted energy as heat)
    ├── Reduced runtime
    ├── Can't deliver rated C-rating
    ├── End of life approaching
    └── Swelling may occur


    IR INCREASE OVER LIFE:

    New battery:        IR = 10mΩ (baseline)
    After 50 cycles:   IR = 12-15mΩ (slight increase)
    After 100 cycles:  IR = 15-20mΩ (noticeable sag)
    After 200 cycles:  IR = 25-35mΩ (poor performance)
    After 300 cycles:  IR = 40-60mΩ (end of life)
```

## LiPo Connectors

### Common Connector Types

```
LIPO CONNECTOR GUIDE

    JST (Small cells):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ┌───┐                                                   │
    │   │   │ 2-pin                                             │
    │   │   │ 2.5mm pitch                                       │
    │   └───┘                                                   │
    │                                                             │
    │   Current: 2-5A                                           │
    │   Use: 1-2S small batteries (150-1000mAh)                 │
    │   Example: Tiny whoop, small RC, micro drones             │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    Micro Losi (Walkera):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ┌───┐                                                   │
    │   │   │ 2-pin                                             │
    │   │   │ 2.0mm pitch                                       │
    │   └───┘                                                   │
    │                                                             │
    │   Current: 3-8A                                           │
    │   Use: Small drones, micro RC                              │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    JST-PH (Balance connectors):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ┌───┬───┬───┐                                           │
    │   │   │   │   │ 2-7 pin (cell count +1)                   │
    │   │   │   │   │ 2.0mm pitch                               │
    │   └───┴───┴───┘                                           │
    │                                                             │
    │   Current: 2-3A (signal only)                              │
    │   Use: Balance charging (all multi-cell LiPo)              │
    │   Pin count = cells + 1 (3S needs 4 pins)                 │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    XT30 (Medium power):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ┌─┐   ┌─┐                                               │
    │   │ │   │ │ 2-pin (yellow housing)                        │
    │   │ │   │ │ 30A continuous                                │
    │   └─┘   └─┘                                               │
    │                                                             │
    │   Current: 30A continuous, 45A burst                      │
    │   Use: 2-4S packs 1000-2000mAh                            │
    │   Example: 3S 1500mAh drone                               │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    XT60 (Standard):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ┌─┐   ┌─┐                                               │
    │   │ │   │ │ 2-pin (yellow housing)                        │
    │   │ │   │ │ 60A continuous                                │
    │   └─┘   └─┘                                               │
    │                                                             │
    │   Current: 60A continuous, 90A burst                       │
    │   Use: 3-6S packs 1300-5000mAh (MOST COMMON)              │
    │   Example: 6S 5000mAh drone, RC car, plane                │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    XT90 (High power):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ┌─┐   ┌─┐                                               │
    │   │ │   │ │ 2-pin (yellow housing)                        │
    │   │ │   │ │ 90A continuous                                │
    │   └─┘   └─┘                                               │
    │                                                             │
    │   Current: 90A continuous, 140A burst                      │
    │   Use: 6-12S large packs 5000-20000mAh                    │
    │   Example: Large drone, e-bike, e-skateboard              │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    EC5 (High power alternative):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ┌─┐   ┌─┐                                               │
    │   │~│   │~│ 2-pin (circular)                              │
    │   │~│   │~│ 60-120A                                       │
    │   └─┘   └─┘                                               │
    │                                                             │
    │   Current: 60-120A                                        │
    │   Use: High power RC, planes, large drones                │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    Deans / T-Connector:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ┌─┐                                                      │
    │   │ └─┐   2-pin (T-shaped)                                │
    │   └─┐ │   50-60A                                          │
    │     │ │                                                   │
    │     └─┘                                                   │
    │                                                             │
    │   Current: 50-60A                                         │
    │   Use: Older RC equipment (phasing out for XT)            │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

### LiPo Connector Guide

```
SELECTING THE RIGHT CONNECTOR

    Battery Size (mAh)    Max Current (approx)    Recommended Connector
    ──────────────────────────────────────────────────────────────
    <300mAh               2-5A                    JST (2-pin)
    300-600mAh            5-10A                   JST or Micro Losi
    600-1000mAh           10-20A                  Micro Losi or XT30
    1000-2000mAh          20-40A                  XT30
    2000-3500mAh          40-60A                  XT60
    3500-5000mAh          60-80A                  XT60 or XT90
    5000-10000mAh         80-120A                 XT90 or EC5
    >10000mAh             >120A                   XT150 or custom


    MATCHING CONNECTORS:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ⚠ NEVER force incompatible connectors together!         │
    │                                                             │
    │   XT30 does NOT fit XT60                                  │
    │   Deans does NOT fit XT60                                 │
    │   EC5 is NOT compatible with XT                           │
    │   Wrong connector = poor contact = heat = fire            │
    │                                                             │
    │   Always use matching connectors (or adapters with caution)│
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

## LiPo Harness and Balance Leads

### Balance Lead Wiring

Multi-cell LiPo packs have balance leads for safe charging.

```
BALANCE LEAD CONFIGURATION

    2S (7.4V) pack balance connector:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ┌─────────────────────────────────────────────────────┐   │
    │   │  Pins:  1    2    3                                │   │
    │   │         │    │    │                                 │   │
    │   │         B-   B1   B+  (3 pins)                      │   │
    │   │                                                     │   │
    │   │   Wire colors: Black (B-), Red (B+), Yellow (mid)  │   │
    │   │                                                     │   │
    │   └─────────────────────────────────────────────────────┘   │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    3S (11.1V) pack balance connector:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ┌─────────────────────────────────────────────────────┐   │
    │   │  Pins:  1    2    3    4                          │   │
    │   │         │    │    │    │                           │   │
    │   │         B-   B1   B2   B+  (4 pins)                │   │
    │   │                                                     │   │
    │   │   Wire colors: Black (B-), Red (B+),               │   │
    │   │                 Yellow (B1), Orange (B2)           │   │
    │   │                                                     │   │
    │   └─────────────────────────────────────────────────────┘   │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    4S (14.8V) pack balance connector:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ┌─────────────────────────────────────────────────────┐   │
    │   │  Pins:  1    2    3    4    5                     │   │
    │   │         │    │    │    │    │                      │   │
    │   │         B-   B1   B2   B3   B+  (5 pins)           │   │
    │   │                                                     │   │
    │   │   Wire colors: Black (B-), Red (B+),               │   │
    │   │                 Yellow, Orange, Blue               │   │
    │   │                                                     │   │
    │   └─────────────────────────────────────────────────────┘   │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    MAIN LEADS (Power):

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ┌─────────────────────────────────────────────────────┐   │
    │   │                                                     │   │
    │   │   Black wire = Negative (-)                         │   │
    │   │   Red/Black stripe wire? = Positive (+)             │   │
    │   │                                                     │   │
    │   │   Wire gauge:                                       │   │
    │   │   ├── 2-5A: 22-24 AWG                              │   │
    │   │   ├── 10-20A: 18-20 AWG                            │   │
    │   │   ├── 30-60A: 14-16 AWG (XT60)                     │   │
    │   │   ├── 60-100A: 12 AWG (XT90)                       │   │
    │   │   └── >100A: 8-10 AWG (XT150)                      │   │
    │   │                                                     │   │
    │   └─────────────────────────────────────────────────────┘   │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    COMPLETE 3S LIPO PACK:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ┌─────────────┐                                         │
    │   │  Main lead  │  Red (+) ────► XT60 (positive)         │
    │   │  (power)    │  Black (-) ──► XT60 (negative)         │
    │   └─────────────┘                                         │
    │                                                             │
    │   ┌─────────────┐                                         │
    │   │ Balance lead│  Pin1 (B-)  ──► Black                  │
    │   │  (charging) │  Pin2 (B1)  ──► Yellow                 │
    │   │             │  Pin3 (B2)  ──► Orange                 │
    │   │             │  Pin4 (B+)  ──► Red                    │
    │   └─────────────┘                                         │
    │                                                             │
    │   B- ── Cell 1 ── B1 ── Cell 2 ── B2 ── Cell 3 ── B+     │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

## LiPo Applications

### RC / Drone / FPV

The most demanding application for LiPo batteries.

```
RC LIPO PACK GUIDE

    APPLICATION         S (cells)   Capacity    C-rating    Connector
    ──────────────────────────────────────────────────────────────
    Micro drone        1S          150-300mAh  30-50C      JST/PH2.0
    Tiny whoop         1S          300-500mAh  30-50C      JST/PH2.0
    ️ Mini drone        2S          450-800mAh  50-80C      XT30
    ️ Racing drone      3S-4S       1300-1800mAh 80-120C     XT60
    ️ Freestyle drone   4S-6S       1300-2200mAh 80-120C     XT60
    ️ RC car (1/16)    2S           800-1200mAh 50C         Deans/XT60
    ️ RC car (1/10)    2S-3S        4000-6000mAh 50-100C     XT60/Deans
    ️ RC plane         3S-4S        2200-5000mAh 30-50C      XT60/Deans
    ️ RC helicopter    6S-12S       5000-10000mAh 50-80C     XT90/EC5


    RECOMMENDED CONFIGURATIONS:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Racing drone (5-inch):                                    │
    │   ├── 4S or 6S (14.8V or 22.2V)                           │
    │   ├── 1300-1500mAh                                        │
    │   ├── 100C+ rating (high discharge)                       │
    │   ├── XT60 connector                                      │
    │   └── Weight: 150-200g                                    │
    │                                                             │
    │   Long-range drone (7-10 inch):                            │
    │   ├── 6S (22.2V)                                         │
    │   ├── 3000-6000mAh                                       │
    │   ├── 30-50C rating                                       │
    │   ├── XT60 or XT90 connector                              │
    │   └── Weight: 400-800g                                   │
    │                                                             │
    │   RC car (1/10 buggy):                                     │
    │   ├── 2S or 3S (7.4V or 11.1V)                          │
    │   ├── 5000-6000mAh                                       │
    │   ├── Soft case or hard case                              │
    │   ├── 50-100C rating                                     │
    │   └── XT60 or Deans connector                            │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

### Consumer Electronics

LiPo pouch cells in everyday devices.

```
CONSUMER DEVICE LIPO CELLS

    Device              S count    Voltage    Capacity    Typical Size
    ──────────────────────────────────────────────────────────────
    Smartwatch          1S         3.85V      200-400mAh   3x30x40mm
    Bluetooth earbuds   1S         3.7V       30-50mAh     3x10x20mm
    Smartphone          1S         3.85V      3000-5000mAh 5x50x80mm
    Tablet              1S-2S      3.85-7.7V  5000-10000mAh 6x100x150mm
    Power bank (single) 1S         3.7V       5000-20000mAh multiple
    Laptop (internal)   2S-4S      7.4-14.8V  40-99Wh      Custom shape
    E-reader            1S         3.7V       1000-2000mAh 4x60x100mm
    Fitness tracker     1S         3.7V       100-200mAh   3x20x30mm


    SPECIAL VOLTAGES (Smartphones):

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Standard Li-ion: 3.7V nominal, 4.2V full                │
    │   High voltage Li-ion: 3.85V nominal, 4.35V-4.4V full    │
    │                                                             │
    │   High-voltage cells are used in phones for:               │
    │   ├── Higher energy density (5-10% more)                  │
    │   ├── Thinner devices                                     │
    │   ├── Requires special charger (not compatible)           │
    │   └── Shorter cycle life (300-500 cycles)                 │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

## LiPo Safety and Handling

### The Dangers of LiPo

LiPo pouch cells are the most dangerous Li-ion format.

```
LIPO RISK ASSESSMENT

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   HAZARD LIKELIHOOD:                                        │
    │   (Compared to cylindrical Li-ion)                         │
    │                                                             │
    │   Puncture fire:      MUCH HIGHER (no steel case)         │
    │   Swelling:           MUCH HIGHER (age, damage)           │
    │   Thermal runaway:    HIGHER (less robust)                │
    │   Fire severity:      HIGHER (vents with flame)           │
    │   Physical damage:    MUCH HIGHER (delicate)              │
    │   Manufacturing defect: HIGHER (less automation)          │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    WHAT MAKES LIPO DANGEROUS:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   1. NO STEEL CASE                                         │
    │      ├── No mechanical protection                          │
    │      ├── Easily punctured                                  │
    │      └── No built-in CID or PTC                           │
    │                                                             │
    │   2. SWELLING                                              │
    │      ├── Normal end-of-life indication                     │
    │      ├── Gas from electrolyte decomposition                │
    │      └── Swollen cell = DANGER (stop using)               │
    │                                                             │
    │   3. PUNCTURE = IMMEDIATE FIRE                             │
    │      ├── No vent mechanism                                 │
    │      ├── Jet of flame (2-3 feet long)                     │
    │      ├── Reaches 2000°C                                   │
    │      └── Difficult to extinguish                          │
    │                                                             │
    │   4. DELICATE LEAD CONNECTIONS                             │
    │      ├── Tabs can break internally                         │
    │      ├── Broken tab = internal short                      │
    │      └── Can cause fire during charging                   │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

### Warning Signs of LiPo Failure

```
WARNING SIGNS (DANGER - STOP USING!)

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ☐ SWELLING / PUFFING                                     │
    │       Battery looks puffy, bloated, or "squishy"          │
    │       Place on flat surface – rotate – spins easily?      │
    │       → IMMEDIATE DANGER – STOP USING – DISPOSE          │
    │                                                             │
    │   ☐ UNUSUAL SMELL                                         │
    │       Sweet, solvent-like smell (electrolyte leak)        │
    │       → Immediate danger – ventilate – dispose           │
    │                                                             │
    │   ☐ EXCESSIVE HEAT                                        │
    │       Too hot to touch (>50°C) during charge/discharge    │
    │       → Stop use – monitor – may be failing              │
    │                                                             │
    │   ☐ DISCOLORATION / DAMAGE                                │
    │       Brown/black spots, wrinkled foil, dents            │
    │       → Likely damaged – dispose                         │
    │                                                             │
    │   ☐ PUNCTURE OR CUT                                       │
    │       Any breach of the foil pouch                         │
    │       → IMMEDIATE FIRE RISK – move outdoors – dispose    │
    │                                                             │
    │   ☐ RAPID SELF-DISCHARGE                                  │
    │       Loses >5% charge per day (when idle)                │
    │       → Internal short – fire risk – dispose            │
    │                                                             │
    │   ☐ BALANCE CONNECTOR ISSUES                              │
    │       Wires broken, burnt, or melted                       │
    │       → Stop using – may short – dispose                 │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    WHAT TO DO WITH WARNING SIGNS:

    1. STOP USING IMMEDIATELY
    2. Move to fire-safe location (concrete, outdoors)
    3. Place in LiPo safe bag or metal container with sand
    4. Dispose at recycling center ASAP
    5. DO NOT store indoors or near flammables
    6. DO NOT attempt to use or charge
```

### Safe Charging Practices

LiPo charging requires extra precautions.

```
LIPO CHARGING RULES

    DO:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ✓ Use LiPo-specific charger ONLY (CC/CV algorithm)       │
    │   ✓ Set correct cell count (S value)                       │
    │   ✓ Connect balance lead (multi-cell packs)                │
    │   ✓ Use LiPo safety bag or fireproof container            │
    │   ✓ Charge on non-flammable surface (concrete, ceramic)    │
    │   ✓ Monitor temperature periodically                        │
    │   ✓ Stay nearby (never leave unattended!)                  │
    │   ✓ Use 1C charge rate (or as marked)                     │
    │   ✓ Charge puffed/damaged cells – NEVER (dispose)        │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    DON'T:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ✗ Never leave charging unattended (especially LiPo)      │
    │   ✗ Never overcharge (>4.20V per cell)                     │
    │   ✗ Never charge damaged or swollen battery                │
    │   ✗ Never fast charge >1C unless rated for it              │
    │   ✗ Never charge below 0°C (32°F)                         │
    │   ✗ Never charge above 45°C (113°F)                       │
    │   ✗ Never use NiMH or lead-acid charger                    │
    │   ✗ Never charge on wood, carpet, or near flammables      │
    │   ✗ Never charge in sealed container                       │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    LIPO CHARGING STATION:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Recommended home LiPo charging setup:                    │
    │                                                             │
    │   ┌─────────────────────────────────────────────────────┐   │
    │   │  Concrete block or ceramic tile                     │   │
    │   │  ┌─────────────────────────────────────────────┐    │   │
    │   │  │                                             │    │   │
    │   │  │         LiPo Safety Bag                    │    │   │
    │   │  │         (battery inside)                   │    │   │
    │   │  │                                             │    │   │
    │   │  └─────────────────────────────────────────────┘    │   │
    │   │          │                                          │   │
    │   │          │ (wires exit bag)                         │   │
    │   │          │                                          │   │
    │   │    ┌─────┴─────┐                                   │   │
    │   │    │  Charger  │                                   │   │
    │   │    └───────────┘                                   │   │
    │   │          │                                          │   │
    │   │        Smoke detector above                         │   │
    │   │        Fire extinguisher nearby                     │   │
    │   │                                                      │   │
    │   └─────────────────────────────────────────────────────┘   │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

### LiPo Storage

```
LIPO STORAGE GUIDELINES

    STORAGE VOLTAGE (CRITICAL!):

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   LiPo MUST be stored at 3.75-3.85V (50-60% charge)        │
    │                                                             │
    │   Fully charged (4.20V) storage:                           │
    │   ├── Causes swelling (gas generation)                     │
    │   ├── Accelerates aging (capacity loss)                    │
    │   ├── Increased internal resistance                        │
    │   └── Fire risk increases                                  │
    │                                                             │
    │   Fully discharged (<3.3V) storage:                        │
    │   ├── Copper dissolution (permanent damage)                │
    │   ├── Cannot be recharged (reduced capacity)               │
    │   ├── Increased internal resistance                        │
    │   └── Risk of fire when recharging                        │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    STORAGE CONDITIONS:

    ├── Temperature: 5-25°C (41-77°F) – cool is better
    ├── Humidity: 40-60% RH (dry)
    ├── Location: LiPo safe bag or metal container
    ├── Check voltage every 3-6 months
    ├── Recharge to storage voltage if below 3.7V
    └── NEVER store swollen or damaged LiPo indoors


    STORAGE LIFE:

    Condition                Capacity Loss/year
    ──────────────────────────────────────────────────────────────
    Storage voltage, 0°C     2-4%
    Storage voltage, 25°C    10-15%
    Storage voltage, 35°C    20-30%
    Full charge, 25°C        20-30% (plus swelling!)
    Discharged, 25°C         30-50% (plus permanent damage)
```

## Common LiPo Problems

### Problem 1: Swollen / Puffed LiPo

```
SYMPTOMS:
├── Battery visibly swollen or puffed
├── Case bulging in the middle
├── Battery spins easily on flat surface (puffed)
├── Device case no longer closes properly

CAUSES:
├── Normal aging (gas from electrolyte decomposition)
├── Overcharging (>4.25V per cell)
├── Over-discharging (<2.5V per cell)
├── Excessive temperature (during use or storage)
├── Manufacturing defect
├── Physical damage (internal short)

DIAGNOSIS:
├── Place on flat surface – if it spins easily → puffed
├── Compare thickness to new battery (20%+ more)
├── Check voltage of each cell
├── Look for other damage (leaks, discoloration)

SOLUTIONS:
├── STOP USING IMMEDIATELY – swollen LiPo is DANGEROUS!
├── DO NOT CHARGE (fire risk)
├── DO NOT PUNCTURE (explosion/flame)
├── DO NOT STORE INDOORS
├── Place in LiPo safe bag or metal container with sand
├── Take to recycling center ASAP
├── Do NOT ship (dangerous goods regulations)

WARNING: Swollen LiPo can catch fire spontaneously!
Never store swollen LiPo in your home, car, or garage.
```

### Problem 2: LiPo Fire During Charging

```
IF LIPO CATCHES FIRE:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   1. DO NOT PANIC                                           │
    │      (but act quickly)                                     │
    │                                                             │
    │   2. UNPLUG CHARGER (if safe)                              │
    │                                                             │
    │   3. EVACUATE THE AREA                                     │
    │      (toxic smoke)                                         │
    │                                                             │
    │   4. CALL 911 (fire department)                            │
    │                                                             │
    │   5. IF SAFE TO APPROACH:                                  │
    │      ├── Move burning battery outdoors (with shovel)      │
    │      ├── Smother with sand or Class D extinguisher        │
    │      └── DO NOT use water (except large amounts cooling)  │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    PREVENTION (BEFORE FIRE):

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ✓ Always charge in LiPo safe bag                         │
    │   ✓ Charge on non-flammable surface                        │
    │   ✓ Never leave unattended                                 │
    │   ✓ Monitor temperature                                    │
    │   ✓ Use balance charger                                   │
    │   ✓ Set correct cell count                                 │
    │   ✓ Inspect battery before charging                        │
    │   ✓ Keep fire extinguisher nearby                          │
    │   ✓ Work in area with smoke detector                       │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

### Problem 3: Cell Imbalance (Multi-cell packs)

```
SYMPTOMS:
├── Charger takes very long to finish (balancing)
├── Voltage difference between cells >0.1V
├── Reduced runtime (one cell drains first)
├── One cell gets hot during charging

CAUSES:
├── Manufacturing variation (different capacities)
├── Aging (cells degrade at different rates)
├── Temperature differences between cells
├── Damaged cell (high internal resistance)
├── Balance lead broken or poor connection

DIAGNOSIS:
├── Check individual cell voltages (balance port)
├── Normal difference: <0.05V
├── Warning difference: 0.05-0.10V
├── Danger difference: >0.10V (replace pack)

SOLUTIONS:
├── Balance charge (charger will fix small imbalance)
├── If imbalance returns each cycle → one cell is failing
├── Replace entire pack (do not replace single cell)
├── Check balance leads for damage
├── Storage charge at 3.8V (reduces imbalance)

WARNING: Ignoring imbalance will lead to overcharging of good cells!
Overcharging = fire risk.
```

### Problem 4: Broken Tabs / Leads

```
SYMPTOMS:
├── Battery voltage 0V (tab broken inside)
├── Intermittent connection (device powers off)
├── Sparking at terminal when flexed
├── Charger error (connection break)

CAUSES:
├── Flexing of tabs (normal in drones/RC)
├── Poor soldering (cold joint)
├── Physical damage (crash, drop)
├── Corrosion (moisture ingress)
├── Overheating (melted insulation)

DIAGNOSIS:
├── Gently wiggle leads while measuring voltage
├── Check for continuity from tab to connector
├── Inspect for visible damage or cracks
├── Test with multimeter (resistance mode)

SOLUTIONS:
├── DO NOT attempt to repair broken tabs (VERY DANGEROUS!)
├── Soldering on LiPo tabs can cause fire/explosion
├── Replace battery if damaged (do not attempt repair)
├── For loose connectors: replace connector (cut one wire at a time!)
├── Use strain relief (tape, zip ties, hot glue)

WARNING: NEVER solder directly to LiPo cell tabs!
The heat can ignite the electrolyte. Use spot welding only.
```

## LiPo Disposal and Recycling

```
LIPO END-OF-LIFE DISPOSAL

    WHEN TO DISPOSE:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ☑ Swollen or puffed                                      │
    │   ☑ Not holding charge (<50% original capacity)           │
    │   ☑ High internal resistance (>2× new value)              │
    │   ☑ Physical damage (dents, cuts, punctures)              │
    │   ☑ Leaking or smell                                      │
    │   ☑ Age >3-5 years (depending on usage)                   │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    PREPARATION FOR RECYCLING:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   1. DISCHARGE to 0V (if safe)                            │
    │      ├── Use resistor (1-10Ω) across terminals            │
    │      ├── DO for swollen or damaged cells (skip – too risky)│
    │      ├── Do outdoors, away from flammables                │
    │      └── Leave overnight                                   │
    │                                                             │
    │   2. TAPE TERMINALS                                        │
    │      ├── Electrical tape over connectors                  │
    │      ├── Prevents short circuits                          │
    │      └── Do not cover labels (recycling info)             │
    │                                                             │
    │   3. PLACE IN PLASTIC BAG (separate)                      │
    │      ├── Each battery in own bag                          │
    │      ├── Prevents terminal contact                        │
    │      └── Do not store in metal container                  │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    RECYCLING LOCATIONS:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   US:                                                        │
    │   ├── Call2Recycle: (800) 822-8837                         │
    │   ├── Best Buy                                             │
    │   ├── Home Depot                                           │
    │   ├── Lowe's                                               │
    │   ├── Staples                                              │
    │   ├── Batteries Plus                                      │
    │   └── Local hazardous waste facility                       │
    │                                                             │
    │   DO NOT:                                                   │
    │   ✗ Throw in trash (fire hazard)                          │
    │   ✗ Store for extended period (especially swollen)        │
    │   ✗ Ship (dangerous goods regulations)                    │
    │   ✗ Burn or incinerate                                    │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    SWOLLEN LIPO HANDLING:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ⚠ SWOLLEN LIPO = EXTREME DANGER                         │
    │                                                             │
    │   DO NOT:                                                   │
    │   ├── Do not store indoors                                 │
    │   ├── Do not try to discharge                              │
    │   ├── Do not puncture                                      │
    │   ├── Do not charge                                        │
    │   └── Do not use                                           │
    │                                                             │
    │   DO:                                                       │
    │   ├── Place in LiPo safe bag                               │
    │   ├── Place bag in metal container with sand               │
    │   ├── Store OUTDOORS (away from buildings)                 │
    │   ├── Take to hazardous waste facility ASAP                │
    │   └── Call ahead – some accept swollen batteries          │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

## Quick Reference Table

| Parameter | 1S LiPo | 2S LiPo | 3S LiPo | 4S LiPo | 6S LiPo |
|-----------|---------|---------|---------|---------|---------|
| Nominal voltage | 3.7V | 7.4V | 11.1V | 14.8V | 22.2V |
| Full charge | 4.2V | 8.4V | 12.6V | 16.8V | 25.2V |
| Storage voltage | 3.75-3.85V | 7.5-7.7V | 11.25-11.55V | 15.0-15.4V | 22.5-23.1V |
| Discharge cutoff | 3.0-3.3V | 6.0-6.6V | 9.0-9.9V | 12.0-13.2V | 18.0-19.8V |
| Balance pins | N/A | 3 | 4 | 5 | 7 |
| Common use | Phone, Tinywhoop | Mini drone | RC car, drone | Racing drone | Large drone, e-bike |

## Summary

1. **"LiPo" usually means pouch cell** – flexible foil packaging, not necessarily polymer electrolyte

2. **Pouch cells** are lighter, thinner, and can be custom-shaped (0.5-20mm thick)

3. **More dangerous than cylindrical** – no steel case, no CID/PTC, puncture = fire

4. **Swollen LiPo = DANGER** – gas buildup from normal aging or abuse (stop using!)

5. **Storage voltage** is critical: 3.75-3.85V (50-60% charge) – never full or empty

6. **1S** (3.7V) – single cell, common in phones, watches, small drones

7. **2S-6S** – multi-cell packs for RC, drones, power tools (7.4V to 25.2V)

8. **C-rating** = max discharge rate (20C-120C for RC, 1C-2C for phones)

9. **Balance charging** mandatory for multi-cell packs (prevents overcharge)

10. **Internal resistance** increases with age – high IR = end of life

11. **Connectors:** JST (small), XT30 (medium), XT60 (standard), XT90 (large)

12. **Charge rate** 1C is safest (1 hour charge time) – never exceed battery rating

13. **Never leave LiPo charging unattended** – fire risk is real

14. **Use LiPo safety bag** for charging and storage (contains fire)

15. **Dispose swollen/damaged LiPo immediately** – hazardous waste only

*This documentation belongs to https://github.com/InterCentury*