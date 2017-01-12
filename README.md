# Adafruit_SSD1306
<!-- START COMPATIBILITY TABLE -->

## Mod for "3-wire" SPI
Some SPI versions of the SSD1306 display can be used without the DC line, eliminating an output pin. This currently only works with the custom (bit-bang) SPI method, since it requires sending of 9-bit packets instead of 8. To use, call the constructor without the DC argument.
```Adafruit_SSD1306 display(OLED_MOSI, OLED_CLK, OLED_RESET, OLED_CS);```
This mod also allows you to pass -1 as a value for OLED_CS, if you have only one SPI device and are not using the CS line.

## Compatibility

MCU                | Tested Works | Doesn't Work | Not Tested  | Notes
------------------ | :----------: | :----------: | :---------: | -----
Atmega328 @ 16MHz  |      X       |             |            | 
Atmega328 @ 12MHz  |      X       |             |            | 
Atmega32u4 @ 16MHz |      X       |             |            | 
Atmega32u4 @ 8MHz  |      X       |             |            | 
ESP8266            |      X       |             |            | change OLED_RESET to different pin if using default I2C pins D4/D5.
Atmega2560 @ 16MHz |      X       |             |            | 
ATSAM3X8E          |      X       |             |            | 
ATSAM21D           |      X       |             |            | 
ATtiny85 @ 16MHz   |             |      X       |            | 
ATtiny85 @ 8MHz    |             |      X       |            | 
Intel Curie @ 32MHz |             |             |     X       | 
STM32F2            |             |             |     X       | 

  * ATmega328 @ 16MHz : Arduino UNO, Adafruit Pro Trinket 5V, Adafruit Metro 328, Adafruit Metro Mini
  * ATmega328 @ 12MHz : Adafruit Pro Trinket 3V
  * ATmega32u4 @ 16MHz : Arduino Leonardo, Arduino Micro, Arduino Yun, Teensy 2.0
  * ATmega32u4 @ 8MHz : Adafruit Flora, Bluefruit Micro
  * ESP8266 : Adafruit Huzzah
  * ATmega2560 @ 16MHz : Arduino Mega
  * ATSAM3X8E : Arduino Due
  * ATSAM21D : Arduino Zero, M0 Pro
  * ATtiny85 @ 16MHz : Adafruit Trinket 5V
  * ATtiny85 @ 8MHz : Adafruit Gemma, Arduino Gemma, Adafruit Trinket 3V

<!-- END COMPATIBILITY TABLE -->
