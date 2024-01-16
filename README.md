# Custom SPI Driver for STM32F401 Black Pill

## Overview

This project provides a custom SPI driver for the STM32F401 Black Pill microcontroller. The driver supports full-duplex communication, hardware slave management, and configurable SPI speed. Additionally, a custom-written timer header is included to enable delay functionality using General Purpose Timer 2.

## Files

- **main.c**: This sample driver script demonstrates SPI communication with the popular MPU9250 IMU. The SPI frame size is set to 16 bits.

- **SPI.h / SPI.c**: These files contain the implementation of the custom SPI driver. The driver supports full-duplex communication and hardware slave management. SPI baud rate is set to HSI (16MHz) divided by 64, but it can be modified as needed by changing bits 5:3 (BR[2:0]) of the SPI1_CR1 register.

- **Timer.h / Timer.c**: The custom-written timer header and source files. These provide delay functionality using General Purpose Timer 2.

## Usage

1. **Download**: Clone or download the repository to your local machine.

    ```bash
   https://github.com/Adithyan-m/STM32f401_SPI_driver
    ```

2. **Integration with STM Cube IDE**:

    - Add the `inc` directory to your STM Cube IDE project.
    - Make sure to include the necessary device headers that are auto-added when selecting STM32F401 as the target in STM Cube IDE.

3. **Configuration**:

    - Customize the `main.c` file to implement your specific application logic. The provided script demonstrates SPI communication with the MPU9250 IMU, and the SPI frame size is set to 16 bits.
    - Modify SPI configurations and timing parameters in `spi.h` and `timer.h` as needed.

4. **Build and Flash**:

    - Build the project using STM Cube IDE.
    - Flash the firmware onto your STM32F401 Black Pill.

## Functions

Refer to the inline comments included the timer.c and spi.c files to understand the funtions
