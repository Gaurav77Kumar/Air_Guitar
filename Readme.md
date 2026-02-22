# 🎸 Air Guitar 

> Play invisible guitar strings in mid-air using motion sensors and real-time audio synthesis.

![Python](https://img.shields.io/badge/language-python-blue?style=flat\&logo=python)
![C++](https://img.shields.io/badge/language-c%2B%2B-blue?style=flat\&logo=c%2B%2B)
![Platform](https://img.shields.io/badge/platform-Arduino-green)
![Status](https://img.shields.io/badge/status-active-success)

---

## ✨ Overview

**Air Guitar** is an IoT + audio signal processing project that lets you play a virtual guitar using hand movements.
It uses an **MPU6050 accelerometer/gyroscope** connected to an **Arduino**, which sends motion data to a **Python audio engine**. The Python program synthesizes realistic guitar sounds using the **Karplus-Strong algorithm**.

Move your wrist left or right to change notes and strum by shaking your hand to produce sound — just like playing a real guitar in the air.

---

## 🎯 Features

* 🎸 Six virtual guitar strings (Open E tuning)
* 🖐️ Gesture-based note selection
* 💥 Strum detection using accelerometer force
* 🔊 Real-time sound synthesis
* ⚡ Low latency audio playback
* 🧠 Physics-based sound generation (Karplus-Strong)
* 🛠️ Easy hardware setup
* 📈 Calibration routine for accuracy

---

## 🧰 Tech Stack

### Hardware

* Arduino Uno
* MPU6050 Accelerometer + Gyroscope

### Software

* Python
* Arduino C++
* NumPy
* SoundDevice
* PySerial

---

## 🧱 Hardware Components Required

| Component       | Quantity |
| --------------- | -------- |
| Arduino Uno     | 1        |
| MPU6050 Sensor  | 1        |
| Jumper wires    | 4        |
| USB cable       | 1        |
| Computer/Laptop | 1        |

---

## 🔌 Circuit Connections

| MPU6050 Pin | Arduino Pin |
| ----------- | ----------- |
| VCC         | 5V          |
| GND         | GND         |
| SCL         | A5          |
| SDA         | A4          |



---

## 🏗️ Project Structure

```
Air_Guitar/
│
├── Air_Guitar.py          # Main Python audio engine
├── Ardunio_Code.ino       # Arduino sensor code
├── README.md
└── requirements.txt
```

---

## ⚙️ How It Works

1️⃣ MPU6050 detects wrist movement and acceleration
2️⃣ Arduino reads sensor data via I2C
3️⃣ Arduino sends motion data to computer via Serial
4️⃣ Python script reads serial data
5️⃣ Motion mapped to notes and strum force
6️⃣ Karplus-Strong algorithm generates sound
7️⃣ Audio played in real time

---



---

## 🚀 Getting Started

### Prerequisites

* Python ≥ 3.8
* Arduino IDE installed
* USB drivers for Arduino
* Speakers/headphones

---

## 📥 Installation

### 1️⃣ Clone repository

```bash
git clone https://github.com/Gaurav77Kumar/Air_Guitar.git
cd Air_Guitar
```

---

### 2️⃣ Install Python dependencies

```bash
pip install numpy sounddevice pyserial
```

---

### 3️⃣ Upload Arduino code

1. Open **Arduino IDE**
2. Open `Ardunio_Code.ino`
3. Select board → Arduino Uno
4. Select correct COM port
5. Click Upload

---

### 4️⃣ Run Python script

```bash
python Air_Guitar.py
```

---

## 🎮 Usage Instructions

1️⃣ Keep wrist steady during calibration
2️⃣ Rotate wrist left → lower notes
3️⃣ Rotate wrist right → higher notes
4️⃣ Shake wrist to strum
5️⃣ Adjust sensitivity in code if needed

---

## 🎼 Note Mapping (Example)

| Angle Range | Note   |
| ----------- | ------ |
| -45°        | Low E  |
| -20°        | A      |
| 0°          | D      |
| 20°         | G      |
| 40°         | B      |
| 60°         | High E |

---

## ⚙️ Configuration

You can adjust:

* Sensitivity threshold
* Strum detection force
* Sampling rate
* Volume
* String frequencies

Inside `Air_Guitar.py`.

---

## 📊 System Flow

Sensor → Arduino → Serial → Python → Audio Engine → Speaker

---



## 📈 Future Improvements

* Bluetooth sensor support
* GUI interface
* Multiple instrument modes
* Recording feature
* Machine learning gesture recognition
* Wireless version using ESP32

---

## 🤝 Contributing

Contributions are welcome!

1. Fork repo
2. Create feature branch
3. Commit changes
4. Open pull request

---

## 🧑‍💻 Maintainer

**Gaurav Kumar**
GitHub → https://github.com/Gaurav77Kumar

---



---

## ⭐ Support

If you like this project, consider giving it a ⭐ on GitHub!

---



---

> 🎶 Build, experiment, and play music in the air — no strings attached!
