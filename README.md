🔧 #Analog Temperature Control System – Two-Position (Bang-Bang) Regulation
This project presents the design and implementation of a complete analog temperature regulation system using two-position (bang-bang) control logic. The system was realized using discrete analog components and simulated within Proteus Design Suite, followed by the development of a custom PCB layout.

📐 #System Overview
The objective was to develop an autonomous temperature control system capable of maintaining a setpoint temperature by actuating either a heater (resistive lamp) or a fan depending on deviations from the desired temperature range. The project integrates principles of analog electronics, measurement systems, control theory, and PCB design.

🧩 #Key Components & Functional Blocks
🔌 ##Power Supply Unit
Designed to convert 230V AC / 50 Hz mains input into symmetrical ±12V DC outputs.

Implemented using a step-down transformer, Graetz bridge rectifier, smoothing capacitors, and linear voltage regulators (7812).

Ripple voltage was analyzed and minimized using appropriate capacitor and resistor sizing.

🌡️ #Temperature Sensing – Measurement Transducer
Utilized an NTC thermistor (NTCLE100E3103) within a Wheatstone bridge configuration.

A reference voltage source was created using a Zener diode (1N4737A) and an LM741 op-amp configured as a voltage follower.

The output signal, proportional to temperature variation, was used to drive the comparator.

⚙️ #Actuator Stage – Heater and Fan Control
Control logic executed via a relay (RTD34012F) driven by a BC141 transistor, dimensioned for saturation and cut-off operation.

Actuation signal toggles between a 230V AC heater and a 12V DC fan, depending on the temperature relative to set thresholds.

🧠 #Regulator – Schmitt Trigger Implementation
A Schmitt trigger was realized using a comparator configuration of the LM741 op-amp with hysteresis thresholds tuned via resistor feedback.

The regulator exhibits dual-threshold switching behavior, ensuring system stability and noise immunity during rapid temperature transitions.

🧪 #Simulation & Validation
All subsystems were independently modeled and validated in Proteus ISIS.

Simulated oscilloscope readings confirmed expected behaviors: regulated voltage levels, ripple minimization, and correct switching action in response to thermal changes.

The full system was integrated into a single schematic and subsequently designed as a two-layer PCB layout (including 2D and 3D views).

🧾 #Tools & Technologies Used
Proteus Design Suite – for circuit simulation and PCB layout

LTSpice-like simulations (within Proteus) – for ripple and comparator waveform analysis

Analog components only – no microcontrollers or digital logic

PCB layout with 3D visualization – for prototyping and practical deployment

🎯 #Outcome
The project successfully demonstrates:

Theoretical and practical knowledge of analog signal processing

Design of robust, noise-immune control logic (Schmitt trigger)

Practical power supply design with ripple suppression

Full analog control loop implemented without microcontrollers

Custom PCB design ready for fabrication and deployment
