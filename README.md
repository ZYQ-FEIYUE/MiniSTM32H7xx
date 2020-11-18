# WeAct Studio STM32H7xx Core Board

* [中文版本](./README-zh.md)

> `0.96''` ST7735 TFT, TF Card, 8MB QSPI FLASH(SPI1)， 8MB QSPI FLASH(QSPI1), 8Bit DVP Port

> support Openmv firmware, see [SDK/openmv](./SDK/openmv)

> The program can run in external Flash, browse for details[SDK/QSPI_Flasher](https://github.com/WeAct-TC/WeAct-Studio-Product.git)

## STM32H750VBT6 128KB ROM, 1MB RAM

* ARM Cortex M7
* 480Mhz Max. Freq
* 128KB ROM, 1MB RAM
* 8MB SPI Flash, 8MB QSPI Flash

## STM32H743VIT6 2048KB ROM, 1MB RAM

* ARM Cortex M7
* 480Mhz Max. Freq
* 2048KB ROM, 1MB RAM
* 8MB SPI Flash, 8MB QSPI Flash

!["WeAct H7 View"](Images/STM32H750VB_1.jpg)

### Interface and Keys

* 2*22 Pin 2.54mm I/O x 2
* 4 Pin 2.54mm SW x 1
* USB C (type C)  x 1
* MicroSD TF x 1
* 8Bit DCMI x 1
* User Key K1 (PC13) x 1
* NRST Key x 1
* BOOT0 Key x 1

### Design and Quality

* `TG155` plate with gold sinking process is designed with four layers
* Use `Lead-Free` welding process
* Use the button to set BOOT
* Use high quality crystal vibration, metal shell, all can be good vibration
* Always use the original ST chip

> We do not provide the factory test firmware to prevent the appearance of duplicates, affecting the quality

### Chip Date Code

| STM32H750VBT6 | STM32H743VIT6 |
| :--: | :--: |
|Date Code|Date Code|
|930 (2020.06)|----|
|031 (2020.10)|036 (2020.10)|

### Taobao purchase link

1. [WeAct Studio官方店](https://shop118454188.taobao.com/index.htm?spm=2013.1.w5002-17867322799.2.212f5cb16nqwNP)

### Aliexpress purchase link

1. [WeAct Studio offical store](https://www.aliexpress.com/store/910567080)

## Begin to use

### Install 0.96'' ST7735 TFT

![step1](./Images/ST7735/Install-1.png)

1. Bend down 90° along the red line, and use the edge of the core plate to assist bending
2. Bend up 90° along the blue line, and use the edge of the core plate to assist bending
3. Do not bend the green line to avoid breaking the screen line
4. Double-sided adhesive tape is pasted at the installation place of the core board screen, and then screen installation can be easily completed according to the line folding pattern of the screen

> Note: When pasting the installation, make sure that the screen border does not touch the electronic components on the board

![step2](./Images/ST7735/Install-2.png)

### Install Camera

* Support Sensor: OV7670, OV2640, OV7725, OV5640-AF
* 如果使用OV5640自动对焦功能，务必焊接SB4，SB5
* If USING OV5640 auto focus function, be sure to weld SB4, SB5

![](./Images/ST7735/Install-3.png "Camera Install")

### Factory test firmware introduction

1. Screen test
2. Camera test
3. ADC test
4. Flash and TF card test

> Click `K1` to switch to the next test item

### How to enter ISP mode

#### Instructions

* Method 1: When the power is on, press the BOOT0 key and the reset key, then release the reset key, and release the BOOT0 key after 0.5 seconds
* Method 2: When the power is off, hold down the BOOT0 key, and release the BOOT0 at 0.5s after the power is on
* DFU Mode: Use the data line to connect to the computer.
* Serial Port Mode: Connect PA9 and PA10 of core board with USB serial port
* Soft: STM32CubeProg。

### Power supply and Board Shape

* Input Voltage: 3.3V-5.5V
* DC-DC Output Current: 1A Max.
* Size: 40.64mm * 66.88mm

![WeAct H7 View](Images/BoardShape.png)

![WeAct H7 View](Images/STM32H750VB_2.jpg)
