# Continuous Signal Sampling and Display using ADC Converter

## Author

- **Name:** Maksim Kalutski
- **Login:** xkalut00

## Overview

This laboratory exercise focuses on the continuous sampling of a variable using an ADC (Analog-to-Digital Converter) and
displaying the processed samples on a 4-digit 7-segment LED display. The exercise involves setting up the ADC for
continuous data collection and handling the data via an interrupt service routine to update the display.

## Expected Behavior

- The ADC converter continuously samples the specified variable at a frequency determined by the Bus clock/2 with a
  clock divider set to 8.
- Each ADC sample is an 8-bit value obtained by hardware-averaging 32 consecutive samples.
- The sample processing and display update are triggered by an ADC interrupt.

## Implementation Guidelines

- **ADC Initialization**: Configure the ADC for continuous sampling with the required settings for clock source,
  averaging, and interrupt generation.
- **Interrupt Handling**: In the ADC0 interrupt handler, process the sampled data to calculate the display values.
  Convert these values to a suitable format for displaying on the 7-segment LED display.
- **Display Control**: Implement time multiplexing to update each digit of the 7-segment display sequentially.
