# IoT25-HW01: ESP32 LED Blink Test

This project uses an ESP32 development board to blink an onboard or external LED at 1-second intervals.

---

## 🧾 Project Objectives

- Set up the ESP32 development environment using the Arduino IDE
- Practice GPIO output control (LED blinking)

---

## 🧰 Components Used

- ESP32 DevKit v1
- LED module (or onboard LED)
- Micro USB cable

---

## 🔌 Circuit Connection

- LED Module → ESP32
  - V (VCC) → 3.3V
  - G (GND) → GND
  - S (Signal) → GPIO 2
---

## 🧾 Code Explanation

```cpp
#define LED 2

void setup() {
  Serial.begin(115200);
  pinMode(LED, OUTPUT);
}

void loop() {
  digitalWrite(LED, HIGH);
  Serial.println("LED is on");
  delay(1000);
  digitalWrite(LED, LOW);
  Serial.println("LED is off");
  delay(1000);
}
```

- Sets GPIO 2 as an output.
- Turns the LED on and off every second, and logs “LED is on” / “LED is off” to the Serial Monitor.

---
## ▶ Screenshots

![스크린샷 1](https://github.com/DannyLimDH/IoT25-HW01/blob/main/media/hw1-1.png)
![스크린샷 2](https://github.com/DannyLimDH/IoT25-HW01/blob/main/media/hw1-2.png)

---
## ▶ Demo GIF

![GIF 설명](./media/IoT25-HW01.gif)

---
## References
Rui Santos, VSCode + PlatformIO IDE: ESP32 & ESP8266, Arduino (Random Nerd Tutorials)
https://RandomNerdTutorials.com/vs-code-platformio-ide-esp32-esp8266-arduino/

---
