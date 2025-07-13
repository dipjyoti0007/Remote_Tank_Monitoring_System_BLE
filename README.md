# 💧📡 BLE-Based Remote Tank Level Monitoring System 🚰🔋  
*Internship Project at Techavo Systems*  
🔧 By **Dipjyoti Kodali**, AEIE Dept., Heritage Institute of Technology

---

## 🌍 Overview

This project presents a **Ultra Low-Power, BLE-enabled remote tank monitoring system**, ideal for the tankers they run in Rajasthan areas.  
It detects water levels via sensors and **transmits real-time updates wirelessly** to nearby devices using **Bluetooth Low Energy (BLE)**.

🔑 **Keywords:** BLE, IoT, Nordic nRF52, GATT, Ultra Low Power Design, Sensor Interface, Embedded C

---

## 🧠 Tech Stack at a Glance

| 💻 Software Stack             | 🔧 Hardware Tools                |
|------------------------------|----------------------------------|
| ✅ Segger Embedded Studio v8.24 | 📘 Nordic nRF52 DK (nRF52832)    |
| ✅ Nordic nRF5 SDK v17.1.0     | ⚡ CR2032 Coin Cell Battery       |
| ✅ nRF Connect Mobile App      | 📶 3-Level Digital Water Sensor   |
| ✅ GATT Custom Service Dev     | 🔌 Micro USB / Battery Power      |

---

## 🧪 Project Highlights

### 🧰 Conceptualization & Goal
- 📦 Create a **wireless water level monitoring** system
- 🔋 Run on **ultra-low power** using coin cell batteries
- 📲 Transmit level info via BLE to a smartphone app

---

### 🛠️ Experimental Flow

#### ✅ 1. Board Bring-Up  
🔹 Blinking LEDs as startup test  
🔹 UART serial communication setup  
🔹 Segger IDE + Nordic SDK integration  

#### 📥 2. Digital Sensor Input  
🔸 Simulated with onboard buttons (P13–P15)  
🔸 3 digital inputs: 🟢 FULL | 🟡 HALF | 🔴 EMPTY  
🔸 Debouncing for clean signal logic

#### 📡 3. BLE Advertising  
🔹 Custom BLE device name: `TankSensor01`  
🔹 GATT service for querying level  
🔹 Real-time broadcast to nRF Connect app

#### 💤 4. Power Optimization  
🔋 Wake → Sense → Transmit → Sleep loop (every 5 mins)  
⚡ Achieves multi-month operation on a single CR2032  

#### 📲 5. Real-Time Monitoring  
📲 BLE notifications seen on **nRF Connect Mobile App**  
🧪 Case-by-case level simulation with live feedback

---

## 🔍 Sample BLE Output

| Tank Status      | BLE Output                 |
|------------------|----------------------------|
| 🟢 FULL          | "Level: 3"                 |
| 🟡 HALF          | "Level: 2"                 |
| 🔴 EMPTY         | "Level: 1"                 |

---

## 🔋 Power Design

- 🧠 MCU enters **deep sleep mode** after each transmission  
- 🌡️ Ultra-low leakage from CR2032 (<1µA in sleep)  
- ⚙️ Active Mode: ~1-3 mA only during broadcast  
> 📈 Result: **Battery life of several months** with efficient duty cycling!

---

## 🌱 Scalability & Future Scope

✅ Add support for **multiple tanks**  
✅ Integrate **mobile app UI** for easier monitoring  
📶 Upgrade to **LoRaWAN** or **Wi-Fi** for broader coverage  
🔋 Real-time **battery health display** via ADC  
📦 Enclose in **IP-rated waterproof casing**

---

## 🧑‍💻 Developer's Note

> “This internship helped me apply classroom knowledge to real-world systems and gave me hands-on experience in embedded C, BLE protocol design, and low-power hardware optimization.”  
> — *Dipjyoti Kodali*

---



## 📄 References

- [nRF52 DK Board](https://www.nordicsemi.com/Products/Development-hardware/nRF52-DK)  
- [Segger Embedded Studio](https://www.segger.com/products/development-tools/embedded-studio/)  
- [nRF Connect App](https://www.nordicsemi.com/Products/Development-tools/nRF-Connect-for-mobile)  
- [CR2032 Battery Specs](https://www.mikroe.com/lithium-battery-3v-cr2032)

---

> 📍 *Due to a Non-Disclosure Agreement (NDA), I am unable to share the circuit design and the working code in a public repository.As, it was a project for the client of Techavo Systems.*  

