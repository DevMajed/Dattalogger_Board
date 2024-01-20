# MCU Datalogger with memory and clock


## Project Overview: 
**Project Name:**  
MCU Data Logger for ATmega328-AU  
  
  
![07FD53B6-CE86-47E1-A673-1FB48E3DFB10](https://github.com/DevMajed/Dattalogger_Board/assets/66625688/db87df5f-a7b5-4126-9f52-43b864b4d0c5) 
  
  
**Objective :**  
The MCU Data Logger is designed to log data from various sensors or peripherals connected to an ATmega328-AU microcontroller.  
The project incorporates features such as external EEPROM memory (24LC1025), a real-time clock (DS1337S), and essential connectors for communication and programming.


## Block Diagram / Circuit Schematic :

![<img width="610" alt="Schematic" src="https://github.com/DevMajed/Dattalogger_Board/assets/66625688/9fec3444-7fc9-431f-9d06-08b488d1c6a3">  
](link_to_your_image.jpg)
<br>  

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
