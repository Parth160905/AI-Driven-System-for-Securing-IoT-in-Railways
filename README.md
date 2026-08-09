#AI-Driven System for Securing IoT in Railways

A web-based railway IoT security platform that simulates live railway telemetry, applies statistical anomaly detection with railway-specific security rules, generates severity-based alerts, and provides role-based device administration and audit logging.

---

## 🌐 Live Demo

🚀 **Live Website:**

https://parth160905.github.io/AI-Driven-System-for-Securing-IoT-in-Railways/

---

## 📌 Project Overview

Modern metro and railway systems rely on interconnected IoT devices such as trains, track sensors, signals, cameras, and automated fare gates.

While these connected systems improve efficiency and automation, they also introduce cybersecurity risks such as abnormal traffic, spoofed telemetry, communication interception, and sensor manipulation.

**SecureMetro IoT** is a front-end security platform designed to demonstrate how railway IoT telemetry can be monitored and analyzed for potential threats.

The application includes a simulated railway IoT environment where devices continuously generate telemetry data. An anomaly-detection engine learns the normal behaviour of each device and identifies significant deviations using statistical analysis and predefined railway security rules.

---

## ✨ Key Features

### 📡 Live IoT Fleet Simulation

The system simulates telemetry from multiple railway IoT devices, including:

- 🚆 Trains
- 🌡️ Track sensors
- 🚦 Signal nodes
- 📷 Platform cameras
- 🎫 Automated fare gates

Each device generates simulated readings such as:

- Packet rate
- Network latency
- Train speed
- Vibration
- Temperature
- Humidity
- Voltage
- FPS
- Passenger/tap activity

Telemetry is updated automatically every **2.5 seconds**.

---

### 🤖 AI-Based Anomaly Detection

The application includes a statistical anomaly-detection engine based on **rolling z-score analysis**.

For each device, the system:

1. Collects historical telemetry.
2. Builds a rolling behavioural baseline.
3. Calculates the mean and standard deviation.
4. Measures how far new readings deviate from the baseline.
5. Converts the deviation into an anomaly score.
6. Classifies the event based on severity.

The system maintains up to **40 historical readings per metric** for each device.

Anomaly detection begins after sufficient historical data has been collected.

---

### 🛡️ Railway-Specific Threat Detection

In addition to statistical anomaly detection, the application uses domain-specific rules to identify potential railway IoT security threats.

#### Possible DDoS-like Flood

Triggered when:

```text
Packet Rate > 900 packets/sec
