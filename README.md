# ESP32 Dasai Mochi 🚗😠

An open-source, DIY animated dashboard companion powered by the ESP32 and an OLED display. This project aims to replicate and expand upon the beloved "Dasai Mochi" concept, allowing for custom animations, expressions, and hardware logging.

## 🌟 Features
*   **Animated Expressions:** A variety of idle, happy, sad, and angry faces.
*   **ESP32 Powered:** Plenty of memory for smooth, frame-by-frame animations.
*   **I2C OLED Display:** Crisp, high-contrast visuals using an SSD1306 screen.
*   **Hardware Logged:** Fully documented schematics, BOM, and wiring diagrams for easy replication.

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

### Schematic
*(Note: Replace the image link below once you upload your schematic to the repository)*

![Project Schematic](Hardware/Schematics/placeholder_schematic.png)

## 💻 Firmware & Software Setup

To flash the code to your ESP32, you will need the Arduino IDE or PlatformIO.

**Required Libraries:**
*   `Adafruit GFX Library` (For graphics handling)
*   `Adafruit SSD1306` (For the OLED driver)

**Installation Steps:**
1. Clone this repository to your local machine.
2. Open the source code in your preferred IDE.
3. Install the required libraries via the IDE's Library Manager.
4. Select your specific ESP32 board model and COM port.
5. Compile and upload!

## 📂 Repository Structure
*   `/Hardware` - Schematics, PCB files, and 3D enclosure designs.
*   `/Firmware` - Source code for the ESP32.
*   `/Docs` - Datasheets for the ESP32, OLED, and other peripherals.
*   `BOM.md` - Bill of Materials / Parts list.

## 🚀 To-Do / Roadmap
- [ ] Draw base schematic and upload PDF/PNG.
- [ ] Code base idle animation logic.
- [ ] Add button interrupt to switch expressions.
- [ ] Design a 3D-printable case.

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

*Note: If you plan to add OBD2/CAN Bus integration to read car telemetry in the future, you will also need an MCP2515 CAN Bus module.*
