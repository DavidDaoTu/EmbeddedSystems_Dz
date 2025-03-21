# EmbeddedSystems_Dz
Communication &amp; Embedded Systems

## Labs
Lab#1: Priority inversion (before/after)

Scenario:
In a modern car, both the Anti-Lock Braking System (ABS) and Traction Control System (TCS) rely on the Electronic Control Unit (ECU) to control wheel speed and prevent skidding.

- Low-Priority Task (TractionControlTask): Adjusts engine power and braking to maintain traction when wheels slip.
- High-Priority Task (BrakeTask): Engages the ABS when the driver slams the brakes, preventing wheel lockup.
- Shared Resource: The CAN Bus Mutex, which both tasks need to send commands to the ECU.
The Problem (Priority Inversion)
- TractionControlTask holds the CAN Bus mutex while adjusting traction settings.
- Suddenly, BrakeTask needs to send an ABS activation command.
- If TractionControlTask does not release the mutex quickly, the braking command is delayed, reducing braking efficiency and increasing stopping distance—which could lead to a crash!


Lab#2: Tutorial on reading datasheet and reference manual: UART use-case

- A SoC may have multiple UART with configurable pins, how to 'read' the pins
- On ESP32-WROOM 32, why it supports maximum 3 UARTs? (while GPIO can be used)
- How to identify which UART connects to the micro-usb port
- In which situation we look at the datasheet or the reference manual?

Lab#3: CMSIS-RTOS: change OS? A complete demo on MG12? Wifi Commissioning

- Show CMSIS API/FreeRTOS API/Micrium OS API conversion
- Show the important included cmsis/<rtos> header files
- Show the application/driver written using CMSIS APIs
 