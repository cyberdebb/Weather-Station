# Arduino DV10 Wind Direction Indicator
![image-removebg-preview (5)](https://github.com/cyberdebb/estacao_meteorologica/assets/107296659/5addfcc9-ec4f-4d65-b7c1-ada5bca67632)

The Wind Direction Indicator is another component for a weather station, a climate monitoring tool capable of providing several types of data. Among them, we can highlight wind speed measurement through an anemometer and rainfall measurement through a rain gauge.

In many projects, this information is extremely important, as it can influence crops, indicate possible weather events, and consequently help assess the possibility of taking preventive action to avoid damage to crops, residences, and related infrastructure.

The DV10 Wind Direction Indicator is a product manufactured almost entirely from aluminum, with the exception of the sensor mounting areas, which are designed to increase insulation against external interference.

To assist with installation processes, the Wind Direction Indicator features an exclusive mounting system compatible with different mast models and thicknesses. Below is an image demonstrating its operation: a threaded system with nuts.

![image](https://github.com/cyberdebb/estacao_meteorologica/assets/107296659/c993cbd7-67a6-452e-bcf8-3362f92fddd9)

Mounting system for supports and masts.

The sensing module of the Wind Direction Indicator uses a distinctive measurement system based on resistance variation to indicate the direction from which the wind blows. Each direction is directly associated with a 10 kΩ resistor, according to the electrical schematic available on the Usinainfo website, which uses a 4.7 kΩ resistor in its connection. The operating values are shown below:

![image](https://github.com/cyberdebb/estacao_meteorologica/assets/107296659/4f825205-755d-4b9b-b003-d3b23d771006)

Resistance and wind direction value table using a 4.7 kΩ resistor

As shown in the table above and in the image below, the Wind Direction Sensor has eight reed switches connected to eight 10 kΩ resistors arranged in a series configuration. Depending on the vane movement, the resistance values are summed, resulting in different output voltage levels for analog measurement.

![image](https://github.com/cyberdebb/estacao_meteorologica/assets/107296659/0ca2bc1a-e1a5-4402-a312-2b8f93202c88)

Wind Direction Indicator operating module

The reed switches are actuated by a unique magnet fixed to one of the moving parts of the Wind Direction Indicator. This magnet is responsible for bringing the plates of the reed switch closer together, closing the circuit and connecting the resistors. See the image below showing the magnet and its location:

![image](https://github.com/cyberdebb/estacao_meteorologica/assets/107296659/e7b69386-434b-4e62-ae16-ae04ea37a05e)

Reed switch activation system

The operating principle of the Wind Direction Indicator is extremely simple: as the vane moves, the output voltage varies, and this voltage is then associated with a specific wind direction through software running on the Arduino. However, it is important to pay attention to the following detail:

![image](https://github.com/cyberdebb/estacao_meteorologica/assets/107296659/2e8ad047-bb83-4340-863e-c2f4247f71de)

Wind Direction Indicator and vane

For those who want a direct, non-digital visualization of the information, it is worth highlighting the wind direction indicators and the vane, which are responsible for aligning and positioning the sensor according to the wind direction at the measurement location.

## Features
- Can be used with other microcontrollers;  
- Shaft with sealed bearing (maintenance-free);  
- Sealed magnetic sensor;  
- Easy installation;  
- High precision;  
- Good stability;  
- Data linearity;  
- Strong anti-interference protection;  
- Clamp for mounting;  
- Weather-resistant;  
- Ideal for greenhouses, monitored environmental protection areas, weather stations, ports, agricultural areas, among other environments;

## Specifications
| INFORMATION                        | Arduino SV10 Wind Direction Indicator |
| ---------------------------------- | ------------------------------------- |
| MATERIAL                           | Aluminum and durable plastic          |
| OPERATING VOLTAGE                  | 5 V DC                                |
| TYPE                               | Analog                                |
| TRANSMISSION MEDIUM                | Cable                                 |
| OPERATING TEMPERATURE              | -40°C ~ 80°C                          |
| CABLE LENGTH                       | ~5 meters                             |
| SUPPORT LENGTH                     | 205 mm                                |
| MAXIMUM TUBE DIAMETER FOR MOUNTING | 35 mm                                 |
| ROTATION                           | 360°                                  |
| ACCURACY                           | ~95%                                  |

## Connections
| Wind Direction Sensor | ESP WROOM 32 | ESP32 Pin Number |
|:---------------------:|:------------:|:---------------:|
|          VCC          |      5V      |       5V        |
|          GND          |      GND     |       GND       |
|          DAT          |     GPIO     |     GPIO26      |

## Results
![WhatsApp Image from 2024-06-18 at 14:12:54_f64e1a8b](https://github.com/cyberdebb/estacao_meteorologica/assets/107296659/805abf03-ba21-4d5a-897c-72530602b2bb)
