# WeAct Studio STM32H7xx 核心板

* [English Version](./README.md)

> `0.96''` ST7735 TFT, TF Card, 8MB QSPI FLASH(SPI1)， 8MB QSPI FLASH(QSPI1), 8Bit DVP Port

> 相关数据手册，详情浏览[Datasheet](https://github.com/WeAct-TC/WeAct-Studio-Product.git)

> 使用资料，详情浏览[SDK](https://github.com/WeAct-TC/WeAct-Studio-Product.git)

> 核心板
> 可刷入Openmv固件, 详情浏览[SDK/openmv](https://github.com/WeAct-TC/WeAct-Studio-Product.git)

> 程序可运行在外部Flash，详情浏览[SDK/QSPI_Flasher](https://github.com/WeAct-TC/WeAct-Studio-Product.git)

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

### 接口和按键

* 2*22 Pin 2.54mm I/O x 2
* 4 Pin 2.54mm SW x 1
* USB C (type C)  x 1
* MicroSD TF x 1
* 8Bit DCMI x 1
* User Key K1 (PC13) x 1
* NRST Key x 1
* BOOT0 Key x 1

### 设计和质量

* 采用沉金TG155板材，四层板设计
* 采用无铅焊接工艺
* 采用按键的形式设置BOOT
* 采用高质量晶振，金属外壳，均能良好起振
* 始终使用原装ST芯片

> 不提供出厂测试程序，防止翻版出现，影响质量

### 芯片批号

| STM32H750VBT6 | STM32H743VIT6 |
| :--: | :--: |
|Date Code|Date Code|
|930 (2020.06)|-----|
|031 (2020.10)|036 (2020.10)|

### 淘宝购买链接

1. [WeAct Studio官方店](https://shop118454188.taobao.com/index.htm?spm=2013.1.w5002-17867322799.2.212f5cb16nqwNP)

### 速卖通购买链接

1. [WeAct Studio官方店](https://www.aliexpress.com/store/910567080)

## 开始使用

### 安装 0.96'' ST7735 TFT(现购买带屏幕的板子已经预装)

![step1](./Images/ST7735/Install-1.png)

#### 重要说明

1. 沿红色划线处向下弯折90°，可使用核心板板边辅助弯折
2. 沿蓝色划线处向上弯折90°，可使用核心板板边辅助弯折
3. 绿色划线处请勿弯折，避免造成屏幕排线断路
4. 核心板屏幕安装处粘贴双面胶，之后按照屏幕排线折叠纹路可轻松完成屏幕安装

> 注：粘贴安装时，请确保屏幕边框未接触板上的电子元件

![step2](./Images/ST7735/Install-2.png)

### 安装摄像头

* 支持的摄像头: OV7670, OV2640, OV7725, OV5640-AF
* **如果使用OV5640自动对焦功能，务必焊接SB4，SB5**

![step3](./Images/ST7735/Install-3.png "Camera Install")

### 出厂例程说明

1. 屏幕测试
2. 摄像头测试
3. ADC 测试
4. Flash 和 TF卡测试

> 点击按键`K1`切换到下一个测试项目 Click `K1` to switch to the next test item

### 如何进入ISP模式

#### 说明

* 方法1：上电状态下，按住BOOT0键和复位键，然后松开复位键，0.5秒后松开BOOT0键
* 方法2：掉电状态下，按住BOOT0键，上电后0.5S松开BOOT0
* DFU模式：使用数据线连接电脑即可
* 串口模式：使用USB转串口连接核心板的PA9,PA10即可
* 软件： STM32CubeProg。

### 电源及尺寸

* 输入电压: 3.3V-5.5V
* DC-DC 输出电流: 1A Max.
* 尺寸: 40.64mm * 66.88mm

![WeAct H7 View](Images/BoardShape.png)

![WeAct H7 View](Images/STM32H750VB_2.jpg)
