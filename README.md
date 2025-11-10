

## 📘 Project Overview
This project focuses on developing a **voice-controlled IoT robot** capable of performing human-like gestures, collecting environmental data, and responding to user commands intelligently.  
The system integrates **Raspberry Pi**, various **sensors**, **servo motors**, and **IoT cloud monitoring** for remote observation and control.

---

## 🎯 Aim
To design and implement a **voice-controlled intelligent robot** that can monitor its environment, perform gestures, and respond to commands through IoT connectivity.

---

## 🧩 Objectives
- Control the robot using **voice commands**.
- Collect **real-time data** from sensors like PIR, DHT11, and Ultrasonic.
- Perform **robotic gestures** using servo motors.
- Enable **IoT-based remote monitoring** via an IoT hub or cloud platform.
- Demonstrate **human-robot interaction** through movement and gesture response.

---

## ⚙️ Components Required

| S.No | Component Name | Quantity | Description |
|------|----------------|-----------|-------------|
| 1 | Raspberry Pi | 1 | Central controller for sensors and motors |
| 2 | Ultrasonic Sensor (HC-SR04) | 1 | Measures object distance for obstacle detection |
| 3 | PIR Motion Sensor | 1 | Detects human movement |
| 4 | DHT11 Temperature & Humidity Sensor | 1 | Captures environmental data |
| 5 | MQ-3 Gas Sensor | 1 | Detects alcohol or harmful gases |
| 6 | Servo Motors (Neck, Left, Right) | 3 | Used for gestures like waving or nodding |
| 7 | L298N Motor Driver | 1 | Controls motor direction and speed |
| 8 | Microphone & Speaker | 1 each | For voice command input and responses |
| 9 | Power Supply & Jumper Wires | 1 set | Provides stable power connections |

---

## 🔌 Hardware Pin Configuration

| Component | Raspberry Pi GPIO Pins |
|------------|-----------------------|
| Servo Motors | BCM 18, 23, 24 |
| Ultrasonic Sensor | TRIG → GPIO 27, ECHO → GPIO 22 |
| PIR Sensor | GPIO 17 |
| DHT11 Sensor | GPIO 4 |
| MQ-3 Sensor (via MCP3008 ADC) | CLK-11, MISO-9, MOSI-10, CS-8 |
| Audio Input | USB Microphone |
| Audio Output | USB / 3.5mm Speaker |

---

## 🧠 Working Principle

### 1. Voice Command Processing
The user gives voice commands via a **microphone**, which are processed by the **Raspberry Pi** using speech recognition libraries (e.g., `SpeechRecognition`, `Google Voice API`).  
Commands like “Move forward” or “Wave hand” are translated into executable actions.

### 2. Motor Control
The Raspberry Pi sends PWM signals to the **motor driver** to move the robot forward, backward, or turn based on the recognized command.

### 3. Sensor Data Collection
Sensors collect environmental data — obstacle distance, temperature, humidity, and gas presence — and send it to the Raspberry Pi for processing and decision-making.

### 4. Gesture Simulation
**Servo motors** enable gestures like waving, nodding, and rotating the head to make interaction more natural.

### 5. IoT Cloud Monitoring
Sensor readings and robot status are uploaded to platforms like **ThingSpeak**, **Blynk**, or **Azure IoT Hub** for **real-time monitoring and control** through dashboards or mobile apps.

---

## 🖼️ System Design (Block Diagram)

