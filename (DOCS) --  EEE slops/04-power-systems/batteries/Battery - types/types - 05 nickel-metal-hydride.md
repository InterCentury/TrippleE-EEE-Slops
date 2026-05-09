# Types - 05: Nickel-Metal Hydride (NiMH) Battery

## What is a Nickel-Metal Hydride Battery?

The nickel-metal hydride (NiMH) battery is a rechargeable battery that uses a nickel oxide hydroxide positive electrode and a hydrogen-absorbing alloy negative electrode. It was developed as a replacement for toxic NiCd batteries, offering higher capacity and reduced environmental impact.

NiMH batteries were commercialized in the late 1980s and became the dominant rechargeable battery for consumer electronics throughout the 1990s and 2000s. They powered early digital cameras, portable CD players, and the first generation of hybrid vehicles (Toyota Prius). While largely replaced by Li-ion for high-energy applications, NiMH remains popular for AA/AAA rechargeable batteries, hybrid vehicles, and applications where safety and cost outweigh energy density.

## Basic Chemistry and Construction

### How NiMH Batteries Work

NiMH batteries store energy through the movement of hydrogen ions (protons) between electrodes.

```
NICKEL-METAL HYDRIDE CHEMISTRY

    DISCHARGE REACTION:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Positive: NiOOH + H₂O + e⁻ → Ni(OH)₂ + OH⁻              │
    │   Negative: MH + OH⁻ → M + H₂O + e⁻                       │
    │   Overall: NiOOH + MH → Ni(OH)₂ + M                       │
    │                                                             │
    │   Where M = metal alloy (hydrogen storage)                │
    │         MH = metal hydride (hydrogen absorbed)            │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    CHARGE REACTION (reverse):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Ni(OH)₂ + M → NiOOH + MH                                │
    │                                                             │
    │   Hydrogen moves from positive to negative electrode       │
    │   (stored in metal alloy)                                 │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    KEY CHARACTERISTICS:

    ├── Nominal cell voltage: 1.2V (same as NiCd)
    ├── Full charge voltage: 1.4-1.45V
    ├── Discharge cutoff: 1.0V (per cell)
    ├── Higher capacity than NiCd (2-3×)
    ├── Less toxic than NiCd (no cadmium)
    ├── Mild memory effect (much less than NiCd)
    ├── Higher self-discharge than Li-ion (but LSD improved)
    └── Good high-rate discharge (5-10C typical)
```

### Physical Construction

```
NiMH BATTERY CONSTRUCTION (Cylindrical)

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ┌─────────────────────────────────────────────────────┐   │
    │   │  ┌─────────────────────────────────────────────┐    │   │
    │   │  │                                             │    │   │
    │   │  │   Positive terminal (+)                     │    │   │
    │   │  │   (with safety vent)                       │    │   │
    │   │  └─────────────────────────────────────────────┘    │   │
    │   │                                                     │   │
    │   │  ┌─────────────────────────────────────────────┐    │   │
    │   │  │  ████████████████████████████████████████   │    │   │
    │   │  │  ██   Sealing plate                     ██   │    │   │
    │   │  │  ██   (safety vent)                     ██   │    │   │
    │   │  │  ████████████████████████████████████████   │    │   │
    │   │  └─────────────────────────────────────────────┘    │   │
    │   │                                                     │   │
    │   │  ┌─────────────────────────────────────────────┐    │   │
    │   │  │  ████████████████████████████████████████   │    │   │
    │   │  │  ██   Positive electrode (nickel)      ██   │    │   │
    │   │  │  ██   (Ni(OH)₂ / NiOOH)                ██   │    │   │
    │   │  │  ██   on foam or sintered plate        ██   │    │   │
    │   │  │  ████████████████████████████████████████   │    │   │
    │   │  └─────────────────────────────────────────────┘    │   │
    │   │                                                     │   │
    │   │  ┌─────────────────────────────────────────────┐    │   │
    │   │  │  ████████████████████████████████████████   │    │   │
    │   │  │  ██   Separator (nylon/polypropylene) ██   │    │   │
    │   │  │  ██   (soaked in KOH electrolyte)      ██   │    │   │
    │   │  │  ████████████████████████████████████████   │    │   │
    │   │  └─────────────────────────────────────────────┘    │   │
    │   │                                                     │   │
    │   │  ┌─────────────────────────────────────────────┐    │   │
    │   │  │  ████████████████████████████████████████   │    │   │
    │   │  │  ██   Negative electrode (MH)          ██   │    │   │
    │   │  │  ██   (hydrogen-absorbing alloy)       ██   │    │   │
    │   │  │  ██   (rare earth + nickel)            ██   │    │   │
    │   │  │  ████████████████████████████████████████   │    │   │
    │   │  └─────────────────────────────────────────────┘    │   │
    │   │                                                     │   │
    │   │  Negative terminal (-)                              │   │
    │   │  (case / can)                                       │   │
    │   │                                                     │   │
    │   └─────────────────────────────────────────────────────┘   │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    NEGATIVE ELECTRODE ALLOYS:

    Alloy Type                  Composition                    Use
    ──────────────────────────────────────────────────────────────
    AB5 (Misch metal)           LaNi₅ (with Co, Mn, Al)       Most common
    AB2 (Laves phase)           ZrNi₂, TiNi₂                   High capacity
    A2B7                         (rare earth)                  LSD NiMH
    Superlattice                 Advanced rare earth           Highest capacity
```

## NiMH Specifications

### Voltage

NiMH shares the same voltage characteristics as NiCd (1.2V nominal).

```
NiMH VOLTAGE CHARACTERISTICS

    Individual cell (1.2V nominal):

    State              Voltage        Notes
    ──────────────────────────────────────────────────────────────
    Fresh off charger  1.4-1.45V      Right after charge
    Resting (full)     1.35-1.40V     After 10-30 minutes
    Nominal            1.2V           During most of discharge
    Under load (heavy) 1.0-1.1V       Normal (similar to NiCd)
    Discharge cutoff   1.0V           End of useful capacity
    Deep discharge     <0.8V          Damage risk (reversal)
    Fully dead         0V             Shorted cell


    DISCHARGE CURVE (Similar to NiCd but steeper at end):

    Voltage (V)
        │
    1.5 ┼●───────────────────────────────────────────────────────
        │ ╲
    1.4 ┼  ╲
        │   ╲
    1.3 ┼    ╲
        │     ╲
    1.2 ┼      ●═════════════════════════════════════════●
        │                                            ╱  │
    1.1 ┼                                          ╱
        │                                        ╱
    1.0 ┼                                      ●
        │                                    ╱
    0.9 ┼                                  ●
        │
        └────────────────────────────────────────────────► Time
         0%        25%        50%        75%       100%

    Slightly sloping plateau (less flat than NiCd)
    Sharper voltage drop at end (easier to detect empty)
```

### Capacity

NiMH offers significantly higher capacity than NiCd.

```
NiMH CAPACITY (Typical, 2024)

    Size          Low Capacity    Standard      High Capacity    LSD (Low Self-Discharge)
    ──────────────────────────────────────────────────────────────────────────────────
    AAA           500-600 mAh     800-900 mAh   1000-1150 mAh    800-900 mAh
    AA            1500-1800 mAh   2000-2500 mAh 2700-2800 mAh    1900-2000 mAh
    C             3000-4000 mAh   4500-5000 mAh 5500-6000 mAh    4000-4500 mAh
    D             4000-6000 mAh   8000-9000 mAh 10000-12000 mAh   8000-9000 mAh
    9V (7-cell)   150-200 mAh     250-300 mAh   -                200-250 mAh
    Prismatic     Varies          Varies        Varies            Varies


    CAPACITY COMPARISON (AA size):

    Battery Type                Typical Capacity    Notes
    ──────────────────────────────────────────────────────────────
    NiCd                        600-1000 mAh        Low energy
    NiMH (standard)             2000-2500 mAh       Good (disappears in months)
    NiMH (LSD / Eneloop)        1900-2000 mAh       Excellent (holds charge years)
    NiMH (high capacity)        2700-2800 mAh       Very high (disappears quickly)
    Alkaline (primary)          2800-3000 mAh       Not rechargeable
    Lithium primary             3000-3500 mAh       Not rechargeable


    STANDARD vs LSD NiMH:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Standard NiMH (e.g., generic 2500mAh):                   │
    │   ├── Higher capacity (2500mAh)                            │
    │   ├── High self-discharge (20-30% in first 24 hours!)     │
    │   ├── Los es 50% in 1-2 months                            │
    │   └── Best for: Frequent use (weekly charging)            │
    │                                                             │
    │   LSD NiMH (e.g., Eneloop, 1900-2000mAh):                 │
    │   ├── Lower capacity (1900-2000mAh)                       │
    │   ├── Very low self-discharge (70-85% after 1 YEAR)       │
    │   ├── Ready to use (even after long storage)              │
    │   └── Best for: Emergencies, flashlights, remotes         │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

### Self-Discharge

NiMH is known for high self-discharge, but LSD versions solved this.

```
SELF-DISCHARGE RATES

    STANDARD NiMH (room temperature):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Time after charge    Remaining Capacity                  │
    │   ──────────────────────────────────────────────────────────│
    │   Fresh off charger    100%                                │
    │   After 24 hours       70-80%  (biggest loss!)            │
    │   After 1 week         60-70%                              │
    │   After 1 month        50-60%                              │
    │   After 3 months       30-40%                              │
    │   After 6 months       20-30%                              │
    │   After 1 year         <20%                                │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    LSD (Low Self-Discharge) NiMH (e.g., Eneloop):

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Time after charge    Remaining Capacity                  │
    │   ──────────────────────────────────────────────────────────│
    │   Fresh off charger    100%                                │
    │   After 1 month        90-95%                              │
    │   After 3 months       85-90%                              │
    │   After 6 months       80-85%                              │
    │   After 1 year         75-80% (claimed)                    │
    │   After 5 years        50-60% (real world)                 │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    LOSS VS TEMPERATURE:

    Temperature    Self-Discharge Rate (Standard NiMH)
    ──────────────────────────────────────────────────────────────
    0°C (32°F)     5-10% per month (best)
    20°C (68°F)    15-25% per month (normal)
    30°C (86°F)    25-35% per month
    40°C (104°F)   35-50% per month (severe)

    LSD NiMH affected less by temperature (still best kept cool)
```

## NiMH vs NiCd vs Alkaline vs Li-ion

### Comprehensive Comparison

```
BATTERY TYPE COMPARISON (AA size)

    Feature                 NiMH (LSD)    NiMH (std)    NiCd        Alkaline    Li-ion (14500)
    ───────────────────────────────────────────────────────────────────────────────────────
    Nominal voltage         1.2V          1.2V          1.2V        1.5V        3.6-3.7V
    Full charge voltage     1.45V         1.45V         1.45V       1.65V       4.2V
    Capacity (mAh)          1900-2000     2000-2800     600-1000    2800-3000   600-900
    Energy density (Wh/kg)  60-100        80-120        40-60       130-150     150-200
    Rechargeable            Yes           Yes           Yes         No          Yes
    Cycle life              500-1000      300-500       500-1000    N/A         300-500
    Self-discharge          Very low      High          High        Very low    Low
    Memory effect           Mild          Mild          Severe      N/A         None
    High-rate discharge     Good          Good          Excellent   Poor        Good
    Temperature range       -20 to 50°C   -20 to 50°C   -40 to 60°C -20 to 50°C -20 to 60°C
    Toxicity                Low           Low           High        Low         Moderate
    Cost per cell           $$            $             $           $           $$$
    Best for                Remotes,      High drain    Power       Clocks,     Flashlights,
                            flashlights   devices       tools       remotes     high power


    VOLTAGE COMPATIBILITY WARNING:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   NiMH (1.2V) vs Alkaline (1.5V):                          │
    │                                                             │
    │   Most devices designed for alkaline WILL work with NiMH  │
    │   (1.2V vs 1.5V). The device may think battery is low     │
    │   earlier (when NiMH hits 1.0V, alkaline still at 1.2V)   │
    │                                                             │
    │   Some devices (clocks, some flashlights) may NOT work    │
    │   properly with NiMH (voltage too low). Test first!       │
    │                                                             │
    │   NEVER replace alkaline with Li-ion 14500 (3.7V)!        │
    │   That will DESTROY the device (overvoltage).             │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

## LSD (Low Self-Discharge) NiMH

### What Makes LSD Different

The most important innovation in NiMH technology.

```
LSD NiMH EXPLANATION

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Traditional NiMH:                                         │
    │   ├── Standard separator                                    │
    │   ├── High self-discharge (20-30% in first day)            │
    │   ├── Useless after 6 months on shelf                      │
    │   └── Cheap                                                │
    │                                                             │
    │   LSD NiMH (e.g., Eneloop, Fujitsu, IKEA LADDA):          │
    │   ├── Improved separator (thicker, better material)        │
    │   ├── Superior electrode alloys                            │
    │   ├── Very low self-discharge (15% per YEAR)              │
    │   ├── Ready to use after years in drawer                  │
    │   ├── Slightly lower capacity (1900-2000 vs 2500)         │
    │   ├── Longer cycle life (2000+ cycles claimed)            │
    │   └── More expensive                                     │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    LSD NOMENCLATURE:

    ├── Eneloop (Panasonic) – the original (2005)
    ├── Fujitsu (same factory as older Eneloop)
    ├── IKEA LADDA (Eneloop Pro equivalent, white = standard)
    ├── AmazonBasics (varies, older were Eneloop)
    ├── Duracell Rechargeable (some LSD, some not)
    └── EBL, Tenergy (true LSD? varies by model)


    CAPACITY vs SELF-DISCHARGE TRADEOFF:

    Type                Capacity    Self-discharge/month    Best for
    ──────────────────────────────────────────────────────────────
    Eneloop (white)     2000mAh     <1% per month           General (best balance)
    Eneloop Pro (black) 2550mAh     ~3-5% per month         High drain (cameras)
    Standard NiMH       2500mAh     20-30% first day!       Daily use only
    AmazonBasics 2400   2400mAh     ~5-10% per month        Budget LSD
    IKEA LADDA 2450     2450mAh     ~5% per month           Eneloop Pro equivalent

    For most users: Eneloop white (2000mAh) is the best choice.
    For high-drain: Eneloop Pro (2550mAh) but loses charge faster.
```

## NiMH Applications

### Consumer Electronics (AA/AAA)

The most common use for NiMH today.

```
CONSUMER NiMH APPLICATIONS

    REMOTE CONTROLS:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Best: LSD NiMH (Eneloop)                                 │
    │   Reason: Low drain, needs long standby time               │
    │   Runtime: 6-12 months (with LSD)                         │
    │   Works: Yes (1.2V vs 1.5V usually fine)                  │
    │   Recommendation: Recharge once per year                  │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    FLASHLIGHTS:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Best: LSD NiMH (Eneloop) or Standard (daily use)         │
    │   Reason: High drain, frequent use                         │
    │   Advantage: Works well in cold (better than alkaline)     │
    │   Runtime: 1-4 hours (depending on brightness)             │
    │   Warning: Some flashlights need 1.5V (test first)        │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    DIGITAL CAMERAS (High drain):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Best: High capacity (Eneloop Pro, 2550mAh)               │
    │   Reason: Very high drain (flash, motor, screen)          │
    │   Advantage: NiMH handles high current better than alkaline│
    │   Runtime: 200-500 shots (vs 50-100 with alkaline)        │
    │   Note: Standard LSD 2000mAh also works well              │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    GAME CONTROLLERS:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Best: LSD NiMH (Eneloop)                                 │
    │   Reason: Moderate drain, wants long runtime              │
    │   Runtime: 15-30 hours (Xbox/PlayStation)                  │
    │   Advantage: Cheaper than buying batteries constantly     │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    CLOCKS / LOW DRAIN DEVICES:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Best: LSD NiMH (Eneloop) or use disposable alkaline      │
    │   Reason: Very low drain (1-10mA)                          │
    │   LSD NiMH lasts 1-2 years between charges                │
    │   Alkaline lasts 3-5 years                                │
    │   Caution: Some clocks don't work on 1.2V                 │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

### Hybrid Electric Vehicles (HEV)

NiMH dominates HEV batteries (Toyota Prius).

```
HEV NiMH BATTERY PACKS

    TOYOTA PRIUS (Gen 1-4):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Chemistry: NiMH (Panasonic)                              │
    │   Configuration: 28 modules x 6 cells = 168 cells          │
    │   Voltage: 201.6V nominal (1.2V × 168)                    │
    │   Capacity: 6.5Ah (Gen 3)                                 │
    │   Energy: 1.3 kWh                                          │
    │   Weight: 40-45 kg (88-100 lbs)                           │
    │   Life: 10-15 years / 150,000-200,000 miles                │
    │   Cycle life: 10,000+ shallow cycles (HEV use)            │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    WHY NiMH FOR HYBRIDS (not Li-ion initially):

    ├── Safe (no thermal runaway, stable chemistry)
    ├── Long life (10+ years in HEV use)
    ├── Tolerant of shallow cycling (HEV never deep cycles)
    ├── Wide temperature range (-30°C to +50°C)
    ├── Less expensive than early Li-ion
    ├── Proven reliability (millions of Prius sold)
    └── Simple management (no complex BMS needed)


    LATEST GENERATION (Prius Gen 5, 2024):

    ├── Some use Li-ion (higher energy density)
    ├── NiMH still used in base models
    ├── NiMH for cold climates (better cold performance)
    └── Li-ion for higher efficiency (lower weight)
```

## Charging NiMH Batteries

### Charging Methods

Unlike NiCd, NiMH requires more careful charging.

```
NiMH CHARGING METHODS

    METHOD 1: Slow Charging (C/10, 10-16 hours):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Rate: 0.1C (10-hour rate)                               │
    │   Time: 14-16 hours                                        │
    │   Termination: Timer (no -ΔV detection for NiMH)          │
    │   Safe: Yes (can be left, but not recommended)            │
    │   Use: General purpose, simple chargers                   │
    │                                                             │
    │   Note: NiMH can tolerate C/10 overcharge (some heat)     │
    │   Better than NiCd (less gas generation)                  │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    METHOD 2: Fast Charging (0.3C to 1C):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Rate: 0.3C to 1C                                         │
    │   Time: 1-3 hours                                          │
    │   Termination: -ΔV detection (smaller drop than NiCd)     │
    │   Backup: dT/dt (temperature rise rate)                    │
    │   Backup 2: Absolute temperature cut-off (50°C)           │
    │   Use: Smart chargers                                     │
    │                                                             │
    │   -ΔV for NiMH: 5-10mV per cell (NiCd: 10-30mV)          │
    │   (Smaller drop – harder to detect)                        │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    METHOD 3: dT/dt Termination (Best for NiMH):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   NiMH temperature rises sharply at full charge            │
    │   Detect rate of change: dT/dt > 1°C per minute           │
    │   More reliable than -ΔV for NiMH                         │
    │   Requires temperature sensor (thermistor)                 │
    │   Used in high-end chargers (Opus, SkyRC)                  │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    METHOD 4: Trickle Charge (Maintenance):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Rate: C/20 to C/50 (very low)                           │
    │   Safe for LSD NiMH: Yes (but not needed)                  │
    │   Safe for standard NiMH: Possibly (monitor temperature)  │
    │   Note: NiMH does NOT handle continuous trickle well      │
    │   Better to charge when needed, not float                │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

### NiMH Charging Rules

```
NiMH CHARGING GUIDELINES

    DO:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ✓ Use NiMH-specific charger (or smart charger)           │
    │   ✓ Use slow charge (C/10) if unsure                      │
    │   ✓ Use temperature monitoring for fast charging          │
    │   ✓ Charge at room temperature (10-30°C)                   │
    │   ✓ Use LSD NiMH for emergency applications               │
    │   ✓ Store charged (unlike NiCd)                           │
    │   ✓ Use smart charger with individual cell monitoring     │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    DON'T:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ✗ Never trickle charge at >C/20 (causes damage)          │
    │   ✗ Never charge frozen battery                            │
    │   ✗ Never overcharge (causes heat, venting, capacity loss) │
    │   ✗ Never use NiCd charger without -ΔV detection          │
    │   ✗ Never charge at >1C unless battery rated              │
    │   ✗ Don't leave on trickle for weeks (unlike NiCd)        │
    │   ✗ Never reverse charge (destroy battery)                 │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    CHARGING TIME TABLE:

    Charge Rate    Charging Time    Termination Method           Safety
    ────────────────────────────────────────────────────────────────────
    C/10           14-16 hours      Timer                         Good
    C/5            6-8 hours        Timer or -ΔV                  Good
    C/3 (0.33C)    3.5-4 hours      -ΔV + temperature            Good
    0.5C           2-2.5 hours      -ΔV + temperature + timer    Fair
    1C             1-1.5 hours      -ΔV + temperature + timer    Risky

    For longest life: Charge at 0.3-0.5C (3-4 hours)
    For fastest charge: Use rated fast-charge cells only
```

## NiMH vs Li-ion for AA/AAA

### Which Should You Choose?

```
NiMH vs Li-ion 14500 (AA-sized Li-ion)

    Feature                 NiMH AA (1.2V)      Li-ion 14500 (3.7V)
    ──────────────────────────────────────────────────────────────
    Voltage                 1.2V                3.7V (NOT COMPATIBLE!)
    Capacity (mAh)          2000-2800           600-900
    Energy (Wh)             2.4-3.4 Wh          2.2-3.3 Wh (similar)
    Weight                  26-30g              18-20g (lighter)
    Cycle life              500-1000            300-500
    Self-discharge          Low (LSD)           Low
    Safety                  Very safe            Moderate (BMS required)
    Cost per cell           $2-4                $4-6
    Device compatibility    Most 1.5V devices   ONLY 3.7V devices

    WARNING: Li-ion 14500 is NOT a replacement for AA!
    3.7V will destroy devices designed for 1.5V alkaline/1.2V NiMH.
    Only use in devices specifically designed for 3.7V.

    VERDICT for AA/AAA replacements:
    ├── For most devices: NiMH (Eneloop) is best choice
    ├── For high-drain (camera flash): NiMH or Li-ion (if compatible)
    ├── For emergency (flashlights): LSD NiMH
    └── For 1.5V devices that need 1.5V: Use alkaline or LiFePO4 + dummy cell
```

## Common NiMH Problems

### Problem 1: High Self-Discharge (Standard NiMH)

```
SYMPTOMS:
├── Battery dead after a few weeks (not used)
├── Device doesn't work when picked up
├── Voltage normal after charging, low next day

CAUSES:
├── Normal for standard NiMH (20-30% loss first day)
├── High temperature storage
├── Old battery (aged separator)
├── Overcharged (damaged separator)

DIAGNOSIS:
├── Check self-discharge rate (measure voltage daily)
├── Normal standard NiMH: 30% loss in 24 hours
├── Problematic: >50% loss in 24 hours
├── Compare to known good battery

SOLUTIONS:
├── For standard NiMH: Accept (that's how they work)
├── Switch to LSD NiMH (Eneloop) for emergency use
├── Store in refrigerator (slows self-discharge)
├── If >50% loss in 24 hours: Battery is failing (replace)
├── Use charger with refresh mode (may help)
```

### Problem 2: Device Thinks Battery is Low

```
SYMPTOMS:
├── Device shows low battery warning (but NiMH is full)
├── Device shuts off early (before battery empty)
├── Runs fine on alkaline, but not on NiMH

CAUSES:
├── NiMH voltage (1.2V) lower than alkaline (1.5V)
├── Device designed for alkaline voltage
├── Device cutoff voltage too high (e.g., 1.2V per cell)
├── Some devices expect 1.5V as "full"

DIAGNOSIS:
├── Check device type (clocks, some flashlights problematic)
├── Measure NiMH voltage when device shows "low"
├── Try different brand NiMH (some have higher voltage)
├── Test with known good device

SOLUTIONS:
├── For clocks: Use alkaline (NiMH not suitable)
├── For flashlights: Try Li-ion (if compatible) or accept
├── Use "high voltage" NiMH (some brands slightly higher)
├── Modify device (if experienced) to lower cutoff
├── Accept shorter runtime (device thinks battery low earlier)

DEVICE COMPATIBILITY TABLE:

    Device Type              Works with NiMH?    Notes
    ──────────────────────────────────────────────────────────────
    Digital camera          YES                 Better than alkaline!
    Flashlight              Usually             Some need 1.5V
    Remote control          YES                 Most work fine
    Clock                   Sometimes           Test first
    Mouse/keyboard          YES                 Works well
    Wireless headset        YES                 Good
    Smoke detector          NOT RECOMMENDED     Use alkaline
    Medical device          Check manual        Some require alkaline
```

### Problem 3: Memory Effect (Mild)

```
SYMPTOMS:
├── Slightly reduced capacity after many partial discharges
├── Not as severe as NiCd
├── Voltage depression (voltage dips early)
├── Device runtime gradually decreases

CAUSES:
├── Repeated partial discharges (e.g., always 50%)
├── Same cause as NiCd, but MUCH less severe
├── Some chemistries more prone than others
├── More noticeable in older NiMH

DIAGNOSIS:
├── Compare runtime to new battery
├── Perform full discharge/charge cycle
├── If runtime improves: memory effect present

SOLUTIONS:
├── Perform 1-3 full discharge/charge cycles
├── Use smart charger with refresh mode
├── Prevention: occasional full discharge
├── Unlike NiCd, NiMH rarely needs this
├── LSD NiMH (Eneloop) almost immune

PREVENTION:
├── Occasionally run device until it stops
├── Use refresh cycle on charger every 10-20 cycles
├── For most users: not a significant issue
```

### Problem 4: Won't Charge / Charger Rejects

```
SYMPTOMS:
├── Charger shows error (blinking light)
├── Battery voltage 0V (or very low)
├── Charger refuses to start charging
├── Battery gets hot immediately (reject)

CAUSES:
├── Deep discharge (cell voltage <0.5V)
├── Over-discharge (reversed cell in pack)
├── Cell shorted (0V)
├── Charger cannot detect battery (voltage too low)
├── Damaged separator

DIAGNOSIS:
├── Measure cell voltage
├── 0.8-1.0V: Deep discharged but recoverable
├── 0.5-0.8V: Possibly recoverable
├── <0.5V: Likely damaged
├── 0V: Shorted cell (replace)

SOLUTIONS (for deep discharge <0.8V):
├── Try charger with "revive" mode (some smart chargers)
├── Apply low current (C/20) manually until voltage rises
├── Method: Use USB cable + resistor (100Ω) for 1-2 hours
├── Once above 1.0V, normal charger should work
├── If still won't charge after revive: Replace battery

WARNING: Severely over-discharged NiMH may have internal damage.
If battery gets hot during revive attempt: STOP (danger).
```

## NiMH Disposal and Recycling

```
NiMH DISPOSAL REQUIREMENTS

    TOXICITY:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   NiMH is MUCH LESS TOXIC than NiCd                         │
    │   No cadmium (carcinogen)                                  │
    │   Contains nickel (allergy risk, but not toxic)            │
    │   Contains rare earth metals (not hazardous)               │
    │   Electrolyte (KOH) is caustic but not toxic               │
    │                                                             │
    │   Still should be recycled (valuable materials)            │
    │   Not hazardous waste in most countries                    │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    RECYCLING STATUS:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   US: Not regulated as hazardous waste                     │
    │   US: Encouraged to recycle (Call2Recycle)                 │
    │   EU: Must recycle (Battery Directive)                     │
    │   Some states: Can trash (not recommended)                 │
    │                                                             │
    │   Best practice: ALWAYS recycle (recovers nickel)          │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    RECYCLING LOCATIONS:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   US/Canada:                                                │
    │   ├── Call2Recycle (800-822-8837) – FREE                   │
    │   ├── Best Buy                                             │
    │   ├── Home Depot                                           │
    │   ├── Lowe's                                               │
    │   ├── Staples                                              │
    │   ├── Batteries Plus                                      │
    │   └── Some local recycling centers                         │
    │                                                             │
    │   PREPARATION:                                              │
    │   ├── No need to discharge (safe to recycle charged)      │
    │   ├── Tape terminals (prevent shorts)                      │
    │   └── Place in separate bag                                │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

## Quick Reference Table

| Parameter | Standard NiMH | LSD NiMH (Eneloop) | NiCd (for comparison) |
|-----------|---------------|---------------------|----------------------|
| Nominal voltage | 1.2V | 1.2V | 1.2V |
| Full charge | 1.45V | 1.45V | 1.45V |
| Capacity (AA) | 2000-2800 mAh | 1900-2000 mAh | 600-1000 mAh |
| Energy density | 80-120 Wh/kg | 60-100 Wh/kg | 40-60 Wh/kg |
| Cycle life | 300-500 | 500-1000+ | 500-1000 |
| Self-discharge (1 mo) | 40-50% | 5-10% | 15-25% |
| Self-discharge (1 yr) | 70-80% | 20-25% | 50-60% |
| Memory effect | Mild | Very mild | Severe |
| High-rate discharge | Good | Good | Excellent |
| Temperature range | -20 to 50°C | -20 to 50°C | -40 to 60°C |
| Toxicity | Low | Low | High |
| Cost | $ | $$ | $ |
| Best for | High drain daily | Emergencies, remotes | High power, cold |

## Summary

1. **Nickel-Metal Hydride (NiMH)** replaced NiCd with higher capacity and less toxicity

2. **Nominal voltage:** 1.2V (same as NiCd, lower than alkaline 1.5V)

3. **Higher capacity than NiCd:** AA 2000-2800mAh vs 600-1000mAh (2-3×)

4. **Standard NiMH:** High self-discharge (20-30% in first day!) – good for frequent use

5. **LSD NiMH (Eneloop):** Low self-discharge (70-85% after 1 year) – revolutionary

6. **LSD uses:** Emergency lights, remotes, clocks, anything needing standby

7. **Eneloop (Panasonic)** is the gold standard (2005 invention) – 2000mAh, 2000+ cycles

8. **Eneloop Pro:** 2550mAh (higher capacity), 500 cycles, higher self-discharge

9. **Memory effect:** Mild (unlike NiCd), not a significant issue for most users

10. **No cadmium** – much less toxic, easier disposal (recycle encouraged)

11. **Charging:** Needs -ΔV or dT/dt detection (smaller voltage drop than NiCd)

12. **Do not trickle charge** NiMH (>C/20 damages cells) – unlike NiCd

13. **Compatibility:** Most 1.5V devices work with 1.2V NiMH (except clocks, some flashlights)

14. **HEV use:** Toyota Prius uses NiMH (proven reliability, 10+ years, safe)

15. **Cold performance:** Good (better than Li-ion below 0°C)

16. **High-rate discharge:** Good (5-10C) – works for digital cameras, power tools

17. **Store charged** (unlike NiCd) – LSD holds charge for years

18. **Recycle NiMH** at Call2Recycle, Best Buy, Home Depot (recovers nickel)

19. **Do not replace alkaline with Li-ion 14500 (3.7V)** – will destroy device!

20. **For most AA/AAA users: Eneloop (white) is the best choice**

*This documentation belongs to https://github.com/InterCentury*