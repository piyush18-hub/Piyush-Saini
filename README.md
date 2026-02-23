# 🌱 Capacitive Soil Moisture Sensor with Arduino  
### ICT Workshop Project

---

## 📌 Project Overview
This project demonstrates how to interface a **Capacitive Soil Moisture Sensor v1.2** with an **Arduino** to measure soil moisture levels.  

The system reads analog values from the sensor and displays the moisture level on the Serial Monitor.  

This project was developed as part of my **ICT Workshop**.

🔗 Reference Project:  
https://srituhobby.com/capacitive-soil-moisture-sensor-v1-2-arduino-code/

---

## 🎯 Objectives
- Understand the working principle of a capacitive soil moisture sensor  
- Interface the sensor with Arduino  
- Read and analyze analog sensor data  
- Display soil moisture values using Serial Monitor  

---

## 🛠️ Components Used
- Arduino Uno (or compatible board)  
- Capacitive Soil Moisture Sensor v1.2  
- Jumper Wires  
- USB Cable  
- Breadboard (optional)  

---

## 🔌 Circuit Connections

| Sensor Pin | Arduino Pin |
|------------|-------------|
| VCC        | 5V          |
| GND        | GND         |
| AOUT       | A0          |

---

## 💻 Arduino Code

```cpp
// Capacitive Soil Moisture Sensor with Arduino

const int sensorPin = A0;
int sensorValue = 0;

void setup() {
  Serial.begin(9600);
}

void loop() {
  sensorValue = analogRead(sensorPin);

  Serial.print("Soil Moisture Value: ");
  Serial.println(sensorValue);

  delay(1000);
}
