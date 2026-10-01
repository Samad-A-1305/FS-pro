# FreshShield

## Smart IoT-Based Storage-Air Management System for Fruits and Flowers

FreshShield is an IoT-based storage-air management system designed to continuously monitor and manage storage-air conditions for fruits and flowers.

The system monitors ethylene, temperature and relative humidity using sensors connected to an ESP32. Based on the monitored conditions, the system supports automated air circulation and a multi-stage air-treatment process consisting of pre-filtration, KMnO4 treatment, enclosed UV treatment and activated carbon filtration.

## Problem

Post-harvest fruits and flowers continue to release ethylene, while changes in temperature and relative humidity can influence quality deterioration.

Conventional storage monitoring may focus mainly on temperature and humidity, while continuous monitoring and management of ethylene and the overall storage-air environment can be limited.

FreshShield addresses this gap through continuous sensing, processing, air treatment and IoT-based monitoring.

## Proposed Solution

FreshShield follows the process:

SENSE → ANALYSE → TREAT → MONITOR

### SENSE
The system monitors:

- Ethylene
- Temperature
- Relative Humidity

### ANALYSE
The ESP32 receives and processes sensor data.

### TREAT
Storage air is circulated through:

1. Pre-filter
2. KMnO4 treatment stage
3. Enclosed UV chamber
4. Activated carbon filter

### MONITOR
System status can be viewed locally through an OLED and remotely through an IoT interface where implemented.

## System Flow

Storage Chamber
↓
Sensors
↓
ESP32
↓
Air Circulation
↓
Pre-filter
↓
KMnO4 Treatment
↓
Enclosed UV Chamber
↓
Activated Carbon
↓
Treated Air
↓
Storage Chamber

## Key Features

- Continuous ethylene monitoring
- Temperature monitoring
- Relative humidity monitoring
- ESP32-based processing
- Automated control logic
- Multi-stage air treatment
- Air recirculation
- OLED local monitoring
- IoT connectivity
- Modular architecture
- Expandable monitoring and analytics

## Hardware

The prototype uses or is designed around:

- ESP32
- Ethylene sensor
- SHT31/SHT3x temperature and humidity sensor
- OLED display
- Fan
- Relay/MOSFET driver
- UV treatment module
- KMnO4 treatment media
- Activated carbon
- Pre-filter
- Power supply

Exact models and quantities should be updated according to the final prototype.

## Software

- Embedded C/C++
- ESP32 firmware
- Arduino IDE or PlatformIO
- I2C/GPIO/ADC interfaces as applicable
- Wi-Fi
- IoT dashboard/service as implemented

## Architecture

The system consists of five main functional layers:

1. Sensing Layer
2. Processing Layer
3. Decision/Control Layer
4. Air-Treatment Layer
5. Monitoring Layer

Detailed architecture is available in:

`docs/ARCHITECTURE.md`

## Control Flow

Sense
↓
Read Sensor Data
↓
Validate Data
↓
Process Data
↓
Apply Control Logic
↓
Control Fan/Treatment
↓
Update OLED
↓
Send IoT Data
↓
Repeat

## Installation

### 1. Install Arduino IDE

Install Arduino IDE on your computer.

### 2. Install ESP32 Board Support

Add ESP32 board support to Arduino IDE.

### 3. Install Required Libraries

Install the libraries required by the exact sensors and display used in the prototype.

Typical libraries may include:

- Wire
- Adafruit SHT31
- Adafruit GFX
- Adafruit SSD1306

Use only the libraries required by the final implementation.

### 4. Connect Hardware

Connect:

- Ethylene sensor
- SHT31/SHT3x
- OLED
- Fan driver
- Treatment control
- ESP32

according to the final circuit diagram.

### 5. Configure Firmware

Open:

`src/freshshield.ino`

Update:

- GPIO pins
- Sensor configuration
- Display configuration
- Control parameters
- IoT configuration

### 6. Upload Firmware

Connect ESP32 through USB and upload the firmware.

### 7. Verify

Check:

- Sensor readings
- OLED display
- Fan operation
- Treatment control
- IoT communication

## Configuration

Do not publish real Wi-Fi passwords, API keys or cloud credentials.

Use the configuration approach documented in:

`.env.example`

Example:

WIFI_SSID=your_wifi_name
WIFI_PASSWORD=your_wifi_password

## Safety

### UV

The UV treatment stage must remain enclosed during operation to prevent direct UV exposure.

### KMnO4

KMnO4 treatment media should be securely contained and handled according to appropriate safety procedures.

### Electrical Safety

Use suitable drivers, isolation and power ratings for all connected loads.

### Airflow

Verify airflow direction and circulation before continuous operation.

## Testing

Test procedures are documented in:

`tests/TEST_CASES.md`

Tests include:

- ESP32 startup
- Temperature sensing
- Humidity sensing
- Ethylene sensing
- OLED output
- Fan control
- Treatment control
- IoT communication
- Connectivity failure handling

## Sample Data

Sample sensor data is provided in:

`data/sample_sensor_data.csv`

Sample data must not be represented as experimental results.

## Documentation

Technical design:

`docs/TECHNICAL_DESIGN.md`

Architecture:

`docs/ARCHITECTURE.md`

Control logic:

`docs/CONTROL_LOGIC.md`

Block diagram:

`docs/block_diagram.md`

## Project Status

Prototype development and testing.

## Future Scope

- Adaptive treatment control
- Cloud-based historical analytics
- Spoilage prediction
- AI/ML-based quality prediction
- Multi-chamber monitoring
- Energy optimization
- Advanced ethylene sensing
- Data-driven control optimization

## Team

FreshShield is developed by a three-member Computer Science and Engineering team.

## License

This project is released under the MIT License.

See `LICENSE`.
