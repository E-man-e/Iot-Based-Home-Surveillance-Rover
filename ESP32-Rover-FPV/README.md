# Iot-Based Home Surveillance Rover

A dual-ESP32 robotics platform featuring live FPV video streaming, real-time telemetry, and keyboard-driven motor controls.

## System Architecture
* **Master Controller (`Master_ESP32/`)**: Configures a standalone Wi-Fi Access Point (`ESP32_Rover`), serves the main control webpage on port 80, executes directional motor commands, and samples distance (HC-SR04) and motion (PIR) sensors.
* **Camera Unit (`Camera_ESP32/`)**: Operates on the AI Thinker board layout to stream raw video frames to the Master Dashboard via port 81 (`http://192.168.4.2:81/stream`).

## Network Credentials
* **AP SSID**: `ESP32_Rover`
* **AP Password**: `ControlPanel123`
* **Default IP**: `192.168.4.1`

## Hardware Setup
* 1x ESP32 Dev Module (Master)
* 1x ESP32-CAM (AI Thinker Camera)
* 1x L298N Dual H-Bridge Motor Driver
* 1x HC-SR04 Ultrasonic Distance Sensor
* 1x PIR Motion Sensor
* 2x DC Gear Motors
