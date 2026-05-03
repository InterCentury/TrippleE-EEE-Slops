# 04.18 - Overcharging

## What is Overcharging?

Overcharging occurs when a battery continues to receive electrical charge after it has reached its maximum safe voltage and full capacity. This forces the battery to accept more energy than it can safely store, leading to chemical breakdown, gas generation, overheating, and potentially catastrophic failure.

Overcharging is one of the most dangerous conditions for rechargeable batteries and is the leading cause of battery fires, explosions, and premature battery death. Understanding overcharging and proper charging practices is essential for anyone working with rechargeable batteries.

## The Overcharging Process

### What Happens Inside a Battery During Overcharge

Different battery chemistries react differently to overcharging, but all experience degradation and potential failure.

```
OVERCHARGING PROCESS (General)

    NORMAL CHARGING:                 OVERCHARGING:
    
    Charger ──► Battery ──► 100%    Charger ──► Battery ──► 110%
         │                              │
         ▼                              ▼
    Energy stored                   Excess energy
    chemically                      → HEAT
                                    → GAS
                                    → PRESSURE
                                    → DAMAGE
    
    Safe!                           DANGEROUS!


BATTERY VOLTAGE DURING OVERCHARGE (Li-ion example):

    Voltage (V)
        │
    5.0 ┼                           ╱
        │                          ╱
    4.5 ┼                         ╱
        │                        ╱
    4.2 ┼───────────────────────● (full charge)
        │                      ╱
    4.0 ┼                     ╱
        │                    ╱
    3.5 ┼                   ╱
        │                  ╱
    3.0 ┼─────────────────●──────────► Time
        │                 │    │
        │                 │    │
        │            Normal    Overcharge
        │          Charging    Region
        │
    
    Voltage rises sharply after full charge!
    This triggers protection circuits (if present)
```

### By Battery Chemistry

```
OVERCHARGE BEHAVIOR BY CHEMISTRY

LITHIUM-ION (Li-ion) - MOST DANGEROUS:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

    Normal full voltage: 4.2V per cell
    Absolute maximum: 4.25-4.30V per cell
    
    Overcharge effects:
    ├── Lithium plating on anode (metallic lithium)
    ├── Electrolyte decomposition (gas generation)
    ├── Internal pressure increase
    ├── Temperature runaway (can exceed 200°C)
    ├── Thermal runaway → FIRE or EXPLOSION!
    └── Permanent capacity loss (even if no immediate failure)

    Time to failure (at 4.5V): Minutes to hours
    Time to failure (at 5.0V): Seconds to minutes

    SAFETY: Requires protection circuit (never charge without!)


LEAD-ACID - MORE TOLERANT:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

    Full charge voltage: 2.40-2.45V per cell (14.4-14.7V for 12V)
    Float voltage: 2.25-2.30V per cell (13.5-13.8V for 12V)
    
    Overcharge effects:
    ├── Electrolysis of water (H₂ and O₂ gas production)
    ├── Electrolyte loss (water decomposes)
    ├── Grid corrosion (positive plate)
    ├── Plate shedding (active material loss)
    ├── Drying out (requires water addition in flooded types)
    └── Can tolerate moderate overcharge (vented)

    TOLERANCE: Can survive limited overcharge (hours at float)

    Sealed (VRLA) batteries: Gas recombines, but pressure builds
    Can vent and dry out permanently


NICKEL-BASED (NiMH, NiCd) - FAIRLY TOLERANT:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

    Full charge detection: Voltage dip (-ΔV) or temperature rise
    
    Overcharge effects:
    ├── Oxygen generation at positive electrode
    ├── Oxygen migrates to negative electrode (recombines)
    ├── Heat generation (can be severe)
    ├── Pressure increase (cell may vent)
    ├── Capacity loss (permanent if severe)
    └── Can tolerate low-rate overcharge (C/10)

    Seal rupture at high pressure (hydrogen/oxygen mixture - explosive!)

    NiCd more tolerant than NiMH
    NiMH has lower overcharge tolerance


OVERCHARGE TOLERANCE COMPARISON:

    Chemistry      Max Safe V   Overcharge Tolerance   Consequences
    ──────────────────────────────────────────────────────────────
    Li-ion         4.25V        Very low (minutes)     FIRE, EXPLOSION
    LiFePO₄        3.65V        Low (tens of minutes)  Swelling, failure
    Lead-acid      2.45V/cell   Moderate (hours)       Gas, water loss
    NiMH           1.45V/cell   Moderate (hours)       Heat, venting
    NiCd           1.45V/cell   Moderate (hours)       Heat, venting
```

## Causes of Overcharging

### Faulty Charger

The most common cause of overcharging is a malfunctioning or improper charger.

```
CHARGER-RELATED OVERCHARGING

    CAUSE 1: Wrong Charger Voltage
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Battery: 7.4V Li-ion (2S) → needs 8.4V charger            │
    │   Wrong charger: 12V lead-acid charger                      │
    │                                                             │
    │   Result: Immediate overvoltage → FIRE!                     │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    CAUSE 2: Charger Fails to Stop
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Normal: Charger stops when battery reaches 4.2V           │
    │   Fault: Charger continues applying voltage                 │
    │                                                             │
    │   Result: Battery voltage rises beyond safe limit           │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    CAUSE 3: Incorrect Charge Algorithm
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Li-ion charger on NiMH battery                            │
    │   ├── Li-ion: Constant current → Constant voltage (4.2V)    │
    │   ├── NiMH: Needs voltage dip detection (-ΔV)               │
    │   └── Li-ion algorithm won't stop NiMH charging             │
    │                                                             │
    │   Result: NiMH battery overcharges, heats, vents            │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    CAUSE 4: Open Circuit Voltage Sensing
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Charger measures battery voltage to know when to stop     │
    │   If sense wire breaks:                                     │
    │   ├── Charger sees LOW voltage (0V)                         │
    │   ├── Charger continues charging FOREVER                    │
    │   └── Battery overcharges until destruction!                │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    PREVENTION:

    ├── Always use correct charger for battery type
    ├── Use reputable chargers (UL, CE certified)
    ├── Never leave charging unattended (especially Li-ion)
    ├── Check charger output voltage before connecting
    └── Replace chargers that show signs of failure
```

### Imbalanced Cells (Multi-cell Batteries)

In multi-cell packs, one cell can overcharge while others are still charging.

```
CELL IMBALANCE OVERCHARGE

    Single cell (balanced):        Multi-cell (imbalanced):
    
    ┌─────────┐                    ┌─────────────────────────────┐
    │ Cell 1  │ 4.2V               │ Cell 1 │████████████░░░░░░░░│ 3.8V
    │ Full    │                    │        │                    │
    └─────────┘                    ├─────────────────────────────┤
                                   │ Cell 2 │████████████████████│ 4.2V
                                   │ Full   │ FULL(overcharging!)│
    All cells balanced             ├─────────────────────────────┤
                                   │ Cell 3 │██████████░░░░░░░░░░│ 3.6V
                                   │        │                    │
    Normal charging stops          │ Charger sees AVERAGE 3.9V   │
    when any cell reaches 4.2V     │ Continues charging!         │
                                   │ Cell 2 → 4.5V → FIRE!       │
                                   └─────────────────────────────┘

    CAUSES OF IMBALANCE:

    ├── Manufacturing differences (capacity, internal resistance)
    ├── Age differences (one cell degrades faster)
    ├── Temperature differences (hot cells charge faster)
    ├── No balancing circuit (cheap battery packs)
    ├── Damaged cell (high self-discharge)
    └── Different charge states when assembled

    SOLUTIONS:

    ├── Use battery management system (BMS) with balancing
    ├── Use matched cells (same brand, batch, age)
    ├── Balance charge before use
    ├── Replace entire pack when one cell fails
    └── Monitor individual cell voltages
```

### Over-temperature Charging

Charging batteries at extreme temperatures accelerates damage.

```
TEMPERATURE EFFECTS ON OVERCHARGING

    COLD CHARGING (<0°C / 32°F):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Internal resistance increases greatly                     │
    │   Voltage rises faster (false full indication)              │
    │   Lithium plating occurs (even at normal voltage)           │
    │   Charger may not detect true state of charge               │
    │                                                             │
    │   RISK: Severe Li-ion damage, capacity loss, short circuits │
    │                                                             │
    │   RULE: Never charge Li-ion below 0°C!                      │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    HOT CHARGING (>45°C / 113°F):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Charging efficiency decreases                             │
    │   Heat from charging adds to ambient heat                   │
    │   Thermal runaway threshold lowers                          │
    │   Pressure builds faster (gassing)                          │
    │   Sealed batteries may vent                                 │
    │                                                             │
    │   RISK: Thermal runaway, fire, explosion                    │
    │                                                             │
    │   RULE: Stop charging if battery exceeds 45°C               │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    SAFE CHARGING TEMPERATURE RANGES:

    Chemistry      Min Temp     Max Temp     Ideal Range
    ──────────────────────────────────────────────────────────────
    Li-ion         0°C (32°F)   45°C (113°F) 10-30°C (50-86°F)
    LiFePO₄        -10°C (14°F) 55°C (131°F) 10-35°C (50-95°F)
    Lead-acid      -20°C (-4°F) 50°C (122°F) 10-30°C (50-86°F)
    NiMH           0°C (32°F)   45°C (113°F) 10-30°C (50-86°F)

    WARNING: Charging Li-ion below 0°C causes permanent damage
              even at normal voltages!
```

## Signs of Overcharging

### Visual Indicators

```
VISUAL WARNING SIGNS

    SWOLLEN BATTERY (Li-ion):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Normal battery:      Swollen battery:                     │
    │   ┌─────────────┐      ┌─────────────────┐                  │
    │   │  ████████   │      │  ████████████   │                  │
    │   │  ██    ██   │      │  ██        ██   │  (puffed)        │
    │   │  ██    ██   │      │  ██   ○    ██   │                  │
    │   │  ████████   │      │  ██        ██   │                  │
    │   └─────────────┘      └─────────────────┘                  │
    │                                                             │
    │   Flat, rectangular    Bulging, puffed                      │
    │                                                             │
    │   WARNING: Swollen Li-ion is DANGEROUS!                     │
    │            Stop use immediately!                            │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    VENTING (Gas Release):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Sealed batteries have pressure relief vents               │
    │                                                             │
    │   Signs of venting:                                         │
    │   ├── White crust around vent hole                          │
    │   ├── Electrolyte smell (sweet for Li-ion, rotten eggs for  │
    │   │    lead-acid, ammonia for NiMH)                         │
    │   ├── Bulging case (before vent)                            │
    │   ├── Hissing sound (gas escaping)                          │
    │   └── Visible smoke or vapor                                │
    │                                                             │
    │   AFTER VENTING: Battery is permanently damaged/DANGEROUS!  │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    DISCOLORATION / MELTING:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Signs of severe overheating:                              │
    │   ├── Melted plastic case                                   │
    │   ├── Discolored wrapper (brown/black)                      │
    │   ├── Melted wires or insulation                            │
    │   ├── Burn marks on contacts                                │
    │   └── Melted battery holder                                 │
    │                                                             │
    │   THESE ARE FIRE DAMAGE SIGNS!                              │
    │   Disconnect immediately (if safe)                          │
    │   Evacuate area if smoke present                            │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

### Electrical Indicators

```
ELECTRICAL WARNING SIGNS

    ABNORMAL VOLTAGE:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Li-ion cell:                                              │
    │   ├── Normal full: 4.15V - 4.20V                            │
    │   ├── Overcharged: >4.25V (danger)                          │
    │   ├── Critical: >4.30V (immediate danger)                   │
    │   └── Catastrophic: >4.50V (fire imminent)                  │
    │                                                             │
    │   Lead-acid cell (12V battery = 6 cells):                   │
    │   ├── Normal full: 12.6V - 12.8V                            │
    │   ├── Overcharged: >14.4V (gassing)                         │
    │   └── Critical: >15.0V (severe damage)                      │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    HIGH TEMPERATURE:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Temperature during charging:                              │
    │                                                             │
    │   Normal:     20-30°C (68-86°F) - warm                      │
    │   Warning:    35-45°C (95-113°F) - hot                      │
    │   Danger:     45-60°C (113-140°F) - very hot (stop!)        │
    │   Critical:   >60°C (140°F) - thermal runaway risk!         │
    │                                                             │
    │   Touch test: If too hot to hold comfortably → STOP!        │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    CHARGER BEHAVIOR:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Signs charger is overcharging:                            │
    │   ├── Charger LED stays RED much longer than normal         │
    │   ├── Charger never indicates "full" (GREEN)                │
    │   ├── Charger very hot                                      │
    │   ├── Charging current does not decrease (CV phase fails)   │
    │   └── Battery gets hot while charger indicates charging     │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

## Effects of Overcharging

### Immediate Effects

```
IMMEDIATE CONSEQUENCES

    GAS GENERATION:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Li-ion:  Decomposition of electrolyte                     │
    │            → CO₂, CO, hydrocarbons (flammable!)             │
    │                                                             │
    │   Lead-acid: Electrolysis of water                          │
    │             → HYDROGEN (EXPLOSIVE!) + OXYGEN                │
    │                                                             │
    │   NiMH:  Oxygen evolved at positive, recombines at negative │
    │          (slow overcharge safe, fast = heat)                │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    PRESSURE BUILDUP:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Sealed batteries cannot release gas easily                │
    │   Pressure increases → case swells → vent ruptures          │
    │                                                             │
    │   Vented gases are often:                                   │
    │   ├── Toxic (lead-acid: sulfuric acid mist)                 │
    │   ├── Flammable (hydrogen, hydrocarbons)                    │
    │   └── Explosive (hydrogen-air mixture)                      │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    TEMPERATURE RISE (Li-ion):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Thermal Runaway cycle:                                    │
    │                                                             │
    │   Overcharge → Internal heat → SEI layer breakdown          │
    │        ↑                                ↓                   │
    │        │                          Anode + electrolyte       │
    │        │                                ↓                   │
    │      More heat ← More reactions ← Higher temperature        │
    │                                                             │
    │   Once started, cannot stop! → FIRE (2000°C+)               │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

### Long-term Effects

```
PERMANENT CAPACITY LOSS

    Overcharge cycles vs capacity (Li-ion):

    Capacity (%)
        │
    100 ┼●───────────────────────────────────────────────────────
        │ ╲
     90 ┼  ╲
        │   ╲
     80 ┼    ╲
        │     ╲
     70 ┼      ╲
        │       ╲
     60 ┼        ╲
        │         ╲
     50 ┼          ╲
        │           ╲
        └────────────────────────────────────────────────► # of overcharges
         0    5    10   15   20   25   30

    Each overcharge event reduces capacity by 5-20%!
    After ~20 overcharges, battery is unusable.


INTERNAL DAMAGE:

    ├── Lithium plating (Li-ion) → internal shorts
    ├── Grid corrosion (lead-acid) → high resistance
    ├── Crystal formation (NiMH) → voltage depression
    ├── Separator damage → short circuits
    └── Electrolyte dry-out → no ion transport


SAFETY RISKS:

    Overcharged batteries become unstable:
    ├── Spontaneous fire (hours or days later!)
    ├── Internal short circuit (failure under load)
    ├── Thermal runaway when recharged again
    └── Catastrophic failure during normal use
```

## Prevention Methods

### Protection Circuits (BMS)

The most important safety device for Li-ion batteries.

```
BATTERY MANAGEMENT SYSTEM (BMS)

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ┌─────────────────────────────────────────────────────┐   │
    │   │                   BMS IC                            │   │
    │   │  ┌─────────┐    ┌─────────┐    ┌───────────┐        │   │
    │   │  │Voltage  │    │Current  │    │Temperature│        │   │
    │   │  │Monitor  │    │Monitor  │    │Monitor    │        │   │
    │   │  └────┬────┘    └────┬────┘    └────┬──────┘        │   │
    │   │       │              │              │               │   │
    │   │       └──────────────┼──────────────┘               │   │
    │   │                      │                              │   │
    │   │                 ┌────┴────┐                         │   │
    │   │                 │  FET    │                         │   │
    │   │                 │Switches │                         │   │
    │   │                 └────┬────┘                         │   │
    │   │                      │                              │   │
    │   └──────────────────────┼──────────────────────────────┘   │
    │                          │                                  │
    │   Battery (+) ───────────┼─────────────────── Load (+)      │
    │                          │                                  │
    │   Cell 1 ──┬─────────────┤                                  │
    │            │             │                                  │
    │   Cell 2 ──┤             │                                  │
    │            │             │                                  │
    │   Cell 3 ──┤             │                                  │
    │            │             │                                  │
    │   Battery (-) ───────────┼─────────────────── Load (-)      │
    │                          │                                  │
    │                          ▼                                  │
    │                    FET switches can                         │
    │                    DISCONNECT battery!                      │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘

    BMS PROTECTIONS:

    Protection              Trigger                  Action
    ──────────────────────────────────────────────────────────────
    Over-voltage            Any cell >4.25V          Stop charging
    Under-voltage           Any cell <2.8V           Stop discharging
    Over-current            >rated current           Disconnect load
    Short circuit           Instant high current     Instant disconnect
    Over-temperature        >65°C (149°F)           Disconnect both
    Cell imbalance          ΔV >0.3V                 Balance charge


    WITHOUT BMS: Li-ion battery is a fire waiting to happen!
    ALWAYS use BMS with multi-cell Li-ion packs!
```

### Smart Chargers

Modern chargers prevent overcharging automatically.

```
SMART CHARGER FEATURES

    CHARGE ALGORITHMS:

    Li-ion (CC/CV):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Current (A)     Voltage (V)                               │
    │        │               │                                    │
    │    1.0 ┼●──────────────┼───────────┐ (Current drops in CV)  │
    │        │               │ 4.2 ┼─────┴────────● (Voltage flat)│
    │    0.8 ┼               │     │        /                     │
    │        │               │ 4.0 ┼       /                      │
    │    0.6 ┼               │     │      /                       │
    │        │      / (V)    │ 3.8 ┼     / (Voltage rising in CC) │
    │    0.4 ┼     /         │     │    /                         │
    │        │    /          │ 3.6 ┼   /                          │
    │    0.2 ┼   /           │     │  /                           │
    │        │  /            │ 3.4 ┼●                             │
    │    0.0 ┼─●─────────────┴─3.2 ┼─────────────●──────► Time    │
    │                                                             │
    │        Constant Current (CC)  Constant Voltage (CV)         │
    │        Charging stops when current drops to C/10            │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘

    Charging stops automatically at correct voltage!
    No risk of overcharge (if functioning properly).


    NiMH (-ΔV Detection):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Voltage                                                   │
    │        │                                                    │
    │    1.5 ┼─────────────────────────────────────────────────   │
    │        │                                                    │
    │    1.4 ┼──────────────────●                                 │
    │        │                 ╱ ╲                                │
    │    1.3 ┼───────────────╱    ╲                               │
    │        │             ╱       ╲                              │
    │    1.2 ┼───────────●          ╲                             │
    │        │         ╱             ●─────                       │
    │    1.1 ┼───────●                                            │
    │        │     ╱                                              │
    │    1.0 ┼───●                                                │
    │        │                                                    │
    │                                                             │
    │                  │                                          │
    │                  ▼                                          │
    │            Voltage DIP (-ΔV)                                │
    │            Charger STOPS!                                   │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    SMART CHARGER BENEFITS:

    ├── Automatically stops when battery is full
    ├── Temperature monitoring (stops if too hot)
    ├── Timer backup (stops after max time)
    ├── Cell balancing (multi-cell packs)
    ├── Fault detection (bad battery, no connection)
    └── Safe for unattended charging (with precautions)
```

### Charge Termination Methods

```
CHARGE TERMINATION BY BATTERY TYPE

    LITHIUM-ION:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Method: Constant Current → Constant Voltage (CC/CV)       │
    │   Termination: Current drops to C/10 (or 1/20)              │
    │   Typical: 1C charge → stop at 0.1C (200mA for 2000mAh)     │
    │   Backup: Timer (3 hours max)                               │
    │   Safety: Temperature cutoff (45°C)                         │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    LEAD-ACID:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Method: Constant Current → Constant Voltage               │
    │   Bulk: Constant current (0.1C-0.3C) to 14.4V (12V battery) │
    │   Absorption: Constant voltage (14.4V) until current drops  │
    │   Float: Constant voltage (13.6V) maintenance               │
    │   Termination: Current drops to 0.02C-0.05C                 │
    │                                                             │
    │   Float charging is NOT overcharging! (safe voltage)        │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    NICKEL-BASED (NiMH/NiCd):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Primary method: -ΔV detection (voltage dip)               │
    │   Backup 1: dT/dt (temperature rise rate)                   │
    │   Backup 2: Absolute temperature cutoff (50°C)              │
    │   Backup 3: Timer (1.5× expected charge time)               │
    │   Backup 4: Maximum voltage (1.6V/cell)                     │
    │                                                             │
    │   Trickle charge safe at C/20 rate                          │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

### User Practices

What YOU can do to prevent overcharging.

```
SAFE CHARGING PRACTICES

    DO:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ✓ Use correct charger for battery type                   │
    │   ✓ Charge on non-flammable surface (concrete, ceramic)    │
    │   ✓ Monitor battery temperature during charging            │
    │   ✓ Remove battery when charging completes                 │
    │   ✓ Use reputable batteries and chargers                   │
    │   ✓ Inspect batteries before charging (swelling, damage)   │
    │   ✓ Balance charge multi-cell packs regularly              │
    │   ✓ Keep area ventilated (especially lead-acid)            │
    │   ✓ Have fire extinguisher nearby (Class D for Li-ion)     │
    │   ✓ Charge in visible area (not behind furniture)          │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    DON'T:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ✗ Leave charging unattended (especially Li-ion)          │
    │   ✗ Charge damaged or swollen batteries                    │
    │   ✗ Use damaged chargers (cracked, frayed wires)           │
    │   ✗ Override protection circuits                           │
    │   ✗ Charge below 0°C (Li-ion)                             │
    │   ✗ Charge above 45°C (all types)                         │
    │   ✗ Mix different battery types in same charger            │
    │   ✗ Charge near flammable materials                        │
    │   ✗ Block charger ventilation                              │
    │   ✗ Use "universal" chargers (often unsafe)                │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    CHARGE IN SAFE LOCATION:

    Good:                           Bad:
    ┌─────────────────────┐        ┌─────────────────────┐
    │  Concrete floor     │        │  Wooden desk        │
    │  Ceramic plate      │        │  Near curtains      │
    │  No flammables      │        │  On carpet          │
    │  Ventilated area    │        │  Under pillow       │
    │  Smoke detector     │        │  Overnight alone    │
    └─────────────────────┘        └─────────────────────┘
```

## Emergency Response

### If You Suspect Overcharging

```
IMMEDIATE ACTIONS

    STEP 1: DISCONNECT!
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Unplug charger immediately                               │
    │   (Do not touch battery if very hot)                       │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    STEP 2: MOVE TO SAFE LOCATION
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   If safe to handle: Move battery to non-flammable surface │
    │   Concrete floor, ceramic pot, metal tray                  │
    │   Away from flammable materials                            │
    │   Away from occupied areas                                 │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    STEP 3: MONITOR
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Watch for:                                                │
    │   ├── Smoke emission                                       │
    │   ├── Flames                                               │
    │   ├── Swelling (Li-ion)                                    │
    │   ├── Hissing sound                                        │
    │   └── Extreme heat                                         │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    STEP 4: EVACUATE IF NECESSARY
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Evacuate area if:                                         │
    │   ├── Battery is smoking                                   │
    │   ├── You see flames                                       │
    │   ├── You hear venting (hiss)                              │
    │   ├── Strong chemical smell                                │
    │   └── Battery is swelling rapidly                          │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

### Battery Fire Response

```
Li-ion / LiPo BATTERY FIRE

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   DO NOT use water! (except large amounts for cooling)     │
    │   DO NOT use standard fire extinguisher (Class A, B, C)    │
    │                                                             │
    │   Fires are Class D (metal fire) or electrical (Class C)   │
    │                                                             │
    │   WHAT TO DO:                                               │
    │                                                             │
    │   1. EVACUATE area immediately                             │
    │   2. CALL emergency services (fire department)             │
    │   3. If safe: Use Class D extinguisher (Lithium-specific)  │
    │   4. If available: Smother with sand or baking soda        │
    │   5. If nothing else: LARGE amounts of water (cooling)     │
    │                                                             │
    │   Li-ion batteries burn at 2000°C (3632°F)                 │
    │   They produce toxic, flammable gases                       │
    │   They can re-ignite hours later!                          │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


LEAD-ACID BATTERY FIRE / EXPLOSION

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Hydrogen gas explosion risk!                             │
    │                                                             │
    │   WHAT TO DO:                                               │
    │                                                             │
    │   1. EVACUATE area (explosion risk)                        │
    │   2. NO open flames! (don't turn lights on/off)            │
    │   3. VENTILATE area (open windows, doors)                  │
    │   4. Use Class B or C fire extinguisher                    │
    │   5. Baking soda neutralizes acid (after fire out)         │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


NiMH / NiCd BATTERY FIRE

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Less severe than Li-ion, but still dangerous              │
    │                                                             │
    │   WHAT TO DO:                                               │
    │                                                             │
    │   1. Unplug charger                                        │
    │   2. Use ABC fire extinguisher                             │
    │   3. Water may be used (cooling)                           │
    │   4. Ventilate area (toxic fumes)                          │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

### After Overcharge Event

```
DISPOSAL OF OVERCHARGED BATTERIES

    DO NOT:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ✗ Throw in trash (fire hazard!)                          │
    │   ✗ Attempt to recharge (will likely catch fire)           │
    │   ✗ Crush or puncture (immediate fire/explosion)           │
    │   ✗ Store with other batteries                             │
    │   ✗ Leave unattended (can spontaneously ignite)            │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    SAFE HANDLING:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Li-ion:                                                   │
    │   1. Discharge to <1V (using resistor, outdoors)           │
    │      (or skip if already bulging - too dangerous)          │
    │   2. Place in metal container with sand                    │
    │   3. Take to battery recycling facility immediately        │
    │                                                             │
    │   Lead-acid:                                                │
    │   1. Neutralize acid with baking soda                      │
    │   2. Take to recycling center (some pay for scrap)         │
    │                                                             │
    │   NiMH/NiCd:                                                │
    │   1. Discharge fully (low current)                         │
    │   2. Take to recycling center (NiCd is hazardous waste)    │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    PROFESSIONAL RECYCLING:

    ├── Call2Recycle (US/Canada) - free recycling
    ├── Local hazardous waste facility
    ├── Battery retail stores (Home Depot, Lowe's, Best Buy)
    ├── Electronics stores (Staples, Office Depot)
    └── Municipal hazardous waste collection events
```

## Quick Reference Table

| Chemistry | Full Voltage | Max Safe V | Overcharge Tolerance | Protection Required |
|-----------|--------------|------------|---------------------|---------------------|
| Li-ion | 4.2V | 4.25V | Very low | BMS mandatory |
| LiFePO₄ | 3.65V | 3.70V | Low | BMS required |
| Lead-acid (12V) | 12.8V | 14.4V (charging) | Moderate | Smart charger |
| NiMH (1.2V) | 1.45V | 1.60V | Moderate | Smart charger |
| NiCd (1.2V) | 1.45V | 1.60V | Moderate | Smart charger |

## Summary

1. **Overcharging** is continuing to charge a battery after it reaches full capacity

2. **Li-ion is most dangerous** - overcharge causes thermal runaway → FIRE!

3. **Overcharge effects:** gas generation, pressure buildup, heat, permanent damage

4. **Causes:** wrong charger, faulty charger, imbalanced cells, temperature extremes

5. **Li-ion overcharge voltage:** >4.25V is dangerous, >4.5V is critical

6. **Signs of overcharging:** swelling (Li-ion), venting (hissing), extreme heat, never reaching "full"

7. **Never leave Li-ion charging unattended** - check periodically

8. **BMS (Battery Management System)** is MANDATORY for multi-cell Li-ion packs

9. **Smart chargers** automatically stop at correct voltage (CC/CV for Li-ion)

10. **NiMH chargers** use -ΔV detection (voltage dip)

11. **Lead-acid** can float charge at reduced voltage (13.6V for 12V)

12. **Cold charging (<0°C)** damages Li-ion even at normal voltage

13. **Hot charging (>45°C)** accelerates failure and thermal runaway

14. **Imbalanced cells** cause one cell to overcharge while others are still charging

15. **If battery swells (Li-ion)** - STOP USE immediately, dispose safely

16. **Battery fires** are extremely dangerous - evacuate, call fire department

*This documentation belongs to https://github.com/InterCentury*