# 💡 Smart Lighting System Using Hand Gesture Recognition (Arduino + Python)

Control your room lights with just a wave of your hand! This project combines **real-time hand gesture detection** and **Arduino hardware** to create a seamless, touchless lighting system. Simply show 1–5 fingers to the webcam — and watch the corresponding number of LEDs light up instantly! ⚡

---

## 📌 Project Highlights

- ✋ **Finger gesture detection** using Python, OpenCV, and MediaPipe
- 🔄 **Real-time serial communication** with Arduino Uno
- 💡 **Dynamic LED control** (1 to 5 LEDs) based on number of fingers shown
- 🏠 Ideal for **smart homes**, **touchless switches**, and **accessibility applications**

---

## 🧰 Tech Stack

### 🖥️ Software:
- Python (OpenCV, MediaPipe, PySerial)
- Arduino IDE (C++ for microcontroller)

### 🔌 Hardware:
- Arduino Uno
- 5x LEDs + 220Ω–330Ω resistors
- Breadboard & jumper wires
- USB cable (for Arduino–PC connection)
- Webcam (for gesture input)

---

## ✋ Finger-to-LED Mapping

| 🖐️ Fingers Shown | 💡 LEDs Turned ON |
|------------------|------------------|
| 0                | All OFF          |
| 1                | LED 1            |
| 2                | LED 1, 2         |
| 3                | LED 1, 2, 3      |
| 4                | LED 1–4          |
| 5                | LED 1–5          |

---

## 🧠 System Architecture


+----------------------------+        Serial (USB)        +-----------------------+
|      Python + OpenCV      | <------------------------> |      Arduino Uno      |
|  - MediaPipe Hand Tracker |                            |  - LED Controller     |
|  - Finger Counting Logic  |                            |  - Pins 2–6 Output    |
+----------------------------+                            +-----------------------+




---

## 📁 Folder Structure

SmartGestureLighting/
│
├── python/
│ ├── main.py # Finger detection + serial communication
│ └── finger_counter.py # Utility to count raised fingers
│
├── arduino/
│ └── gesture_lights.ino # Arduino code for LED control
│
├── README.md
└── requirements.txt

## 🛠️ Setup Instructions
1. Arduino
Upload gesture_lights.ino using Arduino IDE.

Connect LEDs to pins 2–6 with resistors and GND.

2. Python Environment
     ```bash
     pip install opencv-python mediapipe pyserial

3. Run Python Script
   ```bash
   python main.py

Make sure COM3 (or /dev/ttyUSB0 on Linux) matches your Arduino port.

## 🎥 Demo
Show hand with 3 fingers → 3 LEDs glow instantly!

## 🚀 Future Upgrades
Gesture-to-color mapping (RGB lights)

Bluetooth/Wi-Fi control (ESP32)

Voice + gesture hybrid control

Energy monitoring system integration
