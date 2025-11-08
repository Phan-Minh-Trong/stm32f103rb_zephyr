# STM32F103RB_ZEPHYR
## Introduction
This is a personal project, I've created it to port Zephyr RTOS and build applications for a custom nucleo_f103rb board

## Build and Flash the program
Build the program:
```
west build -p always -b nucleo_f103rb/stm32f103xb -- -DDTC_OVERLAY_FILE=boards/nucleo_f103rb.overlay
```

Flash the program (Make sure STM32_Programmer_CLI is installed):
```
STM32_Programmer_CLI.exe --connect port=swd reset=HWrst --download build/zephyr/zephyr.hex --start
```

Or you can flash the program you using STM32 Cube Programmer, just select the `build/zephyr/zephyr.hex` when the program is successfully built.
