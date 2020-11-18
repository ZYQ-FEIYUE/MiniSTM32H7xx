# Download instructions

* [中文版本](./README-zh.md)

## Internal Flash

> The Openmv firmware download is at the internal address, starting at 0x08000000

> Firmware Download needs to use USB mode, st-link Download will have size limit, you can use  [WeAct Studio USB Download Tool](https://github.com/WeAct-TC/WeAct-Studio-Product.git) (located in `Soft` folder) , Windows 7 need `STM32CubeProg` to Download, to burn `openmv.bin` file(Just burn this file, and it is a combination of bootloader.bin and Firmware. Bin)

``` bash
>> Download the burn video tutorial
Baidu cloud: https://pan.baidu.com/s/1wPy3f_cRzPJc_YnOVKTprA 
Extract the code: rji7
```

## QSPI Flash
> The Openmv firmware is placed on the external 8MB QSPI Flash, so download 0x080000000.hex, initialize the QSPI peripheral, and map QSPI Flash to 0x90000000.

Firmware needs to use STM32CubeProg software, check enable QSPI Flash download algorithm, use ST-Link to download

> Bin file need to define the Download address, please note that STM32CubeProg `Download` button on the right side of the down `arrow`, click to customize the Download address

