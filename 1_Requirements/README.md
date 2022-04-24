This crystal not only present in clock but present in all computing real time systems. 
This crystal generates clock pulses, which is needed for timing calculations.Although there are some other ways to get clock pulses but for accuracy and higher
frequency most prefer crystal based clock.We are going to connect a crystal to ATMEGA32 for getting accurate clock.


Components:
1.32.768kHz crystal oscillator

2.Atmel ATMEGA328 microcontroller

3.7-segmet LED display

4.MAX7221 7-segment 8 digit LED driver

5.Buttons, wires, battery, switch, etc.

Detail Explaination:

Atmel ATMEGA328:

I used the popular Atmel ATMEGA328, which is one of the most popular Atmel AVR models and is used in the Arduino.This is a 28 pin microcontroller that has 32kB of
program memory and 2kB of RAM.I used the microcontroller to interface with the MAX7221 LED driver using the SPI interface protocol.

MAX7221 8 digit LED driver:

This IC can control an 8x8 led matrix or an 8 digit 7-segment LED display and uses the Serial Peripheral Intercom (SPI) protocol. 
This chip is desigend to work with common-cathode LEDS. In this project, the MAX7221 took commands from the ATMEGA328 through the SPI protocol, to display the the 
current circumstances of the alarm clock onto the 7-segment LED dispaly.

7-segment LED display:

This is where the time, alarm value or current circumstance of the alarm is displayed.

32.768kHz crystal oscillator:

The 32.768kHz crystal oscillator was used as the timing mechanism in the alarm clock. The crystal has an Equivalent Series Resistance (ESR) of 30 kOhms and load 
capacitance of 12.5 pF. The crystal has a precision of +- 20 parts per million.The crystal controls the frequency of an 8-bit counter on the ATMEGA328. 
The 32.768kHz frequency of the crystal divides exactly into 1 second intervals when the counter is configured to have a prescale of 64 and to overflow after the
standard 256 ticks. The exact division of this crystal to one second and it's precision are why it was used to control the clock.
