
# STM32 Connection

STM32 -> STLINK-V3

```
RESET 15 -> 31
GND   4  -> 8, 24, 26, 27, 29
SWDIO 7  -> 4
SWCLK 9  -> 13
SWO   13 -> 6
```

![[Pasted image 20221016195218.png]]

## Read Flash

```shell
openocd -f interface/stlink.cfg -f target/stm32f2x.cfg -c init -c "reset halt" -c "flash read_bank 0 firmwareF1.bin 0 0x7D000" -c "reset" -c shutdown
```

