# FreshShield Technical Design Document

## 1. Project Objective

FreshShield is designed to monitor storage-air conditions for fruits and flowers and support automated air management.

The system combines sensing, embedded processing, air treatment, air circulation and IoT monitoring.

---

## 2. Functional Requirements

The system should:

1. Monitor ethylene.
2. Monitor temperature.
3. Monitor relative humidity.
4. Process sensor readings using ESP32.
5. Control air circulation.
6. Support the multi-stage treatment process.
7. Display local system information.
8. Provide IoT monitoring where implemented.
9. Record sensor data for testing and analysis.

---

## 3. System Modules

### Module 1 — Sensing

Inputs:

- Ethylene sensor
- Temperature sensor
- Humidity sensor

---

### Module 2 — Processing

Controller:

ESP32

Responsibilities:

- Sensor acquisition
- Data processing
- Control logic
- Actuator control
- Display communication
- Wi-Fi communication

---

### Module 3 — Air Circulation

A fan draws storage air through the treatment module and returns treated air to the chamber.

---

### Module 4 — Air Treatment

Treatment sequence:

Pre-filter
↓
KMnO4
↓
Enclosed UV
↓
Activated Carbon

---

### Module 5 — Local Monitoring

OLED displays:

- Ethylene
- Temperature
- Humidity
- Fan status
- Treatment status

---

### Module 6 — IoT Monitoring

Where implemented, sensor data is sent through Wi-Fi to an IoT/mobile/web monitoring service.

---

## 4. Data Flow

Sensors
↓
ESP32
↓
Data Processing
↓
Control Decision
↓
Actuator Control
↓
OLED
↓
IoT Platform

---

## 5. Control Flow

Sense
↓
Validate
↓
Analyse
↓
Decide
↓
Actuate
↓
Monitor
↓
Repeat

---

## 6. Air Treatment Flow

Storage Chamber
↓
Pre-filter
↓
KMnO4 Treatment
↓
UV Chamber
↓
Activated Carbon
↓
Treated Air
↓
Storage Chamber

---

## 7. Safety Design

### UV Safety

The UV source should be physically enclosed so that direct exposure is prevented during operation.

### KMnO4 Safety

Treatment media should be securely contained and protected from direct handling during normal operation.

### Electrical Safety

Use appropriate power supplies, drivers, isolation and protection for all actuators.

### Airflow

Airflow should be tested to verify the intended direction and adequate circulation.

---

## 8. Testing Strategy

Testing should cover:

- Sensor operation
- Sensor stability
- Data processing
- Control logic
- Fan operation
- Treatment operation
- OLED operation
- IoT communication
- Failure handling

---

## 9. Future Development

Potential extensions:

- Adaptive control
- Cloud analytics
- AI/ML-based spoilage prediction
- Multi-chamber monitoring
- Energy optimization
- Historical trend analysis
