# PLC & Industrial Controls Notes

## PanelView Plus: Standard vs Performance
- **Performance**
  - For large, complex, industrial systems.  
  - Higher processing power, memory, screen options, and enhanced connectivity.  
- **Standard**
  - For smaller, standalone systems.  
  - Limited processing power, memory, and screen size.  
- **Key Difference:** Different firmware and hardware.

---

## Pushbutton Types
- **Momentary Pushbutton** – Active only while pressed.  
- **Maintained Pushbutton** – Latches in pressed position until pressed again.  
- **Multistate Pushbutton** – More than 2 states; increments on each press.  

---

## Sensor Types
- **Diffuse Sensor** – Emits infrared light, detects reflection.  
- **Retroreflective Sensor** – Detects light cut off from reflector.  
- **Capacitive Sensor** – Detects capacitance changes (non-metal, e.g., plastic).  
- **Inductive Sensor** – Detects metal by magnetic field disruption.  
- **Proximity Sensor** – Detects close magnetic objects.  
- **Optical Sensor** – Uses light, longer range, but dirt sensitive.  
- **Ultrasonic Proximity Sensor** – Detects objects using high-frequency sound.  
- **Analog Sensor** – Converts physical quantity to voltage/current.  
- **Inductive Proximity Switch** – Different ranges for ferrous vs non-ferrous metals.  

---

## Example Machine Operation
- **Modes**: Manual / Auto.  
- **Emitter**: Produces Blue, Green, and Metal pieces.  
- **Infeed Conveyor**:
  - Uses capacitive + inductive sensors to classify (plastic vs metal).  
  - Could be replaced by a vision sensor.  
  - Counts raw parts.  
  - Moves forward by 1 each machine cycle.  
  - Must be sequenced to avoid overproduction.  
- **Machining Centre**:
  - HMI displays total assembled parts (plastic vs metal).  
  - Count based on:
    - Output sensor OR  
    - Machine completion bit matched to infeed scan.  
- **Outfeed Conveyor**:
  - Scaled (weight).  
  - Metal detection + pusher to side conveyor.  
  - Non-metal → popup sorter by color.  
- **Palletizer**:
  - Spawns pallets only when needed (least full or empty line).  
  - Sorted onto conveyor → stacked into inventory.  

---

## IO Categories
- Conveyor IO  
- Machining Center IO  
- Sensor IO  
- Weight Scale & Display IO  
- Pusher IO  
- Roller Pins Conveyor  
- Popup Wheel (L, R, F) IO  
- Palletizer IO  
- Chain Transfer IO  
- Auto/Manual Mode Selector IO  

---

## Signal Types
- **Analog**: 4–20 mA common.  
- **Digital/Binary Sensors**: Return 1+ bits (limit switch).  
- **Auxiliary Contact**: Relay status feedback.  

---

## Valves
- **Directional Control / Solenoid / Spool Valves**  
- Limit switches can handle high current.  
- Most applications → **meter-out** flow control.  
- **5/3 valve** → 5 ports, 3 positions.  
- **Meter-in vs Meter-out** – speed regulation method.  
- **Shielded vs Unshielded Mounting** – affects sensing range.  

---

## Sensor Characteristics
- **Through Beam Sensors** → Longest range.  
- **Diffuse Photoelectric with Background Suppression** → Learns to ignore background objects.  

---
## Industrial Control Devices
### Solid State Relay (SSR)

  SSRs can be used for:
  -High speed applications
  -High vibration environemnts
  -Applications where a relay needs to be located near sensitive automation components (PLCs, HMI's, temperature controls)
  -Dusty or humid environments
  -
    SSR's can fail closed or open
    The solid State relay has no moving components and is replaying EMRs due to ease of use, low nose production, extra safety feautures and long lifespan
    SSR's produce a lot of heat and need heat sinks for dissipation
## Contorl Relays
A control relay is a swithc controlled by a electircal current. There are 2 types, EMR, and SSR.
A  contorl relay will consist of a coul and a combinaiton of N.O nad N.C dry contacts. Relays open and close contacts in another
electical circuit.
### Electromechanical Relay
  Built to fail open or closed,if wired to desirable failure mode.
  Make clack noise when switched on, and erode during prolonged switching\
  Shorter lifespan that SSR 
### Limit Switch
  Used to get inputs from moving parts of a machine
  Mechanical switch tat uses contact with a part to physically move its internal contacts
  No electronics built inside (Dry Contact)
  Often used with "Door closed" or "Part PResent"
### Contactor
Devices used to establish and disconnect power to a load (lights,heaters transformers)
AC contactors generally have multiple contacts. DC contactors generally have one.
They also have AUX contacts used to control other components.

### Motor Contactor
Used to start and stop motors, a motor starter is equipped with na overload relay. A Contact is not. The overload relay has bimetallic sensors that disconnect the circuit.
## Diagram Types

### Pictorial Diagram
- Uses pictures of components.  
- Shows more detail than wiring diagrams.
    

### Wiring Diagram
- Shows connections + assembly details.  
- Simplified pictorial, arranged like physical layout.  

### Ladder / Line / Schematic Diagram
- Most common for PLC/controls.  
- Inputs on left, outputs on right.  
- Shows circuit logic, not physical layout.  
- Includes voltages, test points, etc.  

### Single Line Diagram
- Minimalistic: 1 line represents many (e.g., 3-phase power).  
- Used in **power distribution drawings**.  
- Includes Cable ID, Wire ID, Junction Box ID.  
- Divided into: Power Circuit, Instrumentation Circuit, Control Circuit.

### Wiring References

<img width="897" height="276" alt="wiring references" src="https://github.com/user-attachments/assets/7f687232-18f9-4abf-96dc-4e580596f3e9" />

### Wiring Numbers
<img width="900" height="438" alt="image" src="https://github.com/user-attachments/assets/2ce3e13e-da5d-46ba-874d-0637fb8dab92" />
<img width="1004" height="460" alt="image" src="https://github.com/user-attachments/assets/a999b0ee-1f6c-440f-8129-58eb964d9cd6" />
### 3 Phase Wiring Numbers
<img width="963" height="472" alt="image" src="https://github.com/user-attachments/assets/c89839d7-922a-42fd-a87b-a4d025c0e804" />
### Wiring Number Changes
<img width="969" height="455" alt="image" src="https://github.com/user-attachments/assets/27cfb47d-c6f1-4338-be63-832ecb55f649" />
<img width="1024" height="459" alt="image" src="https://github.com/user-attachments/assets/a4b0526b-0c8a-4ef5-8d32-cbaa5082f5ec" />
Because the voltages stay the same it does not change wire numbers
<img width="1015" height="462" alt="image" src="https://github.com/user-attachments/assets/b5834a96-fba2-4407-87ef-f0e57de6295f" />
### Device Nunmbers
<img width="916" height="406" alt="image" src="https://github.com/user-attachments/assets/b10a78e8-2974-442d-b9fb-b111ae6f3bbd" />
<img width="970" height="456" alt="image" src="https://github.com/user-attachments/assets/f2f823bd-c64d-46ce-b6b7-b4b890d22eb8" />
<img width="1013" height="470" alt="image" src="https://github.com/user-attachments/assets/9cb9d8d4-bf70-4c29-b109-3fb8666ef5a7" />


## Motor Control and Proteciton
  A manual control circuit requires a person to initiate an action for the circuit to operate.
  A motor goes through 3 stages during normal operation:
  Resting
  Starting
  A motor that is starting draws in a major inruhs current (normally 6-8 times the Running current)
  When starting, fuses or crcuit breakers must have a sufficiently high ampere rating to avoid immediate opening of the circuit.
  Operating under load         

  ### Locked Rotor Current
  Higest level of inrush current which occurs the moment the motor is turned on.
  ### Fully Loaded Current
  Current level required to produce full load torque on the motor shaft at rated speed.
  ### Ambient Temperature
  Tempurature of air surrounding a piece of euipment.
  ### Temperature Rise
  The difference between the winding tempurate of a running motor and its ambient temperature. The temperature rise at FLC is not harmful providd that the ambient rempaerature
  does not exceed the ambient temperature limit.
  
---

## Standard Diagram Layout
1. Table of Contents / Index  
2. Machine / Device Layouts  
3. High Voltage Distribution  
4. Low Voltage Distribution  
5. PLC / IO Sheets / Safety  
6. BOM (Bill of Materials)  
