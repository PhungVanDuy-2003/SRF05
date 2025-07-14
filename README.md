# SRF05
Utilizing the STM32F103C8T6 microcontroller in conjunction with the SRF05 ultrasonic sensor to measure the distance to an object.

- The schematic diagram includes the STM32F103C8T6 microcontroller connected to the SRF05 ultrasonic sensor. The TRIG pin of the SRF05 is connected to a GPIO output pin of the STM32, while the ECHO pin is connected to a GPIO input (preferably with interrupt or timer capture functionality). A 5V power supply is used for the SRF05, and a voltage divider is implemented to protect the STM32's 3.3V input from the 5V ECHO signal.

- Schematic:
 + TRIG: GPIOA4 of the STM32.
 + ECHO: GPIOA5 of the STM32.
 + 5V.
 + GND.
 
- Using The ECHO pin of the SRF05 is connected to pin GPIOA5 of the STM32F103C8T6 via a voltage divider circuit using two resistors: 3.3kΩ (connected to the ECHO pin) and 1.8kΩ (connected to ground), in order to safely step down the 5V signal to a 3.3V-compatible logic level.
