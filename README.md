# 🌡️ Temperature & Humidity-Based Fan Control System (DHT11 + Relay)

This Arduino project uses a **DHT11 sensor** to measure **temperature and humidity**, and controls a **fan** (via relay) based on preset threshold values. It's ideal for creating a simple **automatic climate control system**.

---

## 📦 Components Used

- Arduino Uno / Mega / Compatible Board
- DHT11 Temperature and Humidity Sensor
- Relay Module (to control the fan)
- Fan (or any AC/DC load via relay)
- Jumper wires and breadboard

---

## 📐 Pin Configuration

| Component         | Arduino Pin |
|------------------|-------------|
| DHT11 Sensor      | D19         |
| Relay Module (Fan)| D5          |

> ⚠️ Make sure the DHT11 sensor's data pin is correctly wired to pin 19 on your board (check your specific board’s pinout if you’re using something like a Mega).

---

## 🚀 How It Works

1. Every 2 seconds, the DHT11 sensor reads:
   - Temperature in °C
   - Humidity in %

2. Thresholds:
   - **Temperature ≥ 23°C**
   - **Humidity ≥ 60%**

3. If **both conditions** are met:
   - The **relay turns ON** the fan
   - Serial monitor shows: `Fan turned ON`

4. If **any condition is not met**:
   - The **relay turns OFF** the fan
   - Serial monitor shows: `Fan turned OFF`

---

## 🖥️ Serial Monitor Output Example

Temperature: 24.5°C Humidity: 62%
Fan turned ON

Temperature: 22.3°C Humidity: 55%
Fan turned OFF
