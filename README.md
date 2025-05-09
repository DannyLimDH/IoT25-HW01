# IoT25-HW01: ESP32 LED Blink Test

이 프로젝트는 ESP32 개발 보드를 사용하여 내장 또는 외장 LED를 1초 간격으로 점멸시키는 과제입니다.

---

## 🧾 과제 목표

- Arduino IDE를 이용한 ESP32 개발 환경 구축
- GPIO 출력 제어 실습 (LED 점멸)
- 시리얼 모니터 출력 확인

---

## 🧰 사용 부품

- ESP32 DevKit v1
- LED 모듈 (또는 내장 LED)
- Micro USB 케이블

---

## 🔌 회로 연결

- LED 모듈 → ESP32
  - V (VCC) → 3.3V
  - G (GND) → GND
  - S (Signal) → GPIO 2

> 📸 회로 사진은 `/media/hw1-1.png`, `/media/hw1-2.png` 참고

---

## 🧾 코드 설명

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

- `GPIO 2` 핀을 출력으로 설정
- 1초 간격으로 LED를 켜고 끄며, 시리얼 모니터에 상태 출력

---

## ▶ 실행 영상

📹 [실행 결과 보기](./media/IoT25-HW01.mp4)

---

## ✅ 확인 사항

- [x] 코드가 정상 컴파일 및 업로드됨
- [x] LED가 1초 간격으로 깜빡임
- [x] 시리얼 모니터에 메시지 출력 확인
