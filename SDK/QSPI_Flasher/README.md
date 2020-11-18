# QSPI Flasher

* [中文版本](./README-zh.md)

Program running in external Flash download algorithm using instructions, support MDK-Keil and STM32CubeProg

## MDK-Keil Project configuration

### STM32H7xx_W25Qxx_WeActStudio.FLM

The.FLM format file is the download algorithm used by MDK Keil
> Keil MDK
Support 4MB ~ 16MB W25Qxx Flash

Please copy the file to `"KeilInstallationDirectory"\ARM\Flash`

Keil needs to configure files when it runs programs using external Flash

1. The configuration of engineering

    ![keilSetup1](Images/KeilSetup1.png)
2. Configure the ROM download address

    ![keilSetup2](Images/KeilSetup2.png)
3. Configure download algorithm

    ![keilSetup3](Images/KeilSetup3.png)
4. Remove other download algorithms, add external download algorithms, and note that there is only one download algorithm

    ![keilSetup4](Images/KeilSetup4.png)

## STM32CubeProg Download configuration

### STM32H7xx_W25Qxx_WeActStudio.stldr

The .stldr file is the download algorithm used by STM32CubeProg

> STM32CubeProgrammer
Support 4MB ~ 16MB W25Qxx Flash

Please copy the file to `"STM32CubeProgrammerInstallationDirectory"\bin\ExternalLoader\`

1. Configure the external Flash download algorithm

    ![STM32CubeProgSetup01](Images/STM32CubeProgSetup01.png)
2. hex or firmware download address (for example .hex file)

    ![STM32CubeProgSetup02](Images/STM32CubeProgSetup02.png)
3. If you are downloading a file in bin format, you need to set it as shown in the figure below (note the.bin format)

    ![STM32CubeProgSetup03](Images/STM32CubeProgSetup03.png)
