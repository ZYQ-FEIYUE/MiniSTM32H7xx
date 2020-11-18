# Directions for use

* [中文版本](./README-zh.md)

## QSPI Flash Firmware

The Openmv firmware is placed in the external 8MB QSPI Flash, so bootloader is needed. In this case, we need to download 0x08000000.hex, initialize QSPI peripheral, and map QSPI Flash to 0x90000000.

### firmware download address definition

0x08000000.hex -> 0x08000000

0x90000000.bin -> 0x90000000

## 0x08000000.hex burning method

### Download method

1. Win10 user 0x08000000.hex can be downloaded by `WeAct Studio Download Tools` or `STM32cubeProg`, enter DFU/ISP mode, and select USB mode to Download
2. Win7 user 0x08000000.hex needs to use `STM32cubeProg`, enter DFU/ISP mode, and select USB mode to download

### 0x08000000.hex instructions

1. Press the K1 key to power up or reset, and release the K1 key to enter WeAct HID Flash when LED is slow flashing. You can use the WeAct HID Flash host computer to burn openmv app: 0x90000000.bin
2. Press and hold K1 to power up or reset, and the LED will flash slowly. Continue to press and hold K1, and the LED will turn into flash, and release K1 to enter DFU mode

## 0x90000000.bin burning method

1. Use upper computer `weact_hid_flash_net Frame.exe` in the current directory, hold down the K1 key to power up or reset, release the K1 key to enter `WeAct HID Flash` in the case of LED slow Flash, and drag 0x90000000.bin into upper computer to burn
    > Be sure to ignore the engineering setup step for the WeAct HID Flash host, which is for the STM32F4x1 chip

2. Use official download tool `STM32cubeProg`, only use ST-Link to download, need to check enabled QSPI Flash download algorithm, press and hold K1 to power up or reset, LED slow Flash, continue to press and hold K1, LED into Flash, release the K1 key into DFU mode, select ST-Link mode, connect, drag 0x90000000.bin into `STM32cubeProg` to download
    > The Bin file needs to define the Download address by itself. Please note that there is a `small arrow` on the right side of the STM32CubeProg `Download` button. Click to customize the Download address
