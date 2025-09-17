# Arduino-Powered Hand Gesture Controlled Car 🚗✋

This project implements a **hand gesture controlled robotic car** using **Arduino microcontrollers**, an **MPU6050 sensor**, and **nRF24L01 wireless communication modules**.  
By tilting your hand in different directions, you can control the car’s movement — forward, backward, left, right, or stop.

---

## 📌 Features
- **Gesture Recognition** using MPU6050 (accelerometer + gyroscope).
- **Wireless Communication** with nRF24L01 module.
- **Motor Control** through L298N H-Bridge driver.
- **4WD Car Chassis** powered by Li-ion 18650 cells.
- Supports **five commands**: Forward, Backward, Left, Right, Stop.

---

## 🛠️ Hardware Used
- Arduino Uno (Receiver)
- Arduino Nano (Transmitter)
- MPU6050 Accelerometer + Gyroscope
- nRF24L01 Wireless Modules
- L298N Motor Driver
- 4WD Car Kit (chassis + DC motors)
- 18650 Li-ion Battery Cells

---

## 📂 Repository Structure

---

## ⚙️ Setup & Usage
1. **Transmitter (Hand Unit)**:
   - Upload `transmitter.ino` to Arduino Nano.
   - Connect MPU6050 via I2C (SDA → A4, SCL → A5).
   - Connect nRF24L01 via SPI (MISO, MOSI, SCK, CE, CSN).

2. **Receiver (Car Unit)**:
   - Upload `receiver.ino` to Arduino Uno.
   - Connect nRF24L01 via SPI.
   - Interface L298N with motor driver pins and motors.
   - Power using 2–3 Li-ion 18650 cells.

3. **Operation**:
   - Tilt hand forward → Car moves forward.
   - Tilt backward → Car moves backward.
   - Tilt left/right → Car turns left/right.
   - Neutral → Car stops.

---

## 📊 Performance
- Latency: ~160–200 ms (gesture to response).
- Wireless Range: ~15 meters indoors.
- Commands: 5 basic movements.

---

## 📸 Schematics
- [Transmitter Circuit](Schematics/HandGestureCar_Tx.pdf)
- [Receiver Circuit](Schematics/HandGestureCar_Rx.pdf)

---

## 🚀 Future Improvements
- Replace L298N with BTS7960 motor driver for better efficiency.
- Add obstacle detection (ultrasonic sensors).
- Use glove-based transmitter with flexible PCB.
- Upgrade wireless modules to nRF24L01+ PA/LNA for extended range.

---

## 👨‍💻 Authors
- **Soham Rajesh Deshmukh** (Hardware Design, Coding, Testing)
- Group members (Contributions in system assembly and validation)

---
