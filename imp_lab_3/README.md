# Pulse Width Modulation (PWM) using Timer and its Application (Controlling RGB LED Brightness)

## Task Details
- Utilize the Reference Manual, Chapter 31 (from page 507 onwards), and the Laboratory Kit Schema (for identifying timer channels usable for controlling LED via PWM signal from MCU interface).
- After programming and launching the built-in application template, the application will not show any external manifestations. However, it will enter an infinite loop in the main() function. In this loop, the 'compare' variable will first be incremented (until reaching the final value of OVERFLOW), and then decremented to a value of 0 (Note: switching between increment/decrement modes is controlled by the 'increment' variable).
- Complete the built-in application template, i.e., the Timer0Init() and main() functions, so that the resulting application behaves as expected (see also comments in *.c):

## Expected Behavior
The application will cyclically perform the following activities: smoothly increase brightness until reaching the maximum, then smoothly decrease brightness until reaching the minimum, of the three-color (RGB) LED. To ensure specific brightness on each R, G, B channel, utilize the respective PWM signal generated by the timer available on the MCU.

## Implementation Notes
- Follow the guidelines in the Reference Manual, Chapter 31, and refer to the Laboratory Kit Schema for identifying timer channels.
- Modify the Timer0Init() and main() functions in the built-in application template to achieve the specified behavior.
