# 🚗ESP8266 IoT Controlled Car with Blynk App

This project demonstrates how to control a car using an ESP8266 microcontroller and the Blynk IoT platform. The car's movements—forward, backward, left, and right—are controlled via a smartphone app, and a servo motor is included for additional functionality.

## ✨ Features

- 🔧 Remote control of car movements through the Blynk app.
- 📱 Real-time control using Wi-Fi.
- 🎯 Servo motor integration for added features like steering or other mechanisms.
- 🚦 Supports smooth operations for forward, backward, left, and right movements.

---

## 🗂️ Components Required

1. ESP8266 (NodeMCU or similar)
2. L298N Motor Driver Module
3. DC Motors (2 or 4 depending on your car design)
4. Servo Motor
5. Power supply for motors and ESP8266
6. Connecting wires
7. Blynk App (available on Android and iOS)

---

## 🖥️ Code Explanation

The provided code does the following:

- Connects to a Wi-Fi network using the Blynk library.
- Listens for virtual pin commands from the Blynk app.
- Executes motor control logic based on the received commands.
- Controls a servo motor for additional functionality.

### 📜 Pin Configuration
| **Function**       | **Pin**       |
|---------------------|---------------|
| Left Motor Forward  | GPIO 12 (l1) |
| Left Motor Backward | GPIO 13 (l2) |
| Right Motor Forward | GPIO 14 (r1) |
| Right Motor Backward| GPIO 15 (r2) |
| Servo Motor         | GPIO 3       |

---

## 🚀 Getting Started

### 📥 Installation

1. Install the [Arduino IDE](https://www.arduino.cc/en/software) if not already installed.
2. Add the ESP8266 board to your Arduino IDE through **File > Preferences > Additional Board Manager URLs**:
   ```
   http://arduino.esp8266.com/stable/package_esp8266com_index.json
   ```
3. Install the following libraries:
   - **ESP8266WiFi**: Built-in for ESP8266.
   - **BlynkSimpleEsp8266**: Install via the Arduino Library Manager.
   - **Servo**: Install via the Arduino Library Manager.

### 🔧 Setup

1. Replace the following placeholders in the code with your actual credentials:
   - `auth` → Your Blynk authentication token.
   - `ssid` → Your Wi-Fi network name.
   - `pass` → Your Wi-Fi password.
2. Upload the code to your ESP8266 using the Arduino IDE.
3. Connect the motors, servo, and power supply as per the pin configuration.

---

## 📱 Blynk App Configuration

1. Download the Blynk app from the [Google Play Store](https://play.google.com/store/apps/details?id=cc.blynk) or [Apple App Store](https://apps.apple.com/app/blynk-iot/id808760481).
2. Create a new project in the app and note down the authentication token sent to your email.
3. Add virtual buttons for:
   - **V1**: Forward (`f`)
   - **V2**: Backward (`b`)
   - **V3**: Left (`l`)
   - **V4**: Right (`r`)
   - **V5**: Servo (`ser`)
4. Link these buttons to the corresponding virtual pins in the app.

---

## 🛠️ Functionality

- **Forward (`fd`)**: Moves the car forward.
- **Backward (`bw`)**: Moves the car backward.
- **Left (`lw`)**: Turns the car left.
- **Right (`rw`)**: Turns the car right.
- **Servo (`servo.write()`)**: Moves the servo motor to different angles.

---

## ⚠️ Precautions

- Ensure a stable power supply to avoid unexpected behavior.
- Double-check your motor and servo connections.
- Test in a safe environment to prevent damage to components.

---

## 📸 Demo

Upload photos or videos of the project in action to inspire others! 📷🎥

---

## 🤝 Contribution

Feel free to fork this repository, improve the code, or add new features. Submit a pull request when ready! ✨

---

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details. 📜

---

Enjoy building your IoT car! 🛠️🚀
