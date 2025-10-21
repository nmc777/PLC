

### Wiring Diagram
- Shows connections + assembly details.  
- Simplified pictorial, arranged like physical layout.  

### Ladder / Line Diagram
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

# PLC & Industrial Controls Reference Guide

---

## Table of Contents

1. [HMI Systems](#1-hmi-systems)
2. [Input Devices](#2-input-devices)
   - 2.1 [Pushbutton Types](#21-pushbutton-types)
   - 2.2 [Sensor Types](#22-sensor-types)
   - 2.3 [Limit Switches](#23-limit-switches)
3. [Control Devices](#3-control-devices)
   - 3.1 [Relays](#31-relays)
   - 3.2 [Contactors](#32-contactors)
4. [Motor Control](#4-motor-control)
   - 4.1 [Motor Operating Stages](#41-motor-operating-stages)
   - 4.2 [Current Types](#42-current-types)
   - 4.3 [Temperature Specifications](#43-temperature-specifications)
   - 4.4 [Motor Protection](#44-motor-protection)
5. [Valve Systems](#5-valve-systems)
6. [Signal Types](#6-signal-types)
7. [Diagram Types](#7-diagram-types)
8. [Wiring Standards](#8-wiring-standards)
9. [Example System Architecture](#9-example-system-architecture)
10. [Quick Reference Tables](#10-quick-reference-tables)

---

## 1. HMI Systems

### PanelView Plus Comparison

| Feature | Standard | Performance |
|---------|----------|-------------|
| **Application** | Smaller, standalone systems | Large, complex industrial systems |
| **Processing Power** | Limited | High |
| **Memory** | Limited | Enhanced |
| **Screen Options** | Limited sizes | Multiple size options |
| **Connectivity** | Basic | Enhanced |
| **Firmware/Hardware** | Different architecture | Different architecture |

---

## 2. Input Devices

### 2.1 Pushbutton Types

| Type | Description | Behavior |
|------|-------------|----------|
| **Momentary** | Active only while pressed | Returns to default state when released |
| **Maintained** | Latches in position | Stays pressed until pressed again |
| **Multistate** | More than 2 states | Increments through states on each press |

### 2.2 Sensor Types

| Sensor Type | Detection Method | Best Use Case | Notes |
|-------------|------------------|---------------|-------|
| **Diffuse** | Infrared light reflection | General object detection | Short to medium range |
| **Retroreflective** | Light interruption from reflector | Long-range detection | Requires reflector installation |
| **Through Beam** | Direct light beam interruption | Longest range applications | Emitter and receiver separate |
| **Capacitive** | Capacitance changes | Non-metallic materials (plastic, liquid) | Can detect through containers |
| **Inductive** | Magnetic field disruption | Metal detection | Different ranges for ferrous vs non-ferrous |
| **Inductive Proximity** | Magnetic field | Metal proximity detection | Range varies by metal type |
| **Proximity** | Magnetic field | Close-range magnetic objects | Limited range |
| **Optical** | Light beam | Long-range detection | Sensitive to dirt/contamination |
| **Ultrasonic** | High-frequency sound waves | Various materials | Works in dusty environments |
| **Analog** | Physical quantity conversion | Continuous measurement | Outputs voltage/current signal |
| **Diffuse with Background Suppression** | Learned background filtering | Cluttered environments | Ignores background objects |

### 2.3 Limit Switches

- **Function**: Obtain inputs from moving machine parts
- **Operation**: Mechanical contact physically moves internal contacts
- **Construction**: No internal electronics (dry contact)
- **Common Uses**: 
  - Door position sensing ("Door Closed")
  - Part presence detection ("Part Present")

---

## 3. Control Devices

### 3.1 Relays

#### Control Relay Overview
A switch controlled by electrical current consisting of a coil and combination of N.O. (Normally Open) and N.C. (Normally Closed) dry contacts. Opens and closes contacts in another electrical circuit.

#### Electromechanical Relay (EMR)

| Characteristic | Description |
|----------------|-------------|
| **Failure Mode** | Built to fail open or closed (configurable) |
| **Operation** | Makes audible "clack" noise when switched |
| **Wear** | Contact erosion during prolonged switching |
| **Lifespan** | Shorter than SSR |
| **Noise** | Audible operation |

#### Solid State Relay (SSR)

| Characteristic | Description |
|----------------|-------------|
| **Moving Parts** | None |
| **Heat Generation** | Significant (requires heat sinks) |
| **Noise** | Silent operation |
| **Lifespan** | Longer than EMR |
| **Failure Mode** | Can fail open or closed |
| **Safety Features** | Enhanced compared to EMR |

**SSR Applications:**
- High-speed switching applications
- High-vibration environments
- Near sensitive automation components (PLCs, HMIs, temperature controls)
- Dusty or humid environments

### 3.2 Contactors

#### General Contactors

| Type | Contacts | Purpose |
|------|----------|---------|
| **AC Contactor** | Multiple contacts | Establish/disconnect power to loads (lights, heaters, transformers) |
| **DC Contactor** | Generally one contact | Establish/disconnect DC power |

**Features:**
- Include auxiliary (AUX) contacts for controlling other components
- Used for high-power switching applications

#### Motor Contactors/Starters

**Key Difference**: Motor starter includes an overload relay; basic contactor does not.

**Overload Protection:**
- Bimetallic sensors monitor current
- Automatically disconnect circuit during overload conditions
- Heating elements act as sensing components (not switches)
- Trigger auxiliary contacts that open the circuit

**Voltage Considerations:**
- 240V starters contain TWO load contacts
- 240V systems use two hot wires at 120V each (two-phase systems)

---

## 4. Motor Control

### 4.1 Motor Operating Stages

| Stage | Description |
|-------|-------------|
| **Resting** | Motor is stopped, no current draw |
| **Starting** | High inrush current (6-8× running current) |
| **Operating Under Load** | Steady-state current at rated speed |

### 4.2 Current Types

| Current Type | Description | Typical Value |
|--------------|-------------|---------------|
| **Locked Rotor Current** | Highest inrush current at startup | 6-8× FLC |
| **Fully Loaded Current (FLC)** | Current required for full load torque at rated speed | Nameplate rating |

### 4.3 Temperature Specifications

| Parameter | Definition |
|-----------|------------|
| **Ambient Temperature** | Temperature of air surrounding equipment |
| **Temperature Rise** | Difference between winding temperature and ambient temperature during operation |

**Note**: Temperature rise at FLC is acceptable if ambient temperature stays within equipment limits.

### 4.4 Motor Protection

**Fuse/Circuit Breaker Sizing:**
- Must have sufficiently high ampere rating to accommodate startup inrush current
- Prevents nuisance tripping during normal motor starting

**Three-Phase Systems:**
Used in:
- HVAC systems
- Water pumps
- Machine shop machinery

---

## 5. Valve Systems

### Valve Types

| Type | Description |
|------|-------------|
| **Directional Control Valve** | Controls flow direction |
| **Solenoid Valve** | Electrically operated valve |
| **Spool Valve** | Uses sliding spool to control flow |

### Valve Specifications

**5/3 Valve**: 5 ports, 3 positions

### Flow Control Methods

| Method | Description | Application |
|--------|-------------|-------------|
| **Meter-In** | Controls flow entering actuator | Speed regulation |
| **Meter-Out** | Controls flow exiting actuator | Most common application |

### Installation Considerations

| Mounting Type | Effect |
|---------------|--------|
| **Shielded** | Reduced sensing range |
| **Unshielded** | Increased sensing range |

---

## 6. Signal Types

| Signal Type | Description | Common Standard |
|-------------|-------------|-----------------|
| **Analog** | Continuous signal | 4-20 mA |
| **Digital/Binary** | Discrete on/off signal | Returns 1+ bits |
| **Auxiliary Contact** | Relay status feedback | Dry contact |

---

## 7. Diagram Types

### Diagram Comparison Table

| Diagram Type | Purpose | Key Features |
|--------------|---------|--------------|
| **Pictorial** | Visual component representation | Uses component pictures, most detailed |
| **Wiring** | Physical connections | Shows assembly details and physical layout |
| **Ladder/Line** | Logic representation | Inputs left, outputs right; shows circuit logic |
| **Single Line** | Power distribution | One line represents multiple (e.g., 3-phase) |

### Line Diagram Details

**Most Common for PLC/Controls**

**Layout:**
- Inputs positioned on left side
- Outputs positioned on right side
- Shows circuit logic (not physical layout)
- Includes voltages and test points

**Line Identification:**
- Sequential line reference numbers
- Numbered from top to bottom
- Distinguishes each line uniquely

**Cross-Reference Systems:**
- Numerical references trace auxiliary contacts
- Links controls across motor starters, relays, and contactors
- Dashed lines indicate mechanical connections

### Single Line Diagram

**Purpose**: Power distribution drawings

**Circuit Types:**
1. Power Circuit
2. Instrumentation Circuit
3. Control Circuit

**Includes:**
- Cable ID
- Wire ID
- Junction Box ID

### Wiring Diagram

**Characteristics:**
- Pictorial representation
- Illustrates physical connections
- Shows actual location of connections
- Arranged like physical layout
- Simplified pictorial format

---

## 8. Wiring Standards

### Wire Numbering Rules

**General Principles:**
- Wires maintain numbers when voltage remains constant
- Numbers change when passing through components that change voltage
- Sequential numbering system for organization

### Device Numbering

Components are numbered sequentially for identification and troubleshooting purposes.

---

## 9. Exercise 3.

### Circuit Breakjers
-Will trip during an overcurrent for protection
-GCFI will trip if there is an imbalacne between hot and neutral
### Timing Relays (TR)
-Introduces a Time Delay before Opening or Closing Contacts.
-Acts as a switch that waits for a pre-determined amount of time to pass before
changing its state
### Heating Elements
-The heating elements (heaters) installed in motor starters **do not open during an overload** 
- Heating elements are designed to protect the otor from overheating due to excessive current
- The heat causes the bimetalleic strip to bend or trigger which then de-energises the contactor coil and stops the motor.
### AC Operated Solenoids
-Use laminated metal core to reduce heat caused by eddy currents
### Shading Coils
- Used with AC relays and contactors to reduce chatter when the device is turned on.
### Solid State Relays
-When a SSR is used to control a AC load. The load is connected in series with a Triac.
-No mechanical moving parts, use Diodes, Transistors, Thyristors, Triacs.
-Instead of mechanical moving contactors, it converts electrical signals to Optical, by triggering an LED which sines across a small gap onto a photosensitive device.
### What is a Clapper Relay? (Low VoltagE)
-1 Moveable, 1 Stationary Contact
- When the circuit is closed, the movable mechanical component called the "clapper" is pulled to the magnetic coil, the pushrod moves forward the contacts.
-It is possible to control many different circuits at the same time.
-If pushrod is damaged, the lower contacts may be pushed, but not upper contacts
-Cannot be used to control High Voltages
### What is OptoIsolation?
- Optoisolation is used in SSRs to seperate the outputs using a lightbeam. This prevents electrical noise being transmitted to the control side of the circuit

### Bridge Type Contacts (High Voltage)
- 1 Moveable, 2 Stationary Contacts.
- Can be used to control High Voltage
-Bridge shaped moveable contact that switches on or off to physically bridge two stationary contacts together, allowing it to break or make a connection at two points simultaneously, imagine 2 N.O contacts being triggered
at the same time.

### Silver Alloys & Siwtching Contacts
- We use Silver Alloys on switching contacts (such as Bridge Relays) because its arc resistant, low resistantce material with good mechanical strength to endure many opening  abd closings.
- When silver oxidizes it creates an excellent conductor.

### Arc Supression
-Arc supression is requred on contacts and motor starters because of the extremely high voltage and current from arc flashes which make equipment
suceptible to damage.
### DC Arc Suppression
-DC Currents also can cause Arcs, these are more difficult to extingusih because of the continuous flow DC supply causes. Whilst AC goes back an forth giving downtime.
### Solenoid
-Solenoids consist of a Coil , Frame and Plunger
Coil: Creates magnetic field when current is passed through.causes plunger to move
Plunger: Usually a metal rod that can slide in and out of a coil. This si the moving part of the solenoid.
Frame: Houses all the components. Often made of metal or plastic.


## 9. Example System Architecture

### Production Line IO Categories

| Category | Description |
|----------|-------------|
| **Conveyor IO** | Belt control and monitoring |
| **Machining Center IO** | Processing equipment interface |
| **Sensor IO** | Detection and measurement devices |
| **Weight Scale & Display IO** | Weighing system interface |
| **Pusher IO** | Part routing mechanisms |
| **Roller Pins Conveyor** | Material handling |
| **Popup Wheel IO** | Sorting mechanisms (Left, Right, Forward) |
| **Palletizer IO** | Stacking and organizing |
| **Chain Transfer IO** | Product transfer systems |
| **Auto/Manual Mode Selector IO** | Operation mode control |

### System Operation Modes

| Mode | Description |
|------|-------------|
| **Manual** | Operator-controlled operation |
| **Auto** | Automated sequence control |

### Example Production Process

#### Emitter Station
Produces three part types:
- Blue (plastic)
- Green (plastic)
- Metal

#### Infeed Conveyor
- **Sensors**: Capacitive + Inductive (classifies plastic vs metal)
- **Alternative**: Vision sensor
- **Function**: Counts raw parts
- **Movement**: Advances one position per machine cycle
- **Control**: Sequenced to prevent overproduction

#### Machining Centre
- **HMI Display**: Total assembled parts (separated by plastic/metal)
- **Counting Methods**:
  - Output sensor detection, OR
  - Machine completion bit matched to infeed scan

#### Outfeed Conveyor
**Processing Stages:**
1. **Weighing**: Scale measures part weight
2. **Metal Detection**: Identifies metal parts
3. **Metal Routing**: Pusher diverts to side conveyor
4. **Non-metal Sorting**: Popup sorter by color

#### Palletizer
- **Intelligence**: Spawns pallets only when needed
- **Strategy**: Routes to least full or empty line
- **Process**: Parts sorted onto conveyor → stacked into inventory

---

## 10. Quick Reference Tables

### Control Language & Documentation

| Term | Definition |
|------|------------|
| **Control Language** | Communicates function of electrical components and establishes device understanding |
| **Purpose** | Facilitates control circuit design and troubleshooting |

### Standard Documentation Layout

| Section | Content |
|---------|---------|
| 1 | Table of Contents / Index |
| 2 | Machine / Device Layouts |
| 3 | High Voltage Distribution |
| 4 | Low Voltage Distribution |
| 5 | PLC / IO Sheets / Safety |
| 6 | BOM (Bill of Materials) |

### Sensor Range Comparison

| Sensor Type | Relative Range |
|-------------|----------------|
| Through Beam | Longest |
| Retroreflective | Long |
| Diffuse with Background Suppression | Medium |
| Diffuse | Medium-Short |
| Proximity | Short |

### Key Definitions

| Term | Definition |
|------|------------|
| **Manual Control Circuit** | Requires person to initiate action for operation |
| **Dry Contact** | Mechanical contact with no internal electronics |
| **Auxiliary Contact** | Provides relay/contactor status feedback |
| **N.O. (Normally Open)** | Contact open when device is de-energized |
| **N.C. (Normally Closed)** | Contact closed when device is de-energized |

---

## Index

**A**
- Ambient Temperature, 4.3
- Analog Sensors, 2.2, 6

**C**
- Capacitive Sensors, 2.2
- Contactors, 3.2
- Control Language, 10
- Control Relays, 3.1
- Current Types, 4.2

**D**
- Diagram Types, 7
- Diffuse Sensors, 2.2
- Digital Signals, 6

**E**
- Electromechanical Relay (EMR), 3.1

**F**
- Flow Control, 5
- Fully Loaded Current (FLC), 4.2

**H**
- HMI Systems, 1

**I**
- Inductive Sensors, 2.2
- IO Categories, 9

**L**
- Ladder Diagrams, 7
- Limit Switches, 2.3
- Line Diagrams, 7
- Locked Rotor Current, 4.2

**M**
- Maintained Pushbutton, 2.1
- Meter-In/Meter-Out, 5
- Momentary Pushbutton, 2.1
- Motor Control, 4
- Motor Protection, 4.4
- Multistate Pushbutton, 2.1

**O**
- Optical Sensors, 2.2
- Overload Protection, 3.2, 4.4

**P**
- PanelView Plus, 1
- Pictorial Diagrams, 7
- Proximity Sensors, 2.2
- Pushbuttons, 2.1

**R**
- Relays, 3.1
- Retroreflective Sensors, 2.2

**S**
- Sensor Types, 2.2
- Signal Types, 6
- Single Line Diagrams, 7
- Solid State Relay (SSR), 3.1

**T**
- Temperature Rise, 4.3
- Through Beam Sensors, 2.2

**U**
- Ultrasonic Sensors, 2.2

**V**
- Valves, 5

**W**
- Wiring Diagrams, 7
- Wiring Standards, 8

---

*Document Version: 1.0*  
*Last Updated: October 2025*
