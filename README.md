# arduino

C++ / Arduino sketches from my systems-development coursework at IFPR — light sensing, audio output, and the hardware side of an assistive cardiovascular-anatomy project.

This repo is a **study log**, not a library. Each sketch is small, self-contained, and meant to be read alongside its circuit diagram. If you're here to see how the pieces fit together, start with the project table below.

---

## 📁 What's in here

| File | What it does | Notes |
|:--|:--|:--|
| [`SensordeLuz.ino`](./SensordeLuz.ino) | Reads an LDR (light sensor) and responds to light level | Analog input + threshold logic |
| [`buzzerr.ino.ino`](./buzzerr.ino.ino) | Drives a piezo buzzer | The doubled `.ino.ino` is a save artifact, not a bug — sketch still compiles |
| [`arduinoCardiovascular.ino`](./arduinoCardiovascular.ino) | Audio output for the tactile cardiovascular teaching prototype | Pairs with [`tocador_audio`](https://github.com/Sistema-Cardiovascular-Biologia-Tatil/tocador_audio) |
| [`CircuitoVisualI2c.png`](./CircuitoVisualI2c.png) | Circuit diagram for the I2C setup | Wiring reference |
| [`I2cCircuito.txt`](./I2cCircuito.txt) | Pin mappings / I2C notes | Text companion to the diagram |

---

## 🔌 The I2C circuit

`CircuitoVisualI2c.png` + `I2cCircuito.txt` document the I2C wiring used in the sensor sketches:

- **SDA / SCL** — I2C data and clock lines
- **VCC / GND** — power rails
- Pin assignments are listed in `I2cCircuito.txt`; the image is the visual reference

If you're rebuilding this: wire the diagram first, then flash `SensordeLuz.ino` and watch the serial output as you cover/uncover the LDR.

---

## 🫀 Cardiovascular project link

`arduinoCardiovascular.ino` is the firmware half of the tactile-and-audio cardiovascular teaching model presented at **FICIÊNCIAS** and **IFTECH 2025**.

- Audio player logic: [`Sistema-Cardiovascular-Biologia-Tatil/tocador_audio`](https://github.com/Sistema-Cardiovascular-Biologia-Tatil/tocador_audio)
- 3D-printed tactile models: [`Sistema-Cardiovascular-Biologia-Tatil/Modelos3D`](https://github.com/Sistema-Cardiovascular-Biologia-Tatil/Modelos3D)
- This repo holds the sketch that runs on the board

The goal: a student touches a physical heart model, and the corresponding audio description plays — making cardiovascular anatomy accessible to blind and low-vision learners.

---

## 🧰 Stack

![Arduino](https://img.shields.io/badge/Arduino-B23A48?style=flat-square&logo=arduino&logoColor=FAF3EB)
![C++](https://img.shields.io/badge/C++-C94A4A?style=flat-square&logo=cplusplus&logoColor=FAF3EB)
![I2C](https://img.shields.io/badge/I2C-E57373?style=flat-square)
![Breadboard](https://img.shields.io/badge/Breadboard_Prototyping-E57373?style=flat-square)

**Hardware involved:** Arduino board, LDR (light sensor), piezo buzzer, I2C peripherals, breadboard + jumper wires.

---

## 🚧 Status

Study repo — sketches are working but not packaged as a library. No build system; open each `.ino` in the Arduino IDE and flash to the board. PRs and corrections welcome.

---

## 📫 Contact

Ana Clara Batista · [@redStripedClown](https://github.com/redStripedClown) · ana0clara0cordeiro0batista@gmail.com
