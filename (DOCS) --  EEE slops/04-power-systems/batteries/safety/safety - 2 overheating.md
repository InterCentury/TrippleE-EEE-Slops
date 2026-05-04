# 04.19 - Overheating

## What is Overheating?

Overheating occurs when a battery or electrical device operates at temperatures above its designed maximum safe range. Excessive heat accelerates chemical reactions, degrades materials, increases internal resistance, and can lead to thermal runaway, fire, or explosion.

While all batteries generate some heat during normal operation (charging and discharging), overheating represents a dangerous deviation from normal thermal behavior. Understanding the causes, signs, and prevention of overheating is critical for battery safety.

## The Nature of Battery Heat

### Normal Heat Generation

All batteries produce heat during operation due to internal resistance.

```
NORMAL HEAT SOURCES

    HEAT DURING DISCHARGE:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   P_heat = I² × R_internal                                  │
    │                                                             │
    │   Where:                                                    │
    │   P_heat = heat generated (watts)                           │
    │   I = discharge current (amps)                              │
    │   R_internal = internal resistance (ohms)                   │
    │                                                             │
    │   Example: 10A discharge, 0.05Ω internal resistance         │
    │   P_heat = 100 × 0.05 = 5W (noticeable heat)                │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    NORMAL OPERATING TEMPERATURES:

    Condition               Temperature      Touch Sensation
    ──────────────────────────────────────────────────────────────
    Idle (room temp)        20-25°C (68-77°F)  Cool to touch
    Light discharge         25-30°C (77-86°F)  Slightly warm
    Normal discharge        30-40°C (86-104°F) Warm (normal)
    Heavy discharge         40-50°C (104-122°F) Hot but holdable
    Fast charging           35-45°C (95-113°F) Hot (normal for fast charge)


    ACCEPTABLE VS DANGEROUS:

    Temperature              Status
    ──────────────────────────────────────────────────────────────
    <40°C (104°F)           Normal / Safe
    40-50°C (104-122°F)     Warm - acceptable (monitor)
    50-60°C (122-140°F)     Hot - CAUTION (reduce load/charge rate)
    60-80°C (140-176°F)     Very hot - DANGER (stop use!)
    >80°C (176°F)           Critical - thermal runaway risk!
```

### Heat Generation by Chemistry

Different battery chemistries have different thermal characteristics.

```
HEAT GENERATION COMPARISON

    LITHIUM-ION:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Internal resistance: 0.02-0.10Ω (new)                    │
    │   Heat sensitivity: HIGH                                   │
    │                                                             │
    │   Normal operating range: -20°C to 60°C                   │
    │   Charging range: 0°C to 45°C                             │
    │   Thermal runaway threshold: ~80°C (176°F)                │
    │                                                             │
    │   Heat accelerates degradation exponentially               │
    │   10°C above 25°C = 2× degradation rate                   │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    LEAD-ACID:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Internal resistance: 0.005-0.050Ω (varies greatly)       │
    │   Heat sensitivity: MODERATE                               │
    │                                                             │
    │   Normal operating range: -40°C to 50°C                   │
    │   Charging range: -20°C to 50°C                           │
    │   Thermal runaway threshold: ~60°C (140°F)                │
    │                                                             │
    │   Heat causes: Water loss, grid corrosion, plate damage   │
    │   Every 10°C above 25°C halves battery life!              │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    NICKEL-BASED (NiMH, NiCd):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Internal resistance: 0.01-0.08Ω                          │
    │   Heat sensitivity: MODERATE                               │
    │                                                             │
    │   Normal operating range: -20°C to 50°C                   │
    │   Charging range: 0°C to 45°C                             │
    │   Thermal runaway threshold: ~70°C (158°F)                │
    │                                                             │
    │   NiMH: Heat causes crystal formation (memory effect-like)│
    │   NiCd: Heat causes separator damage (shorts)              │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

## Causes of Overheating

### Excessive Discharge Current

Drawing more current than the battery is designed for.

```
HIGH CURRENT OVERHEATING

    Battery rating: 2Ah, 10A max continuous
    Actual load: 20A (2× rating)

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Heat generated = I² × R_internal                         │
    │                                                             │
    │   Normal (10A):    100 × 0.05 = 5W   (warm)               │
    │   Overload (20A):  400 × 0.05 = 20W  (HOT! - 4× heat!)     │
    │                                                             │
    │   Result:                                                 │
    │   ├── Rapid temperature rise                               │
    │   ├── Voltage sag (device may reset)                       │
    │   ├── Internal damage (reduced life)                       │
    │   └── Thermal runaway (if severe)                         │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    CONSEQUENCES OF EXCESSIVE CURRENT:

    Current vs Rating    Heat (relative)    Risk Level
    ──────────────────────────────────────────────────────────────
    0.5× rating          0.25×              Very safe
    1.0× rating          1.0×               Safe (rated)
    1.5× rating          2.25×              Caution
    2.0× rating          4.0×               Overheating risk
    3.0× rating          9.0×               High risk - stop!
```

### Fast Charging Overheating

Charging too quickly generates excessive heat.

```
FAST CHARGING HEAT

    Charge Rate (C)    Typical Temp Rise    Safety
    ──────────────────────────────────────────────────────────────
    0.5C (slow)        5-10°C               Very safe
    1.0C (standard)    10-15°C              Safe
    2.0C (fast)        15-25°C              Caution (needs cooling)
    3.0C (very fast)   25-40°C              High risk
    4.0C+ (ultra-fast) 40-60°C+             Dangerous (thermal runaway risk)


    HEAT GENERATION DURING CHARGING:

    P_heat = I_charge² × R_internal + (V_charge - V_cell) × I_charge

    First term: I²R loss (resistive heating)
    Second term: Overpotential heating (inefficiency)


    Li-ion example (2Ah battery, 0.05Ω internal resistance):

    1C (2A) charge:
    I²R = 4 × 0.05 = 0.2W + overpotential ≈ 1W total
    Temp rise: ~10°C above ambient

    3C (6A) charge:
    I²R = 36 × 0.05 = 1.8W + overpotential ≈ 5W total
    Temp rise: ~30°C above ambient (45°C on 25°C day - HOT!)
```

### External Heat Sources

Environmental heat can push batteries into dangerous territory.

```
EXTERNAL HEAT SOURCES

    COMMON CULPRITS:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ├── Direct sunlight (car dashboard: 70-90°C / 158-194°F)│
    │   ├── Near engines or motors                               │
    │   ├── Poorly ventilated enclosures                         │
    │   ├── Adjacent hot components (voltage regulators, CPUs)   │
    │   ├── Heaters or radiators                                 │
    │   └── Other hot batteries                                  │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    DANGEROUS ENVIRONMENTS:

    Location                Typical Temp     Risk to Li-ion
    ──────────────────────────────────────────────────────────────
    Car cabin (shade)       40-50°C          Degradation (60% life)
    Car dashboard (sun)     70-90°C          SEVERE DAMAGE
    Attic (summer)          50-60°C          Damage
    Near CPU/GPU            50-70°C          Damage (don't put near!)
    Inside black box (sun)  60-80°C          DANGER - fire risk

    RULE: If it's too hot for YOU, it's too hot for your battery!
```

### Internal Short Circuit

A partial short inside the battery generates continuous heat.

```
INTERNAL SHORT CIRCUIT HEATING

    Normal cell:          Internally shorted cell:
    
    ┌─────────────┐       ┌─────────────┐
    │  +  ███ -   │       │  +  ███ -   │
    │     │       │       │     │       │
    │     │       │       │   ┌─┴─┐     │
    │   Normal    │       │   │ █ │     │ (dendrite/short)
    │   current   │       │   └─┬─┘     │
    │     │       │       │     │       │
    │     ▼       │       │   High heat │
    └─────────────┘       └─────────────┘


    Internal short causes:
    ├── Continuous self-discharge (battery drains itself)
    ├── Constant heat generation (even when not in use)
    ├── Battery stays warm/hot at idle
    ├── Rapid capacity loss
    └── EVENTUAL THERMAL RUNAWAY

    WARNING: Battery that is warm when disconnected is DANGEROUS!
    Internal short is imminent failure - dispose safely!
```

### Poor Ventilation

Batteries need airflow to dissipate heat.

```
VENTILATION EFFECTS

    Enclosed space (no airflow):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Battery generates 5W of heat                             │
    │   No airflow → heat accumulates                            │
    │   25°C → 35°C → 45°C → 55°C (runaway!)                    │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    Vented space (with airflow):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Same 5W of heat                                          │
    │   Airflow removes heat                                     │
    │   25°C → 28°C → stabilizes (safe)                          │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    VENTILATION REQUIREMENTS:

    Application                 Ventilation Needed
    ──────────────────────────────────────────────────────────────
    Low power (<0.5W heat)      Minimal
    Medium power (0.5-5W heat)  Some airflow (holes)
    High power (5-20W heat)     Active cooling (fan)
    Very high (>20W heat)       Forced air + heatsink
```

## Signs of Overheating

### Physical Indicators

```
VISUAL AND TACTILE WARNINGS

    TOUCH TEST (Carefully!):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Temperature          Sensation          Action           │
    │   ──────────────────────────────────────────────────────────│
    │   20-30°C (68-86°F)    Cool/warm         Normal           │
    │   30-40°C (86-104°F)   Warm              Normal (monitor)  │
    │   40-50°C (104-122°F)  Hot (holdable)    Caution           │
    │   50-60°C (122-140°F)  Very hot (can't    REDUCE LOAD      │
    │                        hold >10 sec)                        │
    │   60-80°C (140-176°F)  Burning hot        STOP USE!        │
    │   >80°C (>176°F)       Painful            DANGER! Evacuate │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    VISUAL INDICATORS:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Normal battery:          Overheated battery:             │
    │   ┌─────────────┐          ┌─────────────────┐              │
    │   │  ████████   │          │  ████████████   │              │
    │   │  ██    ██   │          │  ██   ░░   ██   │  (discolored)│
    │   │  ██    ██   │          │  ██   ░░   ██   │              │
    │   │  ████████   │          │  ████████████   │              │
    │   └─────────────┘          └─────────────────┘              │
    │                                                             │
    │   Flat, clean              Bulging, discolored,            │
    │   No odor                  melted wrapper                   │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘

    Other visual signs:
    ├── Melted or softened plastic case
    ├── Discolored wrapper (brown, yellow, black)
    ├── Cracking or splitting of case
    ├── Leaking electrolyte (white crust or liquid)
    ├── Bulging or swelling (especially Li-ion)
    └── Burnt or melted wires/connectors
```

### Behavioral Indicators

How the device behaves when battery overheats.

```
DEVICE BEHAVIOR WARNINGS

    PERFORMANCE ISSUES:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ├── Device runs slower (throttling due to heat)          │
    │   ├── Screen dims (thermal protection)                     │
    │   ├── Unexpected shutdowns (battery protection)            │
    │   ├── Reduced runtime (increased internal resistance)      │
    │   ├── Charging takes longer (reduced charge acceptance)    │
    │   └── "Battery too hot" warning message (smart devices)    │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    SMELL INDICATORS:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Smell                     Indication                     │
    │   ──────────────────────────────────────────────────────────│
    │   Sweet, solvent-like       Li-ion electrolyte leak        │
    │   Rotten eggs               Lead-acid (hydrogen sulfide)   │
    │   Ammonia-like              NiMH electrolyte               │
    │   Burnt plastic             Severe overheating            │
    │   Acrid smoke               Thermal runaway (FIRE!)        │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    CHARGING BEHAVIOR:

    ├── Charger never indicates "full" (battery won't accept charge)
    ├── Battery gets hot during charging (normal: warm, not hot)
    ├── Charger shuts off prematurely (thermal protection)
    ├── Charging current much lower than normal
    └── Battery voltage rises very quickly (high resistance)
```

### Measurement Indicators

Quantitative measurements of overheating.

```
TEMPERATURE MEASUREMENT

    SAFE MEASUREMENT METHODS:

    ├── Infrared thermometer (point at battery surface)
    ├── Thermal camera (shows hot spots)
    ├── Thermocouple attached to battery surface
    ├── Battery management system (BMS) temperature sensor
    └── (Do NOT touch battery directly if very hot!)


    TEMPERATURE LIMITS BY CHEMISTRY:

    Chemistry    Max Operating   Max Charging   Max Storage
    ──────────────────────────────────────────────────────────────
    Li-ion       60°C (140°F)     45°C (113°F)   35°C (95°F)
    LiFePO₄      65°C (149°F)     55°C (131°F)   45°C (113°F)
    Lead-acid    50°C (122°F)     50°C (122°F)   30°C (86°F)
    NiMH         50°C (122°F)     45°C (113°F)   35°C (95°F)
    NiCd         50°C (122°F)     45°C (113°F)   30°C (86°F)


    CRITICAL TEMPERATURE WARNING:

    If temperature is above limits:
    ├── STOP using immediately
    ├── Move to fire-safe location
    ├── Monitor for thermal runaway
    └── Dispose if temperature doesn't return to normal
```

## Effects of Overheating

### Immediate Effects

What happens when a battery overheats right now.

```
IMMEDIATE CONSEQUENCES

    INTERNAL RESISTANCE INCREASE:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Heat → R_internal ↑ → More heat → R_internal ↑↑          │
    │                                                             │
    │   This is a POSITIVE FEEDBACK LOOP                         │
    │   (starts thermal runaway if not stopped)                  │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    VOLTAGE DEPRESSION:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Under load:   Normal: 3.7V → Hot: 3.2V (same current)   │
    │                                                             │
    │   Device may reset or shut down                            │
    │   (brownout from voltage sag)                               │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    GAS GENERATION:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Heat accelerates electrolyte decomposition                │
    │   Gases produced: CO₂, CO, hydrocarbons (flammable!)       │
    │   Pressure builds → case swells → vent → FIRE              │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    SEPARATOR DAMAGE:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Plastic separator shrinks/melts at high temperature      │
    │   Anode and cathode touch → internal short                 │
    │   Short → instantaneous high current → FIRE                │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

### Long-term Effects

Permanent damage from repeated or extended overheating.

```
PERMANENT DAMAGE

    CAPACITY LOSS (Li-ion):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Capacity vs Cycles at different temperatures:            │
    │                                                             │
    │   Capacity (%)                                             │
    │        │                                                  │
    │    100 ┼●═══════════════════════════════════════════════   │
    │        │║         ╱╱                                     │
    │     80 ┼║       ╱╱   25°C (77°F)                         │
    │        │║     ╱╱                                         │
    │     60 ┼║   ╱╱                                            │
    │        │║ ╱╱    45°C (113°F)                             │
    │     40 ┼╬╱                                                │
    │        │╱                                                  │
    │     20 ┼                                                   │
    │        │                                                   │
    │      0 ┼─────────────────────────────────────────► Cycles │
    │        0   200  400  600  800  1000  1200                 │
    │                                                             │
    │   45°C operation reduces life by 50%!                     │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    LEAD-ACID LIFE vs TEMPERATURE:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Life (years)                                             │
    │        │                                                  │
    │     10 ┼●────────────────────────────                       │
    │        │ ╲                                                │
    │      8 ┼  ╲                                               │
    │        │   ╲                                              │
    │      6 ┼    ╲                                             │
    │        │     ╲                                            │
    │      4 ┼      ╲                                           │
    │        │       ╲                                          │
    │      2 ┼        ╳                                         │
    │        │         ╲                                        │
    │      0 ┼──────────●─────────────────────────────► Temp    │
    │       25°C   35°C   45°C   55°C   65°C                    │
    │                                                             │
    │   Every 10°C above 25°C = 50% life reduction!              │
    │   55°C operation = 75% life loss (2 years → 6 months)      │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    OTHER PERMANENT DAMAGE:

    ├── Increased internal resistance (slower charging, less power)
    ├── Crystal formation (NiMH: voltage depression)
    ├── Grid corrosion (lead-acid: shedding active material)
    ├── Separator degradation (risk of internal short)
    ├── Seal failure (leaking electrolyte)
    └── Case deformation (swelling, cracking)
```

## Prevention Methods

### Proper Sizing

Using the right battery for the application.

```
BATTERY SIZING FOR HEAT MANAGEMENT

    CONTINUOUS DISCHARGE RATING:

    Rule: Battery continuous rating ≥ 1.5× actual load current

    Example: Load = 10A
    Required battery rating = 10A × 1.5 = 15A minimum


    PEAK DISCHARGE RATING:

    Rule: Battery peak rating ≥ 3× peak load current

    Example: Motor startup = 30A (1 second)
    Required battery peak = 30A × 1.5 = 45A minimum


    TEMPERATURE RISE CALCULATION:

    Expected temp rise = (I_actual² × R_internal) / (cooling_factor)

    For enclosed space: cooling_factor = 5-10°C per watt (poor)
    For vented space: cooling_factor = 2-5°C per watt (good)
    For forced air: cooling_factor = 1-2°C per watt (excellent)

    Example: 5W heat, enclosed box (5°C/W)
    Temp rise = 5W × 5°C/W = 25°C above ambient
    At 25°C ambient = 50°C battery temp (acceptable but warm)
```

### Cooling Solutions

Methods to keep batteries cool.

```
COOLING METHODS

    PASSIVE COOLING:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ├── Ventilation holes in enclosure                       │
    │   ├── Separating batteries (air gaps)                      │
    │   ├── Metal heatsinks attached to batteries                │
    │   ├── Thermal pads to chassis (metal case)                 │
    │   └── Keep away from heat sources (motors, CPUs)           │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    ACTIVE COOLING:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ├── Fans (12V brushless, 5V USB fans)                    │
    │   ├── Peltier coolers (for high power, energy inefficient) │
    │   ├── Liquid cooling (high-end electric vehicles)          │
    │   └── Compressor cooling (EV batteries, rare)              │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    THERMAL MANAGEMENT MATERIALS:

    Material                Use                      Thermal Conductivity
    ──────────────────────────────────────────────────────────────
    Air gap                 Free                     0.02 W/m·K
    Thermal paste           Between battery and sink 5-10 W/m·K
    Thermal pad             Gap filling              1-5 W/m·K
    Aluminum heatsink       Heat spreading           200 W/m·K
    Copper heatsink         Heat spreading           400 W/m·K
    Heat pipe               Remote cooling           1000-5000 W/m·K
```

### Charging Practices

Smart charging prevents overheating during charge.

```
COOL CHARGING PRACTICES

    CHARGE RATE SELECTION:

    Application                 Recommended Charge Rate
    ──────────────────────────────────────────────────────────────
    Maximum cycle life          0.5C (slow charge)
    Standard use                1.0C (normal)
    Convenience                 2.0C (fast - with temp monitoring)
    Emergency only              3.0C+ (high risk)


    TEMPERATURE-BASED CHARGING:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Battery Temp      Action                                 │
    │   ──────────────────────────────────────────────────────────│
    │   <0°C (32°F)       DO NOT CHARGE (Li-ion - damage)        │
    │   0-10°C (32-50°F)  Charge at 0.2C max (very slow)         │
    │   10-30°C (50-86°F) Normal charging (1C)                   │
    │   30-45°C (86-113°F) Reduce rate (0.5C) - monitor closely  │
    │   >45°C (>113°F)    STOP CHARGING - too hot!               │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    CHARGE TERMINATION AT HIGH TEMP:

    Smart chargers should reduce or stop charge when hot:
    ├── 40°C: Reduce current to 0.5C
    ├── 45°C: Reduce current to 0.2C
    ├── 50°C: Stop charging (fault)
    └── Resume charging only when cooled below 35°C
```

### Thermal Monitoring

Always monitor battery temperature, especially during charging.

```
THERMAL MONITORING METHODS

    METHOD 1: Touch Test (For accessible batteries)
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Check battery temperature periodically during charging   │
    │   If too hot to hold for 10 seconds → STOP CHARGING!       │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    METHOD 2: Infrared Thermometer
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Point at battery surface                                 │
    │   Read temperature                                          │
    │   Log readings over time                                   │
    │   Set alarm at 45°C                                       │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    METHOD 3: BMS with Temperature Sensor
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Thermistor attached to battery (or inside pack)          │
    │   BMS monitors continuously                                 │
    │   Automatically disconnects if over-temperature            │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    METHOD 4: Thermal Camera
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Best for finding hot spots                               │
    │   Shows temperature distribution                           │
    │   Identifies poor connections (high resistance spots)      │
    │   Identifies imbalanced cells (one cell hotter)            │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

## Emergency Response

### If Battery is Overheating

```
IMMEDIATE ACTIONS

    STEP 1: DISCONNECT
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Immediately stop using/discharging the battery           │
    │   If charging: UNPLUG charger immediately                  │
    │   If in device: TURN OFF device                            │
    │   (Do not handle if extremely hot)                         │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    STEP 2: MOVE TO SAFE LOCATION
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   If safe to handle:                                        │
    │   ├── Move battery to non-flammable surface                │
    │   ├── Concrete floor, ceramic plate, metal tray           │
    │   ├── Away from flammable materials (curtains, paper)      │
    │   ├── Away from occupied areas                             │
    │   └── Outdoors if possible                                 │
    │                                                             │
    │   If too hot to handle: LEAVE IT ALONE                    │
    │   Move flammable materials away from it                    │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    STEP 3: COOL DOWN
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Passive cooling (recommended):                            │
    │   ├── Place in cool area (not refrigerator)               │
    │   ├── Use fan to blow air over battery                     │
    │   ├── Wait for natural cooling                             │
    │   └── Monitor temperature (check every few minutes)        │
    │                                                             │
    │   DO NOT:                                                   │
    │   ├── Put in refrigerator or freezer (condensation)        │
    │   ├── Submerge in water (short circuit risk)               │
    │   ├── Spray with CO₂ (thermal shock)                       │
    │   └── Leave unattended if still hot                        │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    STEP 4: MONITOR
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Watch for:                                                │
    │   ├── Smoke emission                                       │
    │   ├── Swelling (especially Li-ion)                         │
    │   ├── Leaking electrolyte                                  │
    │   ├── Rapid temperature rise (thermal runaway precursor)   │
    │   └── Hissing sound (venting)                             │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

### Thermal Runaway Response

If battery enters thermal runaway (self-heating, smoking).

```
THERMAL RUNAWAY (Li-ion)

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   WARNING: Thermal runaway is SELF-SUSTAINING              │
    │   NOTHING you do will stop it once started!                │
    │                                                             │
    │   SIGNS:                                                    │
    │   ├── Smoke (white/grey, acrid smell)                      │
    │   ├── Rapid swelling (case expanding)                      │
    │   ├── Hissing or popping sounds                            │
    │   ├── Flames (jet of fire from vent)                       │
    │   └── Temperature >150°C (302°F) and rising                │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    IMMEDIATE RESPONSE:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   1. EVACUATE THE AREA IMMEDIATELY                         │
    │      (Toxic smoke is dangerous to breathe)                 │
    │                                                             │
    │   2. CALL EMERGENCY SERVICES (Fire Department)             │
    │                                                             │
    │   3. IF SAFE: Move battery outdoors (if accessible)        │
    │      (Use heat-resistant gloves, shovel, etc.)             │
    │                                                             │
    │   4. DO NOT use water (except large volumes for cooling)   │
    │      DO NOT use standard fire extinguisher (Class ABC)     │
    │      Use Class D (metal fire) extinguisher if available   │
    │                                                             │
    │   5. SMOTHER with sand or baking soda (if safe to approach)│
    │                                                             │
    │   6. CLOSE DOORS to contain fire (if indoors)              │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    AFTER THERMAL RUNAWAY:

    ├── Battery is destroyed (DO NOT TRY TO USE)
    ├── Area may have toxic residue (clean with PPE)
    ├── Battery can re-ignite hours later
    ├── Dispose via hazardous waste (not regular trash)
    └── Replace with new battery (same type/size)
```

### Post-Overheating Disposal

```
DISPOSING OF OVERHEATED BATTERIES

    DO NOT:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ✗ Throw in trash (fire hazard)                           │
    │   ✗ Attempt to recharge (will overheat again)              │
    │   ✗ Use in device (unreliable, dangerous)                  │
    │   ✗ Puncture or crush (fire/explosion)                     │
    │   ✗ Store with other batteries                             │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    SAFE DISPOSAL METHOD (Li-ion):

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   1. Discharge to <1V (if safe - use resistor)             │
    │      (Skip if battery is swollen or damaged)               │
    │                                                             │
    │   2. Place in metal container with sand or cat litter      │
    │      (prevents fire spread if it ignites)                  │
    │                                                             │
    │   3. Take to battery recycling facility:                   │
    │      ├── Call2Recycle (US/Canada)                          │
    │      ├── Best Buy, Home Depot, Lowe's                      │
    │      ├── Local hazardous waste facility                    │
    │      └── Municipal recycling center                        │
    │                                                             │
    │   4. DO NOT store damaged batteries longer than necessary  │
    │      (Take within 24-48 hours if possible)                 │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    IF BATTERY IS SWOLLEN:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Swollen Li-ion battery = IMMINENT FAILURE RISK           │
    │                                                             │
    │   Do NOT store indoors!                                    │
    │   Place in fire-safe container (metal with sand)           │
    │   Store OUTDOORS away from buildings                       │
    │   Dispose at recycling center ASAP (same day if possible)  │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

## Temperature Limits Quick Reference

| Chemistry | Max Operating | Max Charging | Max Storage | Thermal Runaway |
|-----------|---------------|--------------|-------------|-----------------|
| Li-ion | 60°C (140°F) | 45°C (113°F) | 35°C (95°F) | ~80°C (176°F) |
| LiFePO₄ | 65°C (149°F) | 55°C (131°F) | 45°C (113°F) | ~100°C (212°F) |
| Lead-acid | 50°C (122°F) | 50°C (122°F) | 30°C (86°F) | ~60°C (140°F) |
| NiMH | 50°C (122°F) | 45°C (113°F) | 35°C (95°F) | ~70°C (158°F) |

## Summary

1. **Overheating** is operation above maximum safe temperature

2. **Normal heat** comes from I²R losses (P = I² × R_internal)

3. **Normal range:** 20-40°C (68-104°F) - warm but safe

4. **Dangerous range:** >50°C (>122°F) - stop use immediately!

5. **Causes:** excessive current, fast charging, external heat, poor ventilation, internal shorts

6. **Li-ion most sensitive** - thermal runaway at ~80°C (176°F)

7. **Every 10°C above 25°C** halves lead-acid battery life

8. **Signs:** too hot to touch, swelling (Li-ion), smell, performance issues

9. **Prevent with:** proper sizing, ventilation, cooling, temperature monitoring

10. **Charge rate:** 1C max for normal use, 0.5C for long life

11. **Do not charge Li-ion below 0°C** (permanent damage even at normal voltage)

12. **Stop charging if battery exceeds 45°C (113°F)**

13. **Thermal runaway** is self-sustaining - EVACUATE immediately

14. **Never leave charging unattended** - check temperature periodically

15. **Swollen Li-ion battery = DANGER** - dispose immediately

*This documentation belongs to https://github.com/InterCentury*