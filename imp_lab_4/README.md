# Continuous Signal Sampling using ADC Converter, Sample Processing

## Assignment Details

In solving this task, refer to the Reference Manual, Part 28 (from page 423), and the Schema of the laboratory kit (for studying the connection of the display with MCU and identifying the pins (channels) of the ADC converter for continuous sampling of a variable from the MCU interface).

After programming and running the built-in application template, the application will not exhibit any external behavior. However, it will enter an infinite loop in the `main()` function, where it will handle the update of the content of a 4-digit 7-segment LED display on the laboratory kit. The individual digits to be displayed are drawn sequentially from left to right, using time multiplexing—only one digit is displayed at a time.

Complete the embedded application template, i.e., the bodies of the functions `ADC0_Init()` and `ADC0_IRQHandler()`, so that the resulting application behaves according to the expectations outlined below (also see comments in *.c):

- The ADC converter will continuously sample the specified continuous variable with a conversion cycle given by Bus clock/2 and clock divider = 8.
- The resulting ADC sample will be 8 bits, created from a hardware-averaged series of 32 consecutive samples.
- The creation of the resulting ADC sample will be signaled by an interrupt.

In the interrupt service routine, the resulting ADC sample will be read/stored, e.g., in a suitable local variable. From its value, the units, tenths, and hundredths of the measured variable will be determined. This information will be appropriately inserted into the "result" string for its correct display on the laboratory kit's display.
