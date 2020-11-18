# WeAct Studio STM32H7xx Openmv Firmware

* [中文版本](./README-zh.md)

1. Example -> routine
2. Firmwares -> Openmv firmware, has a tutorial for burning and downloading
3. Ports -> WeAct Studio STM32H750 Core board interface definition

## Interface Definition

> Concrete interface definition. The Path：`Ports\micropython\boards\WeActStudioSTM32H7xx\mpconfigboard.h`

``` c
代号，实际管脚名
Code name, Actual pin name
P0,PB15
P1,PB14
P2,PB13
P3,PB12
P4,PB10
P5,PB11
P6,PA5
P7,PD12
P8,PD13
P9,PD14
P10,PD15
P11,PA13
P12,PA14
P13,PA0
P14,PA1
P15,PA2
P16,PA3
LED_BLUE,PE3
```

## How to Build OpenMV

1. Clone openmv source code

    ``` bash
    git clone https://github.com/WeActTC/openmv.git --depth=1
    ```

2. Init source code

    ``` bash
    cd openmv
    git submodule init
    git submodule update --depth=1
    cd src/micropython
    git submodule init
    git submodule update --depth=1
    cd ..
    ```

3. Install gcc-arm-none-eabi

    ``` bash
    sudo apt-get install gcc-arm-none-eabi
    ```

4. Bulid

    First, copy the relevant folder in the current data Port folder to the corresponding location
    1. Copy `Ports/omv/boards/WeActStudioSTM32H7xx` to `openmv/src/omv/boards/`
    2. Copy `Ports/micropython/boards/WeActStudioSTM32H7xx` to `openmv/src/micropython/ports/stm32/boards/`
    3. Copy `Ports/micropython/micropython-Add-WeAct-Studio-STM32H7xx-Support.patch` to `openmv/src/micropython/`
    4. Go to `openmv/src`
    5. Enter relevant commands

        ``` c
        cd micropython
        git am micropython-Add-WeAct-Studio-STM32H7xx-Support.patch
        cd mpy-cross
        make -j
        cd ../../
        make TARGET=WeActStudioSTM32H7xx -j
        ```

The address of firmware burning, generally burning openmv. bin, this firmware is bootloader. bin and Firmware. bin together

> bootloader.bin 0x08000000

> firmware.bin 0x08040000

> opemmv.bin 0x08000000