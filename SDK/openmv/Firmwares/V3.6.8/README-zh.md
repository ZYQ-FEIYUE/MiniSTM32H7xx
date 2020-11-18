# 下载说明

* [English Version](./README.md)

## Internal Flash(推荐)

> Openmv 固件放在MCU内部存储地址，从0x08000000开始

固件下载需要使用USB模式下载，ST-Link下载会有大小限制，可以使用[WeAct Studio USB Download Tool](https://github.com/WeAct-TC/WeAct-Studio-Product.git)（位于Soft文件夹）Win7系统需要使用STM32CubeProg进行下载，烧录openmv.bin文件(烧录此文件即可,是bootloader.bin和firmware.bin的组合)，百度网盘有下载烧录视频教程

``` bash
>> 下载烧录视频教程
百度网盘: https://pan.baidu.com/s/1wPy3f_cRzPJc_YnOVKTprA 
提取码: rji7
```

## QSPI Flash

> Openmv 固件放在外部8MB QSPI Flash，所以需要下载0x08000000.hex，初始化QSPI外设，将QSPI Flash映射到0x90000000。

固件下载需要使用STM32CubeProg软件，勾选使能QSPI Flash下载算法，使用ST-Link进行下载

> Bin文件需要自己定义下载地址，请注意，STM32CubeProg `Download`按钮右边有向下的`小箭头`，点击可以自定义下载地址
