# UART Communication and Embedded Application Laboratory

## Author

- **Name:** Maksim Kalutski
- **Login:** xkalut00

## Introduction

This laboratory exercise focuses on learning UART communication and the basics of programming and debugging embedded
applications. It includes tasks such as event detection (incoming data) using polling techniques.


## Programming and Running the Embedded Application

1. Flash the provided embedded application template to the laboratory kit. Ensure that the LED flashes followed by a
   short beep indicating successful upload.
2. Modify the template to implement the following behavior:
    - Characters are entered from the PC keyboard through the terminal.
    - Each character is received on the MCU side by the UART receiver module and sent back to the PC by the UART
      transmitter module to be displayed in the terminal.
    - Store incoming characters in the "login" character array.
    - After receiving 8 characters, compare the array with the reference string "corrl".
    - If matched, produce a beep sound indicating access permission. If not, display "STOP" on the PC terminal and allow
      for re-entry.

## Implementation Guidelines

- Follow the embedded comments in the `*.c` files at relevant places for more specific instructions.
- Implement the character reception function using a polling loop.
