
# ⚙️ IoT-Based Machine Health Monitoring System Using ESP32 & MATLAB

This project focuses on real-time monitoring and analysis of machine health using multiple sensors, ESP32 microcontrollers, Firebase cloud, and MATLAB-based fault analysis.

---

## 🚀 Project Overview

The system continuously monitors machine parameters such as vibration, temperature, current, voltage, and RPM to detect abnormal behavior and early faults.

Sensor data is collected using ESP32, transmitted wirelessly via ESP-NOW, stored in Firebase, and analyzed in MATLAB for fault detection and visualization.

---

## 🧠 System Architecture
![Experimental setup](https://github.com/user-attachments/assets/2ebfd410-bfe8-468e-bfe2-05dff3480c7f)


- **Sensor Node (ESP32):**
  - Collects data from vibration, temperature, current, voltage, and RPM sensors
  - Performs initial processing (RMS calculation)
  - Sends data via ESP-NOW
    
![System_architecture_of_multi_sensor_machine_condition_monitoring_system](https://github.com/user-attachments/assets/ffdef100-0690-4850-b9b0-39c2030cd272)

- **Communication Node (ESP32 Gateway):**
  - Receives sensor packets
  - Adds timestamps
  - Uploads data to Firebase cloud
    
![Firebase_cloud](https://github.com/user-attachments/assets/ccc824c5-fddc-4a5e-9d95-51849ac4e315)

- **Cloud + Analytics:**
  - Firebase stores real-time data
  - MATLAB retrieves and analyzes data
  - Fault detection using FFT, Time domain analysis, crest factor, kurtosis
  - Sends data to the server for realtime monitoring

---

![FFT_healthy](https://github.com/user-attachments/assets/c380e796-1ca7-47b5-a43d-a277f4ac6ff2)

![Time_domain_analysis](https://github.com/user-attachments/assets/854b6056-d048-49bc-b938-9b8a18e38e28)

## 🔬 Data Analysis Methods

- RMS vibration monitoring
- FFT spectrum analysis
- Envelope analysis for bearing faults
- Crest factor & kurtosis for impact detection
- Multi-sensor correlation for machine condition assessment
  
![MATLAB_output](https://github.com/user-attachments/assets/bf4388a0-e1be-440f-a1bc-c7dc630e9acd)

---
## 📡 Sensors Used

- ADXL345 – Vibration monitoring(16G)
- DS18B20 – Temperature
- ACS712 – Current(5A)
- ZMPT101B – Voltage
- IR Sensor – RPM measurement

---

## 🧩 Dual-ESP32 Architecture

The system uses two ESP32 modules to ensure stable performance.

- One ESP32 handles sensor data acquisition  
- Another ESP32 handles wireless communication and cloud upload  

This separation prevents voltage drops, timing delays, and data distortion caused by Wi-Fi activity during high-speed sensor sampling.

---
## ⚙️ Key Features

- 📊 Real-time machine monitoring  
- 📡 Wireless data transfer using ESP-NOW  
- ☁️ Cloud storage using Firebase  
- 🧠 MATLAB-based fault analysis  
- 🔍 Multi-parameter condition monitoring  
- ⚡ Burst mode for high-frequency vibration capture  

---

## 📂 Project Workflow

1. Sensors collect machine parameters  
2. ESP32 processes and transmits data via ESP-NOW  
3. Gateway ESP32 uploads data to Firebase  
4. MATLAB retrieves data from cloud  
5. Signal processing and fault analysis performed  
6. Results visualized for condition monitoring  

---

## 🛠️ Tools & Technologies

- ESP32
- Arduino IDE
- MATLAB
- Firebase Realtime Database
- ESP-NOW protocol
- Rendor workspace
![Dashboard_DTC](https://github.com/user-attachments/assets/c47d1850-db08-4c37-8feb-79674aa5a0cb)

---

## 📈 Expected Outcomes

- Early detection of machine faults  
- Reduced downtime  
- Improved maintenance planning  
- Real-time health visualization  

---
