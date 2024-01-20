# MCU Datalogger with memory and clock


## Project Overview: 
**Project Name:**  
MCU Data Logger for ATmega328-AU  
  
  
![07FD53B6-CE86-47E1-A673-1FB48E3DFB10](https://github.com/DevMajed/Dattalogger_Board/assets/66625688/db87df5f-a7b5-4126-9f52-43b864b4d0c5) 
  
  
**Objective :**  
The MCU Data Logger is designed to log data from various sensors or peripherals connected to an ATmega328-AU microcontroller.  
The project incorporates features such as external EEPROM memory (24LC1025), a real-time clock (DS1337S), and essential connectors for communication and programming.


## Block Diagram / Circuit Schematic :

![Schematic](https://github.com/DevMajed/Dattalogger_Board/assets/66625688/9fec3444-7fc9-431f-9d06-08b488d1c6a3)


**ATmega328-AU:**  
Main microcontroller responsible for data processing, sensor interfacing, and overall control of the system.

**EEPROM (24LC1025):**  
External EEPROM memory for storing data logs, and it rovides non-volatile extended storage capacity.

**Real-Time Clock (DS1337S):**  
Provides accurate timekeeping for timestamping data logs.

**Real time Crystal Oscillator:**  
32.768 kHz: Connected to DS1337S for precise real-time tracking.

**High speed Crystal Oscillator :**  
16 MHz, Connected to Pins B6 and B7 of the AVR, with capacitors for stable clock operation.

**Connectors:**  
UART: For serial communication.  
ICSP: In-Circuit Serial Programming for firmware updates.  
I2C: General-purpose I2C communication.  
GPIO: General-purpose input/output for additional peripherals.  

**Interactions between Blocks:**  
* The ATmega328-AU communicates with the EEPROM over the I2C bus, storing and retrieving data logs.  
* The DS1337S sends real-time information to the ATmega328-AU, allowing accurate timestamping of data.  
* The 16 MHz crystal oscillator provides the main clock signal for the ATmega328-AU, ensuring proper execution of instructions.  
* Connectors facilitate external communication and programming, enhancing the project's versatility.  

## Specifications:  
Microcontroller: ATmega328-AU  
EEPROM: 24LC1025  
Real-Time Clock: DS1337S  
Crystal Oscillators:  
32.768 kHz (for DS1337S)  
16 MHz (for ATmega328-AU)  
Connectors: UART, ICSP, I2C, GPIO  
Power Supply: 5V battery "MCU 1.8V to 5.5V, EEPROM and DS1337S 2.3V to 5.5V. Oscillators 5V."  
Communication Protocols: I2C, UART  
Programming Language: C/C++  

## PCB Specifications:  
Sginals Track width : 0.25 mm  
VCC/GND Track width : 0.35 mm  
Signal Layers: Top F.Cu + Ln2.Cu  
Power Layer  : Ln1.Cu with Copper fills  
Ground Layer : Bottom B.Cu with Copper fills

## BOM : Bill of materials

#	Reference	Qty	Value	Footprint
1	BT1	1	Battery	Connector_PinHeader_2.54mm:PinHeader_2x01_P2.54mm_Vertical
2	C1, C4	2	0.1uF	Capacitor_SMD:C_0805_2012Metric
3	C2, C3	2	22pF	Capacitor_SMD:C_0805_2012Metric
4	C5	1	100nF	Capacitor_SMD:C_0805_2012Metric
5	D1, D2	2	LED	LED_SMD:LED_0805_2012Metric
6	H1, H2, H3, H4	4	MountingHole	MountingHole:MountingHole_2.1mm
7	J1, J2	2	Conn_01x04_Pin	Connector_PinHeader_2.54mm:PinHeader_1x04_P2.54mm_Vertical
8	J3	1	Conn_02x03_Odd_Even	Connector_PinHeader_2.54mm:PinHeader_2x03_P2.54mm_Vertical
9	J4	1	Conn_01x09_Pin	Connector_PinHeader_2.54mm:PinHeader_1x09_P2.54mm_Vertical
10	R1, R2, R6	3	10K	Resistor_SMD:R_0805_2012Metric
11	R3, R4	2	4.7K	Resistor_SMD:R_0805_2012Metric
12	R5, R7	2	330	Resistor_SMD:R_0805_2012Metric
13	U1, U3	2	24LC1025	Package_SO:SOIC-8_5.23x5.23mm_P1.27mm
14	U2	1	DS1337S_	Project_Libraries:SOIC127P600X175-8N
15	U4	1	ATMEGA328P-AU	Project_Libraries:QFP80P900X900X120-32N
16	Y1	1	32.768 KHz	Crystal:Crystal_SMD_5032-2Pin_5.0x3.2mm_HandSoldering
17	Y2	1	16 MHz	Crystal:Crystal_SMD_5032-2Pin_5.0x3.2mm_HandSoldering
![image](https://github.com/DevMajed/Dattalogger_Board/assets/66625688/7aab2fb6-d9c1-4db3-83a2-ff03075fc0a7)

