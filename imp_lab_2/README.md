## Application of Ports for GPIO and Interrupts

The purpose of this document is to outline the application of ports as generally applicable digital inputs/outputs (GPIO), event detection (button press) using interrupts, and event response through interrupt handling.

### Assignment Details

When working on this assignment, please refer to the following documents and resources:

- **Reference Manual:** Section 3.3.2 (from page 48) and Section 11.5 (from page 161).
- **Cortex-M0+ Devices Generic User Guide:** Section 4.2 (from page 87).
- **Laboratory Kit Schema:** Use this for identifying the MCU pins used for button state detection and the button connection method.

### Application Behavior

After programming and launching the embedded application template, the following behavior is expected:

1. The LED on the laboratory kit should blink.
2. A short beep should sound.
3. The application will enter an infinite loop (`while(1);` in `main()`).
4. When any of the five buttons are pressed, the application will cyclically trigger the `PORTB_IRQHandler()` function, resulting in repeated LED blinking (see the `flash()` function call).

### Completing the Template

You should complete the embedded application template by filling in the body of the `PORTB_IRQHandler()` function to meet the following expectations (also refer to the comments in `*.c`):

- The user can press any of the five buttons (up, down, left, right, center).
- The event of pressing an individual button is captured by the interrupt system, leading to one invocation of the `PORTB_IRQHandler()` handler.
- Other events, such as simultaneous button presses or button releases, do not need to be addressed.

You should ensure that each button press is correctly detected and handled, for example, by using the `flash()` or `beep()` functions.
