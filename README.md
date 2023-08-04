<a href="https://www.microchip.com" rel="nofollow"><img src="images/microchip.png" alt="MCHP" width="300"/></a>

# AVR128DA48 LED Blink using PWM Code Example

This repository provides a MPLAB X project with a MCC generated code example for an LED blink driven by a PWM signal. The example demonstrates how to generate a PWM signal using a timer. The output waveform is connected to the on-board LED. The PWM duty cycle value is set at 50%. For half of the period the LED is turned ON, and for the other half the LED is turned OFF.

## Related Documentation

More details and code examples on the AVR128DA48 can be found at the following links:

- [AVR128DA48 Product Page](https://www.microchip.com/wwwproducts/en/AVR128DA28)
- [AVR128DA48 Code Examples on GitHub](https://github.com/microchip-pic-avr-examples?q=avr128da48)
- [AVR128DA48 Project Examples in START](https://start.atmel.com/#examples/AVR128DA48CuriosityNano)


## Software Used

- [MPLAB® X IDE](http://www.microchip.com/mplab/mplab-x-ide) v6.10 or newer
- [MPLAB® XC8](http://www.microchip.com/mplab/compilers) 2.41 or newer
- [AVR-Dx Device Family Pack](https://packs.download.microchip.com/) v2.3.272 or newer

## Hardware Used

- [AVR128DA48 Curiosity Nano](https://www.microchip.com/Developmenttools/ProductDetails/DM164151) Development Board is used as test platform:
<br><img src="images/AVR128DA48_CNANO.png" width="600">

## Operation

To program the Curiosity Nano board with this MPLAB® X project, follow the steps provided in the [How to Program the Curiosity Nano Board](#how-to-program-the-curiosity-nano-board) chapter.<br><br>

## Setup

The following configurations must be made for this project:

- Clock Control:
  - Clock Selection: Internal high-frequency oscillator
  - Internal Oscillator Frequency: 1-32 MHz internal oscillator
  - Oscillator Frequency Selection: 4 MHz system clock
  - Prescaler Enable: Yes
  - Prescaler Division: 16X
  <br><img src="images/clock_control.PNG" width="600">

- Configuration Bits:
  - Watchdog Timeout Period: Watch-Dog timer off
  <br><img src="images/configuration_bits.PNG" width="600">

- Interrupt Manager:
  - Global Interrupt Enable: No
  <br><img src="images/interrupt_manager.PNG" width="600">

- TCA1:
  - Enable Timer: Yes
  - Clock Selection: System Clock
  - Requested Timeout: 262 ms
  - Waveform Generation Mode: Single Slope PWM
  - Enable Channel 2: Yes
  - Duty Cycle 2: 50%
  <br><img src="images/tca1_1.PNG" width="600">
  <br><img src="images/tca1_2.PNG" width="600">
  

|     Pin      |    Configuration   |
| :----------: | :----------------: |
|  PC6 (LED0)  |    Digital Output  |

<br><img src="images/pin_manager.PNG" width="600">

## Demo

<br><img src="images/AVR-DA_led_blink_pwm.gif" width="600">

## Summary

The demo shows how to generate a PWM signal using Timer/Counter Type A (TCA). The output of the TCA is connected to the on-board LED of the AVR128DA48 Curiosity Nano board and a waveform signal is generated.

##  How to Program the Curiosity Nano board

This chapter shows how to use the MPLAB X IDE to program an AVR® device with an `Example_Project.X`. This can be applied for any other projects. 

1. Connect the board to the PC.

2. Open the `Example_Project.X` project in MPLAB X IDE.

3. Set the `Example_Project.X` project as main project:
  <br>Right click on the project in the **Projects** tab and click Set as Main Project.
  <br><img src="images/Program_Set_as_Main_Project.PNG" width="400">

4. Clean and build the `Example_Project.X` project:
  <br>Right click on the `Example_Project.X` project and select Clean and Build.
  <br><img src="images/Program_Clean_and_Build.PNG" width="400">

5. Select AVRxxxxx Curiosity Nano in the Connected Hardware Tool section of the project settings:
  <br>Right click on the project and click Properties.
  <br>Click on the arrow under the Connected Hardware Tool.
  <br>Select the AVRxxxxx Curiosity Nano (click on the SN). 
  <br>Click Apply and then OK.
  <br><img src="images/Program_Tool_Selection.PNG" width="600">

6. Program the project to the board:
  <br>Right click on the project and then Make and Program Device.
  <br><img src="images/Program_Make_and_Program_Device.PNG" width="600">

<br>

- [Back to Setup](#setup)
- [Back to Demo](#demo)
- [Back to Summary](#summary) 
- [Back to Top](#avr128da48-led-blink-using-pwm-code-example)