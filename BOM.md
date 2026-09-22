# Bill of Materials (BOM)

This document lists all the hardware components required to build the ESP32 Dasai Mochi project.

| Reference | Component | Value / Part Number | Qty | Notes / Description |
| :--- | :--- | :--- | :--- | :--- |
| **U1** | Microcontroller | ESP32-WROOM-32 DevKit V1 | 1 | The main brain of the Mochi. (NodeMCU or similar 30/38 pin board works). |
| **DISP1** | OLED Display | 0.96" or 1.3" SSD1306 | 1 | I2C communication (4-pin: GND, VCC, SCL, SDA). |
| **SW1** | Push Button | 6x6x5mm Tactile Switch | 1 | *(Optional)* For changing faces or modes manually. |
| **CBL1** | USB Cable | Micro-USB or USB-C | 1 | For programming and powering the ESP32 (check your specific DevKit). |
| **HW1** | Wires | Dupont Jumper Wires | 1 set | Female-to-Female if connecting directly, or Male-to-Female for a breadboard. |
| **PCB1** | Prototyping | Breadboard / Perfboard | 1 | For assembling and testing the circuit before custom PCB fabrication. |

*Note: If you plan to add OBD2/CAN Bus integration to read car telemetry in the future, you will also need an MCP2515 CAN Bus module.*
