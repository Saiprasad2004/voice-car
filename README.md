# 🤖 Line Follower Robot using Arduino Uno and L298N

## 📌 Project Overview

This project implements an autonomous Line Follower Robot capable of detecting and following a predefined black line on a white surface using IR sensors. The robot continuously adjusts its path by varying the speed of the left and right motors, enabling smooth and accurate navigation.

The project uses proportional (P) control to improve turning performance and includes a line recovery mechanism to regain the track if the robot loses the line.

---

## ✨ Features

- Autonomous line following
- Differential drive control using L298N motor driver
- Proportional (P) based speed correction
- Last known direction recovery when the line is lost
- Smooth left and right turning
- Real-time sensor monitoring through Serial Monitor

---

## 🛠️ Hardware Components

| Component | Quantity |
|-----------|----------|
| Arduino Uno | 1 |
| L298N Motor Driver | 1 |
| IR Sensors | 2 / 3 |
| DC Gear Motors | 2 |
| Robot Chassis | 1 |
| Wheels | 2 |
| Caster Wheel | 1 |
| Battery Pack | 1 |
| Jumper Wires | As required |

---

## 🔌 Circuit Connections

### IR Sensors

| Sensor | Arduino Pin |
|---------|-------------|
| Left IR | D2 |
| Right IR | D4 |

### L298N Motor Driver

| L298N Pin | Arduino Pin |
|------------|-------------|
| ENA | D5 |
| ENB | D6 |
| IN1 | D7 |
| IN2 | D8 |
| IN3 | D9 |
| IN4 | D10 |

### Motors

- Left Motor → OUT1, OUT2
- Right Motor → OUT3, OUT4

---

## ⚙️ Working Principle

1. IR sensors continuously detect the presence of the black line.
2. Sensor readings are processed by the Arduino.
3. Based on sensor inputs, the robot decides whether to:
   - Move Forward
   - Turn Left
   - Turn Right
   - Search for the line using the last known direction
4. Motor speeds are adjusted using PWM signals for smooth navigation.

---

## 📊 Sensor Logic

| Left Sensor | Right Sensor | Robot Action |
|-------------|--------------|--------------|
| 0 | 0 | Search using last direction |
| 0 | 1 | Turn Right |
| 1 | 0 | Turn Left |
| 1 | 1 | Move Forward |

> Sensor Logic: `0 = White Surface`, `1 = Black Line`

---

## 💻 Software

- Arduino IDE
- Embedded C/C++
- PWM Motor Control

---

## 🚀 Future Improvements

- Implement full PID control.
- Add obstacle avoidance using ultrasonic sensor.
- Increase the number of IR sensors for improved tracking.
- Integrate wireless monitoring and control.

---

## 👨‍💻 Author

**Pasupula Sai Prasad**
