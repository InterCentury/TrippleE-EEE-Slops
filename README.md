# DOCS - EEE - Slops

```
This repository is a collection of personal notes and simplified documentation about basic electrical and electronics concepts.

Honestly, I’m not a big fan of EEE as a major. But at the same time, I understand that having a clear idea about these fundamentals is essential—especially for fields like robotics, embedded systems, and hardware-related projects.

```
## 🎯 Purpose

- ``` >>> ``` Build a strong **basic understanding** of electricity and electronics  
- ``` >>> ``` Focus only on **practical and useful concepts**  
- ``` >>> ``` Bridge the gap between **CSE → Robotics / Hardware**  
- ``` >>> ``` Keep everything **simple, structured, and beginner-friendly**

## 📚 What’s inside

This repo includes organized notes on:

- ⚡``` >>> ```Electricity basics (Voltage, Current, Resistance, AC/DC)
- 🔋``` >>> ```Batteries and power systems  
- 🔌``` >>> ```Circuits and grounding  
- ⚙️``` >>> ```Motors (including 775 motor and control basics)  
- 🧠``` >>> ```Electronics fundamentals  
- 🤖``` >>> ```Microcontrollers and robotics bridge  
- 🛠️``` >>> ```Practical projects and debugging  






 
 ### Repostiry sturucture
 
 ```
File Tree: (DOCS) --  EEE slops
Generated on: 5/8/2026, 11:50:13 PM
Root path: h:\programming\git_and_github\TrippleE-EEE-Slops\(DOCS) --  EEE slops
────────────────────────────────────────────────────────────────────────────────

├── 📁 01-basics/
│   ├── 📝 01.01 what-is-electricity.md
│   ├── 📝 01.02 atoms-electrons.md
│   ├── 📝 01.03 current.md
│   ├── 📝 01.04 voltage.md
│   ├── 📝 01.05 resistance.md
│   ├── 📝 01.06 ohms-law.md
│   ├── 📝 01.07 power-watt.md
│   ├── 📝 01.08 ac-vs-dc.md
│   └── 📝 01.09 frequency.md
├── 📁 02-electricity-types/
│   ├── 📝 02.01 - DC Electricity.md
│   ├── 📝 02.02 AC Electricity.md
│   ├── 📝 02.03 sine-wave.md
│   ├── 📝 02.04 transformers.md
│   ├── 📝 02.05 adapters.md
│   └── 📝 02.06 - AC vs DC Efficiency and Use Cases.md
├── 📁 03-components/
│   ├── 📝 03.01 wires.md
│   ├── 📝 03.02 resistors.md
│   ├── 📝 03.03 capacitors.md
│   ├── 📝 03.04 inductors.md
│   ├── 📝 03.05 diodes.md
│   ├── 📝 03.06 transistors.md
│   ├── 📝 03.07 relays.md
│   ├── 📝 03.08 switches.md
│   └── 📝 03.09 breadboard.md
├── 📁 04-power-systems/
│   ├── 📁 batteries/
│   │   ├── 📁 Battery - types/
│   │   │   ├── 📝 types - 01 lead-acid.md
│   │   │   ├── 📝 types - 02 lithium-ion.md
│   │   │   ├── 📝 types - 03 lithium-polymer.md
│   │   │   ├── 📝 types - 04 nickel-cadmium.md
│   │   │   ├── 📝 types - 05 nickel-metal-hydride.md
│   │   │   └── 📝 types - 06 alkaline.md
│   │   ├── 📁 safety/
│   │   │   ├── 📝 safety - 1 overcharging.md
│   │   │   ├── 📝 safety - 2 overheating.md
│   │   │   ├── 📝 safety - 3 battery-explosion.md
│   │   │   └── 📝 safety - 4 safe-handling.md
│   │   ├── 📝 batteries - 0 battery-selection.md
│   │   ├── 📝 batteries - 1 what-is-battery.md
│   │   ├── 📝 batteries - 2 how-battery-works.md
│   │   ├── 📝 batteries - 3 voltage-capacity.md
│   │   ├── 📝 batteries - 4 charging-basics.md
│   │   └── 📝 batteries - 5 series-vs-parallel.md
│   ├── 📝 04.ps - adapters.md
│   ├── 📝 04.ps - dc-to-ac-inverter.md
│   ├── 📝 04.ps - power-supply.md
│   └── 📝 04.ps - voltage-regulators.md
├── 📁 05-circuits/
│   ├── 📁 grounding/
│   │   ├── 📝 05.06 what-is-grounding.md
│   │   ├── 📝 05.07 types-of-grounding.md
│   │   ├── 📝 05.08 earthing-vs-grounding.md
│   │   ├── 📝 05.09 why-grounding-important.md
│   │   └── 📝 05.10 real-world-grounding.md
│   ├── 📝 05.01 what-is-circuit.md
│   ├── 📝 05.02 series-circuit.md
│   ├── 📝 05.03 parallel-circuit.md
│   ├── 📝 05.04 short-circuit.md
│   ├── 📝 05.05 open-circuit.md
│   └── 📝 05.11 circuit-analysis-basics.md
├── 📁 06-measuring-tools/
│   ├── 📝 06.01 multimeter.md
│   ├── 📝 06.02 measuring-voltage.md
│   ├── 📝 06.03 measuring-current.md
│   ├── 📝 06.04 continuity-test.md
│   └── 📝 06.05 safety-measuring.md
├── 📁 07-motors/
│   ├── 📝 07.01 what-is-motor.md
│   ├── 📝 07.02 dc-motor.md
│   ├── 📝 07.03 ac-motor.md
│   ├── 📝 07.04 brushed-vs-brushless.md
│   ├── 📝 07.05 775-motor.md
│   ├── 📝 07.06 motor-specs.md
│   └── 📝 07.07 motor-control.md
├── 📁 08-electronics-basics/
│   ├── 📝 08.01 analog-vs-digital.md
│   ├── 📝 08.02 logic-gates.md
│   ├── 📝 08.03 pwm.md
│   ├── 📝 08.04 signal-basics.md
│   └── 📝 08.05 sensors-intro.md
├── 📁 09-microcontrollers/
│   ├── 📝 09.01 what-is-mcu.md
│   ├── 📝 09.02 arduino-basics.md
│   ├── 📝 09.03 gpio.md
│   ├── 📝 09.04 pwm-control.md
│   ├── 📝 09.05 sensor-reading.md
│   └── 📝 09.06 simple-projects.md
├── 📁 10-robotics-bridge/
│   ├── 📝 10.01 motors-with-code.md
│   ├── 📝 10.02 motor-driver.md
│   ├── 📝 10.03 l298n.md
│   ├── 📝 10.04 power-management.md
│   ├── 📝 10.05 sensors-usage.md
│   ├── 📝 10.06 line-follower.md
│   └── 📝 10.07 obstacle-robot.md
├── 📁 11-practical/
│   ├── 📝 11.01 build-led-circuit.md
│   ├── 📝 11.02 build-fan.md
│   ├── 📝 11.03 battery-project.md
│   ├── 📝 11.04 motor-project.md
│   └── 📝 11.05 debugging.md
├── 📁 12-common-mistakes/
│   ├── 📝 12.01 wrong-voltage.md
│   ├── 📝 12.02 short-circuit.md
│   ├── 📝 12.03 overheating.md
│   ├── 📝 12.04 bad-wiring.md
│   └── 📝 12.05 cheap-components.md
└── 📁 13-cheatsheets/
    ├── 📝 13.01 formulas.md
    ├── 📝 13.02 symbols.md
    ├── 📝 13.03 units.md
    └── 📝 13.04 quick-guide.md



 ```

## ⚠️ Note

These are learning notes, not perfect or complete documentation.  
Things may improve over time as knowledge grows.
