# Weather Station (hardware)

This project aims to develop an integrated solution for monitoring meteorological conditions, using state-of-the-art hardware and communication technologies. In this repository, we focus exclusively on the hardware assembly and the integration of the embedded system with a remote server, detailing each component used, its configuration, and the necessary interconnections for efficient data transmission.

For those interested in the complete implementation—including the server, user interfaces, backend, database, and frontend—these aspects are covered in a separate repository. This separation allows for deeper specialization in each area and facilitates project management and collaboration during development.

[Link to the repository](https://github.com/Ludmilahttps/EstacaoMeteorologica)

---

## Participants 
- Augusto Daleffe
- Ludmila Silveira
- Débora Castro
- Eduardo Swarowsky
- Vinicius Muchulski

---

## Communication Diagram
![communication diagram](https://github.com/cyberdebb/estacao_meteorologica/assets/107296659/a105d673-0c97-417b-b6c3-62494302f3ab)

---

## Materials and Methods

In this project, the BMP280 temperature and pressure sensor was not used due to material usage issues. However, the hardware and software allow its use for integration into the weather station.

This section describes in detail the components and processes used in the construction and operation of the weather station.

---

### Characterization of the Embedded System

- [**ESP32**](https://github.com/cyberdebb/estacao_meteorologica/blob/main/sensors/ESP32): A microcontroller module with integrated Wi-Fi and Bluetooth, ideal for IoT applications.
- [**DHT11**](https://github.com/cyberdebb/estacao_meteorologica/blob/main/sensors/DHT11): Temperature and humidity sensor, used for basic environmental measurements.
- [**Pluviometer**](https://github.com/cyberdebb/estacao_meteorologica/blob/main/sensors/Pluviometer): A device used to measure the amount of precipitation.
- [**Arduino SV10 Anemometer**](https://github.com/cyberdebb/estacao_meteorologica/blob/main/sensors/Anemometer): A sensor used to measure wind speed.
- [**Arduino DV10 Wind Direction Indicator**](https://github.com/cyberdebb/estacao_meteorologica/blob/main/sensors/Wind_Direction_Indicator): A sensor used to determine wind direction.

> The Anemometer and the Wind Direction Indicator for Weather Station are usually found together: Anemometer + Wind Direction Indicator for Weather Station - SVDV10
---

### Component Diagram

The diagram below defines the physical configuration used and the interconnection of the components of the weather station:
![Diagrama PI_Grande](https://github.com/cyberdebb/estacao_meteorologica/assets/107296659/c75c16e5-882f-4b96-8760-c9f6ee9439b8)

![Imagem do WhatsApp de 2024-06-15 à(s) 17 48 53_0760c21e](https://github.com/cyberdebb/estacao_meteorologica/assets/107296659/a055155b-81d3-48e2-a00d-33777d665640)

---

### Local Environment Configuration
To configure the local environment, follow the steps below. This file should contain sensitive information such as the SSID and password of the WiFi network, as well as the server URL:

1. Navigate to the `main` folder of your project and create a file called `settings.h`.
2. Add the following lines to the file:
   
   ```cpp
   const char* ssid = "SeuSSID";  // Substitua pelo SSID da sua rede
   const char* password = "SuaSenha";  // Substitua pela senha da sua rede
   String serverURL = "URLDoSeuServidor"; // Substitua pela URL do seu servidor
   ```

---

### Installing the Driver for the ESP32

1. **Download and Install the Driver:**
    - Before connecting the ESP32 to your computer, you need to install the appropriate driver to ensure the device is recognized correctly. You can find the specific driver for the ESP32 at the following link: [Installing the Driver for ESP32 - RoboCore](https://www.robocore.net/tutoriais/instalando-driver-do-nodemcu)
    - Follow the instructions on the website to download and install the driver that corresponds to your operating system.

2. **Connecting the ESP32 to the Computer:**
    - After installing the driver, connect the ESP32 to your computer using a USB cable. If everything is correct, the device should be recognized and a new COM port will be listed in your system.

---

### Configuration in the Arduino IDE

1. **Install the Arduino IDE:**
    - If you haven't already installed it, download and install the Arduino IDE directly from the official website: [Arduino - Software](https://www.arduino.cc/en/software)

2. **Add the ESP32 Board Management URL:**
    - Open the Arduino IDE.
    - Go to **File > Preferences**.
    - In the "Additional Board Manager URLs" field, add the following URL to allow installation of the ESP32 package:

		```
		https://dl.espressif.com/dl/package_esp32_index.json
		```

3. **Install the ESP32 Package:**
	- Go to **Tools > Board: > Board Manager**.
	- In the search bar, type "ESP32".
	- Locate "esp32 by Espressif Systems" and click "Install".

4. **Select the ESP32 Board and COM Port:**
	- After installing the package, go to **Tools > Board** and select your ESP32 model from the list under the title "ESP32-WROOM-DA Module".
	- Go to **Tools > Port** and select the COM port that appears (associated with the ESP32).

---

### Installing the necessary libraries in the Arduino IDE

To install all the necessary libraries, open the Arduino IDE, go to Sketch > Include Library > Manage Libraries, and search for and install the following libraries:
- Adafruit BMP280 Library by Adafruit
- Adafruit BusIO by Adafruit
- Adafruit Unified Sensor by Adafruit
- ArduinoJson by Benoit
- DHT sensor library by Adafruit

---

### Problem Description and Solutions

Problems with the ESP32 Flash Memory: Sometimes, it may be necessary to erase the ESP32's flash memory to resolve stability issues or failures when loading new programs. This procedure becomes essential especially if the physical reset button (RST) is not working, preventing a soft restart of the device.

**Solution:**

1. **Install the esptool Library:** esptool is a command-line tool that allows communication with the ESP chipset to erase or write to the flash memory.
	- Install esptool using pip, the Python package manager:

		```sh
		 pip install esptool
		```  

2. **Erase the Flash Memory:** To completely erase the ESP32's flash memory, follow the steps below. This process is useful for clearing old settings that may be causing conflicts.
	- Open the terminal or command prompt.
	- Run the following command to erase the flash memory:

		```sh
		python -m esptool --chip esp32 erase_flash
		```

3. **Success Verification:**
	- After erasing the flash memory, reconnect the ESP32 to your computer and try loading a new program. If the program loads and runs correctly, this indicates that the memory was successfully erased.

---

## Photo of the Physical Connection
![IMG_2254](https://github.com/cyberdebb/estacao_meteorologica/assets/107296659/c5bda040-61ea-4b4f-9dab-8303a7e4922a)

---

## Video of the System Working
This video demonstrates the operation of the weather station, focusing on the collection and recording of data in real time: <br>

[![Vídeo](https://img.youtube.com/vi/Y84vYU7VSpE/0.jpg)](https://www.youtube.com/watch?v=Y84vYU7VSpE)

---

## Budget
The price survey for each component was conducted through internet research in Brazil, consulting websites specializing in the sale of electronic components such as Amazon, Eletrogate, and Usinainfo. For reference, the budget was compiled in June 2024. All components used in the construction of the station and described in the embedded system characterization subsection are compiled in the table:

| Components                                                                           | Price    | Source      |
| ------------------------------------------------------------------------------------ | -------- | ---------- |
| ESP32	                                                                               | R$49.90  | Amazon     |
| DHT11                                                                                | R$10.36  | Eletrogate |
| BMP280                                                                               | R$7.50   | Eletrogate |
| Anemômetro Arduino + Indicador de Direção do Vento para Estação Meteorológica SVDV10 | R$749.55 | Usinainfo  |

