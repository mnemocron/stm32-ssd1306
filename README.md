# stm32-ssd1306

This library was adapted to support multiple Displays on multiple I2C Busses. 
See the example for further details.

```c
SSD1306_t holed1;
holed1.hi2cx = &hi2c1;
ssd1306_Init(&holed1);
ssd1306_Fill(&holed1, Black);
ssd1306_SetCursor(&holed1, 2, 0);
ssd1306_WriteString(&holed1, "Hello,", Font_11x18, White);
ssd1306_UpdateScreen(&holed1);

```


Currently missing is the implementaion to use multiple displays on SPI Bus.


---

### original Readme:

STM32 library for working with OLEDs based on SSD1306, SH1106 and SSD1309,
supports I2C and 4-wire SPI.

Tested on STM32F1 and STM32F4 MCUs, with 10 random displays from eBay. Also this
code is known to work with
[afiskon/fpga-ssd1306-to-vga](https://github.com/afiskon/fpga-ssd1306-to-vga).

Please see `examples` directory and `ssd1306/ssd1306.h` for more details.

The code is based on
[4ilo/ssd1306-stm32HAL](https://github.com/4ilo/ssd1306-stm32HAL) library
developed by Olivier Van den Eede ( [@4ilo](https://github.com/4ilo) ) in 2016.

See also:

* https://github.com/afiskon/stm32-ssd1351
* https://github.com/afiskon/stm32-st7735
* https://github.com/afiskon/stm32-ili9341
