 2 how-battery-works

## How a Battery Works

A battery works by converting chemical energy into electrical energy through electrochemical reactions. When a battery is connected to an external circuit (like a light bulb or motor), chemical reactions inside the battery cause electrons to flow from the negative terminal to the positive terminal through the circuit, creating electric current.

This document explains the fundamental physics and chemistry behind battery operation, from the atomic level to complete circuits.

## The Fundamental Principles

### Electrochemical Basis

All batteries rely on two fundamental chemical processes: oxidation and reduction.

```
OXIDATION AND REDUCTION

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   OXIDATION (occurs at ANODE, negative terminal)            │
    │                                                             │
    │   "Loss of electrons"                                       │
    │   LEO: Loss of Electrons = Oxidation                        │
    │                                                             │
    │   Example: Zn → Zn²⁺ + 2e⁻                                  │
    │   (Zinc metal loses 2 electrons, becomes zinc ion)          │
    │                                                             │
    ├─────────────────────────────────────────────────────────────┤
    │                                                             │
    │   REDUCTION (occurs at CATHODE, positive terminal)          │
    │                                                             │
    │   "Gain of electrons"                                       │
    │   GER: Gain of Electrons = Reduction                        │
    │                                                             │
    │   Example: 2MnO₂ + 2H⁺ + 2e⁻ → Mn₂O₃ + H₂O                  │
    │   (Manganese dioxide gains electrons, reduced)              │
    │                                                             │
    ├─────────────────────────────────────────────────────────────┤
    │                                                             │
    │   MEMORY AID: OIL RIG                                       │
    │   Oxidation Is Loss (of electrons)                          │
    │   Reduction Is Gain (of electrons)                          │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    COMPLETE ELECTROCHEMICAL CELL:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   External Circuit (wire)                                   │
    │   ──────────────────────────────────────────────────────►   │
    │                                                             │
    │   ┌─────────┐                                    ┌─────────┐│
    │   │  ANODE  │                                    │ CATHODE ││
    │   │   (-)   │                                    │   (+)   ││
    │   │         │                                    │         ││
    │   │  Zn →   │         ◄── IONS ──►               │  ← MnO₂ ││
    │   │  Zn²⁺ + │                                    │  gains  ││
    │   │  2e⁻    │                                    │  e⁻     ││
    │   │         │                                    │         ││
    │   └────┬────┘                                    └────┬────┘│
    │        │                                              │     │
    │        └──────────────┬───────────────────────────────┘     │
    │                       │                                     │
    │                  ELECTROLYTE                                │
    │              (allows ion flow)                              │
    │                                                             │
    │   ◄─────────────────────────────────────────────────────    │
    │                     Electron flow (opposite)                │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

### The Electrochemical Series

Different materials have different tendencies to lose or gain electrons.

```
ELECTROCHEMICAL SERIES (Reduction Potential)

    More likely to LOSE electrons (better ANODE materials)
    ┌─────────────────────────────────────────────────────────────┐
    │   Lithium (Li)     -3.04V   ← Best anode (most negative)    │
    │   Potassium (K)    -2.93V                                   │
    │   Calcium (Ca)     -2.87V                                   │
    │   Sodium (Na)      -2.71V                                   │
    │   Magnesium (Mg)   -2.37V                                   │
    │   Aluminum (Al)    -1.66V                                   │
    │   Zinc (Zn)        -0.76V   ← Alkaline anode                │
    │   Iron (Fe)        -0.44V                                   │
    │   Cadmium (Cd)     -0.40V   ← NiCd anode                    │
    │   Nickel (Ni)      -0.25V                                   │
    │   Lead (Pb)        -0.13V   ← Lead-acid anode               │
    │   Hydrogen (H)      0.00V   (reference)                     │
    │   Copper (Cu)      +0.34V                                   │
    │   Silver (Ag)      +0.80V                                   │
    │   Oxygen (O₂)      +1.23V                                   │
    │   Chlorine (Cl₂)   +1.36V                                   │
    └─────────────────────────────────────────────────────────────┘
    
    More likely to GAIN electrons (better CATHODE materials)
    ┌─────────────────────────────────────────────────────────────┐
    │   Fluorine (F₂)    +2.87V   ← Best cathode (most positive)  │
    └─────────────────────────────────────────────────────────────┘


    VOLTAGE OF A CELL:

    Cell Voltage = Cathode Potential - Anode Potential

    Example (alkaline cell):
    ┌─────────────────────────────────────────────────────────────┐
    │   Anode (Zinc):      -0.76V                                 │
    │   Cathode (MnO₂):    +0.34V                                 │
    │   Cell Voltage = 0.34 - (-0.76) = 1.10V (theoretical)       │
    │                                                             │
    │   Actual alkaline cell: 1.5V (with different cathode)       │
    └─────────────────────────────────────────────────────────────┘
```

## Step-by-Step Operation

### When a Battery is Connected

The sequence of events when a battery powers a device.

```
BATTERY OPERATION SEQUENCE

    STEP 1: Connect load (light bulb, motor) to terminals
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Battery (-) ──► wire ──► load ──► wire ──► Battery (+)    │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    STEP 2: Chemical reaction starts at anode
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Anode metal oxidizes: M → Mⁿ⁺ + ne⁻                       │
    │                                                             │
    │   Example (zinc): Zn → Zn²⁺ + 2e⁻                           │
    │                                                             │
    │   Excess electrons build up on anode (-)                    │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    STEP 3: Electrons flow through external circuit
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Electrons repel each other (like charges repel)           │
    │   Electrons flow FROM anode (-) TO cathode (+)              │
    │   through the external circuit                              │
    │                                                             │
    │   This electron flow is ELECTRIC CURRENT!                   │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    STEP 4: Chemical reaction at cathode
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Cathode material gains electrons: N + ne⁻ → Nⁿ⁻           │
    │                                                             │
    │   Example (manganese dioxide):                              │
    │   2MnO₂ + 2H₂O + 2e⁻ → Mn₂O₃ + 2OH⁻                         │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    STEP 5: Ions flow through electrolyte
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Positive ions (Zn²⁺) move through electrolyte to          │
    │   balance charge                                            │
    │                                                             │
    │   Negative ions (OH⁻) move opposite direction               │
    │                                                             │
    │   This completes the circuit internally                     │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    CONTINUOUS CYCLE:
    
    Electrons flow through external circuit (doing work)
    Ions flow through electrolyte (completing circuit)
    Chemical reactants are consumed
    Battery eventually "dies" when reactants exhausted
```

### Open Circuit (No Load)

What happens inside a battery when nothing is connected.

```
OPEN CIRCUIT STATE

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   ┌─────────┐                                    ┌─────────┐│
    │   │  ANODE  │                                    │ CATHODE ││
    │   │   (-)   │                                    │   (+)   ││
    │   │         │                                    │         ││
    │   │  Metal  │                                    │  Metal  ││
    │   │         │                                    │  Oxide  ││
    │   │   Zn    │                                    │   MnO₂  ││
    │   │         │                                    │         ││
    │   │   Excess│                                    │ Deficit ││
    │   │  e⁻     │                                    │ of e⁻   ││
    │   │         │                                    │         ││
    │   └────┬────┘                                    └────┬────┘│
    │        │                                              │     │
    │        └──────────────┬───────────────────────────────┘     │
    │                       │                                     │
    │                   ELECTROLYTE                               │
    │                                                             │
    │   No external circuit = No electron flow                    │
    │   Reactions stop (or very slow self-discharge)              │
    │   Voltage measured = Open Circuit Voltage (OCV)             │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘

    Open Circuit Voltage (OCV):
    ├── Measured with no load (no current)
    ├── Highest voltage the battery can produce
    ├── Determined by chemistry (1.5V for alkaline)
    └── Drops under load due to internal resistance
```

## Internal Resistance

### What Causes Internal Resistance

Every battery has inherent resistance that limits current flow.

```
SOURCES OF INTERNAL RESISTANCE

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   1. ELECTRODE RESISTANCE                                   │
    │      └── The metal itself resists electron flow             │
    │                                                             │
    │   2. ELECTROLYTE RESISTANCE                                 │
    │      └── Ions move slowly through electrolyte               │
    │                                                             │
    │   3. SEPARATOR RESISTANCE                                   │
    │      └── Porous material slows ion movement                 │
    │                                                             │
    │   4. CONTACT RESISTANCE                                     │
    │      └── Between materials (electrode/electrolyte)          │
    │                                                             │
    │   5. POLARIZATION RESISTANCE                                │
    │      └── Concentration changes near electrodes              │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    EFFECT OF INTERNAL RESISTANCE:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Equivalent circuit:                                       │
    │                                                             │
    │   ┌─────┬─────R_int─────┬─────┐                             │
    │   │     │               │     │                             │
    │   │  V  │               │     │                             │
    │   │ideal│               │     │                             │
    │   │     │               │     │                             │
    │   └─────┴───────────────┴─────┘                             │
    │         │                     │                             │
    │         │                     │                             │
    │         ▼                     ▼                             │
    │    Actual terminal        When current flows:               │
    │    voltage = V_ideal       V_term = V_ideal - I × R_int     │
    │    when I = 0                                               │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    VOLTAGE DROP EXAMPLE:

    Alkaline AA battery:
    ├── Open circuit voltage: 1.60V
    ├── Internal resistance: 200mΩ (0.2Ω)
    ├── Load current: 500mA (0.5A)
    │
    └── Voltage drop = I × R_int = 0.5A × 0.2Ω = 0.10V
    
    Terminal voltage under load = 1.60V - 0.10V = 1.50V


    HEATING EFFECT:

    Power dissipated as heat = I² × R_int

    Example (0.5A, 0.2Ω):
    P_heat = (0.5)² × 0.2 = 0.25 × 0.2 = 0.05W (small)
    
    Example (10A, 0.2Ω from Li-ion):
    P_heat = 100 × 0.2 = 20W (significant heat!)
```

## Battery Discharge Characteristics

### Discharge Curve

How battery voltage changes over time during use.

```
TYPICAL DISCHARGE CURVES (AA size, 500mA load)

    Voltage (V)
        │
    1.6 ┼●
        │ ╲
    1.5 ┼  ╲
        │   ╲
    1.4 ┼    ╲
        │     ╲        ┌─────────────────────────────────────────┐
    1.3 ┼      ╲       │  ALKALINE  - Sloping curve              │
        │       ╲      │  Voltage gradually drops                │
    1.2 ┼        ╲     │  Many devices stop at 1.0V              │
        │         ╲    │  (leaves 20-30% capacity unused)        │
    1.1 ┼          ╲   │                                         │
        │           ╲  │  NiMH  - Flat curve                     │
    1.0 ┼            ●─┼─────────────────────────────────────────│
        │            │\                                        │
    0.9 ┼            │ ╲                                       │
        │            │  ╲                                      │
    0.8 ┼            │   ●─────────────────────────────────────│
        │            │                                         │
        └────────────┴──────────────────────────────────────────────► Time
         0%     25%     50%     75%     100%  120% (alkaline)
                                            (capacity)


    DISCHARGE CURVE SHAPES BY CHEMISTRY:

    Chemistry           Curve Shape                 Notes
    ──────────────────────────────────────────────────────────────
    Alkaline            Sloping                     Voltage drops steadily
    Zinc-carbon         Sloping (steeper)           Poor regulation
    Lithium primary     Flat then drop              Good for constant power
    NiCd                Very flat                   Excellent regulation
    NiMH                Flat (slightly sloping)     Good regulation
    Lead-acid           Flat                        Good regulation
    Li-ion              Flat (then sharp drop)      Excellent, BMS cutoff
    LiFePO₄             Very flat                   Very stable voltage
```

### Factors Affecting Discharge

```
FACTORS THAT CHANGE DISCHARGE BEHAVIOR

    TEMPERATURE EFFECT:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Cold temperature (-20°C):                                 │
    │   ├── Increased internal resistance                         │
    │   ├── Lower voltage under load                              │
    │   ├── Reduced usable capacity (alkaline: 20-40% left!)      │
    │   └── Device may shut down early                            │
    │                                                             │
    │   Hot temperature (40°C):                                   │
    │   ├── Decreased internal resistance                         │
    │   ├── Higher initial voltage                                │
    │   ├── Slightly increased capacity                           │
    │   └── MUCH shorter cycle life (rechargeable)                │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    DISCHARGE RATE EFFECT:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Higher current = Lower effective capacity (Peukert effect)│
    │                                                             │
    │   Example (AA alkaline, 25°C):                              │
    │   10mA:   3000mAh (100%)                                    │
    │   100mA:  2700mAh (90%)                                     │
    │   500mA:  1800mAh (60%)                                     │
    │   1000mA: 1000mAh (33%)                                     │
    │   2000mA:  400mAh (13%)                                     │
    │                                                             │
    │   NiMH handles high current much better:                    │
    │   1000mA: 2400mAh (95% of 1C rate)                          │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    AGE EFFECT:
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   As battery ages:                                          │
    │   ├── Internal resistance increases                         │
    │   ├── Capacity decreases                                    │
    │   ├── Voltage drops more under load                         │
    │   └── Self-discharge increases                              │
    │                                                             │
    │   New battery:  2000mAh, 50mΩ                               │
    │   Old battery:  1500mAh, 150mΩ (75% capacity)               │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

## Battery Charging (Rechargeable)

### How Charging Works

Reversing the chemical reactions that occurred during discharge.

```
CHARGING PROCESS

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   External power source (charger) pushes electrons          │
    │   back into the anode                                       │
    │                                                             │
    │   DISCHARGE:    Zn → Zn²⁺ + 2e⁻                             │
    │   CHARGE:       Zn²⁺ + 2e⁻ → Zn                             │
    │                                                             │
    │   ┌─────────────────────────────────────────────────────┐   │
    │   │                                                     │   │
    │   │   Charger (+) ──► Battery (+)                       │   │
    │   │   (higher voltage forces current backward)          │   │
    │   │                                                     │   │
    │   │   Charger (-) ◄── Battery (-)                       │   │
    │   │                                                     │   │
    │   └─────────────────────────────────────────────────────┘   │
    │                                                             │
    │   Energy stored as chemical potential                       │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    CHARGE ACCEPTANCE:

    ├── Batteries have maximum charge rate (C-rate)
    ├── Exceeding rate causes overheating
    ├── Li-ion requires constant current/constant voltage (CC/CV)
    ├── NiMH requires -ΔV or dT/dt detection
    └── Lead-acid can be charged with constant voltage
```

### Why Batteries Can't Be 100% Efficient

```
ENERGY LOSSES DURING CHARGE/DISCHARGE

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Charge energy in (Wh)                                    │
    │          │                                                │
    │          ▼                                                │
    │   ┌─────────────────────────────────────────────────────┐   │
    │   │                                                     │   │
    │   │   ENERGY LOSSES:                                    │   │
    │   │   ├── Heat (I²R losses)                            │   │
    │   │   ├── Overpotential (voltage inefficiency)          │   │
    │   │   ├── Side reactions (gas generation)               │   │
    │   │   └── Self-discharge                               │   │
    │   │                                                     │   │
    │   └─────────────────────────────────────────────────────┘   │
    │          │                                                │
    │          ▼                                                │
    │   Discharge energy out (Wh)                              │
    │                                                             │
    │   Round-trip efficiency = Energy out / Energy in × 100%    │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    TYPICAL ROUND-TRIP EFFICIENCY:

    Chemistry               Efficiency           Notes
    ──────────────────────────────────────────────────────────────
    Lead-acid               80-90%               Good
    NiCd                    70-80%               Moderate
    NiMH                    65-75%               Moderate
    Li-ion                  85-95%               Excellent
    LiFePO₄                 90-95%               Excellent
    LTO                     90-95%               Excellent

    Example: 100Wh charged, only 85-95Wh available during discharge
```

## Self-Discharge

### What Causes Self-Discharge

All batteries lose charge over time even when not connected.

```
SELF-DISCHARGE MECHANISMS

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   1. INTERNAL CHEMICAL REACTIONS                           │
    │      └── Spontaneous reactions between materials          │
    │                                                             │
    │   2. MICRO-SHORT CIRCUITS                                  │
    │      └── Tiny conductive paths through separator          │
    │                                                             │
    │   3. SIDE REACTIONS                                        │
    │      └── Unwanted chemical reactions                       │
    │                                                             │
    │   4. ELECTROLYTE DECOMPOSITION                             │
    │      └── Electrolyte breaks down over time                 │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    SELF-DISCHARGE RATES BY CHEMISTRY:

    Chemistry               Self-discharge (per month) at 20°C
    ──────────────────────────────────────────────────────────────
    Alkaline                <1% (very low)
    Lithium primary         <1% (very low)
    NiCd                    15-20% (high)
    NiMH (standard)         20-30% (very high)
    NiMH (LSD)              1-3% (low)
    Lead-acid               3-10% (moderate)
    Li-ion                  2-5% (low)
    LiFePO₄                 2-3% (low)
    LTO                     1-2% (low)


    TEMPERATURE EFFECT ON SELF-DISCHARGE:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Self-discharge rate DOUBLES every 10°C rise              │
    │                                                             │
    │   Example (NiMH standard):                                 │
    │   0°C:   5-10% per month                                  │
    │   20°C:  20-30% per month                                 │
    │   30°C:  40-60% per month                                 │
    │   40°C:  80-120% per month (dead in weeks!)               │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

## Battery End-of-Life

### Why Batteries Die

```
BATTERY FAILURE MECHANISMS

    PRIMARY BATTERIES (non-rechargeable):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   1. REACTANTS EXHAUSTED                                   │
    │      └── All active material consumed                      │
    │                                                             │
    │   2. ELECTROLYTE DRIED OUT                                 │
    │      └── Seals fail, liquid evaporates                     │
    │                                                             │
    │   3. PASSIVATION LAYER                                     │
    │      └── Insulating layer forms on electrode               │
    │                                                             │
    │   4. INTERNAL RESISTANCE INCREASE                          │
    │      └── Voltage drops below useful level                  │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘


    SECONDARY BATTERIES (rechargeable):
    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   1. CYCLE LIFE EXCEEDED                                   │
    │      └── Capacity drops below 80%                          │
    │                                                             │
    │   2. INTERNAL SHORT CIRCUIT (dendrites)                    │
    │      └── Lithium plating (Li-ion) or crystal growth       │
    │                                                             │
    │   3. ELECTROLYTE DECOMPOSITION                             │
    │      └── Chemical breakdown from overcharge/heat          │
    │                                                             │
    │   4. ELECTRODE DEGRADATION                                 │
    │      └── Physical breakdown (cracking, shedding)          │
    │                                                             │
    │   5. SEAL FAILURE (leakage)                                │
    │      └── Gas pressure ruptures seal                        │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

### End-of-Life Indicators

```
SIGNS OF BATTERY FAILURE

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   VISUAL INDICATORS:                                        │
    │   ├── Swelling (pouch cells)                              │
    │   ├── Leaking (white/green crust)                         │
    │   ├── Corrosion on terminals                               │
    │   ├── Cracking or deformation                              │
    │   └── Discoloration (brown/black)                         │
    │                                                             │
    │   PERFORMANCE INDICATORS:                                   │
    │   ├── Runtime significantly reduced                        │
    │   ├── Device shuts down early (voltage sag)               │
    │   ├── Battery gets hot during use/charging                │
    │   ├── Doesn't hold charge (self-discharge high)           │
    │   └── Can't reach full voltage (rechargeable)             │
    │                                                             │
    │   MEASUREMENT INDICATORS:                                   │
    │   ├── Internal resistance >2× new value                    │
    │   ├── Capacity <80% of rated                              │
    │   └── Voltage < cutoff (primary)                          │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

## Practical Demonstration

### Simple Battery Circuit

Understanding battery operation through a simple example.

```
EXAMPLE: BATTERY POWERING AN LED

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   CIRCUIT:                                                 │
    │                                                             │
    │   ┌─────┐                                                  │
    │   │  +  │──┬────[220Ω]────┬───[LED]───┬──┐                │
    │   │ 9V  │  │              │           │  │                │
    │   │ Bat │  │              │           │  │                │
    │   │  -  │  │              │           │  │                │
    │   └─────┘  │              │           │  │                │
    │            │              │           │  │                │
    │            │              ▼           ▼  │                │
    │            │         Resistor        LED │                │
    │            │         220Ω              │                │
    │            │                             │                │
    │            └─────────────────────────────┘                │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘

    WHAT HAPPENS:

    1. Chemical reaction at anode: Zn → Zn²⁺ + 2e⁻
    2. Electrons flow through wire to resistor and LED
    3. Resistor limits current to safe level (~30mA)
    4. LED lights up (electrons recombine, release light)
    5. Electrons return to cathode: 2MnO₂ + H₂O + 2e⁻ → Mn₂O₃ + 2OH⁻
    6. Ions flow through electrolyte to complete circuit
    7. Chemical reactants consumed until battery dies


    VOLTAGE AND CURRENT MEASUREMENT:

    ┌─────────────────────────────────────────────────────────────┐
    │                                                             │
    │   Fresh battery: 9.6V (open circuit)                       │
    │   Under load:    9.2V (drops due to internal resistance)   │
    │                                                             │
    │   Current:       I = V / R = 9.2V / 220Ω = 42mA            │
    │                                                             │
    │   Power:         P = V × I = 9.2V × 0.042A = 0.39W         │
    │                                                             │
    │   Battery capacity: 500mAh                                 │
    │   Theoretical runtime: 500mAh / 42mA ≈ 12 hours            │
    │                                                             │
    │   Actual runtime less due to:                              │
    │   ├── Voltage drops as battery discharges                  │
    │   ├── Internal resistance increases                        │
    │   └── Less efficient at high current                       │
    │                                                             │
    └─────────────────────────────────────────────────────────────┘
```

## Quick Reference Table

| Concept | Description | Key Formula |
|---------|-------------|-------------|
| Oxidation | Loss of electrons (anode) | M → Mⁿ⁺ + ne⁻ |
| Reduction | Gain of electrons (cathode) | N + ne⁻ → Nⁿ⁻ |
| Cell voltage | Potential difference | V_cell = V_cathode - V_anode |
| Internal resistance | Opposition to current | V_term = V_OCV - I × R_int |
| Power loss | Heat from internal resistance | P_loss = I² × R_int |
| Capacity | Charge stored | Ah = current × time |
| Energy | Work capacity | Wh = Ah × V |
| C-rate | Discharge rate relative to capacity | 1C = Ah in 1 hour |
| Efficiency | Energy out / energy in | η = E_out / E_in × 100% |
| Self-discharge | Capacity loss when idle | % per month or year |

## Summary

1. **Battery works** by converting chemical energy to electrical energy through redox reactions

2. **Oxidation** occurs at anode: loss of electrons (LEO)

3. **Reduction** occurs at cathode: gain of electrons (GER)

4. **Electrons flow** from anode (-) to cathode (+) through external circuit

5. **Ions flow** through electrolyte to complete the circuit internally

6. **Open circuit voltage** is measured with no load (highest voltage)

7. **Internal resistance** causes voltage drop under load: V_drop = I × R_int

8. **Higher internal resistance** = more voltage sag = less power to load

9. **Discharge curves** vary by chemistry (flat for NiMH/Li-ion, sloping for alkaline)

10. **Cold temperatures** increase internal resistance, reduce capacity

11. **High discharge rates** reduce effective capacity (Peukert effect)

12. **Battery aging** increases internal resistance, decreases capacity

13. **Self-discharge** causes capacity loss even when not in use

14. **NiMH standard** loses 20-30% per month; **LSD NiMH** loses <3% per month

15. **Li-ion** has best round-trip efficiency (85-95%)

16. **Charging** reverses chemical reactions (for secondary batteries only)

17. **Never charge primary batteries** (alkaline, zinc-carbon, lithium primary)

18. **End-of-life indicators:** swelling, leakage, reduced runtime, high internal resistance

*This documentation belongs to https://github.com/InterCentury*