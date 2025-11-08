# STM32F103RB_ZEPHYR
## Build and Flash the program
Build the program:
```
west build -p always -b nucleo_f103rb/stm32f103xb
```

Flash the program (Make sure STM32_Programmer_CLI is installed):
```
STM32_Programmer_CLI.exe --connect port=swd reset=HWrst --download build/zephyr/zephyr.hex --start
```

Or you can flash the program you using STM32 Cube Programmer, just select the `build/zephyr/zephyr.hex` when the program is successfully built.
