# Arduino-ATMEGA-internal-8MHz-clock-bootloaders
when using Arduino on an ATMEGA, the ATMEGA requires a 16MHz external clock. These bootloaders allow the internal 8MHz to be used instead. This reduces the number of components needed for your project.

## Downloading
Create or locate the hardware folder within the Arduino project folder.
Download all the files and exstract files into hardware folder 

## Loading Bootloader
Open the Arduino application and select the board and programmer then burn the bootloader. 

The board is the Arduino that is to be programmed. The board would be the ATMEGA chip. To select the board, navigate to Tools->Board and select ATmega328 (8 MHz internal clock), ATmega8 (8 MHz internal clock) or any under ATMEGA internal clock.

The programmer is the SPI programming tool to program the board/chip. This would be a different programmer than the serial Arduino on boards like the Arduino UNO. An Arduino UNO can be programmed to act as an SPI programmer, see [here](https://www.arduino.cc/en/tutorial/arduinoISP) for more details. To select the programmer, navigate to Tools->Programmer and select the programmer.

To burn the bootloader, connect the SPI programming tool and navigate to Tools->burn bootloader. The programmer will then try and burn the bootloader to the chip. When it's successful, the programmer can be disconnected and the Arduino can be programmed var the serial. 

## References
[https://todbot.com/blog/2009/05/26/minimal-arduino-with-atmega8/](https://todbot.com/blog/2009/05/26/minimal-arduino-with-atmega8/)
[https://www.arduino.cc/en/Tutorial/ArduinoISP](https://www.arduino.cc/en/Tutorial/ArduinoISP)
[http://ediy.com.my/index.php/tutorials/item/94-arduino-running-at-8mhz-internal-clock-with-optiboot-bootloader/94-arduino-running-at-8mhz-internal-clock-with-optiboot-bootloader](http://ediy.com.my/index.php/tutorials/item/94-arduino-running-at-8mhz-internal-clock-with-optiboot-bootloader/94-arduino-running-at-8mhz-internal-clock-with-optiboot-bootloader)
