# ESP32 & PN532 NFC Reader for Home Assistant

This repository contains an ESPHome configuration to build a local NFC/RFID reader using an ESP32 and a PN532 module. It uses I2C for communication and sends scanned tags directly to Home Assistant's built-in Tag Manager.

## Hardware Required
* ESP32 Development Board
* PN532 RFID/NFC Module
* 4 Jumper Wires

## Wiring Diagram (I2C)

Before wiring, ensure the DIP switches on the PN532 board are set to **I2C mode** (refer to the white table printed on your module—typically Switch 1 is **ON** and Switch 2 is **OFF**).

| ESP32 Pin | PN532 Pin | Purpose |
| :--- | :--- | :--- |
| **3V3** | **VCC** | Power |
| **GND** | **GND** | Ground |
| **GPIO21** | **SDA** | I2C Data |
| **GPIO22** | **SCL** | I2C Clock |

## Installation & Usage

1. **Update Wi-Fi Credentials:** Open the YAML file and replace `YOUR_WIFI_SSID` and `YOUR_WIFI_PASSWORD` with your actual network details.
2. **Flash the ESP32:** Flash the configuration to your ESP32 using the ESPHome dashboard.
3. **Scan a Tag:** Once connected to Wi-Fi and Home Assistant, tap an NFC/RFID tag to the reader. 
4. **Automate:** Navigate to **Settings > Tags** in Home Assistant. Your newly scanned tag will automatically appear. Click the automation icon next to it to trigger your smart home actions.
