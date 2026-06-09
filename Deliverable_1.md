# Semester Project Deliverable 1
## Group Members
- Mary Arop
- Pete Njagi
- Dylan Saisi
- Samuel Wanyoike
- Kelvin Mwaniki
- Daniel Nyabuto

# Question 1
## Environmental Requirements for Tulips

| Parameter | Optimal Requirement | Description |
|------------|-------------------|-------------|
| Temperature Range | 10°C – 18°C | Cool temperatures promote healthy growth and high-quality blooms. |
| Relative Humidity | 60% – 80% | Maintains plant health while reducing the risk of fungal diseases. |
| Soil Type | Well-drained sandy loam soil rich in organic matter | Supports root development and prevents waterlogging. |
| Soil Moisture Content | Moderately moist (50% – 70% field capacity) | Ensures adequate water supply without causing bulb rot. |
| Soil pH Range | 6.0 – 7.0 | Slightly acidic to neutral soil promotes efficient nutrient uptake. |
| Sunlight Exposure | 6 – 8 hours per day | Direct sunlight supports flowering and bulb development. |


# Question 2: Hardware Components for Flower Monitoring System

## 2.0 Introduction

This section presents all the hardware components required to develop an embedded IoT system for monitoring environmental conditions that support optimal flower growth. The system collects environmental data such as temperature, humidity, gas levels, and soil conditions, and uses these inputs for monitoring and control purposes.

## 2.1 Main Controller Unit

### ESP32-S DevKit (30-pin)

The ESP32-S DevKit serves as the central processing unit of the system.

**Functions:**

* Processes data from all connected sensors
* Enables Wi-Fi and Bluetooth communication for IoT connectivity
* Controls output devices such as the relay module and display

## 2.2 Environmental Sensors

### DHT22 (AM2302) Temperature and Humidity Sensor

The DHT22 sensor is used to measure environmental temperature and relative humidity.

**Functions:**

* Measures ambient temperature
* Measures relative humidity
* Provides digital output for easy interfacing with ESP32

### MQ-5 Gas Sensor (LPG, Methane, Coal Gas Sensor)

The MQ-5 sensor is used for detecting flammable gases in the environment.

**Functions:**

* Detects LPG, methane, and coal gas
* Provides analog output proportional to gas concentration
* Requires calibration for accurate readings

## 2.3 Display Unit

### 1.3" I2C OLED Display (128×64)

The OLED display is used to show real-time sensor data.

**Functions:**

* Displays temperature and humidity readings
* Shows gas concentration levels
* Indicates system status and alerts
* Uses I2C communication (SDA/SCL)

## 2.4 Output Control Module

### 5V 1-Channel Relay Module (Low-Level Trigger)

The relay module is used to control external electrical devices.

**Functions:**

* Acts as an electronic switch
* Controls devices such as fans, pumps, or alarms
* Provides electrical isolation between ESP32 and high-power devices

## 2.5 Supporting Electronic Components

These components ensure stable and reliable operation of the system.

### Resistors

* 10kΩ pull-up resistor (used for stabilizing the DHT22 data line)
* Voltage divider resistors (used for MQ-5 signal conditioning if required)

### Capacitors

* 0.1µF ceramic capacitors for noise filtering
* 10µF electrolytic capacitor for power stabilization

### Breadboard

Used for prototyping and testing the circuit without soldering.

### Jumper Wires

Used to connect different modules and components on the breadboard.

### Power Supply

* 5V regulated power supply (USB or adapter)
* Provides stable power to the ESP32 and connected modules

## 2.6 Optional Component

### Soil Moisture Sensor (Capacitive Type)

This sensor measures the water content in the soil.

**Functions:**

* Monitors soil moisture levels
* Helps ensure optimal watering conditions for flower growth
* More durable and corrosion-resistant than resistive sensors

## 2.7 Summary of Components

| Component                       | Function                               | Interface Type           |
| ------------------------------- | -------------------------------------- | ------------------------ |
| ESP32-S DevKit                  | Main processing unit                   | GPIO / Wi-Fi / Bluetooth |
| DHT22 Sensor                    | Temperature and humidity monitoring    | Digital                  |
| MQ-5 Gas Sensor                 | Gas detection (LPG, methane, coal gas) | Analog                   |
| 1.3" OLED Display               | Data visualization                     | I2C                      |
| Relay Module                    | Controls external devices              | Digital                  |
| Resistors                       | Signal stabilization                   | Passive                  |
| Capacitors                      | Noise filtering and power smoothing    | Passive                  |
| Breadboard                      | Circuit prototyping                    | N/A                      |
| Jumper Wires                    | Electrical connections                 | N/A                      |
| Power Supply                    | System power source                    | DC 5V                    |
| Soil Moisture Sensor (Optional) | Soil water monitoring                  | Analog                   |

## 2.8 Conclusion

The selected hardware components provide a complete embedded system capable of monitoring key environmental factors required for proper flower growth. These components ensure accurate sensing, real-time data display, and the ability to control external devices through IoT integration using the ESP32 microcontroller.

# Question 3
## Hardware Component References and Datasheets

### a. 1.3" White IIC 128×64 OLED LCD

This display module utilizes the SH1106 driver integrated circuit (IC).

| Resource | Link |
|----------|------|
| Driver IC Datasheet | https://www.displayfuture.com/Display/Datasheet/Controller/SH1106.pdf |
| Product Reference Wiki | https://www.waveshare.com/wiki/1.3inch_OLED_Module |

### b. ESP32S DevKIT Wi-Fi + BLE Module (30-Pin)

This standard 30-pin development board is built around the ESP32-WROOM-32 system-on-chip (SoC) by Espressif Systems.

| Resource | Link |
|----------|------|
| Official Module Datasheet | https://documentation.espressif.com/esp32-wroom-32_datasheet_en.pdf |
| Hardware Specifications | https://vdoc.ai-thinker.com/en/esp32/docs |

### c. DHT22 (AM2302) Temperature and Humidity Sensor

The DHT22 (AM2302) provides digital output data over a single-bus communication protocol.

| Resource | Link |
|----------|------|
| Manufacturer Datasheet | https://cdn-shop.adafruit.com/datasheets/Digital+humidity+and+temperature+sensor+AM2302.pdf |

### d. MQ-5 LPG, Natural Gas, and Coal Gas Sensor

An analog gas sensor optimized for detecting leakage of combustible gases in domestic and industrial environments.

| Resource | Link |
|----------|------|
| Technical Datasheet | https://www.winsen-sensor.com/d/files/MQ-5.pdf |

### e. 5V 1-Channel Low-Level Trigger Relay Module

This relay module contains a Songle SRD-05VDC-SL-C mechanical relay and an optocoupler for electrical isolation and low-level trigger operation.

| Resource | Link |
|----------|------|
| Core Relay Component Datasheet | https://www.snapeda.com/parts/SRD-05VDC-SL-C/Songle%20Relay/datasheet/ |
| Module Product Webpage | https://lastminuteengineers.com/one-channel-relay-module-arduino-tutorial/ |

# Question 4
## Part a
[View Schematic for part a](schematics/schematic_4a_2026_06_09_v1.pdf)

## Part b
[View Schematic for part b](schematics/Schematic1_question4b.pdf).

## Part c
[View Schematic for part c](schematics/Schematic_Question4c.pdf).
