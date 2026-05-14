# batteries - 4 charging-basics

## Charging Basics

Charging is the process of restoring energy to a rechargeable battery by forcing electrical current back into it. This reverses the chemical reactions that occurred during discharge, returning the battery to a charged state ready for future use.

Proper charging is critical for battery safety, performance, and longevity. Incorrect charging can cause reduced capacity, shortened life, overheating, leakage, fire, or explosion. This document explains the fundamental principles of charging different battery chemistries.

## Why Charging Works

### Reversing the Chemical Reaction

During discharge, chemical reactions convert active materials to reaction products. Charging reverses these reactions.

```
DISCHARGE VS CHARGE

    DISCHARGE (battery powering device):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Anode:  Zn  →  Zn²⁺ + 2e⁻  (oxidation, loses electrons)   │
    │   Cathode: MnO₂ + e⁻ → MnOOH  (reduction, gains electrons)  │
    │                                                             │
    │   Chemical energy → Electrical energy                       │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    CHARGE (charger restoring energy):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Anode:  Zn²⁺ + 2e⁻ → Zn   (reduction, gains electrons)    │
    │   Cathode: MnOOH → MnO₂ + e⁻  (oxidation, loses electrons)  │
    │                                                             │
    │   Electrical energy → Chemical energy (stored)              │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    CHARGER CONNECTION:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Charger (+) ──────► Battery (+)  (higher voltage forces   │
    │                            │        current backward)       │
    │   Charger (-) ◄────── Battery (-)                           │
    │                                                             │
    │   Charger voltage must be HIGHER than battery voltage       │
    │   for current to flow INTO the battery                      │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

### Energy Efficiency

Not all energy put into a battery during charging is recovered during discharge.

```
ROUND-TRIP EFFICIENCY

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Energy in (from charger)                                  │
    │          │                                                  │
    │          ▼                                                  │
    │   ┌─────────────────────────────────────────────────────┐   │
    │   │                                                     │   │
    │   │   LOSSES:                                           │   │
    │   │   ├── Heat (I²R losses)                             │   │
    │   │   ├── Overpotential (voltage inefficiency)          │   │
    │   │   ├── Side reactions (gas, heat)                    │   │
    │   │   └── Self-discharge during charge                  │   │
    │   │                                                     │   │
    │   └─────────────────────────────────────────────────────┘   │
    │          │                                                  │
    │          ▼                                                  │
    │   Energy out (during discharge)                             │
    │                                                             │
    │                                                             │
    │   Round-trip efficiency = Energy_out / Energy_in × 100%     │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    TYPICAL EFFICIENCIES:

    Chemistry               Efficiency        Notes
    ──────────────────────────────────────────────────────────────
    Lead-acid               80-90%            Good
    NiCd                    70-80%            Moderate
    NiMH                    65-75%            Lower
    Li-ion                  85-95%            Excellent
    LiFePO₄                 90-95%            Excellent
    LTO                     90-95%            Excellent

    Example: 100Wh into NiMH battery → only 65-75Wh available
    Example: 100Wh into Li-ion battery → 85-95Wh available
```

## Charging Stages

### The CC/CV Method (Li-ion, Lead-acid)

Most modern rechargeable batteries use Constant Current / Constant Voltage charging.

```
CC/CV CHARGING PROFILE

    
    Current (I)  Voltage (V)
       │            │
       ▼            ▼
    1.0┼━━━━━━━━━━━━┓           4.2┼━━━━━━━━━━━━━━━━━━━━━━━━━━━━━● (V) Constant
       │(I) Constant┃              │                             :
    0.8┼            ┃           4.0┼                            ╱:
       │            ┃              │                           ╱ :
    0.6┼            ┃           3.8┼                          ╱  :
       │            ┃              │                         ╱   :
    0.4┼            ┃           3.6┼                        ╱    :
       │            ┗━━━━╮         │                       ╱     : (I) Drops
    0.2┼                 ╰──●   3.4┼●                     ╱      :
       │                           │ ╲ (V) Rising        ╱       ▼
    0.0┼────────────────────●───3.2┼──●━━━━━━━━━━━━━━━━━╱━━━━━━━━━● (Term)
       └────────────────────┴──────┴─────────────────────────────┴─────> Time
    
       <───── CC PHASE ─────><───────────── CV PHASE ────────────>
    
    STAGES EXPLAINED:

    Stage 1: CC (Constant Current)
    ├── Charger supplies fixed current (e.g., 1A)
    ├── Battery voltage rises slowly
    ├── Most of capacity added here (80-90%)
    └── Ends when battery reaches target voltage

    Stage 2: CV (Constant Voltage)
    ├── Charger holds fixed voltage (e.g., 4.2V for Li-ion)
    ├── Current gradually decreases
    ├── Remaining capacity added (10-20%)
    └── Ends when current drops to termination threshold

    Stage 3: Termination
    ├── Charger stops or switches to float mode
    ├── Prevents overcharge
    └── May use timer backup
```

### The -ΔV Method (NiMH, NiCd)

Nickel-based batteries use voltage drop detection.

```
-ΔV (Negative Delta Voltage) CHARGING

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │  Voltage (V)                                                │
    │      ^                                                      │
    │      │                        Peak                          │
    │  1.5 ┼─────────────────────────●                            │
    │      │                        ╱ ╲  <-- -ΔV (Dip)            │
    │  1.4 ┼───────────────────────╱   ●                          │
    │      │                      ╱    │                          │
    │  1.3 ┼─────────────────────╱     │ Charger                  │
    │      │                    ╱      │ STOPS!                   │
    │  1.2 ┼───────────────────╱       ▼                          │
    │      │                  ╱                                   │
    │  1.1 ┼─────────────────╱                                    │
    │      │                ╱                                     │
    │  1.0 ┼───────●━━━━━━━╱                                      │
    │      │                                                      │
    │      └─────────────────────────────────────────► Time       │
    │                                                             │
    │  -ΔV (Negative Delta Voltage) Details:                      │
    │  ├── NiCd Dip: 10-30mV                                      │
    │  ├── NiMH Dip: 5-10mV                                       │
    │  └── Action: Charger detects drop and terminates            │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    WHY -ΔV WORKS:

    ├── When NiMH/NiCd are fully charged, temperature rises
    ├── Temperature rise causes voltage to drop slightly
    ├── Charger detects this drop (negative delta)
    ├── Stops charging to prevent overcharge
    └── Backup: dT/dt (temperature rise rate) detection
```

### dT/dt Method (Temperature Rise Rate)

More reliable than -ΔV for NiMH.

```
dT/dt (Temperature Rise Rate) CHARGING

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │  Temperature (°C)                                           │
    │      ^                                                      │
    │      │                                  STOPS               │
    │   50 ┼───────────────────────────────────●                  │
    │      │                                  ╱│                  │
    │   45 ┼─────────────────────────────────╱ │                  │
    │      │                                ╱  │                  │
    │   40 ┼───────────────────────────────╱   │                  │
    │      │               Steep Slope    ╱    │                  │
    │   35 ┼─────────────── (dT/dt) ─────╱     │                  │
    │      │                            ╱      │                  │
    │   30 ┼───────────────────────────●       │                  │
    │      │                          ╱        │                  │
    │   25 ┼●────────────────────────╱         ▼                  │
    │      │(Ambient)                                             │
    │      └─────────────────────────────────────────► Time       │
    │                                                             │
    │  (dT/dt) Mechanism:                                         │
    │  ├── Detection: Monitors internal temperature change        │
    │  ├── Threshold: Detects rise > 1°C per minute               │
    │  └── Safety: Prevents thermal runaway in NiCd/NiMH          │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘

    Advantages over -ΔV:
    ├── More reliable (less false termination)
    ├── Works in cold temperatures
    ├── Detects bad batteries (heat immediately)
    └── Used in high-end chargers (Opus, SkyRC, Liitokala)
```

## Charging Parameters by Chemistry

### Lithium-Ion (Li-ion)

The most critical chemistry to charge correctly.

```
Li-ion CHARGING SPECIFICATIONS

    Parameter               Value                   Notes
    ──────────────────────────────────────────────────────────────
    Nominal voltage         3.6-3.7V                Depends on chemistry
    Maximum charge voltage  4.20V ±0.05V            Most common (NMC, NCA)
    LFP charge voltage      3.65V                   LiFePO₄
    High voltage (4.35V)    4.35V                   Some smartphone batteries
    High voltage (4.40V)    4.40V                   Premium phones
    Termination current     C/10 to C/20            0.05-0.1C typical
    Maximum charge current  1C (most cells)         Some support 2-3C
    Temperature range       0-45°C                  NEVER below 0°C!
    Overcharge limit        4.25V                   Dangerous beyond
    Undercharge limit       2.5V                    Permanent damage


    RECOMMENDED CHARGE RATES:

    Use case                C-rate          Current (2000mAh cell)
    ──────────────────────────────────────────────────────────────
    Maximum cycle life      0.5C            1000mA
    Standard charging       1C              2000mA
    Fast charging           2C              4000mA (if rated)
    Ultra-fast              3C+             6000mA+ (special cells only)

    WARNING: Charging Li-ion below 0°C causes permanent damage!
    Lithium plating (dendrites) = internal short = fire risk!
```

### Nickel-Metal Hydride (NiMH)

More tolerant but requires proper termination.

```
NiMH CHARGING SPECIFICATIONS

    Parameter               Value                   Notes
    ──────────────────────────────────────────────────────────────
    Nominal voltage         1.2V                    Per cell
    Peak voltage            1.45-1.50V              During charge
    Termination method      -ΔV (5-10mV) or dT/dt   dT/dt = 1°C/min
    Backup termination      Timer (1.5× expected)   Essential
    Temperature cutoff      50°C                    Stop charging
    Maximum charge current  1C standard             0.5-1C for life
    Trickle charge rate     C/20-C/50               Not for prolonged use
    Self-discharge          High (std), Low (LSD)   LSD holds charge


    CHARGE RATE EFFECTS (2000mAh cell):

    Rate        Current    Time        Life impact
    ──────────────────────────────────────────────────────────────
    0.1C        200mA      14-16 hours  Best (no termination needed)
    0.3C        600mA      4-5 hours    Good (requires timer)
    0.5C        1000mA     2.5 hours    Good (requires -ΔV)
    1C          2000mA     1.2 hours    Acceptable (requires dT/dt)
    2C          4000mA     36 minutes   Reduced life, high heat

    NOTE: Never trickle charge at >C/20 (causes damage)
```

### Lead-Acid

The most forgiving but still requires proper voltage limits.

```
LEAD-ACID CHARGING SPECIFICATIONS (12V battery)

    Stage                   Voltage         Current         Duration
    ──────────────────────────────────────────────────────────────
    Bulk (CC)               10-14.4V       0.1-0.3C        Until 14.4V
    Absorption (CV)         14.4-14.8V     Drops to C/20   1-4 hours
    Float (maintenance)     13.5-13.8V     Very low        Indefinite
    Equalization (flooded)  15.0-15.5V     C/20            1-2 hours


    TEMPERATURE COMPENSATION:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Temperature compensation: -0.03V per cell per 10°C        │
    │                                                             │
    │   For 12V battery (6 cells):                                │
    │   25°C:  14.4V (baseline)                                   │
    │   35°C:  14.4V - 0.18V = 14.22V                             │
    │   45°C:  14.4V - 0.36V = 14.04V                             │
    │    5°C:  14.4V + 0.54V = 14.94V (cold needs higher V)       │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    WARNING: Lead-acid produces HYDROGEN GAS during charging!
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   !!! VENTILATION REQUIRED!                                 │
    │                                                             │
    │   Hydrogen is EXPLOSIVE (4-75% concentration in air)        │
    │   NO sparks, flames, or smoking near charging battery       │
    │   Charge in well-ventilated area (garage with door open)    │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

## Charging Methods

### Slow Charging (Overnight)

The safest method, uses simple timer.

```
SLOW CHARGING (C/10 rate)

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Rate: 0.1C (10-hour rate)                                 │
    │   Time: 14-16 hours                                         │
    │   Termination: Timer only (no voltage detection needed)     │
    │   Safety: Very safe                                         │
    │   Use: Overnight chargers, simple circuits                  │
    │                                                             │
    │   Example: 2000mAh NiMH                                     │
    │   Charge at 200mA for 14-16 hours                           │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘

    Advantages:
    ├── No complex termination circuit needed
    ├── Safe even if left longer (within reason)
    ├── Gentle on batteries (longest life)
    ├── Works for all chemistries (with correct voltage)
    └── Simple timer (mechanical or electronic)

    Disadvantages:
    ├── Very slow (overnight only)
    ├── Not for Li-ion (needs CV stage)
    └── Must set correct timer manually
```

### Fast Charging (1-3 hours)

Requires smart termination.

```
FAST CHARGING (0.3C to 1C)

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Rate: 0.3C to 1C                                          │
    │   Time: 1-3 hours                                           │
    │   Termination: -ΔV, dT/dt, or voltage (CV stage)            │
    │   Safety: Good (requires smart charger)                     │
    │   Use: Smart chargers                                       │
    │                                                             │
    │   Example: 2000mAh NiMH                                     │
    │   Charge at 1000mA (0.5C) for 2.5 hours                     │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘

    Requirements:
    ├── Charger must detect full charge automatically
    ├── Temperature monitoring recommended
    ├── Timer backup essential
    └── Individual cell monitoring for multi-cell packs
```

### Rapid Charging (15-60 minutes)

For compatible batteries only.

```
RAPID CHARGING (1C to 3C+)

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Rate: 1C to 3C (or higher for special cells)              │
    │   Time: 15-60 minutes                                       │
    │   Termination: Sophisticated detection (dT/dt + -ΔV + timer)│
    │   Safety: Requires careful monitoring                       │
    │   Use: High-end chargers, RC/aviation                       │
    │                                                             │
    │   Example: 2000mAh Li-ion                                   │
    │   Charge at 4000mA (2C) for 30 minutes (if rated)           │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘

    WARNING:
    ├── Only use with batteries rated for fast charge
    ├── Never charge unattended
    ├── Use LiPo safety bag
    ├── Monitor temperature closely (stop if >45°C)
    └── Rapid charging reduces cycle life
```

## Charge Termination Methods

### How Chargers Know When to Stop

```
TERMINATION METHODS BY CHEMISTRY

    Li-ion / LiFePO₄:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Method: CC/CV with current threshold                      │
    │   Termination: Current drops to C/10 or C/20                │
    │   Example: 2000mAh cell, 1C charge (2000mA)                 │
    │            Stop when current <200mA (C/10)                  │
    │   Backup: Timer (3 hours maximum)                           │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    NiMH / NiCd:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Primary: -ΔV (voltage drop)                               │
    │   NiCd: 10-30mV per cell drop                               │
    │   NiMH: 5-10mV per cell drop                                │
    │                                                             │
    │   Backup 1: dT/dt (temperature rise >1°C/min)               │
    │   Backup 2: Absolute temperature (>50°C)                    │
    │   Backup 3: Timer (1.5× expected time)                      │
    │   Backup 4: Maximum voltage (1.6V per cell)                 │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    Lead-Acid:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Primary: Voltage reaches absorption setpoint              │
    │   Secondary: Current drops to C/20 (enter float)            │
    │   Float: Maintain 13.5-13.8V indefinitely                   │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

## Charger Types

### Basic (Dumb) Charger

Simple, unregulated chargers.

```
BASIC CHARGER

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Features:                                                 │
    │   ├── Fixed voltage (e.g., 12V for car battery)           │
    │   ├── Fixed current (e.g., 500mA)                         │
    │   ├── No charge termination                               │
    │   ├── No monitoring                                       │
    │   └── User must time charging manually                     │
    │                                                             │
    │   Uses:                                                    │
    │   ├── Overnight NiMH chargers (wall warts)                │
    │   ├── Simple lead-acid chargers (timer)                   │
    │   └── NOT for Li-ion (dangerous!)                        │
    │                                                             │
    │   Risk: Overcharge if left too long                       │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

### Smart Charger

Microprocessor-controlled, safe for most batteries.

```
SMART CHARGER

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Features:                                                 │
    │   ├── Microprocessor control                               │
    │   ├── Automatic charge termination                         │
    │   ├── Multiple chemistries (NiMH/Li-ion/Lead-acid)         │
    │   ├── Individual cell monitoring (balance)                │
    │   ├── Temperature monitoring (thermistor)                 │
    │   ├── LCD display (voltage, current, capacity)            │
    │   ├── Refresh / recondition mode                          │
    │   ├── Automatic trickle / storage charge                  │
    │   └── Safety timers                                       │
    │                                                             │
    │   Examples:                                                 │
    │   ├── Opus BT-C3100 (AA/AAA NiMH/Li-ion)                  │
    │   ├── SkyRC MC3000 (professional)                         │
    │   ├── Nitecore D4 (consumer)                             │
    │   └── Liitokala Lii-500 (budget)                          │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    SMART CHARGER MODES:

    Mode                    Function
    ──────────────────────────────────────────────────────────────
    Charge                  Normal charging (CC/CV or -ΔV)
    Discharge               Battery capacity test
    Refresh                 Charge/discharge cycles (removes memory)
    Test                    Capacity measurement
    Storage                 Charge/discharge to storage voltage (3.7-3.8V for Li-ion)
    Balance                 Equalize cells in multi-cell packs (Li-ion)
```

### Balance Charger (Li-ion Multi-cell)

Essential for multi-cell Li-ion packs.

```
BALANCE CHARGER

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Multi-cell Li-ion pack (3S):                             │
    │                                                             │
    │   ┌─────────────────────────────────────────────────────┐   │
    │   │  Balance Charger                                    │   │
    │   │  ┌─────────────────────────────────────────────┐    │   │
    │   │  │  + ──────────────────► Cell 1 (+)           │    │   │
    │   │  │  B1 ──────────────────► Cell 1 (-) / Cell 2 (+)│    │   │
    │   │  │  B2 ──────────────────► Cell 2 (-) / Cell 3 (+)│    │   │
    │   │  │  - ──────────────────► Cell 3 (-)           │    │   │
    │   │  └─────────────────────────────────────────────┘    │   │
    │   └─────────────────────────────────────────────────────┘   │
    │                                                             │
    │   Balance lead: pin count = cells + 1                       │
    │   3S pack = 4 pins                                         │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘

    Why balancing is necessary:
    ├── Without BMS/balance charger, cells become imbalanced
    ├── One cell overcharges while others are still charging
    ├── Overcharge = fire/explosion risk!
    └── Balance charger monitors individual cell voltages
```

## Charging Safety

### Do's and Don'ts

```
CHARGING SAFETY RULES

    DO:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ✓ Use correct charger for battery chemistry              │
    │   ✓ Charge on non-flammable surface (concrete, ceramic)    │
    │   ✓ Stay nearby (especially Li-ion/LiPo)                   │
    │   ✓ Monitor temperature                                    │
    │   ✓ Disconnect when fully charged                          │
    │   ✓ Use LiPo safety bag for pouch cells                    │
    │   ✓ Ventilate area (lead-acid hydrogen gas)                │
    │   ✓ Check battery for damage before charging               │
    │   ✓ Use charger with automatic termination                 │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    DON'T:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ✗ Never leave charging unattended (especially Li-ion)    │
    │   ✗ Never use damaged or swollen battery                   │
    │   ✗ Never overcharge >4.25V per cell (Li-ion)             │
    │   ✗ Never charge Li-ion below 0°C (32°F)                  │
    │   ✗ Never charge on flammable surface (wood, carpet)       │
    │   ✗ Never mix old/new batteries in same charger            │
    │   ✗ Never use NiCd/NiMH charger on Li-ion                  │
    │   ✗ Never reverse polarity (charger to battery)            │
    │   ✗ Never block charger ventilation                        │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

### What to Watch For

```
WARNING SIGNS DURING CHARGING

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   UNPLUG IMMEDIATELY if you observe:                        │
    │                                                             │
    │   ☐ Battery too hot (>50°C / 122°F)                        │
    │   ☐ Swelling or puffing (Li-ion/LiPo)                      │
    │   ☐ Hissing or clicking sounds                             │
    │   ☐ Smoke or unusual smell (sweet, rotten eggs)            │
    │   ☐ Charger won't stop (endless charging)                  │
    │   ☐ Battery case cracking or deforming                     │
    │   ☐ Sparking or arcing                                     │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    ACTION:

    1. UNPLUG charger immediately (if safe)
    2. Move battery to fire-safe location
    3. Monitor for thermal runaway (Li-ion)
    4. Dispose of damaged battery (hazardous waste)
    5. Never use that battery again
```

## Charging Troubleshooting

### Battery Won't Charge

```
PROBLEM: Charger doesn't start, battery voltage 0V or very low

    POSSIBLE CAUSES:
    ├── Battery over-discharged (<2.5V for Li-ion)
    ├── Battery has internal short (0V)
    ├── BMS tripped (Li-ion protection circuit)
    ├── Charger not compatible
    ├── Dirty or corroded contacts
    └── Battery at end of life

    SOLUTIONS:
    ├── For Li-ion <2.5V: Attempt recovery (with caution)
    │   └── Charge at C/20 until voltage >3.0V (then normal)
    ├── For 0V battery: Replace (internal short, dangerous)
    ├── For BMS trip: Some chargers can reset (leave 10 minutes)
    ├── Clean contacts with isopropyl alcohol
    └── Replace old battery

    WARNING: Severely over-discharged Li-ion can catch fire!
    Only attempt recovery if you understand the risks.
```

### Charger Never Stops

```
PROBLEM: Charger continues charging past normal time

    POSSIBLE CAUSES:
    ├── Wrong charger for chemistry
    ├── Bad battery (won't reach termination voltage)
    ├── Defective charger (termination circuit failed)
    ├── Temperature too low (NiMH -ΔV not detected)
    └── High internal resistance (voltage never rises)

    SOLUTIONS:
    ├── Check battery temperature (if hot, unplug!)
    ├── Use correct charger for battery type
    ├── Replace old battery (won't reach full voltage)
    ├── Replace defective charger
    ├── For NiMH in cold: warm battery to 20°C
    └── Set manual timer (emergency backup)
```

### Battery Gets Very Hot

```
PROBLEM: Battery too hot to touch (>50°C)

    CAUSES:
    ├── Overcharging (charger didn't stop)
    ├── Too high charge rate (>1C for standard cells)
    ├── Internal short (self-heating)
    ├── Poor connection (high resistance)
    └── Battery old or damaged

    ACTION:
    ├── UNPLUG IMMEDIATELY
    ├── Move to fire-safe location
    ├── Allow to cool (do not use until cold)
    ├── Check for swelling (Li-ion)
    ├── If swollen: Dispose (dangerous)
    └── Reduce charge rate for future charges

    NORMAL temperatures:
    ├── Warm (30-40°C): Acceptable
    ├── Hot (40-50°C): Reduce rate
    ├── Very hot (>50°C): STOP
    └── Burning hot (>60°C): DANGER (thermal runaway risk)
```

## Quick Reference Table

| Parameter | Li-ion | NiMH | Lead-Acid (12V) |
|-----------|--------|------|-----------------|
| Nominal voltage | 3.7V | 1.2V | 12.0V |
| Max charge voltage | 4.20V | N/A | 14.4-14.8V |
| Charge method | CC/CV | -ΔV or dT/dt | CC/CV + float |
| Max charge current | 1C (standard) | 1C | 0.3C |
| Termination | C/10 | Voltage drop | Current <C/20 |
| Float voltage | N/A | N/A | 13.5-13.8V |
| Temp range | 0-45°C | 0-45°C | -20-50°C |
| Needs balancing | Yes (multi-cell) | No | No |
| Gas venting | No | No | YES (H₂) |

## Summary

1. **Charging** reverses chemical reactions to restore battery energy

2. **Round-trip efficiency** is energy out / energy in (Li-ion 85-95%, NiMH 65-75%)

3. **Li-ion charging** requires CC/CV method: 1C constant current to 4.2V, then constant voltage until C/10

4. **NiMH charging** uses -ΔV detection (5-10mV drop) or dT/dt (>1°C/min)

5. **Lead-acid charging** has three stages: bulk (CC), absorption (CV), float (maintenance)

6. **Never charge Li-ion below 0°C** – causes lithium plating (permanent damage, fire risk)

7. **Proper termination** is critical to prevent overcharge (fire/explosion)

8. **Slow charging** (C/10) is safest, requires only timer

9. **Fast charging** (1C) requires smart charger with multiple termination backups

10. **Balance charger** mandatory for multi-cell Li-ion packs (prevents overcharge)

11. **Lead-acid produces hydrogen gas** – MUST ventilate (explosion risk!)

12. **Do not trickle charge NiMH** at >C/20 (causes damage)

13. **Smart chargers** have automatic termination, multiple chemistries, LCD displays

14. **Signs of trouble:** excessive heat, swelling, hissing, smoke – unplug immediately!

15. **Never leave charging unattended** (especially Li-ion/LiPo)

16. **Use correct charger** – NiMH charger on Li-ion = fire risk

*This documentation belongs to https://github.com/InterCentury*