# STM32G431 Development Board (v1.0)

## Overview
This is a high-performance development platform based on the **STM32G431Vx** microcontroller (ARM® Cortex®-M4 with FPU). The board is engineered for advanced power electronics and motion control applications, integrating high-speed communication interfaces, precision power monitoring, and wireless connectivity.

## Key Hardware Features

### 1. Processing Core
* **MCU**: STM32G431Vx, 32-bit ARM® Cortex®-M4 with FPU, high-performance analog peripherals, and mathematical accelerators (CORDIC/FMAC).
* **Clocking**: 8MHz High-Speed External (HSE) crystal and 32.768kHz Low-Speed External (LSE) crystal for RTC.

### 2. Power Management
* **Dual Power Domains**: 
    * **Logic Power**: 5V input via USB Type-C, converted to 3.3V via **TLV62569** (DC-DC) for high efficiency.
    * **Analog Power**: Dedicated **LP5907** ultra-low noise LDO for VDDA and audio precision.
* **Motor Power (MVCC)**: High-voltage input via XT30 connectors with **SMCJ33A** TVS protection for regenerative braking spikes.

### 3. Integrated Peripheral Modules
* **Motor Driving**: 
    * 4x **A4950** Full-Bridge Motor Drivers for DC motor control.
    * Integrated current and voltage monitoring via 4x **INA226** (I2C) high-side monitors.
* **Wireless Connectivity**: Onboard **ESP32-C6** module supporting Wi-Fi 6, Bluetooth 5 (LE), Zigbee, and Thread.
* **Audio System**:
    * **PCM5102A** High-resolution Audio DAC with 3.5mm Jack output.
    * **ICS-43434** Digital I2S MEMS Microphone.
* **Communication**:
    * **TJA1044GT** Transceiver for FDCAN connectivity.
    * **CH340N** USB-to-UART bridge for debugging and firmware logging.
* **Storage**:
    * 64M-bit SPI Nor Flash (**W25Q64JV**).
    * 256K-bit I2C EEPROM (**AT24C256**).

### 4. User Interface
* **Display**: Dedicated SPI header for 1.77" LCD modules.
* **Interaction**: 4x Programmable User LEDs (Red) and 4x User Push-buttons (KEY1-KEY4).

## Peripheral Pin Mapping
| Component | Interface | Pin Assignment |
| :--- | :--- | :--- |
| **USB-Serial** | UART1 | TX: PA9, RX: PA10 |
| **ESP32-C6** | UART2 | TX: PA2, RX: PA3 |
| **CAN Bus** | FDCAN1 | TX: PD1, RX: PD0 |
| **Power Monitors** | I2C3 | SCL: PC8, SDA: PC9 |
| **Audio DAC/Mic** | I2S | SCK: PB3, WS: PA15, SD: PB5 |
| **External Flash** | SPI1 | SCK: PA5, MISO: PA6, MOSI: PA7 |

## Technical Specifications
* **Logic Voltage**: 3.3V DC
* **Motor Voltage Range**: Up to 30V DC (MVCC)
* **MCU Package**: LQFP-100
* **Communication Support**: FDCAN, Wi-Fi 6, BLE, Zigbee, SPI, I2C, I2S


