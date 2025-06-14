## Aerospike Rocket Engine System (ARES) modeling on NPSS

- At Herrick Labs, under the guidance of Dr. Ziviani, I’ve been developing a full-system model of an Aerospike rocket engine using NASA’s Numerical Propulsion System Simulation (NPSS).
- This work is part of my thesis, focused on one core question:
How resilient is a rocket engine’s thermal management system when things go wrong?

That includes off-nominal operations, mission-induced stress (like orbital maneuvers or throttling), or even internal failures. To answer it, I modeled the pumps, turbine, valves, regenerative cooling channels, and combustion chamber within NPSS—capturing both steady-state and transient behavior under potential damage conditions.
- Steady-state and transient results were obtained, an example of them is illustrated below.

### Images
#### Engine cycle
![Engine cycle: this is just a drawn diagram, it is not the NPSS user interface](images/engineCycle1.png)
#### Example of turbine transient response due to fuel mass flow rate ramp
![turbine response](images/Transient1.png)
this result was achieved using NPSS and MATLAB
