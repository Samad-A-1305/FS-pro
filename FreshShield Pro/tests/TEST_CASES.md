# FreshShield Test Cases

## Test Objective

Verify the operation of the sensing, processing, control, display and IoT components.

> Update the Status column only after performing the actual test.

| ID | Test | Procedure | Expected Result | Status |
|---|---|---|---|---|
| T01 | ESP32 Startup | Power the controller | ESP32 starts normally | TODO |
| T02 | Ethylene Sensor | Connect and read sensor | Reading is obtained | TODO |
| T03 | Temperature | Read SHT31/SHT3x | Temperature displayed | TODO |
| T04 | Humidity | Read SHT31/SHT3x | RH displayed | TODO |
| T05 | OLED | Power display | System data displayed | TODO |
| T06 | Fan | Trigger control | Fan responds correctly | TODO |
| T07 | Treatment | Activate treatment control | Treatment stage responds | TODO |
| T08 | Sensor Processing | Provide sensor readings | Data is processed correctly | TODO |
| T09 | IoT | Connect Wi-Fi | Data reaches IoT interface | TODO |
| T10 | Wi-Fi Failure | Disable network | Local system continues safely | TODO |
| T11 | Invalid Reading | Simulate invalid sensor data | Error/invalid state handled | TODO |
| T12 | Full System | Run integrated prototype | All modules operate together | TODO |

## Test Record

For each completed test, record:

- Date
- Hardware version
- Software version
- Test conditions
- Observed result
- Expected result
- Pass/Fail
- Notes
