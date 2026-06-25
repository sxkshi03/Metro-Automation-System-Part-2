## Metro-Automation-System-Part-2

## Objective
To develop a PLC-based metro train automation system that simulates the movement of a train between stations using sequential control logic, automatic stopping, door operation sequencing, timer-based delays, and safety interlocks. The project demonstrates how industrial PLCs can automate a complete station arrival and departure cycle while maintaining safe operating conditions.

## Features
* Automatic train departure and station approach
* Station detection and automatic brake application
* Timer-based train stopping sequence
* Automatic door opening and closing cycle
* Passenger boarding and alighting delay
* Door obstacle interlocking
* Automatic brake release after door closure
* Continuous station-to-station operation loop
* Emergency stop functionality
* Signal and track safety interlocking
* Memory-based sequence restart
* Latch/unlatch state control

## PLC Instructions Used
* XIC (Examine If Closed)
* XIO (Examine If Open)
* OTE (Output Energize)
* OTL (Output Latch)
* OTU (Output Unlatch)
* TON (On Delay Timer)
* One-Shot Logic (ONS) (if used for Start command)
* Internal Memory Bits
* Timer Done Bits (.DN)
