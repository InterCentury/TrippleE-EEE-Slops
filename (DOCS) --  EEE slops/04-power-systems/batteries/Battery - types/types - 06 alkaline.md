# Types - 06: Alkaline Battery

## What is an Alkaline Battery?

The alkaline battery is a primary (non-rechargeable) battery that uses zinc and manganese dioxide with an alkaline electrolyte (potassium hydroxide). It is the most common household battery, powering everything from remote controls and clocks to toys and flashlights.

Invented by Lewis Urry in the 1950s while working for Eveready (now Energizer), the alkaline battery was commercialized in the 1960s. It offered significantly higher capacity and longer shelf life than the earlier zinc-carbon batteries. Today, alkaline batteries dominate the primary battery market due to their low cost, high energy density, and excellent shelf life (5-10 years).

## Basic Chemistry and Construction

### How Alkaline Batteries Work

Alkaline batteries convert chemical energy to electrical energy through reactions between zinc and manganese dioxide in an alkaline electrolyte.

```
ALKALINE BATTERY CHEMISTRY

    DISCHARGE REACTION:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Positive: 2MnO₂ + H₂O + 2e⁻ → Mn₂O₃ + 2OH⁻                │
    │   Negative: Zn + 2OH⁻ → ZnO + H₂O + 2e⁻                     │
    │   Overall: Zn + 2MnO₂ → ZnO + Mn₂O₃                         │
    │                                                             │
    │   Electrolyte: KOH (potassium hydroxide)                    │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    KEY CHARACTERISTICS:

    ├── Nominal voltage: 1.5V (fresh)
    ├── Open circuit voltage: 1.55-1.65V
    ├── Cutoff voltage: 0.8-1.0V (device dependent)
    ├── High energy density (130-150 Wh/kg)
    ├── Excellent shelf life (5-10 years)
    ├── Non-rechargeable (attempting to recharge is dangerous!)
    ├── Low self-discharge (<1% per year)
    └── Sloping discharge curve (voltage gradually drops)
```

### Physical Construction

```
ALKALINE BATTERY CROSS-SECTION

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │                    Positive Terminal (+)                    │
    │                           ┌───┐                             │
    │                           │   │                             │
    │                           │ █ │  (steel cap with vent)      │
    │                           │ █ │                             │
    │                           └─┬─┘                             │
    │                             │                               │
    │   ┌─────────────────────────┼─────────────────────────┐     │
    │   │                         │                         │     │
    │   │  ██████████████████████████████████████████████   │     │
    │   │  ██              Steel Can                   ██   │     │
    │   │  ██          (Positive Terminal)             ██   │     │
    │   │  ██████████████████████████████████████████████   │     │
    │   │  ██                                          ██   │     │
    │   │  ██   ┌─────────────────────────────┐        ██   │     │
    │   │  ██   │  Cathode (Positive)         │        ██   │     │
    │   │  ██   │  MnO₂ (manganese dioxide)   │        ██   │     │
    │   │  ██   │  + carbon for conductivity  │        ██   │     │
    │   │  ██   │  (pressed against can)      │        ██   │     │
    │   │  ██   └─────────────────────────────┘        ██   │     │
    │   │  ██                                          ██   │     │
    │   │  ██   ┌─────────────────────────────┐        ██   │     │
    │   │  ██   │  Separator                  │        ██   │     │
    │   │  ██   │  (paper/fabric soaked       │        ██   │     │
    │   │  ██   │   in KOH electrolyte)       │        ██   │     │
    │   │  ██   └─────────────────────────────┘        ██   │     │
    │   │  ██                                          ██   │     │
    │   │  ██   ┌─────────────────────────────┐        ██   │     │
    │   │  ██   │  Anode (Negative)           │        ██   │     │
    │   │  ██   │  Zinc powder (gelled)       │        ██   │     │
    │   │  ██   │  mixed with KOH electrolyte │        ██   │     │
    │   │  ██   └─────────────────────────────┘        ██   │     │
    │   │  ██                                          ██   │     │
    │   │  ██   ┌─────────────────────────────┐        ██   │     │
    │   │  ██   │  Brass Current Collector    │        ██   │     │
    │   │  ██   │  (nail)                     │        ██   │     │
    │   │  ██   └─────────────────────────────┘        ██   │     │
    │   │  ██                                          ██   │     │
    │   │  ██████████████████████████████████████████████   │     │
    │   └─────────────────────────┬─────────────────────────┘     │
    │                             │                               │
    │                           ┌─┴─┐                             │
    │                           │ █ │  (steel cover with seal)    │
    │                           │ █ │                             │
    │                           └───┘                             │
    │                    Negative Terminal (-)                    │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    CONSTRUCTION NOTES:

    ├── Steel can is positive (+)
    ├── Bottom/center terminal is negative (-)
    ├── Zinc anode is in the center (gelled)
    ├── MnO₂ cathode is around the outside
    ├── Separator prevents internal short
    ├── Vent releases pressure (safety)
    └── Seals prevent leakage (when new)
```

## Alkaline Specifications

### Voltage

Alkaline battery voltage decreases gradually during discharge.

```
ALKALINE VOLTAGE CHARACTERISTICS (AA size, 500mA load)

    State of Charge    Open Circuit    Under Load    Notes
    ──────────────────────────────────────────────────────────────
    100% (fresh)       1.60-1.65V      1.50-1.55V    Brand new
    90%                1.55-1.60V      1.45-1.50V
    75%                1.50-1.55V      1.35-1.45V
    50%                1.45-1.50V      1.25-1.35V
    25%                1.35-1.45V      1.10-1.20V
    10%                1.25-1.35V      1.00-1.10V    Low warning
    5%                 1.15-1.25V      0.90-1.00V    End of useful life
    0% (dead)          <1.10V          <0.80V        Replace


    DISCHARGE CURVE (500mA constant current)

    Voltage (V)
        │
    1.6 ┼●
        │ ╲
    1.5 ┼  ╲
        │   ╲
    1.4 ┼    ╲
        │     ╲
    1.3 ┼      ╲
        │       ╲
    1.2 ┼        ╲
        │         ╲
    1.1 ┼          ╲
        │           ╲
    1.0 ┼            ●──────────────────────────────────────────
        │
    0.9 ┼
        │
        └────────────────────────────────────────────────► Time
         0%        25%        50%        75%       100%

    NOTE: Sloping discharge (unlike NiCd's flat plateau)
    Voltage gradually drops as battery depletes.
```

### Capacity

Alkaline batteries have good capacity but degrade at high discharge rates.

```
TYPICAL ALKALINE CAPACITIES (at 25°C, low drain 25mA)

    Size          Capacity (mAh)    Energy (Wh)    Equivalent NiMH
    ────────────────────────────────────────────────────────────────
    AAA           1000-1200         1.5-1.8        800-1100 mAh
    AA            2500-3000         3.8-4.5        2000-2800 mAh
    C             7000-8000         10.5-12.0      4500-6000 mAh
    D             15000-20000       22.5-30.0      8000-12000 mAh
    9V            400-600           3.6-5.4        200-300 mAh


    CAPACITY vs LOAD CURRENT (AA cell)

    Discharge Current    Capacity (mAh)    Relative    Typical Device
    ────────────────────────────────────────────────────────────────
    10 mA               2800-3000         100%        Remote, clock
    25 mA               2700-2900         95%         Mouse, radio
    100 mA              2500-2700         90%         LED light (low)
    250 mA              2000-2300         75%         Digital camera (old)
    500 mA              1500-1800         55%         Motor, high power
    1000 mA (1A)        800-1000          30%         High drain device
    2000 mA (2A)        300-500           15%         Very high drain (poor)

    NOTE: Alkaline performs POORLY at high drain (>500mA).
    For high-drain devices (cameras, motorized toys), use NiMH.
```

### Self-Discharge and Shelf Life

Alkaline batteries have excellent shelf life.

```
SHELF LIFE (at room temperature, 20-25°C)

    Time              Remaining Capacity    Notes
    ──────────────────────────────────────────────────────────────
    Fresh             100%                  Manufacture date
    1 year            95-97%                Very good
    2 years           90-95%                Still good
    3 years           85-90%                Acceptable
    5 years           75-85%                Most brands claim 10 years
    7 years           65-75%                May still work
    10 years          50-60%                End of useful life


    TEMPERATURE EFFECT ON SHELF LIFE

    Temperature       Loss per Year    Storage Life (to 80% capacity)
    ──────────────────────────────────────────────────────────────
    0°C (32°F)       <1%               20+ years
    20°C (68°F)      2-3%              8-10 years (typical)
    30°C (86°F)      5-8%              4-5 years
    40°C (104°F)     10-15%            2-3 years
    50°C (122°F)     20-30%            1 year

    NOTE: Hot cars in summer (>60°C) destroy alkaline quickly.
    A battery left on a dashboard can lose 50% capacity in days.
```

## Alkaline vs Other Primary Batteries

```
PRIMARY BATTERY COMPARISON (AA size)

    Feature                 Alkaline        Zinc-Carbon    Lithium (Li-FeS₂)
    ──────────────────────────────────────────────────────────────────────
    Nominal voltage         1.5V            1.5V           1.5V
    Fresh voltage           1.60-1.65V      1.55-1.60V     1.80V
    Capacity (low drain)    2800-3000 mAh   1000-1500 mAh  3000-3500 mAh
    Capacity (high drain)   Poor (30%)      Very poor       Excellent (90%)
    Energy density (Wh/kg)  130-150         60-80          260-300
    Shelf life (years)      5-10            2-3            15-20
    Temperature range       0 to 50°C       0 to 50°C      -40 to 60°C
    Cost per cell           $0.50-1.00      $0.20-0.50     $2.00-4.00
    Leakage risk            Moderate        Low            Very low
    Rechargeable?           NO              NO             NO

    Zinc-carbon (carbon-zinc): Older technology, lower capacity, cheap.
    Lithium primary (Li-FeS₂): Premium, high performance, long life.
```

## Alkaline Applications

### Suitable Devices

```
GOOD APPLICATIONS FOR ALKALINE

    LOW DRAIN (<100mA):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ✓ Remote controls (TV, AC, stereo)                        │
    │   ✓ Clocks (wall, alarm, desk)                              │
    │   ✓ Smoke detectors (change every 6 months)                 │
    │   ✓ Thermostats                                             │
    │   ✓ Wireless mice/keyboards                                 │
    │   ✓ Calculators                                             │
    │   ✓ Digital scales                                          │
    │   ✓ Blood pressure monitors                                 │
    │   ✓ Emergency flashlights (check regularly)                 │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    MEDIUM DRAIN (100-300mA):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ~ Radio (portable)                                        │
    │   ~ LED flashlight (low mode)                               │
    │   ~ Electric pencil sharpener                               │
    │   ~ Some toys (non-motorized)                               │
    │   ~ Shaver (travel size)                                    │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    POOR APPLICATIONS FOR ALKALINE (Use NiMH or Lithium)

    HIGH DRAIN (>300mA):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   X Digital cameras (flash and motor draw high current)    │
    │   X Motorized toys (RC cars, robots)                       │
    │   X High-power flashlights (over 200 lumens)               │
    │   X Portable gaming devices (Nintendo Switch, etc.)        │
    │   X Electric toothbrushes                                  │
    │   X Power tools (never – use NiMH or Li-ion)               │
    │   X Electronic cigarettes                                  │
    │   X Cold weather outdoors (use Lithium primary)            │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    WHY ALKALINE FAILS AT HIGH DRAIN

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Internal resistance increases at high current            │
    │   Voltage drops below device cutoff (1.0-1.1V)             │
    │   Battery still has 50-70% capacity!                       │
    │   Device thinks battery is dead (but it's not)             │
    │                                                             │
    │   Example: Digital camera takes 50 shots on alkaline       │
    │            (battery still has 60% capacity but low voltage)│
    │            Same camera: 200-300 shots on NiMH              │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

## Safety and Handling

### Leakage Prevention

Alkaline batteries can leak corrosive electrolyte (potassium hydroxide).

```
LEAKAGE CAUSES AND PREVENTION

    WHAT CAUSES LEAKS:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ✓ Depleted battery (internal pressure builds)            │
    │   ✓ Old battery (past expiration date)                     │
    │   ✓ Mixed old and new batteries (reverse charging)         │
    │   ✓ Leaving in device for years                            │
    │   ✓ High temperature storage (hot car, attic)              │
    │   ✓ Poor quality batteries (no-name brands)                │
    │   ✓ Deep discharge (device left on)                        │
    │   ✓ Attempting to recharge (extremely dangerous!)          │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    PREVENTION TIPS:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ✓ Remove batteries from infrequently used devices        │
    │   ✓ Replace all batteries at the same time                 │
    │   ✓ Store in cool, dry place (not garage or attic)         │
    │   ✓ Check expiration dates before buying                   │
    │   ✓ Use brand-name batteries (Duracell, Energizer)         │
    │   ✓ Remove before expiration date                          │
    │   ✓ Don't mix old and new                                  │
    │   ✓ Don't mix different brands                             │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    DAMAGE FROM LEAKS:
    ├── White/green powdery residue (potassium hydroxide)
    ├── Corrodes metal contacts (destroys device)
    ├── Can ruin PCB traces
    ├── Causes bad connections (intermittent)
    └── Leaked device may be irreparable
```

### Do Not Recharge Alkaline Batteries

```
DANGER: NEVER RECHARGE ALKALINE BATTERIES!

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ATTEMPTING TO RECHARGE ALKALINE CAN CAUSE:                │
    │                                                             │
    │   ✗ Explosion (case rupture, shrapnel)                     │
    │   ✗ Fire (internal short, heating)                         │
    │   ✗ Toxic fumes (potassium hydroxide aerosol)              │
    │   ✗ Leakage (corrosive electrolyte)                        │
    │   ✗ Device damage (power supply or charger)                │
    │                                                             │
    │   WHY IT'S DANGEROUS:                                       │
    │   ├── Alkaline chemistry is NOT reversible                 │
    │   ├── Hydrogen gas builds up (explosion risk)              │
    │   ├── Internal pressure exceeds case strength              │
    │   ├── No internal pressure relief                          │
    │   └── Charging creates internal short (fire)               │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    URBAN MYTH: "Alkaline batteries can be recharged a few times"

    TRUTH: Some people have done it, but:
    ├── Capacity after recharge is <20% of original
    ├── Danger of explosion is high
    ├── Leakage almost guaranteed
    ├── May destroy your charger
    └── **DO NOT ATTEMPT** – Buy NiMH rechargeable instead!
```

## Disposal and Recycling

```
ALKALINE BATTERY TOXICITY

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Modern alkaline batteries (1996+ in US):                 │
    │   ├── No added mercury (Mercury-Free)                      │
    │   ├── Low toxicity compared to NiCd                        │
    │   ├── Zinc, manganese, steel, paper, plastic              │
    │   ├── KOH electrolyte (caustic but not toxic)              │
    │   └── Many jurisdictions allow regular trash               │
    │                                                             │
    │   OLD alkaline batteries (pre-1996):                       │
    │   ├── Contained mercury (toxic)                            │
    │   ├── Regulated hazardous waste                            │
    │   └── Should be disposed of carefully                      │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    RECYCLING STATUS (Modern alkaline, 2024)

    Region                  Regulation             Best Practice
    ──────────────────────────────────────────────────────────────
    USA (most states)       Allowed in trash       Recycle if available
    California              Must recycle (Universal Waste)
    EU                      Must recycle (Battery Directive)
    Canada                  Most provinces allow trash
    UK                      Encourage recycling

    NOTE: Check Earth911.com for local recycling options.
```

## Common Problems

### Problem 1: Leaking Battery

```
SYMPTOMS:
├── White/green/blue crust on terminals
├── Device won't power on (corroded contacts)
├── Battery feels sticky or oily
├── Battery case visibly deformed

CAUSES:
├── Old battery (past expiration)
├── Complete discharge (left in device)
├── Mixed old/new batteries
├── High temperature storage
├── Poor quality (no-name brand)

DIAGNOSIS:
├── Visual inspection (crust, corrosion)
├── Smell (ammonia-like odor – KOH)
├── Device contacts green or white

SOLUTIONS:
├── Remove leaking batteries immediately
├── WEAR GLOVES! (KOH is caustic)
├── Clean contacts with vinegar (acid neutralizes base)
├── Use cotton swab or old toothbrush
├── Rinse with isopropyl alcohol
├── Dry thoroughly
├── If corrosion severe, device may be damaged

PREVENTION:
├── Remove batteries from unused devices
├── Replace batteries before expiration date
├── Store in cool, dry place
├── Use quality name-brand batteries
└── Don't mix old and new
```

### Problem 2: Device Won't Work (Battery Not Dead)

```
SYMPTOMS:
├── Device works briefly, then stops
├── Low battery indicator (but new batteries)
├── Device shuts off, batteries measure 1.2V (plenty left!)
├── Same batteries work in another device

CAUSES:
├── High drain device
├── Voltage drops below device cutoff
├── Internal resistance high (normal for alkaline)
├── Device requires high voltage
├── Cold temperature (increases internal resistance)

DIAGNOSIS:
├── Measure battery voltage under load (using device)
├── If voltage <1.0V while device on: normal behavior
├── Try batteries in different device (low drain)
├── Test with NiMH (if they work, device is high drain)

SOLUTIONS:
├── For high-drain devices: use NiMH or Lithium primary
├── For cold weather: use Lithium primary (works to -40°C)
├── Accept that alkaline is wrong battery type
└── Use device's AC adapter if available
```

### Problem 3: Short Battery Life

```
SYMPTOMS:
├── Batteries die quickly (hours instead of weeks)
├── Expensive to keep replacing
├── Device drains batteries in days

CAUSES:
├── Device is high-drain (alkaline performs poorly)
├── High resistance in device (faulty motor, short)
├── Old or poor quality batteries
├── Cold temperature (reduces capacity)
├── Device left on (forgot to turn off)

DIAGNOSIS:
├── Check device current draw (multimeter)
├── Compare to known good alkaline runtime
├── Test with NiMH (if runtime much longer, alkaline wrong)
├── Check for device fault (stuck motor, short circuit)

SOLUTIONS:
├── Switch to NiMH rechargeable for high-drain
├── For low-drain (clocks), alkaline still best
├── Replace faulty device (if short circuit)
├── Store batteries at room temp before use
└── For extreme cold: use Lithium primary
```

## Quick Reference Table

| Parameter | Alkaline | NiMH (rechargeable) | Lithium Primary |
|-----------|----------|---------------------|-----------------|
| Nominal voltage | 1.5V | 1.2V | 1.5V |
| Fresh voltage | 1.60-1.65V | 1.45V | 1.80V |
| Capacity (low drain) | 2800-3000 mAh | 2000-2800 mAh | 3000-3500 mAh |
| Capacity (high drain 1A) | 800-1000 mAh | 2500 mAh | 3000 mAh |
| Energy density | 130-150 Wh/kg | 60-100 Wh/kg | 260-300 Wh/kg |
| Shelf life | 5-10 years | 0.5-1+ year | 15-20 years |
| Self-discharge/year | <2% | High (std) / Low (LSD) | <1% |
| Operating temp | 0 to 50°C | -20 to 50°C | -40 to 60°C |
| Rechargeable | NO | YES | NO |
| Leakage risk | Moderate (old) | Low | Very low |
| Cost per cell | $0.50-$1.00 | $2-$4 (plus charger) | $2-$4 |

## Summary

1. **Alkaline battery** is a primary (non-rechargeable) battery with zinc and MnO₂ in KOH electrolyte

2. **Invented** by Lewis Urry in 1950s, commercialized 1960s

3. **Nominal voltage:** 1.5V (fresh 1.65V, cutoff ~1.0V)

4. **High energy density:** 130-150 Wh/kg (good for primary)

5. **Excellent shelf life:** 5-10 years (50-60% after 10 years)

6. **Low self-discharge:** <2% per year

7. **Poor high-drain performance:** At 1A, capacity drops to 30% (800-1000 mAh)

8. **Good for low-drain devices:** Remotes, clocks, smoke detectors, mice

9. **Bad for high-drain devices:** Digital cameras, motorized toys, high-power flashlights (use NiMH!)

10. **Leakage:** White/green crust (KOH) – can destroy devices

11. **Prevent leakage:** Remove batteries from unused devices, don't mix old/new, store cool

12. **Never recharge alkaline batteries** – explosion/fire risk!

13. **Toxicity:** Modern alkaline are mercury-free, low toxicity

14. **Disposal:** Many areas allow trash, but recycle if possible

15. **Hot cars kill alkaline:** 50°C+ reduces shelf life to months, causes leaks

16. **Cold reduces performance:** Voltage drops, less capacity

17. **Check expiration date** – don't buy old stock

18. **For frequent use, buy NiMH rechargeable** – cheaper long-term, better performance

*This documentation belongs to https://github.com/InterCentury*