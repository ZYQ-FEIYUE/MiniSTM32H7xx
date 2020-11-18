# WeAct Studio STM32H7xx Openmv 固件

* [English Version](./README.md)

1. Example -> 例程
2. Firmwares -> openmv固件，内有烧录下载教程
3. Ports -> WeAct Studio STM32H750 核心板接口定义

## 接口定义

> 具体接口定义 路径位置:
`Ports\micropython\boards\WeActStudioSTM32H7xx\mpconfigboard.h`

``` bash
代号，实际管脚名
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

## Openmv 固件编译方法(所需掌握Linux知识较多，不建议入手，需自行琢磨, 使用我们编译好的固件即可)

1. 克隆仓库代码

    ``` bash
    git clone https://github.com/WeActTC/openmv.git --depth=1
    ```

2. 更新仓库子模块代码

    ``` bash
    cd openmv
    git submodule init
    git submodule update --depth=1
    cd src/micropython
    git submodule init
    git submodule update --depth=1
    cd ..
    ```

3. 安装 gcc-arm-none-eabi

    ``` bash
    sudo apt-get install gcc-arm-none-eabi
    ```

4. 搭建

    首先复制当前资料Port文件夹里的相关文件夹到对应位置

   1. 复制 `Ports/omv/boards/WeActStudioSTM32H7xx` 到 `openmv/src/omv/boards/`

   2. 复制 `Ports/micropython/boards/WeActStudioSTM32H7xx` 到 `openmv/src/micropython/ports/stm32/boards/`
   3. 复制 `Ports/micropython/micropython-Add-WeAct-Studio-STM32H7xx-Support.patch` 到 `openmv/src/micropython/`
   4. 前往源码对应文件夹 `openmv/src`
   5. 输入相关命令

        ``` c
        cd micropython
        git am micropython-Add-WeAct-Studio-STM32H7xx-Support.patch
        cd mpy-cross
        make -j
        cd ../../
        make TARGET=WeActStudioSTM32H7xx -j
        ```

相关固件烧录地址，一般烧录openmv.bin即可，这个固件是bootloader.bin和firmware.bin一起的
> bootloader.bin 0x08000000

> firmware.bin 0x08040000

> opemmv.bin 0x08000000
