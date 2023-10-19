# 1. Communication via UART: Introduction to the Laboratory Kit, Development Environment, and Basics of Programming and Debugging Embedded Applications

# UART Communication and Embedded Application

## Introduction

This document outlines the tasks related to communication via UART, introduction to the laboratory kit, development environment, and basics of programming and debugging embedded applications. The assignment includes event detection (incoming data) using polling.

## Assignment Details

In solving this assignment, use resources such as the Reference Manual (starting from page 635) and the schematic of the laboratory kit for identifying UART receiver and transmitter pins from the MCU interface.

### Terminal Setup

- Set up and run a terminal on the PC (e.g., using the Putty application) for communication between the PC (USB) and the laboratory kit (UART).
- Use the following parameters:
  - Baud rate: 115200 Bd (b/s)
  - 8 data bits in the communication frame
  - 1 stop bit
  - No parity
  - Connection via COMx on the PC (specific value of "x" may vary for individual PCs - check with the instructor and Device Manager)
  - Flow control: None

## Programming and Running the Embedded Application

1. After programming and running the embedded application template:
   - LED on the laboratory kit should flash.
   - Followed by a short beep.

2. Complete the template to achieve the following behavior:

   - The user enters characters from the PC keyboard through the terminal on the PC.
   - Each character is received on the MCU side by the UART receiver module.
   - The character is then sent back to the PC by the UART transmitter module to be displayed in the terminal.

   - The application stores incoming characters in the "login" character array in the order of their arrival.
   - After receiving 8 characters, the application compares the content of the "login" array with the reference text string ("corrl").
   - If there is a match, the application produces a sound ("beep") to signal access permission (using the beep() function).
   - In case of a mismatch, the application prints "STOP" on the PC terminal, informing about access denial and allowing for the repeated entry of eight characters.

## Implementation Guidelines

- Follow the comments in *.c at the relevant places.
- Implement the character reception function using a polling loop.
