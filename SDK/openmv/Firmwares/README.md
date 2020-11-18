# Directory description

* [中文版本](./README-zh.md)

## Related burning tutorial

[STM32 to download the burn tutorial and problem summary, click here](http://www.weact-tc.cn/2019/11/30/STM32Download/)

``` bash
>> Download the burn video tutorial
visit WeAct Studio Download Tool 烧录教程.mp4
Baidu cloud: https://pan.baidu.com/s/1wPy3f_cRzPJc_YnOVKTprA 
Extract the code: rji7
```

## SPI Flash Erase Firmware

> When the USB Flash drive is not recognized (py code error), the firmware can be burned to erase the SPI Flash

Because openMV Firmware cannot Erase the external SPI memory, we provide `SPI Flash Erase` Firmware for the two external `SPI Flash`

* `SPI_Flash_Erase_0x8000000.hex` can be downloaded using the [WeAct Studio USB Download Tool](https://github.com/WeAct-TC/WeAct-Studio-Product.git) to download，After downloading and waiting for the program to run, the core board screen shows `Please Burn Next Fiwmware` after you can re-burn the firmware

* `SPI_Flash_Erase_0x8040000.bin` you can directly use the OpenMV IDE for downloading, as follows:

    1. Open Openmv IDE choose `Tools->Run Bootloader(Load Firmware)`
    2. Choose `SPI_Flash_Erase_0x8040000.bin`, and then click on the run
    3. After downloading, wait for the program to run, the core board screen display `Please Burn Next Fiwmware` go on to the next step
    4. Openmv IDE Continue to choose `Tools->Run Bootloader(Load Firmware)`,Choose our data provide the firmware `firmware.bin` (Vx.x.x/internal/firmware. bin)(Not the firmware in the USB Download software), then click run, and then the core board click reset button, waiting for the firmware download to complete

## Vx.x.x

> Openmv firmware, such as `V3.6.4` is the version of the Openmv firmware

### Internal Flash (recommended)

> Openmv firmware is placed in the internal address, starting from 0x08000000, openmv. Bin can be burned. This firmware is a combination of bootloader.bin and firmware. Bin

### QSPI Flash

> The firmware is placed in the external 8MB QSPI Flash, so you need to download 0x08000000.hex, initialize the QSPI peripheral, and map the QSPI Flash to 0x90000000.bin
