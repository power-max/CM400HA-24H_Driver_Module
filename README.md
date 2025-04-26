# CM400HA-24H driver
Simple IGBT driver module for Mitubisi IGBT CM400HA-24H modules. This driver module should be capable of switching at up to 100kHz, limited by the SN6505 based DC-DC isolation converter.

The 7741F digital isolator IC is chosen for low propagation delay, high speed, and CMTI. 2 standard DIP8 low side driver ICs are used for driving the gate, with 16/20A current capability with the outputs paralelled. In the future I may modify the footprint to allow the use of cheaper SO8 SMD alternative parts as well.

The board features 2 collector voltage feedbacks, one intended for desaturation detection and one for VCC/2 crossover detection to allow output bridge voltage sensing. exact resistor values will need to be determined by the system integrator.

There is also feedback for UV lockout with the Pgood return signal.

Note: at present there is no fault shutdown, as the active HIGH input to the module directly controls the gate of the IGBT. All shutdown protections should be implemented on an upstream controller.

THE DESIGN IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
