# 🔧 Analog Temperature Control System – Two-Position (Bang-Bang) Regulation

This project presents the design and implementation of a complete analog temperature regulation system using two-position (bang-bang) control logic. The system was developed using discrete analog components, simulated in **Proteus Design Suite**, and finalized with a custom **PCB layout**.

---

## 📐 System Overview

The objective of the system is to autonomously maintain a target temperature by switching between a **heater** and a **fan** based on sensor feedback. The design combines analog electronics, signal conditioning, control theory, and PCB design principles, fully realized using only analog components—no microcontrollers involved.

---

## 🧩 Key Components & Functional Blocks

### 🔌 Power Supply Unit
- Converts **230V AC / 50 Hz** mains to **±12V DC** using:
  - Step-down transformer (dual secondary)
  - Full-bridge rectifier (Graetz configuration)
  - Filtering capacitors (470µF electrolytic)
  - Linear voltage regulators (**7812**)
- Ripple analysis and smoothing capacitor dimensioning were carried out analytically and verified in simulation.

### 🌡️ Temperature Sensing – Measurement Transducer
- **NTC thermistor** integrated into a **Wheatstone bridge**
- **Reference voltage** generated using:
  - **Zener diode** (1N4737A, 7.5V)
  - Voltage divider with potentiometer
  - **LM741 op-amp** as voltage follower
- Output voltage varies with temperature, used as input to the control circuit.

### ⚙️ Actuator Stage – Heater and Fan Control
- Actuated by a **relay (RTD34012F)** driven by a **BC141** transistor
- Heater: connected to **230V AC**
- Fan: powered by **12V DC**
- Control ensures that either the heater or fan is active at any time (exclusive switching)
- Flyback diode (1N4001) used for relay protection

### 🧠 Regulator – Schmitt Trigger Implementation
- **LM741-based** comparator with hysteresis
- Implements **two-position control** by comparing temperature voltage to upper/lower thresholds
- Adjustable hysteresis band via resistor tuning
- Stable operation with noise immunity due to positive feedback

---

## 🧪 Simulation & Validation

- All modules simulated in **Proteus ISIS** with oscilloscopic verification:
  - DC regulation and ripple behavior
  - Transducer linearity with respect to temperature
  - Relay operation and switching behavior
  - Comparator hysteresis thresholds and output logic

- **Final schematic** integrates all components into a complete, functioning analog feedback loop for temperature regulation.

---

## 🧾 Tools & Technologies Used

- 🎛️ **Proteus Design Suite** (ISIS + ARES)
- 🧠 **LM741** operational amplifiers
- 🌡️ **NTCLE100E3103** NTC thermistor
- 🔌 **7812** linear voltage regulators
- ⚙️ **Relay RTD34012F**
- 🧲 **BC141** NPN transistor
- 🔩 Zener diode, potentiometers, LED indicators
- 🧾 2D and 3D PCB design with component layout visualization

---

## 🎯 Outcome

This project successfully demonstrates:

- Theoretical and practical knowledge of analog electronics
- Analog implementation of a temperature control loop
- Ripple reduction and power supply design
- Functional separation between sensing, regulation, and actuation
- Design-for-manufacture approach through custom PCB development

---

## 🧑‍🔬 Author & Context

This project was completed as part of the **"Praktikum Elektrotehnike i Elektronike"** course  
🎓 Faculty of Electrical Engineering, University of Sarajevo  
🧑‍🎓 **Student:** Demir Hasičić  
🧑‍🏫 **Mentor:** Prof. Dr. Abdulah Akšamović  
📅 **Date:** June 2021  
