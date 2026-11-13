# ESP32 Dasai Mochi 🚗😠

An open-source, DIY animated dashboard companion powered by the ESP32 and an OLED display. This project aims to replicate and expand upon the beloved "Dasai Mochi" concept, allowing for custom animations, expressions, and hardware logging.

## 🌟 Features
*   **Animated Expressions:** A variety of idle, happy, sad, and angry faces.
*   **ESP32 Powered:** Plenty of memory for smooth, frame-by-frame animations.
*   **I2C OLED Display:** Crisp, high-contrast visuals using an SSD1306 screen.
*   **Power On Noise:** Features some noises as a companion.
*   **Touch Sensitive:** Allows for human interaction.


## 🛠️ Hardware Overview

*Please see the [BOM.md](BOM.md) file for a complete list of required parts.*

### Pinout Mapping
Connect the OLED display to the ESP32 using the standard I2C pins.

| ESP32 Pin | OLED Pin | Description |
| :--- | :--- | :--- |
| `3V3` | `VCC` | 3.3V Power |
| `GND` | `GND` | Ground |
| `GPIO 22` | `SCL` | I2C Clock |
| `GPIO 21` | `SDA` | I2C Data |

Connect the Touch Sensor and Buzzer
| ESP32 Pin | Item | Description |
| :--- | :--- | :--- |
| `GPIO 1` | `Touch Sensor I/O` | Touch Sensor |
| `GPIO 18` | `Buzzer` | Buzzer Control |

### Schematic
<img width="763" height="1080" alt="Project Schematic" src="https://github.com/user-attachments/assets/ec90e3d5-5481-4564-9cd3-f455e9a971d2" />

## 💻 Firmware & Software Setup

Open https://themochi.huykhong.com/ and connect ESP32.
Upon Flashing, device will boot up.

Alternatively, design will be done on:
https://www.oledanimationmaker.com/

## Enclosure

3D Printed Enclosure was taken from Leroyd's Yeti Design, available at:
https://makerworld.com/en/models/2109424-compagnon-309-build-your-expressive-robot?from=search#profileId-2281938

STL file is included in this repository.

# Bill of Materials (BOM)

This document lists all the hardware components required to build the ESP32 Dasai Mochi project.

| Reference | Component | Value / Part Number | Qty | Notes / Description |
| :--- | :--- | :--- | :--- | :--- |
| **U1** | Microcontroller | ESP32-WROOM-32 DevKit V1 | 1 | The main brain of the Mochi. (NodeMCU or similar 30/38 pin board works). |
| **DISP1** | OLED Display | 0.96" or 1.3" SSD1306 | 1 | I2C communication (4-pin: GND, VCC, SCL, SDA). |
| **TOUCH SENSOR** | Touch Sensor | TTP233h | 1 | *(Optional)* For changing faces or modes manually. |
| **BUZZER** | Buzzer | Small Buzzer | 1 | *(Optional)* For emulating the Dasai Mochi noises. |
| **CBL1** | USB Cable | Micro-USB or USB-C | 1 | For programming and powering the ESP32 (check your specific DevKit). |
| **HW1** | Wires | Dupont Jumper Wires | 1 set | Female-to-Female if connecting directly, or Male-to-Female for a breadboard. |
| **PCB1** | Prototyping | Breadboard / Perfboard | 1 | For assembling and testing the circuit before custom PCB fabrication. |
| **3D Printed Shell** | Enclosure | 1 | To hide electronics. |

*Note: If you plan to add OBD2/CAN Bus integration to read car telemetry in the future, you will also need an MCP2515 CAN Bus module.*
