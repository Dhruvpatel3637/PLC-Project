Automated Weight-Based & Vision-Guided Goods Sorting System
Overview

This project demonstrates the design and implementation of an automated industrial goods sorting system developed using Studio 5000 PLC programming and simulated within an industrial automation environment. The system combines weight measurement, machine vision, conveyor automation, and pneumatic sorting mechanisms to classify and route products to their designated stations.

The solution mimics a real-world manufacturing and logistics sorting application where parts are weighed, identified through vision sensors, and automatically sorted while maintaining operational safety and process reliability.

Key Features
Automated conveyor system control
Weight measurement using analog scale input
Analog signal scaling from 0–10V to 0–30 kg
Real-time weight display
Vision-based product identification
Automated sorting using pivot arm mechanisms
Fragile product detection and handling
Emergency stop and safety door interlocks
Alarm and warning light management
Industrial stack light status indication
Start, Stop, and Reset operator controls
Safety-compliant machine guarding simulation
System Components
Material Handling
Multiple Conveyor Belts
Weight Scale Conveyor
Three Pivot Arms
Product Emitter
Product Removers
Product Alignment Wheels and Guides
Sensors
Analog Weight Scale
Diffuse Sensor for Weighing Station
Fragile Part Detection Sensors
Four Vision Sensors
Safety Equipment
Emergency Stop Circuit
Safety Door Interlock
Safety Fencing
Warning Lights
Alarm Sirens
Stack Lights
Operator Interface
Start Button
Stop Button
Emergency Stop Button
Reset Buttons
Weight Display
Process Calculation Displays
Sequence of Operation
1. System Startup

The operator starts the machine using the Start pushbutton. All conveyor systems, including the weighing conveyor and pivot arm conveyors, begin operation.

2. Part Generation

The emitter continuously generates:

Blue Parts
Green Parts
Metal Bases
Metal Caps

3. Weight Measurement

Products travel onto the weighing conveyor where a diffuse sensor detects their presence.

The conveyor temporarily stops for 5 seconds to allow accurate weight stabilization before measurement.

4. Analog Signal Processing

The PLC scales the raw analog input from the weight sensor:

Raw Input: 0–10V
Engineering Units: 0–30 kg

The calculated weight is displayed on the HMI numeric display.

5. Product Identification

After exiting the weighing station, the product passes vision sensors that identify the part type and color.

6. Automated Sorting

Based on vision sensor feedback:

Product Type	Destination
Metal Base	Main Conveyor
Metal Cap	Main Conveyor
Blue Part	Blue Station
Green Part	Green Station

The PLC actuates the appropriate pivot arm to direct each part to its designated station.

7. Fragile Part Monitoring

Dedicated diffuse sensors monitor fragile products and route them to a protected collection platform when required.

8. Safety Monitoring

The PLC continuously monitors:

Emergency Stop Status
Safety Door Position
Alarm Conditions
Conveyor Operation
Sensor Feedback

Any safety fault immediately stops machine operation and activates warning indicators.
