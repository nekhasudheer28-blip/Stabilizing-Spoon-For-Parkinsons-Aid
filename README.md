# Tremor-Compensating Spoon for Parkinson's Patients
A biomechatronic smart assistive device that stabilizes a spoon by actively counteracting involuntary hand tremors experienced by individuals with Parkinson's disease during eating activities — demonstrating human-centered rehabilitation engineering applications.

---

## Overview

Parkinson's disease affects motor control and leads to hand tremors that make simple daily tasks like eating quite challenging. This project presents a smart assistive spoon that detects and counteracts involuntary hand movements in real-time, allowing users to eat with greater comfort, independence, and dignity.

The device combines precise motion detection, quaternion-based orientation tracking, Kalman filtering, and responsive servo actuation to minimize the effects of tremors during mealtime.

---
## Features

- Real-time tremor detection using an IMU sensor (MPU6050)
- Kalman Filter / Quaternion-based signal conditioning to eliminate noise and drift
- Dual-servo feedback control across a ±30° orientation range (pitch and roll)
- 2-axis gimbal mechanism for smooth and stable spoon positioning
- Lightweight and ergonomic design (under 200g)
- Rechargeable Li-ion battery with at least 1 hour of continuous operation
- Toggle switch for easy on/off control
- Food-safe, waterproof, and detachable spoon head for hygiene

---

## How It Works

1. The **MPU6050 IMU sensor** continuously detects angular velocity and acceleration to identify involuntary hand tremors.
2. Raw sensor data is processed using a **Kalman Filter or Quaternion-based algorithm** to accurately distinguish tremors (4–6 Hz frequency) from intentional movements.
3. The **ESP32 / Arduino Nano microcontroller** processes the filtered data in real-time and calculates the compensation needed.
4. **MG90S Servo Motors** adjust the 2-axis gimbal to counteract detected tremors, keeping the spoon stable and level.
5. The entire system is powered by a **3.7V 18650 Li-ion battery** with a **TP4056 charging module** for safe and portable power delivery.

---

## Tools & Technologies

- Arduino IDE
- SolidWorks / Fusion 360
- MPU6050 IMU
- ESP32 / Arduino Nano
- Kalman Filtering & Quaternion Mathematics

---

## Components

| Sl. No. | Function             | Component                                      |
|---------|----------------------|------------------------------------------------|
| 1       | Motion Detection     | IMU Sensor (MPU6050)                           |
| 2       | Signal Conditioning  | Kalman Filter / Quaternion-based Estimation    |
| 3       | Controller           | Microcontroller (ESP32 / Arduino Nano)         |
| 4       | Motion Actuation     | Servo Motors (MG90S or equivalent)             |
| 5       | Motion Assembly      | 2-Axis Gimbal Mechanism                        |
| 6       | Power Supply         | 3.7V Li-ion Battery (18650)                    |
| 7       | Power Regulation     | TP4056 Charging Module + Voltage Regulator     |
| 8       | User Control         | Toggle Switch                                  |
