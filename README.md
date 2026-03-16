Here is a **professional GitHub `README.md`** for your **Fast Line Follower Robot** project. You can paste this directly into your repository.

---

# ⚡ Fast Line Follower Robot

A **high-speed autonomous line follower robot** designed for robotics competitions such as **Techno Main World Cup – World Robotic Championship 2025**.
The robot uses **infrared line sensors and PID control** to follow a track with high accuracy and speed.

This project focuses on **fast response, stable control, and efficient motor driving** for competitive robotics.

---

# 🚀 Features

✔ High-speed line tracking
✔ PID-based control algorithm
✔ IR sensor array for accurate line detection
✔ ESP32 microcontroller for fast processing
✔ Dual motor drive system
✔ Lightweight and compact design
✔ Designed for **robotic competitions**

---

# 📷 Robot Images

## Robot Prototype

![Image]()

![Image]()

![Image]()

![Image]()


---

# 🧠 Working Principle

1. **IR sensors detect the line** on the track.
2. Sensor values are processed by the **ESP32 microcontroller**.
3. A **PID control algorithm** calculates the correction.
4. Motor speeds are adjusted through the **motor driver**.
5. The robot continuously corrects its path to stay on the line at high speed.

---

# 🔧 Hardware Components

| Component                          | Purpose              |
| ---------------------------------- | -------------------- |
| ESP32                              | Main microcontroller |
| IR Line Sensor Array (QTR Sensors) | Line detection       |
| Motor Driver                       | Controls motor speed |
| DC Gear Motors                     | Robot movement       |
| LiPo Battery (2S)                  | Power supply         |
| Voltage Regulators                 | Stable power output  |
| Custom PCB / Perfboard             | Circuit mounting     |
| Robot Chassis                      | Structural support   |

---

# 🔌 Circuit Overview

### Motor Driver → ESP32

```
IN1 → GPIO
IN2 → GPIO
IN3 → GPIO
IN4 → GPIO
ENA → PWM Pin
ENB → PWM Pin
```

### QTR Sensor Array → ESP32

```
Sensor1 → GPIO
Sensor2 → GPIO
Sensor3 → GPIO
Sensor4 → GPIO
Sensor5 → GPIO
```

---

# 🧑‍💻 Software

Developed using **Arduino IDE with ESP32 board support**.

### Libraries Used

```
QTRSensors
Arduino.h
```

---

# 📂 Project Structure

```
Fast-Line-Follower-Bot
│
├── code
│   ├── MotorTestRun.ino
│   ├── QTRAExample.ino
│   ├── QTRARawValuesExample.ino
│   ├── QTRRCExample.ino
│   └── QTRRCRawValuesExample.ino
│
├── images
│   ├── robot1.jpg
│   ├── robot2.jpg
│   └── robot3.jpg
│
└── README.md
```

---

# ⚙️ How to Run

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/yourusername/fast-line-follower-robot.git
```

---

### 2️⃣ Install Arduino IDE Libraries

Install:

* QTRSensors Library

---

### 3️⃣ Upload the Code

Select board:

```
ESP32 Dev Module
```

Upload the program to the ESP32.

---

### 4️⃣ Calibrate Sensors

Before running:

* Place robot over the line
* Run sensor calibration
* Adjust PID parameters if required

---

# 🏁 Applications

* Robotics competitions
* Autonomous navigation
* Line tracking robots
* Embedded systems learning

---

# 🔮 Future Improvements

* Advanced PID tuning for higher speed
* AI-based path prediction
* Wireless tuning via Bluetooth/WiFi
* Lightweight custom PCB

---

# 👨‍💻 Author

**Arnav Domalwar**

Electronics & Robotics Developer

---

# Arduino library for the Pololu QTR Reflectance Sensors

Version: 4.0.0<br>
Release date: 2019-03-15<br>
[![Build Status](https://travis-ci.org/pololu/qtr-sensors-arduino.svg?branch=master)](https://travis-ci.org/pololu/qtr-sensors-arduino)<br>
[www.pololu.com](https://www.pololu.com/)

## Summary

This is a library for the Arduino IDE that helps interface with [Pololu QTR reflectance sensors][qtr].

## Supported platforms

This library is designed to work with the Arduino IDE versions 1.8.x or later; we have not tested it with earlier versions.  This library should support any Arduino-compatible board, including the [Pololu A-Star controllers][a-star].

## Getting started

### Hardware

The QTRSensors library supports Pololu's second-generation dimmable [QTR and QTRX reflectance sensor boards][qtr], as well as [older QTR sensors][older-qtr]. Before continuing, careful reading of the [QTR Reflectance Sensor Application Note][app-note] is recommended.

This library also works with the reflectance sensors built into or designed for Pololu robots, such as the [Zumo 32U4 Front Sensor Array](https://www.pololu.com/product/3122). However, the dedicated libraries for those robots (e.g. the [Zumo32U4 library](https://github.com/pololu/zumo-32u4-arduino-library)) generally provide an interface that is specific to those sensors and is easier to use.

### Software

You can use the Library Manager to install this library:

1. In the Arduino IDE, open the "Sketch" menu, select "Include Library", then "Manage Libraries...".
2. Search for "QTRSensors".
3. Click the QTRSensors entry in the list.
4. Click "Install".

If this does not work, you can manually install the library:

1. Download the [latest release archive from GitHub](https://github.com/pololu/qtr-sensors-arduino/releases) and decompress it.
2. Rename the folder "qtr-sensors-arduino-xxxx" to "QTRSensors".
3. Drag the "QTRSensors" folder into the "libraries" directory inside your Arduino sketchbook directory. You can view your sketchbook location by opening the "File" menu and selecting "Preferences" in the Arduino IDE. If there is not already a "libraries" folder in that location, you should make the folder yourself.
4. After installing the library, restart the Arduino IDE.

## Examples

Several example sketches are available that show how to use the library. You can access them from the Arduino IDE by opening the "File" menu, selecting "Examples", and then selecting "QTRSensors". If you cannot find these examples, the library was probably installed incorrectly and you should retry the installation instructions above.

## Documentation

For complete documentation of this library, see [the qtr-sensors-arduino documentation][doc].  If you are already on that page, see the QTRSensors class reference.

## Version history
* 4.0.0 (2019-03-15): Major library rewrite: instead of a hierarchy of classes for different sensor types, the library now provides a single `QTRSensors` class, and instances of this class can be configured for a specific sensor type. Configuration of sensor pins and other settings is now done using more human-readable class methods instead of constructor parameters. Support for calibration using the odd/even read modes has been added.
* 3.1.0 (2018-08-08): Added support for dimmable QTR and QTRX sensors with separate control of odd/even emitter banks.
* 3.0.0 (2016-08-16): Updated library to work with the Arduino Library Manager.
* 2.1.2 (2015-12-03): Corrected `readLine()` behavior to work with multiple instances (thanks to Tandy Carmichael).
* 2.1.1 (2014-05-02): Minor improvements to `read()` behavior and whitespace cleanup.
* 2.1.0 (2013-04-18): Improved existing examples and added two new examples for printing raw values.
* 2.0.2 (2013-04-17): Made constructors initialize pointers to avoid possible problems.
* 2.0.1 (2012-09-13): Added a 200 us delay after emitter state changes to ensure sensors do not start being sampled before the LEDs turn on/off.
* 2.0.0 (2012-02-14): Initial release of library on GitHub (with Arduino 1.0 compatibility).

[a-star]: https://www.pololu.com/a-star
[app-note]: https://www.pololu.com/docs/0J13
[doc]: https://pololu.github.io/qtr-sensors-arduino/
[older-qtr]: https://www.pololu.com/category/246/older-qtr-sensors
[qtr]: https://www.pololu.com/category/123/pololu-qtr-reflectance-sensors
