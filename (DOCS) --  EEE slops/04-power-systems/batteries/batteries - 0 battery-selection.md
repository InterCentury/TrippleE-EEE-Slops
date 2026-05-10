# batteries - 0 battery-selection

## Selecting the Right Battery for Your Application

Battery selection is a critical design decision that impacts performance, safety, cost, and reliability. Choosing the wrong battery can lead to poor runtime, premature failure, safety hazards, or unnecessary expense. This guide provides a systematic approach to matching battery chemistry and specifications to your specific application requirements.

## The Selection Framework

### Nine Key Selection Criteria

Every battery selection decision should consider these nine factors.

```
BATTERY SELECTION FRAMEWORK

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   1. VOLTAGE                                                │
    │      ├── Required operating voltage                         │
    │      ├── Number of cells in series                          │
    │      └── Voltage tolerance of device                        │
    │                                                             │
    │   2. CAPACITY (Ah / Wh)                                     │
    │      ├── Desired runtime                                    │
    │      ├── Average current draw                               │
    │      └── Physical size constraints                          │
    │                                                             │
    │   3. DISCHARGE CURRENT (C-rate)                             │
    │      ├── Peak current (startup, motors)                     │
    │      ├── Continuous current (steady state)                  │
    │      └── Current capability of chemistry                    │
    │                                                             │
    │   4. RECHARGEABLE OR PRIMARY                                │
    │      ├── Single use vs multiple uses                        │
    │      ├── Cost per cycle                                     │
    │      └── Access for charging                                │
    │                                                             │
    │   5. CYCLE LIFE                                             │
    │      ├── Expected number of charge/discharge cycles         │
    │      ├── Depth of discharge (DoD) per cycle                 │
    │      └── Replacement cost and frequency                     │
    │                                                             │
    │   6. OPERATING TEMPERATURE                                  │
    │      ├── Minimum temperature (cold start)                   │
    │      ├── Maximum temperature (hot environment)              │
    │      └── Ambient vs self-heating                            │
    │                                                             │
    │   7. SHELF LIFE / SELF-DISCHARGE                            │
    │      ├── Time between use (standby)                         │
    │      ├── Storage conditions                                 │
    │      └── Need for maintenance charging                      │
    │                                                             │
    │   8. SAFETY                                                 │
    │      ├── Thermal runaway risk                               │
    │      ├── Leakage / toxicity                                 │
    │      ├── Protection circuit requirements                    │
    │      └── Environmental regulations                          │
    │                                                             │
    │   9. COST                                                   │
    │      ├── Initial purchase cost                              │
    │      ├── Cost per cycle                                     │
    │      ├── Charging equipment (if rechargeable)               │
    │      └── Disposal / recycling fees                          │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

## Selection by Application

### Low Drain Applications (<50mA)

Devices that use very little power and run for months or years on a single charge.

```
LOW DRAIN DEVICE CATEGORIES

    Devices:
    ├── Remote controls (TV, AC, stereo)         10-30mA peak, <1mA standby
    ├── Wall clocks                              50-200µA (microamps)
    ├── Smoke detectors                          5-50µA (microamps)
    ├── Thermostats                              10-50mA peak, low standby
    ├── Wireless sensors                         <10mA average
    ├── Key fobs / garage openers                5-20mA peak, µA standby
    └── Calculators                              1-10mA


    RECOMMENDED BATTERIES:

    Battery Type          Why                        Notes
    ──────────────────────────────────────────────────────────────
    Alkaline              Low cost, long shelf life  5-10 years
    Lithium primary       Extremely long shelf life  15-20 years
    LSD NiMH              Rechargeable, low drain    Charge every 6-12 months
    Standard NiMH         NOT recommended            Self-discharge too high


    SELECTION RULES:

    ├── For standby devices (smoke detectors): Use Alkaline (never rechargeable)
    ├── For occasional use (remotes): Alkaline or LSD NiMH
    ├── For frequent use (wireless mouse): LSD NiMH (Eneloop)
    ├── Avoid standard NiMH (dead after 2 months on shelf)
    └── NEVER use Li-ion in devices designed for 1.5V (overvoltage)
```

### Medium Drain Applications (50-500mA)

Devices that see regular use and draw moderate current.

```
MEDIUM DRAIN DEVICE CATEGORIES

    Devices:
    ├── Computer mice                            100-200mA (gaming)
    ├── Keyboards                                50-100mA (wireless)
    ├── Portable radios                          100-300mA
    ├── LED flashlights (low-med)                100-500mA
    ├── Electric toothbrushes                    200-500mA
    ├── Handheld fans                            300-500mA
    └── Old digital cameras (non-flash)          200-400mA


    RECOMMENDED BATTERIES:

    Battery Type          Why                        Notes
    ──────────────────────────────────────────────────────────────
    LSD NiMH (Eneloop)    Best balance, rechargeable 2000mAh, 2000 cycles
    Alkaline              OK but wasteful           Single use only
    NiCd                  Robust but obsolete        Lower capacity, toxic
    Standard NiMH         Works but self-discharge  Charge every 2-4 weeks


    SELECTION RULES:

    ├── For daily use (mouse/keyboard): LSD NiMH (Eneloop)
    ├── For occasional use (flashlight): Alkaline or LSD NiMH
    ├── For high usage (radio daily): LSD NiMH
    ├── Use standard NiMH only if used frequently (every few days)
    └── Avoid alkaline if device is used daily (too expensive long-term)
```

### High Drain Applications (0.5-5A)

Devices that draw significant current and benefit from low internal resistance.

```
HIGH DRAIN DEVICE CATEGORIES

    Devices:
    ├── Digital cameras (with flash)             1-5A peak
    ├── RC cars (small)                          2-5A continuous
    ├── Power tools (7.2V-12V)                  5-15A
    ├── Drones (small)                           5-20A
    ├── Camera flashes (external)               5-10A brief
    ├── Portable speakers                        1-3A
    └── High-power LED flashlights               1-5A


    RECOMMENDED BATTERIES:

    Application               Best Choice              Alternative
    ──────────────────────────────────────────────────────────────
    Digital camera           NiMH (Eneloop Pro)        Lithium primary
    RC car (hobby)           NiMH or LiPo             (Lithium primary too expensive)
    Power tools              Li-ion (18650/21700)     NiCd (obsolete)
    Drone (racing)           LiPo (high C)            Not applicable
    Camera flash             NiMH (Eneloop)           Lithium primary
    High-power flashlight    Li-ion (18650) or NiMH   Lithium primary (cold)

    NOTE: Alkaline is POOR for high drain (works briefly, then voltage drops)
```

### Extreme High Drain Applications (5-50A+)

High-power devices requiring very low internal resistance.

```
EXTREME HIGH DRAIN DEVICE CATEGORIES

    Devices:
    ├── Racing drones                          30-120A
    ├── RC helicopters                        20-50A
    ├── E-bikes                               15-30A continuous
    ├── EV (electric vehicles)                100-500A
    ├── Industrial power tools                20-80A
    ├── High-end camera flashes               10-30A pulse
    └── Jump starters/boost packs             200-1000A (pulse)


    RECOMMENDED BATTERIES:

    Application               Best Choice                  Secondary
    ──────────────────────────────────────────────────────────────
    Racing drone             LiPo (high C, 80-120C)        -
    E-bike                   Li-ion (18650/21700)         LiFePO₄
    EV                       Li-ion NMC/NCA               LiFePO₄ (safety)
    Power tools              Li-ion (high current)        NiMH (older)
    Jump starter             LiFePO₄ or Li-ion            LiPo (with BMS)


    CRITICAL REQUIREMENTS:

    ├── BMS (Battery Management System) mandatory for Li-ion multi-cell
    ├── High C-rating (C>10 for continuous, C>30 for peak)
    ├── Proper cooling / heatsinking
    ├── Cell balancing for multi-cell packs
    └── Safe charging practices (never unattended)
```

### Standby and Emergency Applications

Devices that sit idle most of the time but must work when needed.

```
STANDBY / EMERGENCY DEVICE CATEGORIES

    Devices:
    ├── Smoke detectors                          5-50µA idle, alarm 50mA
    ├── Emergency lighting                       0mA idle
    ├── Alarm systems (home security)            100-500mA standby
    ├── UPS (uninterruptible power supply)       10-20mA self-discharge
    ├── Medical alert pendants                   1-10mA standby
    ├── EPIRB (emergency beacons)                0mA (long storage)
    └── Car emergency kits (jump starters)       0mA storage


    RECOMMENDED BATTERIES:

    Application               Best Choice                  Alternative
    ──────────────────────────────────────────────────────────────
    Smoke detector          Alkaline                    Lithium primary (10 year)
    Emergency lighting      NiCd (float service)        Lead-acid (sealed)
    Home alarm system       Lead-acid (backup)          Lithium primary (sensors)
    UPS                     Lead-acid (SLA)             LiFePO₄ (premium)
    Medical alert pendant   Lithium primary (long life) Alkaline (change yearly)
    EPIRB                   Lithium primary (Li-SOCl₂)  Very long shelf life
    Jump starter            LiFePO₄ / Li-ion            Keep charged


    SELECTION RULES:

    ├── For critical safety: Use lithium primary (smoke detector, EPIRB)
    ├── For UPS/backup: Use proper float-charge batteries (SLA, LiFePO₄)
    ├── Never use standard NiMH in standby (self-discharges)
    ├── Test alkaline annually (replace if voltage <1.4V)
    └── Mark installation date on batteries
```

### Cold Weather Applications

Batteries behave very differently at low temperatures.

```
COLD WEATHER PERFORMANCE (at -20°C / -4°F)

    Chemistry               Capacity Available    Notes
    ──────────────────────────────────────────────────────────────
    Lithium primary (Li-FeS₂)  90-95%            Excellent, works to -40°C
    NiCd                        70-80%           Good, works to -40°C
    NiMH                        40-60%           Moderate
    Alkaline                    20-40%           Poor (reduced voltage)
    Lead-acid                   30-50%           Reduced CCA
    Li-ion (standard)           NOT RECHARGEABLE below 0°C! (damage)
    Li-ion with heater          70-85%           Must warm before charging
    LiFePO₄                     50-70%           Can charge below 0°C (slowly)


    BEST FOR COLD WEATHER:

    Application               Best Choice
    ──────────────────────────────────────────────────────────────
    Outdoor sensors          Lithium primary (Energizer Ultimate)
    Automatic defibrillator (AED) Lithium primary (10+ year life)
    Remote weather station   Lithium primary or NiCd
    Car starting (cold)      Lead-acid (AGM) with high CCA
    Snowmobile / ATV         LiFePO₄ (with cold weather mode) or lead-acid
    Emergency flashlight     Lithium primary (keeps voltage)


    COLD WEATHER TIPS:

    ├── Keep batteries warm before use (body heat, heated case)
    ├── Lithium primary best for extreme cold (-40°C)
    ├── Do NOT charge Li-ion below 0°C (plating damage)
    ├── NiCd still good in cold (old technology advantage)
    ├── Carry spare batteries (cold reduces runtime)
    └── Consider battery heater for Li-ion EV
```

### High Temperature Applications

Heat is the enemy of most batteries.

```
HIGH TEMPERATURE EFFECTS (>40°C / 104°F)

    Chemistry               Effect                          Max Temp
    ──────────────────────────────────────────────────────────────
    Alkaline                Leakage risk, reduced shelf life 50°C
    NiMH                    Reduced life, capacity loss     50°C
    NiCd                    Reduced life, venting risk      60°C
    Lead-acid               Significantly reduced life      50°C
    Li-ion (NMC)            Degradation, fire risk          60°C
    LiFePO₄                 More tolerant, still degraded   65°C
    Lithium primary (Li-SOCl₂) Good to 85°C (specialty)     85°C


    BEST FOR HIGH TEMPERATURE:

    Application               Best Choice
    ──────────────────────────────────────────────────────────────
    Industrial sensor        Lithium thionyl chloride (Li-SOCl₂)
    Automotive underhood     Lead-acid (AGM) or LiFePO₄
    Solar installation       LiFePO₄ (cooled) or lead-acid
    Medical implant          Li-SOCl₂ (specialty)
    Remote telemetry         Lithium primary (high temp grade)

    NOTE: All batteries degrade faster at high temperature.
    Rule of thumb: Every 10°C above 25°C = 2× degradation rate.
```

## Battery Chemistry Decision Tree

### Step-by-Step Selection Process

```
BATTERY CHEMISTRY DECISION TREE

    START HERE
         │
         ▼
    ┌─────────────────────────────────────────────────────────────┐
    │  Is the device rechargeable or single-use?                  │
    └─────────────────────────────────────────────────────────────┘
         │
         ├──► SINGLE-USE (Primary) ──────────────────────────────┐
         │                                                       │
         │    ┌─────────────────────────────────────────────┐    │
         │    │  Alkaline → Most devices (remotes, clocks)  │    │
         │    │  Lithium primary → Extreme temp, long life  │    │
         │    │  Zinc-carbon → Cheap (obsolete, avoid)      │    │
         │    └─────────────────────────────────────────────┘    │
         │                                                       │
         └──► RECHARGEABLE (Secondary) ──────────────────────────┐
                                                                 │
              ┌─────────────────────────────────────────────────┐│
              │  What is the most important factor?             ││
              └─────────────────────────────────────────────────┘│
                                                                 │
         ┌───────────────┬───────────────┬───────────────┬───────┘
         │               │               │               │
         ▼               ▼               ▼               ▼
    ┌─────────┐    ┌─────────┐    ┌─────────┐    ┌─────────┐
    │ENERGY   │    │POWER    │    │SAFETY   │    │LOW COST │
    │DENSITY  │    │DENSITY  │    │         │    │         │
    └────┬────┘    └────┬────┘    └────┬────┘    └────┬────┘
         │              │              │              │
         ▼              ▼              ▼              ▼
    ┌─────────┐    ┌─────────┐    ┌─────────┐    ┌─────────┐
    │ Li-ion  │    │ LiPo    │    │ LiFePO₄ │    │ Lead-   │
    │ NMC     │    │ (high C)│    │ or NiMH │    │ acid    │
    └─────────┘    └─────────┘    └─────────┘    └─────────┘
    
    Laptops, EVs   Drones, RC    Solar, UPS,   Cars,
                     racing        e-bikes      starting
```

### Quick Reference by Device Type

```
DEVICE-SPECIFIC RECOMMENDATIONS

    Device                     Best Battery            Why
    ──────────────────────────────────────────────────────────────
    TV Remote                  Alkaline                Long life, cheap
    Wireless mouse             LSD NiMH (Eneloop)      Rechargeable, low self-discharge
    Wall clock                 Alkaline                Lasts 2-3 years
    Smoke detector             Alkaline / Lithium      Replace annually (alkaline)
    Digital camera             NiMH (Eneloop Pro)      High current, rechargeable
    Smartphone                 Li-ion (built-in)       High energy density
    Laptop                     Li-ion                  Energy density
    Electric toothbrush        NiMH (built-in)         Safe, rechargeable
    Cordless drill             Li-ion (18650)          High power, lightweight
    E-bike                     Li-ion or LiFePO₄       Range vs safety tradeoff
    Golf cart                  Lead-acid (deep cycle)  Cheap, available
    Solar storage              LiFePO₄                 Long life, safe
    UPS (computer)             Lead-acid (SLA)         Float charge compatible
    Car starting               Lead-acid (AGM)         High CCA, vibration resistant
    Medical implant            Li-SOCl₂ (primary)      Very long life (10+ years)
    Cold weather flashlight    Lithium primary (Energizer) Works at -40°C
    RC drone (racing)          LiPo (high C)           80-120C discharge rate
```

## Selection by Chemistry

### Comparative Summary Table

```
COMPLETE BATTERY COMPARISON TABLE

    Chemistry           Voltage    Energy (Wh/kg)   Cycle Life   Self-Discharge   Cost
    ────────────────────────────────────────────────────────────────────────────────────────
    Alkaline            1.5V       130-150          N/A          1-2%/year        $
    (primary)
    
    Zinc-carbon         1.5V       60-80            N/A          5-10%/year       $
    (primary)
    
    Lithium primary     1.5-3.6V   260-300          N/A          <1%/year         $$$
    (Li-FeS₂, etc.)
    
    NiCd                1.2V       40-60            500-1000     15-20%/month     $$
    
    NiMH (std)          1.2V       80-120           300-500      20-30%/month     $$
    
    NiMH (LSD)          1.2V       60-100           500-1000+    10-15%/year      $$$
    
    Li-ion (NMC)        3.6-3.7V   150-260          300-500      2-5%/month       $$$
    
    LiFePO₄             3.2-3.3V   90-140           2000-5000+   1-3%/month       $$$
    
    LiPo (pouch)        3.7V       230-280          300-500      2-5%/month       $$$
    
    Lead-acid           2.1V/cell  30-50            200-500      3-20%/month      $
    
    LTO                 2.3-2.4V   50-80            10000-20000  1-2%/month       $$$$
```

## Safety and Regulatory Considerations

### Key Safety Requirements by Chemistry

```
SAFETY REQUIREMENTS TABLE

    Chemistry      BMS Required   Ventilation    Storage Temp    Disposal
    ────────────────────────────────────────────────────────────────────
    Alkaline       No             No             5-30°C         Trash (most areas)
    Lithium primary No            No             5-30°C         Recycle (Call2Recycle)
    NiCd           No (single)    Minimal        -20-45°C       MUST recycle (toxic!)
    NiMH           No (single)    Minimal        -20-45°C       Recycle recommended
    Li-ion (single) Optional      No             5-35°C         MUST recycle
    Li-ion (multi) MANDATORY      No             5-35°C         MUST recycle
    LiFePO₄ (multi) MANDATORY     No             -20-60°C       MUST recycle
    LiPo           External BMS   No             5-35°C         MUST recycle (fire risk)
    Lead-acid      No (single)    YES (H₂ gas)    -20-50°C       MUST recycle (hazardous)

    NOTE: "BMS Required" for multi-cell means battery pack must have protection circuit.
```

### International Shipping and Transport

```
BATTERY TRANSPORT REGULATIONS (Summary)

    Battery Type        Air (Passenger)    Air (Cargo)     Ground
    ──────────────────────────────────────────────────────────────
    Alkaline (1.5V)     Unlimited          Unlimited       Unlimited
    Lithium primary     Carry-on only      Restricted      Limited by size
    (≤100Wh)            (never checked)
    Lithium primary     Not allowed        Not allowed     Limited
    (>100Wh)
    NiCd / NiMH         Unlimited          Unlimited       Unlimited
    Li-ion (≤100Wh)     Carry-on only      Restricted      Limited
                        (never checked)
    Li-ion (>100Wh)     Not allowed        Restricted      Restricted
    Lead-acid (wet)     Not allowed        Not allowed      Restricted
    Lead-acid (sealed)  Not allowed        Restricted       Limited

    NOTE: Always check current IATA/DOT regulations before shipping.
```

## Economic Analysis

### Cost Per Cycle Calculation

```
COST PER CYCLE COMPARISON (AA size, daily use)

    Battery Type          Cost per cell    Cycles    Total Energy   Cost per cycle
    ────────────────────────────────────────────────────────────────────────────
    Alkaline (primary)    $0.75            1         3Wh (avg)          $0.75
    NiMH (standard)       $2.00            300       900Wh              $0.007
    NiMH (LSD, Eneloop)   $3.00            500       1500Wh             $0.006
    NiCd (AA)             $1.50            500       750Wh              $0.003
    
    Plus charger cost: $20-50 (one-time)


    PAYBACK ANALYSIS (for a device using 1 AA per week):

    Annual alkaline cost:   52 × $0.75 = $39.00
    Annual NiMH (LSD) cost: 52 × $0.006 = $0.31 (plus charger)
    
    Payback period: ($3 × 4 cells + $25 charger) / ($39 - $0.31) 
                  = $37 / $38.69 ≈ 1 year
    
    CONCLUSION: For frequent use, rechargeable saves money after 1 year.
```

### Total Cost of Ownership

```
TCO FACTORS TO CONSIDER

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Initial Cost:                                             │
    │   ├── Battery purchase                                      │
    │   ├── Charger (if rechargeable)                             │
    │   ├── BMS (if multi-cell Li-ion)                            │
    │   └── Enclosure / holder                                    │
    │                                                             │
    │   Operating Cost:                                           │
    │   ├── Electricity for charging (negligible)                 │
    │   ├── Replacement batteries                                 │
    │   └── Maintenance (water for flooded lead-acid)             │
    │                                                             │
    │   Disposal Cost:                                            │
    │   ├── Recycling fees (NiCd, Li-ion)                         │
    │   ├── Hazardous waste handling (lead-acid)                  │
    │   └── Environmental compliance                              │
    │                                                             │
    │   Hidden Costs:                                             │
    │   ├── Device damage from leaks (alkaline)                   │
    │   ├── Fire risk (Li-ion without BMS)                        │
    │   ├── Downtime (battery failure)                            │
    │   └── Lost data / productivity                              │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

## Common Selection Mistakes

### Mistake 1: Using Alkaline in High Drain Devices

```
PROBLEM:
Digital camera owner uses alkaline batteries, gets only 50 shots.

WHY:
Alkaline internal resistance increases at high current.
Voltage drops below camera's 1.0V cutoff.
Battery still has 60% capacity! Wasted.

SOLUTION:
Use NiMH (Eneloop) for high drain devices.
200-300 shots per charge.
```

### Mistake 2: Using Standard NiMH in Standby Devices

```
PROBLEM:
Smoke detector with standard NiMH dies after 2 months.

WHY:
Standard NiMH self-discharge = 20-30% per month.
After 3 months, battery dead.

SOLUTION:
Use Alkaline (1 year life) or LSD NiMH (Eneloop).
```

### Mistake 3: Charging Li-ion Below 0°C

```
PROBLEM:
EV owner charges battery in freezing weather, loses range permanently.

WHY:
Lithium plating at anode (irreversible damage).
Capacity loss, increased internal resistance.

SOLUTION:
Warm battery before charging (battery heater).
Use LiFePO₄ (can charge below 0°C slowly).
```

### Mistake 4: Mixing Old and New Batteries

```
PROBLEM:
User puts one new and one old alkaline in device.
Old battery leaks, destroys device.

WHY:
Old battery discharges first, then reverse-charged by new battery.
Reverse charging generates gas, pressure, leakage.

SOLUTION:
Always replace all batteries in a device at same time.
Use same brand, same age, same charge level.
```

### Mistake 5: Using Li-ion 14500 as AA Replacement

```
PROBLEM:
User puts 14500 Li-ion (3.7V) in AA (1.5V) device.

WHY:
Overvoltage destroys device instantly.
Smoke, damage, fire risk.

SOLUTION:
Use NiMH for rechargeable AA replacement.
Li-ion 14500 only in devices designed for 3.7V.
```

## Emergency Selection Guide

### What to Use When You Don't Know

```
EMERGENCY QUICK REFERENCE

    I have a device that needs batteries and I'm not sure what to use:
    
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   DEVICE TYPE              BEST GUESS                       │
    │   ──────────────────────────────────────────────────────────│
    │   TV Remote                Alkaline                         │
    │   Wireless mouse           Alkaline or NiMH                 │
    │   Wall clock               Alkaline                         │
    │   Flashlight (LED)         Alkaline (or NiMH if used often) │
    │   Digital camera           NiMH                             │
    │   Kids toy                 Alkaline (or NiMH if heavy use)  │
    │   Smoke detector           Alkaline (change yearly)         │
    │   Thermostat               Alkaline                         │
    │   Cordless phone           NiMH (built-in pack)             │
    │   Car key fob              Alkaline (CR2032 coin cell)      │
    │   Portable radio           Alkaline or NiMH                 │
    │   Medical device           Follow manual (often alkaline)   │
    │   Power tool               NEEDS SPECIFIC (Li-ion pack)     │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    WHEN IN DOUBT (for 1.5V consumer devices):

    ├── For occasional use (<once per week): ALKALINE
    ├── For frequent use (daily): LSD NiMH (Eneloop)
    ├── For cold weather (<0°C): LITHIUM PRIMARY
    ├── For high drain (camera, motor): NiMH or LITHIUM PRIMARY
    └── Never use Li-ion 14500 unless device specifically says 3.7V
```

## Quick Reference Card

```
BATTERY QUICK SELECTION CARD

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   NEED:                     USE:                            │
    │   ──────────────────────────────────────────────────────────│
    │   Long shelf life           Alkaline or Lithium primary     │
    │   High energy density       Li-ion (NMC)                    │
    │   High power (drones)       LiPo (high C)                   │
    │   Low cost                  Lead-acid or alkaline           │
    │   Long cycle life           LiFePO₄ or NiCd                 │
    │   Safety critical           LiFePO₄ or NiMH                 │
    │   Cold weather (-40°C)      Lithium primary or NiCd         │
    │   Hot weather (>50°C)       Lithium primary (special)       │
    │   Small size (thin)         LiPo pouch                      │
    │   Rechargeable AA/AAA       LSD NiMH (Eneloop)              │
    │   Car starting              Lead-acid (AGM)                 │
    │   Solar storage             LiFePO₄                         │
    │   UPS backup                Lead-acid (SLA)                 │
    │   Medical implant           Lithium primary (Li-SOCl₂)      │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    FOR 1.5V DEVICES (AA/AAA):

    ┌─────────────────────────────────────────────────────────────┐
    │   USAGE PATTERN              BEST BATTERY                   │
    │   ──────────────────────────────────────────────────────────│
    │   Emergency (unused for years)  Lithium primary             │
    │   Occasional (once a month)     Alkaline                    │
    │   Weekly use                     LSD NiMH (Eneloop)         │
    │   Daily use                      NiMH (Eneloop Pro)         │
    │   High drain (camera, motor)     NiMH (Eneloop Pro)         │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

## Summary

1. **Nine selection criteria:** Voltage, capacity, discharge current, rechargeable, cycle life, temperature, shelf life, safety, cost

2. **Low drain (<50mA):** Alkaline or Lithium primary (standby), LSD NiMH (frequent use)

3. **Medium drain (50-500mA):** LSD NiMH best for daily use, alkaline for occasional

4. **High drain (0.5-5A):** NiMH for AA/AAA, Li-ion for larger packs

5. **Extreme high drain (>5A):** LiPo (high C) for drones, Li-ion for power tools

6. **Standby / emergency:** Lithium primary or alkaline (change regularly)

7. **Cold weather (<0°C):** Lithium primary best, NiCd good, avoid Li-ion charging below 0°C

8. **Hot weather (>40°C):** All batteries degrade, LiFePO₄ and specialty lithium best

9. **Alkaline** = cheap, long shelf life, poor high drain

10. **NiMH (LSD/Eneloop)** = rechargeable, low self-discharge, good all-rounder for AA/AAA

11. **Li-ion (NMC)** = high energy density, requires BMS for multi-cell

12. **LiFePO₄** = safest Li-ion, longest cycle life, lower energy density

13. **LiPo** = lightweight, high power, most dangerous (pouch)

14. **Lead-acid** = cheap, heavy, good for starting and standby

15. **Never mix old/new batteries** (leakage risk, reverse charging)

16. **Never use Li-ion 14500 in 1.5V devices** (overvoltage destroys device)

17. **For most AA/AAA users: Eneloop (LSD NiMH) is best** – cost effective, low self-discharge

18. **Match chemistry to application** – no single battery works for everything

*This documentation belongs to https://github.com/InterCentury*