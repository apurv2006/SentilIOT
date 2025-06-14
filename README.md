🚨 SentinelIoT: Self-Healing IoT Device Management Platform

> An intelligent, full-stack IoT monitoring and diagnostics system that empowers field operators to independently identify, configure, and recover embedded IoT devices — without hardware/software expertise.

---

📌 Problem Statement

In distributed IoT deployments, technical downtime due to unknown hardware/software failures severely affects reliability. Non-technical users are forced to rely on embedded engineers to debug problems—causing delays, escalations, and high operational costs.

---

🎯 Solution

**SentinelIoT** is a web-based IoT Device Management + Diagnostic + Configuration platform with:

- 📡 **Real-time health monitoring** of ESP32-based devices over MQTT
- 🧠 **Smart diagnostics** using rules to detect faults
- 🧰 **Step-by-step guided recovery** instructions for non-engineers
- ⚙️ **Remote configuration** via secure MQTT channels
- 🌐 **Frontend dashboard** with device visibility and OTA triggers

---

🧠 Key Features

- ✅ ESP32 heartbeat publishing (status, RSSI, uptime)
- ✅ Fault detection engine (e.g., offline, weak signal)
- ✅ Configurator: update device settings over MQTT
- ✅ Recovery assistant: step-by-step recovery instructions
- ✅ OTA firmware push (optional)
- ✅ MongoDB-based logging and dashboard UI

---

🧱 Architecture Overview

graph TD;
    ESP32-->MQTTBroker
    MQTTBroker-->Backend
    Backend-->MongoDB
    Backend-->Frontend
    Frontend-->User
    Backend-->RecoveryEngine
    OTA[OTA Update Server]-->ESP32
