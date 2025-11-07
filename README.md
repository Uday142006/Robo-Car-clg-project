# 🚗 RC Car with Arduino Nano, nRF24L01 & Joystick  

🎮✨ **Wireless Remote-Controlled Car using Arduino Nano and nRF24L01** ✨🎮  
A simple yet powerful project for learning **wireless communication**, **motor control**, and **Arduino programming**.  

---

## 🎯 Project Overview  
This RC car is controlled wirelessly via two **Arduino Nano boards** and **nRF24L01** modules.  
The transmitter reads joystick input and sends data to the receiver, which drives motors and servo for smooth, responsive motion.  

---

## 🧠 Key Learnings  
- 📡 Wireless communication (nRF24L01)  
- ⚙️ Motor driver (L298N) control  
- 💻 Arduino programming  
- 🕹️ Joystick interfacing  
- 🔋 Power management  

---

## 🧩 Hardware Components  

| Component | Quantity | Purpose |
|------------|-----------|----------|
| Arduino Nano | 2 | Transmitter & Receiver |
| nRF24L01 | 2 | Wireless data transfer |
| Joystick Module | 1 | Direction & throttle control |
| L298N Motor Driver | 1 | Dual DC motor control |
| DC Motors | 2 | Drive motors |
| Servo Motor (SG90) | 1 | Steering |
| AMS1117 3.3V Regulator | 1 | Power for nRF24L01 |
| LiPo Battery (7.4V) | 1 | Main power source |

---

## 🔌 Basic Wiring  

### 📡 Transmitter  
- Joystick X → A0  
- Joystick Y → A1  
- nRF24L01 → CE D7, CSN D8, SCK D13, MOSI D11, MISO D12, VCC 3.3V  

### 🚗 Receiver  
- L298N IN1–IN4 → D2–D5  
- ENA (PWM) → D6, ENB (PWM) → D9  
- Servo Signal → D10  
- nRF24L01 → same as transmitter  

---

## 💻 Software Setup  

### Required Libraries  
```cpp
#include <SPI.h>
#include <nRF24L01.h>
#include <RF24.h>
#include <Servo.h>
## 📲 Installation  

**Install Required Libraries:**  
* Open **Arduino IDE**  
* Go to **Tools → Manage Libraries**  
* Search and install **“RF24”** and **“Servo”**  

---

## 🚀 Usage  

1. 🛠️ **Assemble** both transmitter (Tx) and receiver (Rx) circuits  
2. 💾 **Upload** transmitter and receiver codes  
3. ⚡ **Power** both units using 7.4V LiPo batteries (with voltage regulator)  
4. 🎮 **Control** the car by moving joysticks for speed and steering  

---

## ⚠️ Quick Tips  

* ⚡ Use **AMS1117-3.3V** regulator for stable nRF24L01 power  
* 🔋 Add **100µF capacitor** between nRF24L01 **VCC** and **GND**  
* 🔌 Keep **wire length short (<10cm)** to reduce noise  
* 📡 Use **PA+LNA modules** for better wireless range  

---

## 🎨 Optional Add-ons  

* 🛑 **Emergency Stop Button**  
* 💡 **LED Indicators** (Power & Connection)  
* 🔋 **Battery Voltage Monitor**  
* 🚀 **Range Extender (nRF24L01+PA+LNA)**  

---

## 🎉 Thank You  

Built with ❤️ using **Arduino Nano** and **nRF24L01**  
Perfect for learning **IoT**, **Robotics**, and **Wireless Systems** 🚗💨  
