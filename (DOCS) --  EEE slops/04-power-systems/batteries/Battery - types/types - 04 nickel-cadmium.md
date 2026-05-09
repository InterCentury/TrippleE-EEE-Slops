# Types - 04: Nickel-Cadmium (NiCd) Battery

## What is a Nickel-Cadmium Battery?

The nickel-cadmium (NiCd) battery is a type of rechargeable battery that uses nickel oxide hydroxide and metallic cadmium as electrodes. Invented in 1899 by Waldemar Jungner in Sweden, NiCd was the first practical rechargeable battery for portable applications. It dominated the rechargeable market for much of the 20th century before being largely replaced by NiMH and Li-ion.

NiCd batteries are known for their excellent cycle life, high discharge rates, wide temperature tolerance, and extreme robustness. However, they suffer from "memory effect," contain toxic cadmium (banned in many countries), and have relatively low energy density. Despite these drawbacks, NiCd remains in use for certain industrial, aviation, and high-demand applications where reliability outweighs environmental concerns.

## Basic Chemistry and Construction

### How NiCd Batteries Work

NiCd batteries convert chemical energy to electrical energy through reactions involving nickel and cadmium.

```
NICKEL-CADMIUM CHEMISTRY

    DISCHARGE REACTION:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Positive: 2NiOOH + 2H₂O + 2e⁻ → 2Ni(OH)₂ + 2OH⁻           │
    │   Negative: Cd + 2OH⁻ → Cd(OH)₂ + 2e⁻                       │
    │   Overall: 2NiOOH + Cd + 2H₂O → 2Ni(OH)₂ + Cd(OH)₂          │
    │                                                             │
    │   Discharge consumes water, produces nickel and cadmium     │
    │   hydroxides                                                │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    CHARGE REACTION (reverse):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   2Ni(OH)₂ + Cd(OH)₂ → 2NiOOH + Cd + 2H₂O                   │
    │                                                             │
    │   Charge produces water, regenerates active materials       │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    KEY CHARACTERISTICS:

    ├── Nominal cell voltage: 1.2V
    ├── Full charge voltage: 1.4-1.45V
    ├── Discharge cutoff: 1.0V (per cell)
    ├── Very flat discharge curve (constant voltage)             
    ├── Excellent high-rate discharge (10-20C)
    ├── Wide temperature range (-40°C to +60°C)
    └── Long cycle life (500-1000 cycles)
```

### Physical Construction

```
NiCd BATTERY CONSTRUCTION

    CYLINDRICAL CELL (C, D, AA, AAA):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ┌─────────────────────────────────────────────────────┐   │
    │   │  ┌─────────────────────────────────────────────┐    │   │
    │   │  │                                             │    │   │
    │   │  │   Positive terminal (+)                     │    │   │
    │   │  │   (with vent)                               │    │   │
    │   │  └─────────────────────────────────────────────┘    │   │
    │   │                                                     │   │
    │   │  ┌─────────────────────────────────────────────┐    │   │
    │   │  │  ████████████████████████████████████████   │    │   │
    │   │  │  ██   Sealing plate                    ██   │    │   │
    │   │  │  ██   (safety vent)                    ██   │    │   │
    │   │  │  ████████████████████████████████████████   │    │   │
    │   │  └─────────────────────────────────────────────┘    │   │
    │   │                                                     │   │
    │   │  ┌─────────────────────────────────────────────┐    │   │
    │   │  │  ████████████████████████████████████████   │    │   │
    │   │  │  ██   Positive electrode (nickel)      ██   │    │   │
    │   │  │  ██   (foam or sintered plate)         ██   │    │   │
    │   │  │  ████████████████████████████████████████   │    │   │
    │   │  └─────────────────────────────────────────────┘    │   │
    │   │                                                     │   │
    │   │  ┌─────────────────────────────────────────────┐    │   │
    │   │  │  ████████████████████████████████████████   │    │   │
    │   │  │  ██   Separator (nylon/polypropylene)  ██   │    │   │
    │   │  │  ██   (soaked in KOH electrolyte)      ██   │    │   │
    │   │  │  ████████████████████████████████████████   │    │   │
    │   │  └─────────────────────────────────────────────┘    │   │
    │   │                                                     │   │
    │   │  ┌─────────────────────────────────────────────┐    │   │
    │   │  │  ████████████████████████████████████████   │    │   │
    │   │  │  ██   Negative electrode (cadmium)     ██   │    │   │
    │   │  │  ██   (pasted or sintered plate)       ██   │    │   │
    │   │  │  ████████████████████████████████████████   │    │   │
    │   │  └─────────────────────────────────────────────┘    │   │
    │   │                                                     │   │
    │   │  Negative terminal (-)                              │   │
    │   │  (case / can)                                       │   │
    │   │                                                     │   │
    │   └─────────────────────────────────────────────────────┘   │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    CONSTRUCTION TYPES:

    Type               Description                     Use
    ──────────────────────────────────────────────────────────────
    Sintered plate     High power, longer life          Aviation, industrial
    Pocket plate       Very robust, low cost            Stationary, backup
    Bonded (plastic)   Lower cost, consumer            Power tools, toys
    Fiber (fiber)      High capacity, medium power      Cordless phones
    Sealed (consumer)  Maintenance-free, vented         Portable electronics
    Vented (industrial) Replaceable electrolyte         Rail, backup power
```

## NiCd Specifications

### Voltage

NiCd cells maintain a very flat voltage during discharge.

```
NiCd VOLTAGE CHARACTERISTICS

    Individual cell (1.2V nominal):

    State              Voltage        Notes
    ──────────────────────────────────────────────────────────────
    Fresh off charger  1.4-1.45V      Right after charge (surface)
    Resting (full)     1.35-1.40V     After 1-2 hours
    Nominal            1.2V           During most of discharge
    Under load (heavy) 1.0-1.1V       Normal operation
    Discharge cutoff   1.0V           End of useful capacity
    Deep discharge     <0.8V          Damage risk (reversal)
    Fully dead         0V             Shorted cell (replace)


    DISCHARGE CURVE CHARACTERISTIC:

    Voltage (V)
        │
    1.5 ┼●───────────────────────────────────────────────────────
        │ ╲
    1.4 ┼  ╲
        │   ╲
    1.3 ┼    ╲
        │     ╲
    1.2 ┼      ●═════════════════════════════════════════════●
        │                                                 ╱│
    1.1 ┼                                               ╱
        │                                             ╱
    1.0 ┼                                           ●
        │                                         ╱
    0.9 ┼                                       ●
        │
        └────────────────────────────────────────────────► Time
         0%        25%        50%        75%       100%
    
    Very flat discharge (1.2V stable for most of runtime)
    Sharp drop at end (unlike alkaline)


    MULTI-CELL PACK VOLTAGES:

    Cells    Nominal V    Full V    Cutoff V    Common Use
    ──────────────────────────────────────────────────────────────
    1        1.2V         1.4V      1.0V        Single cell
    2        2.4V         2.8V      2.0V        Small devices
    3        3.6V         4.2V      3.0V        Some power tools
    4        4.8V         5.6V      4.0V        Older cordless phones
    5        6.0V         7.0V      5.0V        Power drills
    6        7.2V         8.4V      6.0V        Cordless tools (common)
    7        8.4V         9.8V      7.0V        Some tools
    8        9.6V         11.2V     8.0V        Power tools
    10       12.0V        14.0V     10.0V       Older laptops
```

### Capacity

NiCd capacity is lower than modern batteries.

```
TYPICAL NiCd CAPACITIES

    Size          Typical Capacity    Modern NiMH (for comparison)
    ──────────────────────────────────────────────────────────────
    AAA           300-500 mAh         800-1100 mAh
    AA            600-1000 mAh        2000-2800 mAh
    Sub-C         1200-2000 mAh       3000-5000 mAh
    C             1500-2500 mAh       4500-6000 mAh
    D             2000-4000 mAh       8000-12000 mAh
    9V (7-cell)   120-200 mAh         200-300 mAh


    LOST CAPACITY OVER TIME:

    ├── NiCd loses capacity gradually (100-300 mAh per year)
    ├── "Memory effect" can cause apparent capacity loss
    ├── Deep discharge can restore capacity (memory effect)
    ├── End of life: <60% of original capacity
    └── Typical life: 500-1000 cycles (3-8 years)
```

### Discharge Rates (C-rating)

NiCd batteries excel at high discharge rates.

```
NiCd DISCHARGE CAPABILITY

    Cell Type          Continuous C    Peak C       Notes
    ──────────────────────────────────────────────────────────────
    Standard consumer  1-2C            3-5C         AA/AAA/C/D
    High-power         5-10C           15-20C       Sub-C cells
    Sintered plate     10-20C          30-50C       Industrial
    Aviation           20-30C          50-100C      Aircraft starting


    PRACTICAL EXAMPLES (2000mAh Sub-C cell):

    Discharge Rate    Current    Runtime     Voltage (under load)
    ──────────────────────────────────────────────────────────────
    1C                2.0A       60 min      1.15-1.20V
    5C                10A        12 min      1.10-1.15V
    10C               20A        6 min       1.05-1.10V
    20C               40A        3 min       0.95-1.05V
    30C               60A        2 min       0.85-0.95V

    NiCd holds voltage better than NiMH at high rates
```

## NiCd vs NiMH vs Li-ion

### Comparison Chart

```
COMPARISON: NiCd vs NiMH vs Li-ion

    Feature                 NiCd            NiMH            Li-ion (NMC)
    ────────────────────────────────────────────────────────────────
    Nominal voltage         1.2V            1.2V            3.6-3.7V
    Energy density (Wh/kg)  40-60           60-120          150-260
    Energy density (Wh/L)   100-150         200-300         500-700
    Cycle life (100% DoD)   500-1000        300-500         300-500
    Self-discharge (%/mo)   15-20%          20-30%          2-5%
    Memory effect           YES (severe)    Mild            None
    High-rate discharge     Excellent       Good            Good
    Temperature range       -40 to +60°C    -20 to +50°C    -20 to +60°C
    Toxicity                High (cadmium)  Low             Moderate
    Cost                    $               $$              $$$
    Typical application     Power tools     Hybrid cars,     Smartphones,
                            Aviation        General purpose  EVs, laptops


    ADVANTAGES OF NiCd (reasons still used):

    ├── Best high-rate discharge (can handle 10-20C continuously)
    ├── Widest temperature range (aviation, outdoor)
    ├── Most robust (mechanical, electrical abuse tolerance)
    ├── Longest cycle life (500-1000 cycles typical)
    ├── Simplest charging (no balance charger needed for series)
    ├── Lowest cost per cycle (over lifetime)
    ├── Works at -40°C (Li-ion stops below 0°C)
    └── Very flat discharge voltage (constant power)


    DISADVANTAGES OF NiCd:

    ├── Lowest energy density (heavy for capacity)
    ├── Toxic cadmium (banned in many countries)
    ├── Severe memory effect (requires full discharge)
    ├── High self-discharge (15-20% per month)
    ├── Low nominal voltage (1.2V vs 3.7V Li-ion)
    ├── Poor for low-drain applications (alkaline better)
    └── Environmental disposal challenges (hazardous waste)
```

## Memory Effect

### What is Memory Effect?

The most notorious characteristic of NiCd batteries.

```
MEMORY EFFECT EXPLANATION

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Memory effect (voltage depression):                       │
    │                                                             │
    │   When NiCd is repeatedly discharged to the SAME point      │
    │   before recharging, it "remembers" that point.             │
    │                                                             │
    │   Result: Battery acts as if it has lower capacity          │
    │   (voltage drops prematurely)                               │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    VISUAL EXAMPLE:

    Normal battery:                Battery with memory effect:

    Voltage                        Voltage
        │                              │
    1.4 ┼●                            1.4 ┼●
        │ ╲                               │ ╲
    1.2 ┼  ●════════════════════●        1.2 ┼  ●════════●
        │                     ╱│             │         ╱│
    1.1 ┼                    ╱              1.1 ┼       ╱
        │                  ╱                  │     ╱
    1.0 ┼                ●                   1.0 ┼  ● (voltage
        │              ╱                        │ ╱    drops
    0.9 ┼            ●                         0.9 ┼●     early!)
        │                                          │
        └──────────────────► Time                  └────────────►
         0%      50%     100%                       0%   50%   "false
                                                          empty"


    WHAT CAUSES MEMORY EFFECT:

    ├── Repeated shallow discharges (e.g., 50% always)
    ├── Charging before full discharge
    ├── Trickle charging at elevated temperatures
    ├── Long-term storage at partial charge
    └── Manufacturing variations (some cells more prone)

    REAL EXAMPLE:
    Cordless phone used until beep (20% remaining) each day
    After months: Battery dies at 20% (15 minutes runtime vs 60)
    Battery "remembers" 20% as empty!
```

### Preventing and Fixing Memory Effect

```
PREVENTION:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ✓ Occasionally discharge fully (once per 10-20 cycles)   │
    │   ✓ Use device until it stops (or low voltage cutoff)      │
    │   ✓ Store at discharged state (not recommended for NiMH)   │
    │   ✓ Avoid trickle charging (use smart charger)             │
    │   ✓ Avoid charging warm batteries                          │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    FIXING MEMORY EFFECT (Deep Discharge):

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   METHOD 1: Simple deep discharge                         │
    │   ├── Fully discharge battery (until device stops)         │
    │   ├── Repeat 2-3 times                                    │
    │   └── Usually restores 50-80% of lost capacity            │
    │                                                             │
    │   METHOD 2: "Reconditioning" (professional charger)       │
    │   ├── Charger deep discharges to 0.8V per cell            │
    │   ├── Followed by full charge                             │
    │   ├── Repeat automatically                                │
    │   └── Can restore 90-100% of capacity                     │
    │                                                             │
    │   METHOD 3: "Battery zapping" (high current pulse)        │
    │   ├── Short high-current pulse (10-20A)                   │
    │   ├── Breaks dendrites (internal shorts)                  │
    │   ├── DANGEROUS! (can explode)                           │
    │   └── Only for professional use                          │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    IMPORTANT NOTE:

    Memory effect is temporary and reversible (unlike sulfation in
    lead-acid or lithium plating in Li-ion). A few full discharge/
    charge cycles usually restores most capacity.

    NiMH has MUCH less memory effect (almost none in modern cells)
    Li-ion has NO memory effect
```

## NiCd Applications

### Where NiCd is Still Used

Despite being obsolete for most consumer uses, NiCd remains in specialized applications.

```
CURRENT NiCd APPLICATIONS

    AVIATION (most common remaining use):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Aircraft batteries:                                       │
    │   ├── Emergency lighting                                   │
    │   ├── APU starting                                        │
    │   ├── Backup instruments                                   │
    │   ├── 28V NiCd packs (20 cells)                           │
    │   └── Must work at -40°C to +60°C                         │
    │                                                             │
    │   Why NiCd: Wide temperature range, proven reliability    │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    INDUSTRIAL:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ├── Emergency lighting systems                           │
    │   ├── UPS for high temperature environments                │
    │   ├── Railroad signaling                                   │
    │   ├── Mining equipment (explosion-proof)                   │
    │   ├── Electric forklifts (some)                           │
    │   ├── Solar street lights (cold climates)                  │
    │   └── Military equipment                                   │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    POWER TOOLS (older):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ├── Older cordless drills (7.2V, 9.6V, 12V)             │
    │   ├── Older power screwdrivers                             │
    │   ├── Radio control vehicles (replaced by LiPo)           │
    │   └── Most replaced by NiMH or Li-ion now                 │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    CONSUMER (dying out):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ├── Cordless phones (older, before NiMH)                │
    │   ├── Solar garden lights                                  │
    │   ├── Emergency flashlights                                │
    │   ├── Two-way radios                                       │
    │   └── (Most replaced by NiMH now)                         │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

## Charging NiCd Batteries

### Charging Methods

```
NiCd CHARGING METHODS

    METHOD 1: Standard (overnight) Charging (C/10):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Rate: 0.1C (10-hour rate)                               │
    │   Time: 14-16 hours                                        │
    │   Termination: Timer (no -ΔV needed)                       │
    │   Safe: Yes (can be left charging)                         │
    │   Use: Old chargers, simple circuits                      │
    │                                                             │
    │   Example (2000mAh cell): 200mA for 14-16 hours           │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    METHOD 2: Fast Charging (C/4 to 1C):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Rate: 0.25C to 1C                                        │
    │   Time: 1.2-5 hours                                        │
    │   Termination: -ΔV detection (voltage drop)                │
    │   Backup: Temperature cut-off (50°C)                       │
    │   Use: Smart chargers                                      │
    │                                                             │
    │   -ΔV detection:                                           │
    │   Voltage                                                  │
    │     │                                                     │
    │   1.5 ┼──────────────────────●                             │
    │     │                        ╲│                            │
    │   1.4 ┼───────────────────────●                             │
    │     │                          ╲                           │
    │   1.3 ┼                           ●    ← Voltage drops!   │
    │     │                             ╱                        │
    │   1.2 ┼──────────────────────────●                         │
    │     │                                                     │
    │     └────────────────────────────────────► Time          │
    │                                      │                    │
    │                                      ▼                    │
    │                              Stop charging here!          │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    METHOD 3: Trickle Charge (Maintenance):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Rate: C/20 to C/30 (very low)                           │
    │   Use: Keeps battery topped up                             │
    │   Safe: Yes, indefinitely                                  │
    │   Example (2000mAh): 67-100mA continuous                   │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    CHARGING VOLTAGE LIMITS:

    Single cell:
    ├── Maximum cell voltage: 1.6V (brief, during charge)
    ├── Float/trickle voltage: 1.35-1.40V
    └── Overcharge voltage: >1.65V (gassing, heating)

    Multi-cell pack (e.g., 7.2V, 6 cells):
    ├── Charge voltage: 8.4-9.0V
    ├── Float/trickle: 8.1-8.4V
    └── Overcharge: >9.6V (danger)
```

### NiCd Charging Rules

```
NiCd CHARGING GUIDELINES

    DO:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ✓ Use NiCd-specific charger (or NiMH/NiCd dual)          │
    │   ✓ Use correct charge rate for battery                    │
    │   ✓ Fully discharge occasionally (prevents memory)         │
    │   ✓ Charge at room temperature (10-30°C)                   │
    │   ✓ Use temperature monitoring for fast charging           │
    │   ✓ Ventilate area (hydrogen/oxygen gas possible)          │
    │   ✓ Use trickle charge for storage (C/20-C/30)            │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    DON'T:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ✗ Never trickle charge at >C/10 (damage)                 │
    │   ✗ Never charge frozen battery                            │
    │   ✗ Never overcharge continuously (gassing, dry-out)       │
    │   ✗ Never reverse charge (destroy battery)                 │
    │   ✗ Never charge at >1C unless battery rated              │
    │   ✗ Don't use Li-ion charger (wrong algorithm)            │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    TYPICAL CHARGING TIMES:

    Charge Rate    Charging Time    Termination
    ──────────────────────────────────────────────────────────────
    C/10 (0.1C)    14-16 hours      Timer (safe, no detection needed)
    C/5 (0.2C)     6-8 hours        -ΔV or temperature
    C/2 (0.5C)     2.5-3 hours      -ΔV + temperature + timer
    1C             1-1.5 hours      -ΔV + temperature + timer (fast)

    WARNING: Fast charging (>0.5C) requires smart charger with
    -ΔV detection AND temperature monitoring to prevent overcharge.
```

## NiCd Maintenance

### Regular Maintenance

```
NiCd MAINTENANCE SCHEDULE

    EVERY 10-20 CYCLES:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ☐ Full discharge (prevent memory effect)                 │
    │   ☐ Run device until it stops                             │
    │   ☐ Then full charge                                       │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    YEARLY:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ☐ Recondition (deep discharge to 0.8V/cell)             │
    │   ☐ Check capacity (if <60%, replace)                      │
    │   ☐ Check for leaks (white powder)                         │
    │   ☐ Clean terminals                                        │
    │   ☐ Check for bulging or damage                           │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    FOR STATIONARY (VENTED NiCd):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ☐ Check electrolyte level (every 3-6 months)             │
    │   ☐ Add distilled water                                    │
    │   ☐ Check specific gravity                                │
    │   ☐ Equalization charge                                   │
    │   ☐ Clean vent caps                                       │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

### Storage

```
NiCd STORAGE GUIDELINES

    BEST PRACTICES:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Storage temperature: 0-25°C (32-77°F)                    │
    │   Storage state: DISCHARGED (0V-0.5V per cell)            │
    │   (NiCd damaged by long-term full charge storage)          │
    │                                                             │
    │   Why discharged storage:                                   │
    │   ├── Prevents memory effect                               │
    │   ├── Reduces self-discharge                               │
    │   ├── Extends calendar life                                │
    │   └── Full charge storage degrades capacity               │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    STORAGE LIFE:

    Temperature    Capacity Loss (6 months)    Notes
    ──────────────────────────────────────────────────────────────
    0°C (32°F)     5-10%                       Excellent
    20°C (68°F)    10-20%                      Good
    30°C (86°F)    20-30%                      Acceptable
    40°C (104°F)   30-40%                      Poor
    50°C (122°F)   40-50%                      Severe degradation

    Unlike NiMH and Li-ion, NiCd tolerates storage in discharged
    state without permanent damage. In fact, discharged storage
    is PREFERRED!
```

## Common NiCd Problems

### Problem 1: Memory Effect (Capacity Loss)

```
SYMPTOMS:
├── Battery dies early (e.g., 15 minutes instead of 60)
├── Voltage drops suddenly under load
├── Appears to be dead, but rest voltage normal
├── Device shuts off with battery still warm

CAUSES:
├── Repeated partial discharges (e.g., always to 50%)
├── Always recharging before empty
├── No full discharge cycles
├── Long-term trickle charging

DIAGNOSIS:
├── Note where device stops (always at same point?)
├── Measure voltage under load (should hold 1.0-1.1V)
├── Compare runtime to original specification
├── Try deep discharge cycle

SOLUTIONS:
├── Perform 2-3 full discharge/recharge cycles
├── Use deep discharge (to 0.8V/cell) with reconditioning charger
├── For severe memory: multiple reconditioning cycles
├── If no improvement after 5 cycles: battery beyond recovery
├── Replace if capacity <50% after reconditioning

PREVENTION:
├── Occasionally run device until it stops (once per month)
├── Avoid always recharging at same point
├── Use timer to ensure full discharge sometimes
└── Use smart charger with reconditioning mode
```

### Problem 2: High Self-Discharge

```
SYMPTOMS:
├── Battery loses charge overnight (when idle)
├── Device dead after 2-3 days (even if not used)
├── Voltage drops when sitting on shelf
├── Battery warm even when not in use (internal short)

CAUSES:
├── Normal NiCd characteristic (15-20% per month)
├── Elevated temperature (higher self-discharge)
├── Internal micro-short (dendrites)
├── Old age (separator degradation)
├── Overcharged (separator damaged)

DIAGNOSIS:
├── Measure voltage, then measure again after 24 hours
├── Normal self-discharge: 0.5-1% per day (15-30% per month)
├── Problematic: >5% per day
├── Feel for warmth (warm = internal short)

SOLUTIONS:
├── Acceptable self-discharge: Use or recharge more often
├── High self-discharge (>5%/day): Try reconditioning (breaks dendrites)
├── If still high after reconditioning: Replace battery
├── Store in cool place (slows self-discharge)
├── Use low-rate trickle charger (C/30) for storage

PREVENTION:
├── Store in cool location (refrigerator OK if dry)
├── Don't overcharge (causes dendrites)
├── Avoid high temperatures
└── Use quality cells (less prone to dendrites)
```

### Problem 3: Short Cell (0V)

```
SYMPTOMS:
├── Battery voltage 0V (or very low)
├── Shorted when measured with multimeter (0Ω)
├── Pack voltage lower than cell count suggests
├── Cell gets hot during charging (other cells normal)

CAUSES:
├── Dendrite piercing separator (internal short)
├── Manufacturing defect
├── Overheating (separator melts)
├── Physical damage (dropped, crushed)
├── Over-discharge (reversal, cell death)

DIAGNOSIS:
├── Measure voltage across each cell (if accessible)
├── Shorted cell: 0V (other cells normal voltage)
├── Shorted cell may get hot during charging
├── Measure individual cell resistance (should not be 0Ω)

SOLUTIONS:
├── For single cell in pack: Replace entire pack (can't replace one)
├── For single cell: Recycle (cannot repair)
├── Attempt "zapping" (high current pulse) for large cells
│   └── DANGEROUS – can cause explosion
├── For safety: Dispose of shorted NiCd properly

WARNING: Short cell can overheat and vent toxic cadmium fumes!
Dispose immediately if shorted.
```

### Problem 4: Reverse Polarity (In Pack)

```
SYMPTOMS:
├── Multi-cell pack voltage lower than expected
├── Pack won't charge (charger error)
├── One cell reversed polarity (-0.5V to -1.0V)
├── Cell(s) hot during charging
├── Device runs for very short time

CAUSES:
├── Deep discharging pack (cell runs out first)
├── Cell mismatch (capacity differences)
├── Old battery (one cell weaker than others)
├── Continuing to use when one cell is dead
├── Charging polarity reversed (improper connection)

DIAGNOSIS:
├── Measure each cell voltage individually
├── Reversed cell: Negative voltage (e.g., -0.3V)
├── Other cells may be overcharged (high voltage)
└── Reverse cell likely permanently damaged

SOLUTIONS:
├── Replace entire pack (cannot fix single cell)
├── For large industrial packs: Replace cell (requires matching)
├── Dispose of reversed cells (hazardous waste)
├── Prevent by: Stop using at first sign of low power
├── Use low voltage cutoff protection

PREVENTION:
├── Stop using device when performance drops
├── Don't "push" when battery is clearly dead
├── Use matched cells in packs (same brand, age, capacity)
├── Implement low voltage cutoff in device (1.0V per cell)
```

## NiCd Disposal and Recycling

```
NiCd DISPOSAL REQUIREMENTS

    TOXICITY:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Cadmium is HIGHLY TOXIC!                                 │
    │                                                             │
    │   Health effects:                                           │
    │   ├── Carcinogenic (causes lung cancer)                    │
    │   ├── Kidney damage                                        │
    │   ├── Bone damage (Itai-itai disease)                     │
    │   ├── Lung damage                                          │
    │   └── Environmental persistence (50+ years)               │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    LEGAL STATUS:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   EU: Banned in consumer products (NiCd Directive)        │
    │   USA: Must be recycled (Universal Waste)                  │
    │   Canada: Hazardous waste, banned from landfills          │
    │   Many countries: Illegal to throw in trash               │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    RECYCLING LOCATIONS:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   US/Canada:                                                │
    │   ├── Call2Recycle (800-822-8837)                         │
    │   ├── Batteries Plus                                      │
    │   ├── Home Depot (some locations)                         │
    │   ├── Lowe's (some locations)                             │
    │   ├── Best Buy (some locations)                           │
    │   ├── Local hazardous waste facility                      │
    │   └── (Call ahead – not all accept NiCd)                  │
    │                                                             │
    │   Recycling process:                                       │
    │   ├── Cadmium recovered (99% recycled)                    │
    │   ├── Nickel recovered                                    │
    │   ├── Steel recovered                                     │
    │   └── Electrolyte neutralized                             │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    PREPARING FOR RECYCLING:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ✓ Fully discharge (if possible – use resistor)          │
    │   ✓ Tape terminals (electrical tape)                       │
    │   ✓ Place in separate bag (prevent shorts)                │
    │   ✓ Take to recycler within 30 days                       │
    │   ✗ Never throw in trash (illegal & toxic)                │
    │   ✗ Never burn (toxic fumes)                              │
    │   ✗ Never landfill (groundwater contamination)            │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

## Quick Reference Table

| Parameter | Value | Notes |
|-----------|-------|-------|
| Nominal voltage | 1.2V per cell | 1.2V stable during discharge |
| Full charge | 1.4-1.45V | Drops to 1.35V after rest |
| Discharge cutoff | 1.0V | Below 0.8V = damage |
| Energy density | 40-60 Wh/kg | Poor compared to modern |
| Cycle life | 500-1000 | Excellent for NiCd |
| Self-discharge | 15-20%/month | High (store discharged) |
| Memory effect | YES (severe) | Requires full discharge |
| High-rate discharge | Excellent | 10-20C possible |
| Temperature range | -40°C to +60°C | Widest of any rechargeable |
| Toxicity | HIGH (cadmium) | Must recycle |
| Cost | $ | Low |

## Summary

1. **Nickel-Cadmium (NiCd)** is the oldest rechargeable battery (invented 1899)

2. **Nominal voltage:** 1.2V (full 1.4V, cutoff 1.0V)

3. **Very flat discharge curve** – holds 1.2V for most of runtime

4. **Excellent high-rate discharge** – 10-20C continuous (unique advantage)

5. **Widest temperature range** -40°C to +60°C (aviation, outdoor)

6. **Long cycle life** 500-1000 cycles (excellent durability)

7. **Memory effect is SEVERE** – requires periodic full discharge

8. **Prevent memory effect:** Run device until it stops every 10-20 cycles

9. **Fix memory effect:** 2-3 full discharge/charge cycles or reconditioning

10. **Charging methods:** C/10 overnight (timer), C/4-1C fast (-ΔV detection)

11. **Trickle charge** C/20-C/30 safe for maintenance

12. **Self-discharge:** 15-20% per month (store DISCHARGED, unlike NiMH)

13. **Energy density:** Very poor (40-60 Wh/kg) – heavy for capacity

14. **Cadmium is HIGHLY TOXIC** – MUST recycle (illegal to trash)

15. **Banned in EU** for consumer products, restricted elsewhere

16. **Still used in:** Aviation, industrial, emergency systems (temperature range, reliability)

17. **Consumer use dying** – replaced by NiMH (higher capacity, less toxic) and Li-ion

18. **Recycle NiCd:** Call2Recycle, Batteries Plus, hazardous waste (never trash!)

*This documentation belongs to https://github.com/InterCentury*