# UART-based-home-automation

Home Automation System using PIC Microcontroller

This project demonstrates a simple home automation system using a PIC microcontroller with serial communication control, simulated in Proteus. The system can control fans and lights in multiple rooms using commands sent via a serial interface.

Project Overview

The system uses a PIC microcontroller to control 2 LEDs, 2 motors (fans), and 4 relays. Users can send commands via serial communication (e.g., from a PC or Bluetooth module), and the microcontroller responds by switching the connected devices ON or OFF.

Components Used

PIC Microcontroller (PIC16F877A)

2 LEDs

2 Motors (representing fans)

4 Relays

Proteus simulation environment

Serial communication interface (UART)

Functionality

The system distinguishes commands using 3-character strings sent via UART:

Hall Room:

"HF1" – Turn Hall Fan ON

"HF0" – Turn Hall Fan OFF

"HL1" – Turn Hall Light ON

"HL0" – Turn Hall Light OFF

Bedroom:

"BF1" – Turn Bedroom Fan ON

"BF0" – Turn Bedroom Fan OFF

"BL1" – Turn Bedroom Light ON

"BL0" – Turn Bedroom Light OFF

The microcontroller reads incoming data, stores it in a buffer, and then controls the appropriate devices based on the commands.

Code Highlights

UART Communication

Receives commands via RCREG.

Echoes back received characters via TXREG.

Interrupts

Handles UART receive (RCIF) and external interrupts (INTF) for responsive control.

Delay Functions

delay() and delay1() are used to introduce controlled timing for UART transmission and other operations.

Device Control

Uses PORTB pins to drive LEDs, relays, and motors:

RB0 – Hall Light

RB1 – Hall Fan

RB2 – Bedroom Light

RB3 – Bedroom Fan

Simulation

Simulated in Proteus with LEDs representing lights and DC motors representing fans.

Serial monitor or virtual terminal can be used to send commands to the microcontroller.

How It Works

Load the code into the PIC microcontroller.

Connect the devices to the corresponding PORTB pins.

Send a 3-character command via serial communication.

The microcontroller turns ON/OFF the specified device based on the command.




<img width="1326" height="992" alt="Screenshot 2025-09-29 144237" src="https://github.com/user-attachments/assets/97998b90-63f8-4a04-81f9-bd6a5b2c55e5" />
