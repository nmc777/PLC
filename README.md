# PLC

Panelview Plus Standard vs Performance
Performance is designed for large, complex, industrial systems, offering higher processing power, memory, screen options and enhanced connectivity.
Standard is for smaller, standalone systems with less processing power, limited memory, smaller screen size.
Both use differenct firmware and hardware.

Momentary Pushbutton
Only active during its duration of being pressed, until release.

Maintained Pushbutton
Changes position when pressed, and latches in that position.

Multistate Pushbutton
Same as maintained, but you have more than 2 states. When you click the button, it goes to the next state. Thus it increments by 1 each click.

Diffuse Sensor
Emit infrared light, and detect the reflected light from an object back into the sensor.

Retroreflective Sensor
Emits light tworads sensor on opposite end, when this is cut off, the sensor indicates an object present.

Capactive Sensor
Detect changes in capacitance wehn an object approaches the sensor. For plastic, non-metal

Inductive Sensor
Detect metal objects whent hey enter the field. Disrupts magnetic field.

The machine will have Manual, Auto mode.
There will be a emitter,
It will spew Blue,Green,Metal, pieces. (plastic and metal)
Upon infeed conveyor entry it will be scanned by a capactive and inductive sensor (will a vision sensor accomplish the same?)
to identify a count of the RAW parts produced via metal or plastic.
There will be a lineup waiting at the infeed, so everytime a part is finally done in the machine cycle, the conveyor will move uo by 1. This means that the emitter must be in sequence so it doesnt overproduce parts during the wait.
On the Machining Centre will be an HMI that displays total ASSEMBLED parts produced via metal and plastic, this may need a sensor at the output of the machining sensor to identify assembled parts. OR you can wait for completion bit to finish form machining centre and 
apply count based on what was scanned by the infeed sensor.
On outfeed, it will be scaled,after the scaling cycle, it will move forward and then a sensor will detect if its a metal piece, if it is a pusher will slide it over to the next conveyor, if not. It enters the popup sorter and is sperated by color.
The palletizer will spawn pallets based on what line does not have a pallet/needs one/least full and will not generate one until needed. Once a pallet is made it will all be sorted on one conveyor and then stacked in inventory.
Metal parts can be

Conveyor IO
Machining Center IO
Sensors IO
Weight scale & display IO
Pusher IO
Roller Pins Conveyor
Pop up wheel L,R,F IO
Palletizer IO
Chain Transer IO
Timers based on sensors,
Emitter spawning base don sensor.
Parts created (type) vs Parts Produced.
Auto Manual Mode Selector IO

The most ocmmonly used trigger signals are between 4-20ma
Digital Sesory / Binary Sensor
Returns 1 or more bits of information per sensor, usually triggered by a limit switch (a witch that closes the circuit when it reaches its final position).

Proximity Sensor
USed for detecting close magnetic objects using magtic fields, these have replaced limit switches
Optical Sensors
Much longer range, but suceseptible to dirt and other interferences because they use light as a signal.
Capactivive Sensor
Fror non metal materials, historically have nobeen bery ependable
Ultrasonic Prox sensor
Detet objects using hig frequency sound, sucseptible to dirt and enviornmental interference,
Auxillary Contact
Part of a relay , these tell us whne whatever is controlling the relay is turne don or off.
Analog Sesor
Converts quantity into voltage or current (temp pressure humidity distance speed)
Inductice Proximity Switch
Do not sense metals all the same, they have different sensing ranges for non ferrous and ferrous metals.

Directional Control Valves / Solenoid Valves/ Spool Valves 

Limit switches are able to handle high amoutns of current due to their size.
Most applications default to meter-out for control speed regulation
Through Beam Sensors have the longest range.
A diffuse photoelectric sensor that is able to be taught to ignore objects in the background uses a technique known as Background Suppression
	
If you have a 5/3 valve the 5 represents the number of ports the valve has
Meter in vs Meter Out

Shielded & Unshielded Mounting Options

Diagrams
A typical layout of an industrial control system consists of the following
-Table of Contents/Index
-Machine/Deice Layouts
-High Voltage Distribution
-Low Voltage Distribution
-PLC/IO Sheets/ Safety
-BOM

Electrical Diagram Types
-Pictorial Diagram
	Uses pictures to represent different components and often shows more detail than a wiring 		diagram
-Wiring Diagram
	Contain assembly connection information
	Diagram that is a simpolified pictorial representation of a circuit
	Helps you build and is arranged the same way as the physical layout
-Ladder Diagram/Line Diagram / Schematic Diagram (Most common and preferred)
Describe drawings that show how a specific unit is wired including power, control and instrumentation on one drawing. These drawings are often vendor supplied
	Complete engineering information such as voltage levels and test points,
	Diagram showing the logic of a circuit, but now the physical relationship of the components.
	Helps you understand (inputs o the left outputs on the right)
-Single Line Diagram
	The basic concept behind a one-line drawing is minimalism. Where one lines is used to represent many lines. Used to give a general indication  of the relationship between various aspects
	Used to describe drawings that show cables and connection or juction boxes. They have CableID, Wire ID, and Junciton box ID. They do not show terminations. They are divided into Power Circuit, Instrumentation Circuit, and Control Circuit. They act as a road map to follow how the factory is wired.


	Typically used in power distribution drawings where its understood One Line represents a 3 		phase power system.
	Overall conceptual layout of a circuit, condense three-phase to single lines for simplicity.
