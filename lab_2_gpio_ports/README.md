# Application of Ports for GPIO and Interrupt Handling

## Author

- **Name:** Maksim Kalutski
- **Login:** xkalut00

## Overview
This laboratory exercise focuses on usage General-Purpose Input/Output (GPIO) ports and interrupts for detecting and responding to button presses on a microcontroller unit (MCU).

## Expected Application Behavior

Once the embedded application template is programmed and executed:
1. An LED on the laboratory kit should blink.
2. A short beep should be emitted.
3. The application enters an infinite loop (`while(1);` in the `main()` function).
4. The pressing of any of the five buttons should cyclically trigger the `PORTB_IRQHandler()` function, resulting in repeated LED blinking.

## Implementation Requirements

Complete the embedded application template by:
- Implementing the `PORTB_IRQHandler()` function as per the guidelines provided in the `*.c` files.
- Handling individual button presses using the interrupt system, ensuring that each press results in one function invocation of `PORTB_IRQHandler()`.
- Avoiding the need to address simultaneous button presses or releases.

Implement the `flash()` or `beep()` functions for visual or auditory feedback to button presses.
