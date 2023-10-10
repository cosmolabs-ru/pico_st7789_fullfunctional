An ST7789 driver, originally written by [Floyd-Fish](https://github.com/Floyd-Fish/ST7789-STM32/tree/master) for STM32, ported & adapted for RP2040 by me. This port has kept all functions of the original library. The port is easily configurable. 
BTW, it supports Cyrillic (and other non-latin) fonts very well!

## Deployment
- Add *st7789* folder into your project
- Add  `add_subdirectory(st7789)` into your root CMakeLists.txt file
- define RESET, DC, CS gpio numbers in st7789.h
- change pin numbers for MISO, CLK in prepare_spi() and SPI instance, if needed
- Init the device: call prepare_spi(), then ST7789_Init()
- You're all set! Draw something cool!

### Functions:
Draws pixels, fills, graphic primitives, strings (incl. non-latin), bitmaps.
See [original lib's manual](https://github.com/Floyd-Fish/ST7789-STM32/tree/master) 

### DMA usage
DMA  usage is disabled, and was not ported. Do not uncomment anything related to DMA ~~for your life.~~
