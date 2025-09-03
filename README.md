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


