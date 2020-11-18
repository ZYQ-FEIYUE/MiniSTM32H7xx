# 使用说明

* [English Version](./README.md)

## QSPI Flash Firmware

Openmv 固件放在外部8MB QSPI Flash，所以就需要bootloader，则需要先下载0x08000000.hex，初始化QSPI外设，将QSPI Flash映射到0x90000000。

### 固件下载地址定义

0x08000000.hex -> 0x08000000

0x90000000.bin -> 0x90000000

## 0x08000000.hex 烧写方法

### 下载方法

1. Win10 用户 0x08000000.hex可以用`WeAct Studio Download Tools`或者`STM32cubeProg`下载, 进入dfu/isp模式，选择USB的方式下载
2. Win7 用户 0x08000000.hex需使用`STM32cubeProg`, 进入dfu/isp模式，选择USB的方式下载

### 0x08000000.hex 说明

1. 按住K1键上电或复位，LED慢闪时松开K1键进入WeAct HID Flash，可以使用WeAct HID Flash 上位机烧录openmv app: 0x90000000.bin
2. 按住K1键上电或复位，LED慢闪，继续按住K1键，LED变为快闪，松开K1键进入DFU模式

## 0x90000000.bin 烧写方法

1. 使用当前目录下的上位机 `WeAct_HID_Flash_NETFramework.exe` , 按住K1键上电或复位，LED慢闪时松开K1键进入WeAct HID Flash, 将0x90000000.bin拖入上位机，则可以进行烧录
    > 务必忽略WeAct HID Flash 上位机的工程设置步骤，那个步骤是针对STM32F4x1的芯片

2. 使用官方下载工具`STM32cubeProg`, 只能使用ST-Link下载，需要勾选使能QSPI Flash下载算法，按住K1键上电或复位，LED慢闪，继续按住K1键，LED变为快闪，松开K1键进入DFU模式, 选择ST-Link模式，连接，将0x90000000.bin拖入`STM32cubeProg`，下载
    > Bin文件需要自己定义下载地址，请注意，STM32CubeProg `Download`按钮右边有向下的`小箭头`，点击可以自定义下载地址
