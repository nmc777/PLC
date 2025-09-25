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

---

## Standard Diagram Layout
1. Table of Contents / Index  
2. Machine / Device Layouts  
3. High Voltage Distribution  
4. Low Voltage Distribution  
5. PLC / IO Sheets / Safety  
6. BOM (Bill of Materials)  
