# ZC-3566 (LPDDR3) SBC/Mainboard Specification

| Item | Details |
| --- | --- |
| Product | ZC-3566 (LPDDR3) intelligent mainboard |
| Document version | V5.1 |
| Release status | Mass production |
| Reference release date | 2026.05 |

## Overview

ZC-3566 is an RK3566-based intelligent mainboard for display, multimedia and embedded-control products. It integrates display, networking, audio, USB and serial expansion interfaces to simplify product integration. Supported operating systems include Android 11, Debian 11, Buildroot and Ubuntu 20.04.

Typical applications include AI servers, face-payment terminals, security, medical, transportation, finance, industrial control, smart education and smart retail equipment.

## Key Features

- Rockchip RK3566 quad-core 64-bit Cortex-A55 processor, up to 1.8 GHz.
- ARM Mali-G52 2EE GPU, compatible with OpenGL ES 1.1/2.0/3.2, OpenCL 2.0 and Vulkan 1.1.
- Integrated LVDS, MIPI, eDP, HDMI 2.0, 100M Ethernet, Wi-Fi 6, Bluetooth 5.1, audio amplifier, TF-card expansion and IR remote-control support.
- Four USB interfaces, up to six expandable serial ports, GPIO and ADC-key expansion.
- H.265/H.264/VP9 decoding up to 4K at 60 fps and H.265/H.264 decoding at 1080p up to 100 fps.
- Designed for 7 x 24-hour unattended operation when used in a validated system configuration.

## Board Views And Dimensions

### PCBA Top View

![ZC-3566 PCBA top view](ZC-3566-SBC/ZC-3566-PCBA-top.jpeg?raw=true)

### PCBA Bottom View

![ZC-3566 PCBA bottom view](ZC-3566-SBC/ZC-3566-PCBA-bottom.jpeg?raw=true)

The board image is representative only. Board appearance and populated options may vary by production batch and customer configuration.

### Mechanical Dimensions

| Item | Specification |
| --- | --- |
| Board size | 126.5 mm x 70 mm, tolerance +/- 0.5 mm |
| Board thickness | 1.6 mm, tolerance +/- 10% |
| Mounting holes | 4 x diameter 3.0 mm, tolerance +/- 10% |

![ZC-3566 dimensions](ZC-3566-SBC/ZC-3566-dimensions.png?raw=true)

![ZC-3566 front connector dimensions](ZC-3566-SBC/ZC-3566-front-connectors.png?raw=true)

![ZC-3566 side profile](ZC-3566-SBC/ZC-3566-side-profile.png?raw=true)

> The DC jack is eccentric. Confirm its mechanical position before enclosure design.

## Hardware Specifications

| Category | Specification |
| --- | --- |
| CPU | Quad-core 64-bit Cortex-A55, up to 1.8 GHz |
| GPU | ARM Mali-G52 2EE; OpenGL ES 1.1/2.0/3.2, OpenCL 2.0 and Vulkan 1.1 |
| Memory | 2 GB / 4 GB / 8 GB LPDDR3 options |
| eMMC | 32 GB / 64 GB / 128 GB options |
| Operating systems | Android 11, Debian 11, Buildroot, Ubuntu 20.04 |
| Display outputs | eDP, HDMI 2.0, MIPI and LVDS; default configuration supports one display output at a time |
| MIPI | 31-pin FPC, up to 2560 x 1600 at 60 fps; shared selection with LVDS |
| LVDS | 30-pin connector, up to 1920 x 1080 at 60 fps |
| eDP | 20-pin connector, up to 2560 x 1600 at 60 fps |
| HDMI | Type-A HDMI TX 2.0; up to 4K at 60 fps or 1080p at 120 fps |
| Video decoding | 4K at 60 fps H.265/H.264/VP9; 1080p at 100 fps H.265/H.264 |
| USB | One USB 3.0 host, one USB 2.0/OTG and two internal USB connectors |
| Serial and GPIO | Up to six TTL serial ports, configurable RS232/RS485 options, four GPIOs and ADC-key expansion |
| Touch | One I2C capacitive-touch interface |
| Audio | Stereo output with integrated 2 x 5 W amplifier for 8-ohm speakers |
| Network | 10/100M adaptive Ethernet, Wi-Fi 6 and Bluetooth 5.1; optional 4G peripheral expansion |
| RTC | Supported |
| System update | TF card or PC update |
| Operating environment | 0 to 70 C; recommended 5 to 35 C; 10% to 90% RH, non-condensing |

## Materials And Manufacturing

| Item | Requirement |
| --- | --- |
| PCB | Six-layer FR-4, OSP impedance-controlled board, TG150, matte black, lead-free |
| Electronic components | Original lead-free, RoHS-compliant components |
| Manufacturing | Lead-free environmental process; ISO 9001 quality-management process |

## Electrical Characteristics (Bare Board)

| Parameter | Min. | Typical | Max. | Unit |
| --- | ---: | ---: | ---: | --- |
| Operating voltage | 9 | 12 | 14 | V |
| Operating current | 171 | 181 | 340 | mA |
| Shutdown current | 4.36 | 4.45 | 4.52 | mA |
| Mainboard power | 2.05 | 2.17 | 4.08 | W |
| Speaker output power, 8 ohm | 4 | 4.5 | 5 | W |
| RTC operating current | 0.452 | 0.482 | 0.528 | uA |
| 5 V USB output current, total | 1810 | 2030 | 2320 | mA |
| 3.3 V UART output current, total | 980 | 1270 | 1420 | mA |

Notes:

- USB and UART current values are the total available output current at the same voltage rail. Check the requirement of each connected peripheral.
- Current consumption is measured with the current firmware. Firmware revisions can change the value slightly.
- The 9 to 14 V range applies to bare-board operation. When external devices are connected, select the supply voltage and current capacity according to the whole system.

## Connector Overview

The following figure identifies the main connectors on the top side of the board.

![ZC-3566 connector map](ZC-3566-SBC/ZC-3566-PCBA-top.jpeg?raw=true)

| Connector | Function |
| --- | --- |
| DC / DC-IN | 12 V power input |
| LCD-BL / LCDVCC | LCD backlight and LVDS logic-voltage selection |
| HDMI / eDP-DATA / LVDS-DATA / MIPI LCD | Display output interfaces |
| Wi-Fi/BT | IPEX-1 external antenna connector |
| RJ45 / POE | 100M Ethernet and optional external PoE module connector |
| USB-OTG / USB 3.0 HOST / CUSB2 / CUSB3 | USB interfaces |
| TF / RTC / UBOOT / DEBUG | Storage, RTC battery, firmware download and debug |
| MIC / headphone / SPK | Audio interfaces |
| CTP / IR&LED / GPIO / KEY | Touch, remote-control LED, GPIO and key expansion |
| TTYS0 / TTYS5 / TTYS6 / TTYS7 / TTYS8 / TTYS9 | TTL serial ports with configurable RS232/RS485 options |

## Internal Interface Definitions

### DC-IN

![DC-IN connector](ZC-3566-SBC/DC-IN.jpeg?raw=true)

| Pin | Signal | Attribute | Description |
| ---: | --- | --- | --- |
| 1 | 12V | Input | 12 V power input |
| 2 | 12V | Input | 12 V power input |
| 3 | GND | Ground | Power ground |
| 4 | GND | Ground | Power ground |

- Use this connector for the internal power-input connection.
- Input range is 9 to 14 V. Do not use an adapter outside this range.
- A 2.54 mm connector pin is rated at 2.5 A; two power pins provide a maximum of 5 A.

### LCD-BL Backlight Connector

![LCD-BL connector](ZC-3566-SBC/LCD-BL.jpeg?raw=true)

| Pin | Signal | Attribute | Description |
| ---: | --- | --- | --- |
| 1-2 | BL-12V_IN | Output | 12 V backlight power from the external adapter |
| 3 | ON/OFF | Output | Backlight enable, active high |
| 4 | ADJ | Output | PWM brightness control |
| 5-6 | GND | Ground | Power ground |

- Connect to the LVDS/eDP backlight connector. The 12 V rail is supplied directly from the DC input.
- If ADJ is not required, leave it unconnected or connect it to ON/OFF according to the panel or backlight specification.

### LCDVCC LVDS Logic-Voltage Selection

![LCDVCC jumper](ZC-3566-SBC/LCDVCC.jpeg?raw=true)

| Pins | Selection |
| --- | --- |
| 1-2 | 3.3 V LCD logic voltage |
| 3-4 | 5.0 V LCD logic voltage |
| 5-6 | 12 V LCD logic voltage |

Select the jumper voltage required by the LCD before powering the system. An incorrect selection can damage the panel.

### UBOOT Firmware Download

![UBOOT button](ZC-3566-SBC/UBOOT.jpeg?raw=true)

| Pin | Signal | Description |
| ---: | --- | --- |
| 1 | GND | Ground |
| 2 | UBOOT | Hold during power-on to enter UBOOT firmware download mode |

### Wi-Fi/Bluetooth Antenna

![Wi-Fi and Bluetooth antenna connector](ZC-3566-SBC/WIFI-BT.jpeg?raw=true)

| Pin | Signal | Description |
| ---: | --- | --- |
| 1 | GND | Ground |
| 2 | RF | Wi-Fi/Bluetooth antenna signal |

Use an IPEX-1 compatible external antenna. Remove the connector carefully; pulling the cable directly can damage the PCB pad.

### Audio Interfaces

#### MIC

![MIC connector](ZC-3566-SBC/MIC.jpeg?raw=true)

| Pin | Signal | Description |
| ---: | --- | --- |
| 1 | MIC+ | Microphone positive input |
| 2 | MIC- | Microphone negative input |

#### 3.5 mm Headphone Jack

![Headphone connector](ZC-3566-SBC/headphone.jpeg?raw=true)

| Pin | Signal | Description |
| ---: | --- | --- |
| 1 | PL | Left audio output |
| 2 | PR | Right audio output |
| 3 | SNS | Ground |
| 4 | MIC+ | Microphone input |

The microphone input on the headphone jack and the MIC connector is shared; use only one at a time.

#### SPK

![SPK connector](ZC-3566-SBC/SPK.jpeg?raw=true)

| Pin | Signal | Description |
| ---: | --- | --- |
| 1 | PL+ | Left speaker positive output |
| 2 | PL- | Left speaker negative output |
| 3 | PR- | Right speaker negative output |
| 4 | PR+ | Right speaker positive output |

Use 8-ohm speakers and connect speakers before power-on. The default amplifier configuration is 2 x 5 W at 8 ohms.

### RTC And Keys

#### RTC Battery

![RTC connector](ZC-3566-SBC/RTC.jpeg?raw=true)

| Pin | Signal | Description |
| ---: | --- | --- |
| 1 | GND | Ground |
| 2 | RT+ | RTC battery power output |

Use a dedicated CR2032 RTC battery with extension cable.

#### KEY

![KEY connector](ZC-3566-SBC/KEY.jpeg?raw=true)

| Pin | Signal | Description |
| ---: | --- | --- |
| 1 | POE | Power-on key input |
| 2 | RST | Reset input |
| 3 | KEY | ADC key expansion, up to seven keys |
| 4 | GND | Ground |

### Touch, IR/LED And GPIO

#### CTP

![CTP connector](ZC-3566-SBC/CTP.jpeg?raw=true)

| Pin | Signal | Description |
| ---: | --- | --- |
| 1 | GND | Ground |
| 2 | RST | Touch reset; configurable as GPIO/PWM |
| 3 | INT | Touch interrupt; configurable as GPIO/PWM |
| 4 | SCL | I2C clock; configurable as GPIO |
| 5 | SDA | I2C data; configurable as GPIO |
| 6 | VCC-3.3V | 3.3 V output |

CTP is the default function. GPIO use requires software configuration; all signals use 3.3 V logic.

#### IR&LED

![IR and LED connector](ZC-3566-SBC/IR-LED.jpeg?raw=true)

| Pin | Signal | Description |
| ---: | --- | --- |
| 1 | RED | Red LED positive, shutdown-state indicator |
| 2 | GND | Ground |
| 3 | BLUE | Blue LED positive, running-state indicator |
| 4 | IVC | 3.3 V IR power output |
| 5 | GND | Ground |
| 6 | IR | IR signal input |

The default LED is common-cathode. Remote-control power-on and remote-code learning require the matching software configuration.

#### GPIO

![GPIO connector](ZC-3566-SBC/GPIO.jpeg?raw=true)

| Pin | Signal | Description |
| ---: | --- | --- |
| 1 | GND | Ground |
| 2 | GPIO1 | GPIO; compatible with CTP RST |
| 3 | GPIO2 | GPIO; compatible with CTP INT |
| 4 | GPIO3 | GPIO; compatible with CTP SCL |
| 5 | GPIO4 | GPIO; compatible with CTP SDA |
| 6 | VCC-3.3V | 3.3 V output |

GPIO1 and GPIO2 have 10K pull-down resistors. GPIO3 and GPIO4 have 10K pull-up resistors. All GPIO signals are 3.3 V logic.

### DEBUG And POE

#### DEBUG

![DEBUG connector](ZC-3566-SBC/DEBUG.jpeg?raw=true)

| Pin | Signal | Description |
| ---: | --- | --- |
| 1 | NC | Not connected |
| 2 | DEBUG_TX | Debug transmit |
| 3 | DEBUG_RX | Debug receive |
| 4 | GND | Ground |

Default debug baud rate is 1.5 Mbps. This connector is not populated by default.

#### POE

![POE connector](ZC-3566-SBC/POE.jpeg?raw=true)

| Pin | Signal | Description |
| ---: | --- | --- |
| 1 | VA1 | External PoE module power pin |
| 2 | VA2 | External PoE module power pin |
| 3 | VB2 | External PoE module power pin |
| 4 | VB1 | External PoE module power pin |

This connector is intended for an external PoE power module and is not populated by default.

### TTL/RS232/RS485 Serial Interfaces

All serial connectors provide VCC, TX, RX and GND. The default configuration is TTL at 3.3 V; selected ports can be populated as RS232 or RS485. VCC is 3.3 V by default and can be configured as 5 V. Maximum 3.3 V output current is 500 mA per port.

| Port | Default / optional function | Linux device | Image |
| --- | --- | --- | --- |
| TTYS6 | TTL; optional RS232 paired with TTYS7 | ttyS6 | ![TTYS6](ZC-3566-SBC/TTYS6.jpeg?raw=true) |
| TTYS7 | TTL; optional RS232 paired with TTYS6 | ttyS7 | ![TTYS7](ZC-3566-SBC/TTYS7.jpeg?raw=true) |
| TTYS8 | TTL; optional RS232 paired with TTYS9 | ttyS8 | ![TTYS8](ZC-3566-SBC/TTYS8.jpeg?raw=true) |
| TTYS9 | TTL; optional RS232 paired with TTYS8 | ttyS9 | ![TTYS9](ZC-3566-SBC/TTYS9.jpeg?raw=true) |
| TTYS0 | TTL; optional RS485 | ttyS0 | ![TTYS0](ZC-3566-SBC/TTYS0.jpeg?raw=true) |
| TTYS5 | TTL; optional RS485 | ttyS5 | ![TTYS5](ZC-3566-SBC/TTYS5.jpeg?raw=true) |

| Pin | TTL signal | RS232/RS485 signal | Description |
| ---: | --- | --- | --- |
| 1 | VCC | VCC | 3.3 V default; 5 V optional |
| 2 | UART_TX | A or B, port dependent | Data transmit; may be configured as GPIO |
| 3 | UART_RX | B or A, port dependent | Data receive; may be configured as GPIO |
| 4 | GND | GND | Ground |

### Internal USB Connectors

#### CUSB2

![CUSB2 connector](ZC-3566-SBC/CUSB2.jpeg?raw=true)

#### CUSB3

![CUSB3 connector](ZC-3566-SBC/CUSB3.jpeg?raw=true)

| Pin | Signal | Description |
| ---: | --- | --- |
| 1 | GND | Ground |
| 2 | DP | USB data positive |
| 3 | DM | USB data negative |
| 4 | 5V | 5 V power output |

Both connectors are USB host ports directly provided by the main processor.

### Display Data Connectors

#### eDP-DATA

![eDP-DATA connector](ZC-3566-SBC/EDP-DATA.png?raw=true)

| Pins | Signal |
| --- | --- |
| 1 | EDP-VCC_IN, panel voltage selected by J55: 3.3 V / 5 V / 12 V |
| 3-4, 13-14, 17-18 | GND |
| 5-6 | EDP-TX0- / EDP-TX0+ |
| 7-8 | EDP-TX1- / EDP-TX1+ |
| 9-10 | EDP-TX2- / EDP-TX2+ |
| 11-12 | EDP-TX3- / EDP-TX3+ |
| 15-16 | EDP-AUX- / EDP-AUX+ |
| 19 | +3.3 V output |
| 20 | EDP-HPD |

#### LVDS-DATA

![LVDS-DATA connector](ZC-3566-SBC/LVDS-DATA.png?raw=true)

| Pins | Signal |
| --- | --- |
| 1 | LCDVCC-IN, panel voltage selected by J55: 3.3 V / 5 V / 12 V |
| 4, 13-14, 25-26 | GND |
| 7-8 | RXO0- / RXO0+ |
| 9-10 | RXO1- / RXO1+ |
| 11-12 | RXO2- / RXO2+ |
| 15-16 | RXOC- / RXOC+ |
| 17-18 | RXO3- / RXO3+ |
| 19-20 | RXE0- / RXE0+ |
| 21-22 | RXE1- / RXE1+ |
| 23-24 | RXE2- / RXE2+ |
| 27-28 | RXEC- / RXEC+ |
| 29-30 | RXE3- / RXE3+ |

#### MIPI LCD

![MIPI LCD connector](ZC-3566-SBC/MIPI-LCD.jpeg?raw=true)

| Pins | Signal |
| --- | --- |
| 1-3 | LEDA+, backlight positive |
| 5-8 | LEDK+, backlight negative constant-current drive |
| 9-10, 13, 16, 19, 22, 25, 28 | GND |
| 11-12 | TDP2 / TDN2 |
| 14-15 | TDP1 / TDN1 |
| 17-18 | TCP / TCN |
| 20-21 | TDP0 / TDN0 |
| 23-24 | TDP3 / TDN3 |
| 26, 29 | VDDIO 1.8 V |
| 27 | RESET, active low |
| 30-31 | VDD 3.3 V |

The MIPI connector is not populated by default. Observe the pin-1 marking on every display connector before connection.

### Standard External Connectors

| Connector | Description |
| --- | --- |
| DC jack | Standard 12 V barrel jack, 6.0 mm outer opening, 2.0 mm center pin, center positive |
| TF | Standard TF-card socket |
| HDMI | Standard Type-A HDMI connector |
| RJ45 | Standard 100M RJ45 Ethernet connector |
| Headphone | Standard 3.5 mm US-standard four-pole jack |
| USB-OTG | Standard horizontal USB 2.0 Type-A connector |
| USB-HOST | Standard horizontal USB 3.0 Type-A connector |

The combined current of all four USB ports must not exceed 1.0 A. The total 3.3 V output current must not exceed 1 A.

## Handling And Installation Notes

- Do not connect or disconnect cables while the board is powered.
- Wear an antistatic wrist strap or equivalent protection when handling the PCBA.
- Verify every pin definition before connecting external equipment; do not reverse connectors.
- Prevent PCB bending, board stacking and short circuits during installation.
- Keep sensitive signal cables, such as Wi-Fi antenna and data cables, separate from power cables.
- Confirm panel logic voltage, backlight voltage, current requirement and pin-1 orientation before installing an LCD.
- Confirm external-device signal levels, current consumption and serial TX/RX wiring before connection.
- Calculate the complete system power budget and select an adapter with adequate power margin.
