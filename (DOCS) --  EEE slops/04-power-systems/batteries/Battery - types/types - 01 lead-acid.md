# Types - 01: Lead-Acid Battery

## What is a Lead-Acid Battery?

The lead-acid battery is the oldest type of rechargeable battery, invented in 1859 by French physicist Gaston Planté. Despite being over 160 years old, it remains one of the most widely used battery technologies today, particularly for automotive starting, uninterruptible power supplies (UPS), backup power, and renewable energy storage.

Lead-acid batteries store chemical energy in lead plates submerged in sulfuric acid electrolyte. They are valued for their low cost, high surge current capability, reliability, and ease of recycling (over 99% of lead-acid batteries are recycled in the US, making them one of the most recycled consumer products).

## Basic Chemistry and Construction

### How Lead-Acid Batteries Work

The lead-acid battery converts chemical energy to electrical energy through reactions between lead, lead dioxide, and sulfuric acid.

```
LEAD-ACID BATTERY CHEMISTRY

    DISCHARGE REACTION:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Pb (lead)  +  PbO₂ (lead dioxide)  +  2H₂SO₄ (sulfuric)   │
    │                                                             │
    │                       ↓ (discharge)                         │
    │                                                             │
    │           2PbSO₄ (lead sulfate)  +  2H₂O (water)            │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    CHARGE REACTION (reverse):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   2PbSO₄ (lead sulfate)  +  2H₂O (water)                    │
    │                                                             │
    │                       ↑ (charge)                            │
    │                                                             │
    │   Pb (lead)  +  PbO₂ (lead dioxide)  +  2H₂SO₄ (sulfuric)   │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    KEY OBSERVATIONS:

    ├── Discharge consumes sulfuric acid (electrolyte weakens)
    ├── Discharge produces water (electrolyte becomes more dilute)
    ├── Charge consumes water (electrolyte becomes stronger)
    ├── Charge produces sulfuric acid
    ├── Specific gravity of electrolyte indicates state of charge
    └── Temperature affects reaction rate (colder = slower)
```

### Physical Construction

```
LEAD-ACID BATTERY CROSS-SECTION

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ┌─────────────────────────────────────────────────────┐   │
    │   │  ┌─────────────────────────────────────────────┐    │   │
    │   │  │             Positive Terminal (+)           │    │   │
    │   │  └─────────────────────────────────────────────┘    │   │
    │   │                                                     │   │
    │   │  ┌─────────────────────────────────────────────┐    │   │
    │   │  │             Negative Terminal (-)           │    │   │
    │   │  └─────────────────────────────────────────────┘    │   │
    │   │                                                     │   │
    │   │  ████████████████████████████████████████████████   │   │
    │   │  ██            Plastic Case                    ██   │   │
    │   │  ████████████████████████████████████████████████   │   │
    │   │  ██  ┌─────┐  ┌─────┐  ┌─────┐ ┌─────┐ ┌─────┐ ██   │   │
    │   │  ██  │ +   │  │ -   │  │ +   │ │ -   │ │ +   │ ██   │   │
    │   │  ██  │ PbO₂│  │ Pb  │  │ PbO₂│ │ Pb  │ │ PbO₂│ ██   │   │
    │   │  ██  └──┬──┘  └──┬──┘  └──┬──┘ └──┬──┘ └──┬──┘ ██   │   │
    │   │  ██     │        │        │       │       │    ██   │   │
    │   │  ██     └────────┼────────┼───────┼───────┘    ██   │   │
    │   │  ██              │        │       │            ██   │   │
    │   │  ██         ┌────┴────────┴───────┴────┐       ██   │   │
    │   │  ██         │  Electrolyte             │       ██   │   │
    │   │  ██         │  (Sulfuric Acid + Water) │       ██   │   │
    │   │  ██         └──────────────────────────┘       ██   │   │
    │   │  ██              │              │              ██   │   │
    │   │  ██         ┌────┴──────────────┴────┐         ██   │   │
    │   │  ██         │    Separators (porous) │         ██   │   │
    │   │  ██         └────────────────────────┘         ██   │   │
    │   │  ██            (prevent short circuits)        ██   │   │
    │   │  ██                                            ██   │   │
    │   │  ██            Vent caps (for gases)           ██   │   │
    │   │  ██            (flooded type)                  ██   │   │
    │   │  ████████████████████████████████████████████████   │   │
    │   │                                                     │   │
    │   └─────────────────────────────────────────────────────┘   │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    COMPONENT FUNCTIONS:

    Component               Function
    ──────────────────────────────────────────────────────────────
    Positive plate (PbO₂)   Lead dioxide - accepts electrons during discharge
    Negative plate (Pb)     Sponge lead - releases electrons during discharge
    Separator               Prevents short circuit, allows ion flow
    Electrolyte (H₂SO₄)     Conductive solution, participates in reaction
    Case                    Sealed plastic container for all components
    Vent caps               Release gas during overcharge (flooded type)
    Terminals               Connect to external circuit
```

## Types of Lead-Acid Batteries

### Flooded (Wet Cell) Lead-Acid

The original design, requiring maintenance.

```
FLOODED LEAD-ACID BATTERY

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ┌─────────────────────────────────────────────────────┐   │
    │   │  ████████████████████████████████████████████████   │   │
    │   │  ██          Flooded Lead-Acid                 ██   │   │
    │   │  ██          (Wet Cell)                        ██   │   │
    │   │  ████████████████████████████████████████████████   │   │
    │   │                                                     │   │
    │   │   ┌────┐ ┌────┐ ┌────┐ ┌────┐ ┌────┐                │   │
    │   │   │    │ │    │ │    │ │    │ │    │  Vent caps     │   │
    │   │   └─┬──┘ └─┬──┘ └─┬──┘ └─┬──┘ └─┬──┘                │   │
    │   │     │      │      │      │      │                   │   │
    │   │     └──────┼──────┼──────┼──────┘                   │   │
    │   │            │      │      │                          │   │
    │   │      Liquid electrolyte (free-flowing)              │   │
    │   │      (submerges plates completely)                  │   │
    │   │                                                     │   │
    │   └─────────────────────────────────────────────────────┘   │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘

    CHARACTERISTICS:
    ├── Electrolyte is liquid and free-flowing
    ├── Must be kept upright (spill risk)
    ├── Requires periodic water addition (distilled water only!)
    ├── Vent caps release hydrogen/oxygen gas during charging
    ├── Lower cost than sealed types
    ├── Longer life if properly maintained
    ├── Can tolerate deeper discharges (with proper care)
    └── Use: Automotive starting, golf carts, forklifts, marine


    MAINTENANCE REQUIREMENTS:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ✓ Check electrolyte level monthly                         │
    │   ✓ Add distilled water only (never tap water!)             │
    │   ✓ Keep plates submerged (replace if exposed)              │
    │   ✓ Clean terminals and case                                │
    │   ✓ Equalization charge monthly (some types)                │
    │   ✓ Specific gravity check with hydrometer                  │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

### Sealed Lead-Acid (SLA / VRLA)

Maintenance-free with immobilized electrolyte.

```
SEALED LEAD-ACID (VRLA) BATTERY

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ┌─────────────────────────────────────────────────────┐   │
    │   │  ████████████████████████████████████████████████   │   │
    │   │  ██         SLA / VRLA Battery                 ██   │   │
    │   │  ██      (Sealed Lead-Acid)                    ██   │   │
    │   │  ████████████████████████████████████████████████   │   │
    │   │                                                     │   │
    │   │   ┌─────────────────────────────────────────────┐   │   │
    │   │   │                                             │   │   │
    │   │   │   No vent caps (sealed case)                │   │   │
    │   │   │                                             │   │   │
    │   │   │   Immobilized electrolyte:                  │   │   │
    │   │   │   ├── AGM: Absorbed Glass Mat               │   │   │
    │   │   │   └── Gel: Silica-thickened electrolyte     │   │   │
    │   │   │                                             │   │   │
    │   │   └─────────────────────────────────────────────┘   │   │
    │   │                                                     │   │
    │   └─────────────────────────────────────────────────────┘   │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘

    TWO TYPES:

    AGM (Absorbed Glass Mat):
    ├── Electrolyte absorbed in fiberglass mat between plates
    ├── Lower internal resistance (accepts charge faster)
    ├── Better vibration resistance
    ├── Can handle higher charge/discharge rates
    ├── More expensive than flooded
    └── Use: UPS, medical equipment, high-performance automotive

    GEL (Gelled Electrolyte):
    ├── Electrolyte mixed with silica (gel-like consistency)
    ├── Better deep-cycle capability
    ├── More tolerant of high temperatures
    ├── Slower charging (cannot accept high current)
    ├── More expensive than flooded
    └── Use: Solar storage, marine, mobility scooters


    ADVANTAGES OVER FLOODED:
    ├── Maintenance-free (no water addition)
    ├── Spill-proof (can be mounted in any orientation)
    ├── No gas venting (under normal conditions)
    ├── Longer shelf life (lower self-discharge)
    ├── More vibration resistant
    └── Cleaner (no acid spills)

    DISADVANTAGES:
    ├── More expensive
    ├── Shorter life if overcharged
    ├── Cannot equalize charge (sealed case)
    └── More sensitive to overcharging (dry-out risk)
```

### Starting, Deep Cycle, and Dual Purpose

Different designs for different applications.

```
STARTING BATTERY (SLI - Starting, Lighting, Ignition)

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   DESIGN:                                                   │
    │   ├── Many thin plates (high surface area)                  │
    │   ├── Low internal resistance                               │
    │   ├── High cranking current (CCA - Cold Cranking Amps)      │
    │   └── Shallow depth of discharge (only 2-5% used per start) │
    │                                                             │
    │   CHARACTERISTICS:                                          │
    │   ├── Delivers high current for short time (5-30 seconds)   │
    │   ├── Recharges quickly                                     │
    │   ├── Damaged by deep discharge (sulfation)                 │
    │   ├── Shorter cycle life (50-100 cycles)                    │
    │   └── Use: Car, truck, motorcycle starting                  │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    DEEP CYCLE BATTERY

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   DESIGN:                                                   │
    │   ├── Fewer, thicker plates (more active material)          │
    │   ├── Higher internal resistance                            │
    │   ├── Lower peak current, sustained output                  │
    │   └── Can be discharged to 80% repeatedly                   │
    │                                                             │
    │   CHARACTERISTICS:                                          │
    │   ├── Lower cranking current                                │
    │   ├── Longer cycle life (500-1500 cycles)                   │
    │   ├── More tolerant of deep discharge                       │
    │   ├── Slower charge time                                    │
    │   └── Use: Golf carts, solar storage, marine trolling, RVs  │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    DUAL PURPOSE / MARINE BATTERY

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   DESIGN:                                                   │
    │   ├── Compromise between starting and deep cycle            │
    │   ├── Moderate plate thickness                              │
    │   ├── Moderate CCA and moderate deep cycle capability       │
    │   └── Jack of both trades, master of neither                │
    │                                                             │
    │   CHARACTERISTICS:                                          │
    │   ├── Lower CCA than dedicated starting battery             │
    │   ├── Lower cycle life than dedicated deep cycle            │
    │   ├── Acceptable for occasional deep discharge              │
    │   └── Use: Marine (both starting and trolling), RVs         │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    COMPARISON TABLE:

    Feature                    Starting    Deep Cycle    Dual Purpose
    ─────────────────────────────────────────────────────────────────
    Plate thickness            Thin        Thick         Medium
    CCA (Cold Cranking)        High        Low           Medium
    Reserve capacity           Low         High          Medium
    Cycle life (deep)          50-100      500-1500      200-400
    Deep discharge tolerance   Poor        Excellent     Good
    Price                      Low         Higher        Medium
    Best use                   Starting    Trolling      Marine
```

## Key Specifications

### Voltage

Individual lead-acid cells produce 2.1V nominal.

```
VOLTAGE BY CELL COUNT

    Cells    Nominal V    Application
    ──────────────────────────────────────────────
    1        2V           Single cell (industrial)
    3        6V           Motorcycles, lawn tractors, kids' vehicles
    6        12V          Most common (cars, UPS, solar)
    8        16V          Some high-performance automotive
    12       24V          Trucks, buses, industrial equipment
    24       48V          Forklifts, golf carts, solar systems

    Note: Actual voltage varies with state of charge:
    ├── Fully charged (resting): 12.6-12.8V (6-cell)
    ├── 50% charged (resting): 12.2V
    ├── Discharged (resting): 11.8V
    └── Deeply discharged: <11.0V (damage risk)


    CHARGING VOLTAGES (12V battery):

    Stage               Voltage        Duration    Notes
    ──────────────────────────────────────────────────────────────
    Bulk charge         14.4-14.8V     Variable    Constant current
    Absorption          14.4-14.8V     1-4 hours   Constant voltage
    Float               13.5-13.8V     Indefinite  Maintenance
    Equalization        15.0-15.5V     1-2 hours   Flooded only

    Temperature compensation: -0.03V per cell per 10°C above 25°C
```

### Capacity (Ah)

Capacity in ampere-hours (Ah) indicates how much energy the battery stores.

```
CAPACITY RATINGS

    Ah = Amperes × Hours of discharge

    Example: 100Ah battery can deliver:
    ├── 5A for 20 hours
    ├── 10A for 10 hours
    ├── 20A for 5 hours
    └── 100A for 1 hour (theoretically – Peukert effect applies)


    PEUKERT EFFECT:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Higher current = LOWER effective capacity                 │
    │                                                             │
    │   Discharge Rate    Actual Capacity (100Ah rated)           │
    │   ──────────────────────────────────────────────────────────│
    │   C/20 (5A)         100Ah (100% of rating)                  │
    │   C/10 (10A)        95Ah                                    │
    │   C/5 (20A)         85Ah                                    │
    │   C/2 (50A)         65Ah                                    │
    │   1C (100A)         50Ah                                    │
    │   2C (200A)         30Ah                                    │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    TYPICAL CAPACITIES:

    Battery Type               Capacity Range    Common Application
    ──────────────────────────────────────────────────────────────
    Motorcycle battery         5-30 Ah           Motorcycles, ATVs
    Small car battery          40-60 Ah          Compact cars
    Standard car battery       60-80 Ah          Sedans, SUVs
    Large car/SUV battery      80-100 Ah         Large vehicles
    Truck battery              100-200 Ah        Pickup trucks
    Marine starting            100-200 Ah        Boats
    Marine deep cycle          100-250 Ah        Trolling motors
    Golf cart battery (6V)     200-250 Ah        Golf carts
    UPS battery (12V)          7-100 Ah          Backup power
    Solar storage (12V)        100-400 Ah        Off-grid
    Industrial (2V cells)      500-5000 Ah       Forklifts, substations
```

### Cold Cranking Amps (CCA)

Critical for starting batteries.

```
CCA DEFINITION

    Cold Cranking Amps (CCA):
    ├── Amps a battery can deliver for 30 seconds at -18°C (0°F)
    ├── While maintaining voltage above 7.2V (for 12V battery)
    └── Higher CCA = better cold weather starting


    TYPICAL CCA VALUES (12V car battery):

    Engine Size               CCA Required
    ──────────────────────────────────────────────
    Small (1.0-1.6L)         300-400 CCA
    Medium (1.8-2.5L)        400-600 CCA
    Large (3.0-5.0L)         600-800 CCA
    Diesel                   800-1000+ CCA
    Heavy truck              1000-1500 CCA


    OTHER RATINGS:

    CA (Cranking Amps):      Amps at 0°C (32°F) – higher number
    MCA (Marine CCA):        Similar to CCA for marine use
    HCA (Hot Cranking Amps): Amps at 27°C (80°F) – even higher
    RC (Reserve Capacity):   Minutes at 25A discharge (70-200 min)
```

### Life and Cycle Ratings

```
CYCLE LIFE

    Depth of Discharge (DoD) vs Cycles:

    Depth of Discharge    Flooded Cycles    AGM Cycles    Gel Cycles
    ──────────────────────────────────────────────────────────────
    10% (starting)        5000+             4000+         4000+
    20%                   2000+             2000+         2500+
    30%                   800+              1000+         1200+
    50%                   300-500           500-800       500-800
    80%                   100-200           300-500       400-600
    100%                  50-100            150-200       200-300


    FACTORS AFFECTING LIFE:

    Factor                Effect on Life
    ──────────────────────────────────────────────────────────────
    Temperature (25°C)    Baseline (100% life)
    Temperature (35°C)    50% life reduction
    Temperature (45°C)    75% life reduction
    Temperature (55°C)    90% life reduction
    Overcharging          Severe life reduction (grid corrosion)
    Undercharging         Sulfation (irreversible damage)
    Deep discharge        Permanent capacity loss
    High vibration        Plate damage (flooded)
```

## Lead-Acid Battery Performance

### State of Charge (SoC)

Measuring charge level by voltage and specific gravity.

```
STATE OF CHARGE TABLE (12V flooded, resting 24 hours)

    SoC (%)    Voltage (12V)    Specific Gravity    Action
    ──────────────────────────────────────────────────────────────
    100%       12.70V+          1.265-1.285        Fully charged
    90%        12.60V           1.250              Good
    80%        12.45V           1.230              Recharge soon
    70%        12.30V           1.210              Recharge
    60%        12.20V           1.190              Recharge immediately
    50%        12.10V           1.170              Danger zone
    40%        12.00V           1.150              Damage imminent
    30%        11.90V           1.130              Severe damage
    20%        11.80V           1.100              Likely damaged
    10%        11.60V           1.070              Probably ruined
    0%         11.30V-          1.000-             Dead


    NOTES:

    ├── Voltage must be measured after 24 hours rest (no charging/discharging)
    ├── Surface charge affects readings (remove with headlights for 2 minutes)
    ├── AGM/Gel voltages slightly different (typically +0.1-0.2V)
    ├── Temperature affects voltage: -0.03V per 10°C below 25°C
    └── Specific gravity measured with hydrometer (flooded only)
```

### Self-Discharge

Lead-acid batteries self-discharge even when not in use.

```
SELF-DISCHARGE RATES (at 25°C / 77°F)

    Battery Type           Monthly Self-Discharge    After 6 Months
    ──────────────────────────────────────────────────────────────
    Flooded                5-15%                    30-90%
    AGM                    2-5%                     12-30%
    Gel                    1-3%                     6-18%


    TEMPERATURE EFFECT:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Temperature    Self-Discharge Rate (flooded)              │
    │   ──────────────────────────────────────────────────────────│
    │   0°C (32°F)     2-5% per month                             │
    │   20°C (68°F)    5-8% per month                             │
    │   25°C (77°F)    5-15% per month (wide variation)           │
    │   30°C (86°F)    15-20% per month                           │
    │   40°C (104°F)   25-30% per month                           │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    STORAGE ADVICE:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ✓ Store fully charged                                     │
    │   ✓ Recharge every 3-6 months (flooded)                     │
    │   ✓ Recharge every 6-12 months (AGM/Gel)                    │
    │   ✓ Store in cool location (reduce self-discharge)          │
    │   ✓ Use float charger for long-term storage                 │
    │   X Never store discharged (sulfation damage)               │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

### Temperature Effects

```
TEMPERATURE VS PERFORMANCE

    CAPACITY VS TEMPERATURE:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Capacity (% of 25°C rating)                               │
    │        │                                                    │
    │    120 ┼                             ●                      │
    │        │                           ╱                        │
    │    110 ┼                         ╱                          │
    │        │                       ╱                            │
    │    100 ┼─────────────────────●                              │
    │        │                    ╱                               │
    │     90 ┼                  ╱                                 │
    │        │                ╱                                   │
    │     80 ┼              ╱                                     │
    │        │            ╱                                       │
    │     70 ┼          ╱                                         │
    │        │        ╱                                           │
    │     60 ┼      ●                                             │
    │        │                                                    │
    │        └────────────────────────────────────────► Temp      │
    │        -20°C  -10°C  0°C   10°C  20°C  30°C  40°C           │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘

    -20°C (-4°F):    40-50% of rated capacity (hard starting!)
    -10°C (14°F):    60-70% of rated capacity
    0°C (32°F):      80-90% of rated capacity
    25°C (77°F):     100% (baseline)
    40°C (104°F):    105-110% of rated capacity


    OPERATING LIMITS:

    Temperature           Effect
    ──────────────────────────────────────────────────────────────
    Below -20°C (-4°F)   Electrolyte may freeze (if discharged)
    -20°C to 0°C         Greatly reduced capacity, slower charging
    0°C to 25°C          Normal operation (reduced capacity below 10°C)
    25°C to 45°C         Optimum performance, but reduced life
    45°C to 60°C         Acceptable, significant life reduction
    Above 60°C           Danger (thermal runaway risk, case damage)


    FREEZING POINTS:

    State of Charge    Specific Gravity    Freezing Point
    ──────────────────────────────────────────────────────────────
    100%               1.285               -70°C (-94°F)
    75%                1.230               -35°C (-31°F)
    50%                1.190               -20°C (-4°F)
    25%                1.150               -10°C (14°F)
    0% (discharged)    1.100               -5°C (23°F)

    WARNING: A discharged battery can freeze and crack!
```

## Common Applications

### Automotive Starting

The most common application.

```
CAR STARTING BATTERY REQUIREMENTS

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Starting a typical 2.0L gasoline engine:                  │
    │                                                             │
    │   ├── Peak current: 200-400A for 1-2 seconds                │
    │   ├── Sustained current: 100-200A for 3-5 seconds           │
    │   ├── Energy used: Only 2-5% of battery capacity            │
    │   ├── Immediately recharged by alternator                   │
    │   └── Designed for many shallow cycles (10,000+)            │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    RECOMMENDED SPECS:

    Vehicle Type            CCA Minimum    Reserve Capacity
    ──────────────────────────────────────────────────────────────
    Small car (1.0-1.6L)    300-400        40-60 min
    Midsize (1.8-2.5L)      400-600        60-80 min
    Large car (3.0-5.0L)    600-800        80-100 min
    Diesel car               800-1000       100-120 min
    Light truck              600-800        80-100 min
    Heavy truck              1000-1500      120-180 min


    REPLACEMENT RULES:

    ├── Match or exceed original CCA rating
    ├── Match physical size (BCI group size)
    ├── Match terminal type (top, side, post sizes)
    └── Don't buy more CCA than needed (wastes money)
```

### UPS and Backup Power

Uninterruptible Power Supplies use sealed lead-acid batteries.

```
UPS BATTERY REQUIREMENTS

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Typical UPS (500VA / 300W):                               │
    │                                                             │
    │   ├── Battery: 1-2 x 12V 7-9Ah SLA (sealed)                 │
    │   ├── Runtime at full load: 5-15 minutes                    │
    │   ├── Runtime at half load: 15-30 minutes                   │
    │   ├── Designed to keep you running until generator starts   │
    │   └── Expect 3-5 year life (float service)                  │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    UPS BATTERY SIZING:

    Load (VA)     Approx Runtime (minutes)    Battery Ah Needed
    ──────────────────────────────────────────────────────────────
    200 VA        30                         7Ah
    400 VA        15                         7Ah
    500 VA        8-10                       9Ah
    800 VA        5-8                        12Ah
    1000 VA       4-6                        18Ah (2x9Ah)
    1500 VA       3-5                        24Ah (2x12Ah)


    IMPORTANT: UPS batteries are SPECIAL:
    ├── High power density for short duration
    ├── Designed for occasional use
    ├── Not for deep cycling (will fail early)
    └── Replace every 3-5 years (even if still working)
```

### Solar / Renewable Energy Storage

Deep cycle batteries for off-grid and backup systems.

```
SOLAR BATTERY REQUIREMENTS

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Off-grid solar system (typical cabin):                    │
    │                                                             │
    │   ├── Battery bank: Multiple deep cycle batteries           │
    │   ├── Daily cycling (discharge at night, charge by day)     │
    │   ├── Requires true deep cycle design                       │
    │   ├── Expect 5-10 year life (if properly maintained)        │
    │   └── Typically 24V or 48V systems (multiple batteries)     │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    DAILY ENERGY REQUIREMENTS:

    Daily Load (Wh)    Battery Bank (12V)    Battery Bank (24V)
    ──────────────────────────────────────────────────────────────
    500 Wh             100Ah                50Ah
    1000 Wh            200Ah                100Ah
    2000 Wh            400Ah                200Ah
    3000 Wh            600Ah                300Ah
    5000 Wh            1000Ah               500Ah

    Note: Multiply by 2-3× for cloudy day reserve!
```

### Marine and RV

Deep cycle or dual-purpose batteries for boats and recreational vehicles.

```
MARINE/RV BATTERY REQUIREMENTS

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Marine/RV applications:                                   │
    │                                                             │
    │   ├── Starting (engine) + house loads (lights, fridge)      │
    │   ├── Often use dual-purpose or separate banks              │
    │   ├── Vibration resistant construction required             │
    │   ├── Sealed (AGM) preferred for safety (no spill)          │
    │   └── Deep cycle for house bank, starting for engine        │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    TYPICAL SETUPS:

    Boat Type              Starting Battery    House Battery Bank
    ──────────────────────────────────────────────────────────────
    Small (16-20 ft)       1 x starting        1 x deep cycle
    Medium (20-25 ft)      1 x starting        2 x deep cycle (12V)
    Large (25-30 ft)       1 x starting        4 x deep cycle (24V)
    Sailboat               1 x starting        2-4 x deep cycle

    RV Type                Chassis Battery     House Battery
    ──────────────────────────────────────────────────────────────
    Camper van             1 x starting        1-2 x deep cycle
    Class B motorhome      1 x starting        2-3 x deep cycle
    Class C motorhome      1 x starting        2-4 x deep cycle
    Travel trailer         From tow vehicle    2-4 x deep cycle
```

## Maintenance and Care

### Regular Maintenance (Flooded)

```
FLOODED BATTERY MAINTENANCE SCHEDULE

    MONTHLY:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ☐ Check electrolyte level (plates must be submerged)      │
    │   ☐ Add distilled water ONLY (if low)                       │
    │   ☐ Clean top and terminals                                 │
    │   ☐ Check for corrosion (white/green powder)                │
    │   ☐ Measure specific gravity (if accessible)                │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    EVERY 3 MONTHS:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ☐ Load test (or CCA test)                                 │
    │   ☐ Equalization charge (if applicable)                     │
    │   ☐ Check hold-down clamps (tight)                          │
    │   ☐ Inspect cables (cracks, corrosion)                      │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    WATER ADDITION GUIDELINES:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   RULE: Add water AFTER charging, not before!               │
    │   (Electrolyte expands when charging, can overflow)         │
    │                                                             │
    │   Procedure:                                                │
    │   1. Charge battery fully                                   │
    │   2. Remove vent caps                                       │
    │   3. Add distilled water to fill ring (not to top)          │
    │   4. Never use tap water (minerals damage battery)          │
    │   5. Replace caps securely                                  │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    HOW OFTEN TO ADD WATER:

    Climate           Frequency
    ──────────────────────────────────────────────────────────────
    Cool (temperate)  Every 3-6 months
    Warm (subtropics) Every 1-3 months
    Hot (desert)      Monthly
    Heavy use         More often
    Light use         Less often
```

### Charging Best Practices

```
CHARGING GUIDELINES

    ALWAYS:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ✓ Use correct lead-acid charger                           │
    │   ✓ Charge in ventilated area (hydrogen gas!)               │
    │   ✓ Match charger to battery type (flooded, AGM, gel)       │
    │   ✓ Use multi-stage charger (bulk, absorption, float)       │
    │   ✓ Temperature compensate (if charger supports)            │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    NEVER:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   X Never charge frozen battery (explosion risk)            │
    │   X Never charge in sealed enclosure                        │
    │   X Never use automotive "trickle charger" (unregulated)    │
    │   X Never exceed recommended voltage (14.4-14.8V for 12V)   │
    │   X Never smoke near charging battery (hydrogen explosion)  │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    STORAGE CHARGING (Float charging):

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   For long-term storage (seasonal vehicles, UPS):           │
    │                                                             │
    │   ✓ Use "float" or "maintenance" charger                    │
    │   ✓ Maintains battery at 13.2-13.8V (12V battery)           │
    │   ✓ Prevents self-discharge and sulfation                   │
    │   ✓ Can be left connected indefinitely                      │
    │   ✓ Battery Tender® is popular brand                        │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

### Sulfation Prevention

Sulfation is the #1 cause of lead-acid battery failure.

```
SULFATION EXPLANATION

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Normal operation: PbSO₄ crystals are small and reversible │
    │                                                             │
    │   Sulfation: Large PbSO₄ crystals form (hard to reverse)    │
    │                                                             │
    │   Causes:                                                   │
    │   ├── Leaving battery discharged (>24 hours)                │
    │   ├── Chronic undercharging (short daily trips)             │
    │   ├── Low electrolyte level                                 │
    │   └── High temperature                                      │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    SULFATION PREVENTION:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ✓ Keep battery fully charged (especially flooded)         │
    │   ✓ Recharge immediately after use                          │
    │   ✓ Use float charger for storage                           │
    │   ✓ Equalize charge flooded batteries monthly               │
    │   ✓ Check specific gravity regularly                        │
    │   ✓ Avoid deep discharges (below 50% if possible)           │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    SULFATION REVERSAL (Early stages):

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   For flooded batteries only:                               │
    │                                                             │
    │   1. Equalization charge (15-15.5V for 12V battery)         │
    │   2. Monitor specific gravity (should increase)             │
    │   3. May require multiple equalization cycles               │
    │   4. Desulfator chargers (pulsed) may help                  │
    │                                                             │
    │   If specific gravity won't rise → battery is dead          │
    │   Replace (sulfation irreversible)                          │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

## Common Problems and Troubleshooting

### Problem 1: Battery Won't Hold Charge

```
SYMPTOMS:
├── Battery drains quickly under load
├── Voltage drops rapidly after charging
├── Car won't start after sitting overnight
├── Specific gravity won't rise to full

CAUSES:
├── Sulfation (chronic undercharging)
├── Internal short circuit (worn separator)
├── Shedding (active material on bottom)
├── Corroded internal connections
├── Old age (end of life)
├── Electrolyte low (flooded)

DIAGNOSIS:
├── Check voltage after full charge and 24hr rest
├── Perform load test
├── Measure specific gravity (flooded)
├── Check electrolyte level (flooded)
├── Hydrometer reading: Compare cells (Δ >0.050 indicates bad cell)

SOLUTIONS:
├── Equalization charge (flooded only)
├── Desulfator (may help early sulfation)
├── Replace battery if:
│   ├── More than 5 years old
│   ├── Specific gravity won't rise above 1.225
│   ├── Voltage <10V after full charge
│   └── Won't pass load test
```

### Problem 2: Slow Cranking / Low CCA

```
SYMPTOMS:
├── Engine cranks slowly
├── Battery seems "weak"
├── Lights dim during cranking
├── Voltage drops below 9V during cranking

CAUSES:
├── Battery undercharged
├── Battery at end of life (lost CCA)
├── Corroded connections
├── Undersized battery
├── Cold weather (normal reduction)

DIAGNOSIS:
├── Measure resting voltage (should be 12.6V+ after 24hr)
├── Load test with carbon pile tester
├── Check CCA rating vs required
├── Clean and tighten terminals
├── Test with known good battery

SOLUTIONS:
├── Fully charge battery
├── Clean terminals (baking soda + water)
├── Replace if CCA below 50% of rating
├── Use battery blanket in extreme cold
├── Upgrade to higher CCA battery if needed

LOAD TEST RESULTS:

    Test Result                     Interpretation
    ──────────────────────────────────────────────────────────────
    Holds >9.6V for 15 seconds      Good battery
    Drops to 9.0-9.5V               Marginal (replace soon)
    Drops below 9.0V                Replace battery
    Drops immediately to <5V        Internal short (dangerous)
```

### Problem 3: Corroded Terminals

```
SYMPTOMS:
├── White/green/blue powder on terminals
├── Starting problems
├── Visible corrosion on cables
├── Voltage drop across connection

CAUSES:
├── Gas venting (flooded)
├── Moisture and contamination
├── Loose connection (arcing)
├── Overcharging (excess gas)
├── Electrolyte overflow (overfilled)

DIAGNOSIS:
├── Visual inspection
├── Measure voltage drop across terminal
├── Voltage drop should be <0.2V

SOLUTIONS:
├── Disconnect cables (negative first!)
├── Clean with baking soda/water paste
├── Wire brush or terminal cleaner tool
├── Rinse with water
├── Dry thoroughly
├── Apply dielectric grease or petroleum jelly
├── Reconnect (positive first!)
├── Tighten securely (but not overtight)

PREVENTION:
├── Keep terminals clean and dry
├── Apply corrosion preventive spray
├── Use felt anti-corrosion washers
├── Check vent caps (not blocked)
└── Don't overfill electrolyte
```

### Problem 4: Battery Boiling / Excessive Gassing

```
SYMPTOMS:
├── Hissing sound during charging
├── Electrolyte bubbling vigorously
├── Water loss requiring frequent filling
├── Battery hot to touch
├── Rotten egg smell (hydrogen sulfide)

CAUSES:
├── Overcharging (voltage too high)
├── Defective voltage regulator (automotive)
├── Wrong charger (no voltage regulation)
├── Defective alternator (overvoltage)
├── Cell shorted (causes low voltage → charger overworks)

DIAGNOSIS:
├── Measure charging voltage (should be 13.8-14.8V for 12V)
├── Automotive: 14.0-14.5V at battery after start
├── At idle >15V: Regulator or alternator problem
├── Hydrometer (all cells gassing indicates overcharge)

SOLUTIONS:
├── Reduce charging voltage (adjust regulator)
├── Replace defective voltage regulator or alternator
├── Use correct charger (smart charger recommended)
├── If one cell gassing: cell shorted (replace battery)
├── If all cells gassing: reduce float voltage

SAFETY: Hydrogen gas is EXPLOSIVE!
├── Ventilate area
├── No sparks, flames, or smoking
├── Connect/disconnect charger with power off
└── Always disconnect negative terminal first
```

## End of Life and Recycling

### When to Replace

```
END-OF-LIFE INDICATORS

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ☑ Age >5 years (flooded) or >8 years (AGM/gel)            │
    │   ☑ Won't hold charge overnight                             │
    │   ☑ Specific gravity won't rise above 1.200                 │
    │   ☑ Cranks engine slowly (even after full charge)           │
    │   ☑ Visible case swelling (AGM/gel)                         │
    │   ☑ Cracked or leaking case                                 │
    │   ☑ Fails load test                                         │
    │   ☑ Voltage drops below 10V under load                      │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    RECYCLING:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Lead-acid batteries are the MOST RECYCLED product         │
    │   (99%+ recycling rate in US)                               │
    │                                                             │
    │   WHERE TO RECYCLE:                                         │
    │   ├── Auto parts stores (Advance, AutoZone, O'Reilly)       │
    │   ├── Walmart (automotive department)                       │
    │   ├── Scrap metal recyclers (pay $5-15 per battery)         │
    │   ├── Most car repair shops                                 │
    │   ├── Battery retailers (Interstate Batteries)              │
    │   └── Hazardous waste facilities                            │
    │                                                             │
    │   IMPORTANT:                                                │
    │   ├── Never throw in trash (illegal in most states)         │
    │   ├── Usually pay "core charge" until recycled              │
    │   └── New battery purchase includes environmental fee       │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

## Quick Reference Table

| Parameter | Flooded | AGM | Gel |
|-----------|---------|-----|-----|
| Maintenance | Required | None | None |
| Spill-proof | No | Yes | Yes |
| Vibration resistance | Moderate | Excellent | Good |
| Charge acceptance | Good | Excellent | Poor |
| Deep cycle capability | Good | Good | Excellent |
| Cold cranking amps | High | Very high | Low |
| Self-discharge (monthly) | 5-15% | 2-5% | 1-3% |
| Cycle life (50% DoD) | 300-500 | 500-800 | 500-800 |
| Operating temp | -20 to 50°C | -20 to 60°C | -20 to 55°C |
| Relative cost | $ | $$ | $$ |
| Best use | Starting | UPS, starting | Solar, deep cycle |

## Summary

1. **Lead-acid battery** invented 1859 – oldest rechargeable battery, still widely used

2. **Chemistry:** Pb + PbO₂ + 2H₂SO₄ ⇄ 2PbSO₄ + 2H₂O

3. **Nominal cell voltage:** 2.1V (6 cells = 12V, most common)

4. **Flooded (wet cell):** Requires maintenance (water), must be upright, least expensive

5. **AGM (Absorbed Glass Mat):** Maintenance-free, spill-proof, high CCA, best for UPS

6. **Gel (gelled electrolyte):** Maintenance-free, deep cycle, slower charging, solar storage

7. **Starting battery:** Thin plates, high CCA, short deep discharge life (50-100 cycles)

8. **Deep cycle battery:** Thick plates, lower CCA, long deep discharge life (500-1500 cycles)

9. **CCA (Cold Cranking Amps):** Amps at -18°C for 30 seconds, keeps above 7.2V

10. **State of charge:** 12.7V = 100%, 12.1V = 50%, 11.8V = discharged (damage risk)

11. **Self-discharge:** 5-15% per month (flooded), higher in heat

12. **Temperature effect:** Cold reduces capacity (50% at -20°C), heat reduces life (50% at 35°C)

13. **Sulfation is #1 cause of death:** Keep charged, recharge immediately

14. **Charging:** 14.4-14.8V bulk, 13.5-13.8V float, ventilate (hydrogen explosion risk)

15. **Water addition:** Flooded only – add AFTER charging, distilled water only

16. **Recycling:** 99% recycled – auto parts stores, scrap yards ($5-15)

*This documentation belongs to https://github.com/InterCentury*