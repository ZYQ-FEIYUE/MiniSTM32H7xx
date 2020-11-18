# 说明

* [English Version](./README.md)

## 内部Flash固件

> Openmv 固件放在内部地址，从0x08000000开始

### 8MB SPI Flash

> 8MB SPI Flash 作为Python代码存储器

### 固件下载地址定义

* bootloader.*  -> 0x08000000

* firmware.*    -> 0x08040000

* openmv.*      -> 0x08000000

openmv.* 为bootloader和firmware两个固件的合并固件，按需选择烧录即可
