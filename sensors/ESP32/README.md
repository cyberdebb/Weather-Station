# ESP32
![image-removebg-preview (1)](https://github.com/cyberdebb/estacao_meteorologica/assets/107296659/9e9e1087-d345-4934-84ed-f355491677b7)

The [ESP32 DevKit V1](https://www.espressif.com/sites/default/files/documentation/esp32-wroom-32_datasheet_en.pdf) is one of the development boards created to evaluate the ESP-WROOM-32 module. It is based on the ESP32 microcontroller, which includes support for Wi-Fi, Bluetooth, Ethernet, and low power consumption, all in a single chip.

The ESP32 already features an integrated antenna and RF balun, power amplifier, low-noise amplifiers, filters, and a power management module. This complete solution occupies the smallest possible amount of printed circuit board space. The board uses 2.4 GHz dual-mode Wi-Fi and Bluetooth chips from TSMC built with low-power 40 nm technology, offering excellent power and RF characteristics, making it safe, reliable, and scalable for a wide range of applications.

### Flash Layout
The internal flash of the ESP32 module is organized as a single flash area with 4096-byte pages each. The flash starts at address 0x00000, but many areas are reserved for the ESP32 IDF SDK. There are two different layouts depending on the presence of BLE support.

### Power Supply
Power for the ESP32 DevKit V1 is supplied through the onboard USB Micro-B connector or directly via the “VIN” pin. The power source is selected automatically.

The device can operate using an external power supply ranging from 6 to 20 volts. If more than 12 V is used, the voltage regulator may overheat and damage the device. The recommended range is between 7 and 12 volts.

### Connect, Register, Virtualize, and Program
The ESP32 DevKit V1 comes with an onboard USB-to-serial chip that allows programming and UART access to the ESP32 module. Depending on your operating system (Mac or Windows), drivers may be required and can be downloaded from Espressif’s official documentation page. On Linux systems, the DevKit V1 should work out of the box.

![image](https://github.com/cyberdebb/estacao_meteorologica/assets/107296659/b46d96a6-a364-44a7-8699-3bbed1ecb281)

## Specifications
| INFORMATION                         | ESP32                                           |
|------------------------------------|------------------------------------------------|
| PROCESSOR                          | Tensilica 32-bit Single-/Dual-core Xtensa LX6 CPU |
| OPERATING VOLTAGE                  | 3.3 V                                          |
| INPUT VOLTAGE                      | 7–12 V                                         |
| DIGITAL I/O PINS (DIO)             | 25                                             |
| ANALOG INPUT PINS (ADC)            | 6                                              |
| ANALOG OUTPUT PINS (DAC)           | 2                                              |
| UARTs                              | 3                                              |
| SPIs                               | 2                                              |
| I2Cs                               | 3                                              |
| FLASH MEMORY                       | 4 MB                                           |
| SRAM                               | 520 KB                                         |
| CLOCK SPEED                        | 240 MHz                                        |
| WI-FI                              | IEEE 802.11 b/g/n/e/i                          |
| WI-FI FEATURES                     | Integrated TR switch, balun, LNA, power amplifier, and matching network |
| WI-FI SECURITY                     | WEP or WPA/WPA2 authentication, or open networks |
| DIMENSIONS                         | 51.5 × 29 × 5 mm                               |
