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
