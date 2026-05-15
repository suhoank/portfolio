# 안녕하세요, 장비 메커니즘과 데이터 로직을 이해하는 기술 스페셜리스트 김수환입니다.

> **"고도화된 생체 신호 데이터 해석과 장비 트러블슈팅으로 수술실의 무결성을 지원합니다."**
> 
> 실무적인 센서 데이터 처리(Data Normalization)와 주파수 분석(공진 억제)을 통해 시스템의 신뢰성을 극대화한 경험을 보유하고 있습니다. 하드웨어와 소프트웨어의 유기적인 구동 원리를 깊이 이해하고 있어, 고도화된 의료 장비 시스템을 빠르게 습득합니다. 이를 바탕으로 현장에서 발생하는 기술적 예외 상황에 완벽히 대처하고 의료진에게 신뢰도 높은 가이드를 제공하겠습니다.

---

## 🛠 Tech Stack

| Category | Skills |
| :--- | :--- |
| **Language** | ![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=white) |
| **Embedded** | **ATmega128(AVR)**, **Bitmasking & Bitwise Ops**, **UART/ADC Control** |
| **Tools** | **AVR Studio 4**, **MIT App Inventor**, **GitHub**, **Git** |
| **Knowledge** | **Data Normalization**, **Custom Communication Protocol**, **Cost Optimization** |

---

## 🚀 Featured Projects

### 🧤 복합 센서 융합 실시간 지문자 번역 글로브 시스템
> **Sensor Fusion | Data Normalization | Signal Reliability**

| 하드웨어 구성 (Sensors) | 모바일 UI (TTS) |
| :---: | :---: |
| <img src="https://github.com/suhoank/AVR-Sign-Language-Translator/blob/main/Hardware/Images/glove_top_view.jpg?raw=true" width="350"> | <img src="https://github.com/suhoank/AVR-Sign-Language-Translator/blob/main/Mobile_App/Images/App_UI_안녕_merged.jpeg" width="450" > |

#### 📝 Project Description
4채널 플렉스 센서와 9축 AHRS 센서 데이터를 **ATmega128**로 처리하여, 스마트폰 앱을 통해 지문자를 실시간 텍스트 및 음성(TTS)으로 변환하는 시스템입니다. 인체 움직임에 따른 아날로그 센서 데이터의 임계값을 설정하고 정규화(Normalization)하는 알고리즘을 독자적으로 구축했습니다.

#### 🏆 Key Engineering Points
* **다중 센서 인터페이스 설계:** Flex 센서와 AHRS(UART) 센서를 통합하여 인간의 미세한 제스처 데이터를 실시간으로 수집하는 환경을 구축했습니다.
* **생체 데이터 신뢰성 확보:** 부하 저항 최적화 실험을 수행하여 센서의 Dynamic Range를 극대화했고, 현장 데이터 수집의 정확도를 높였습니다.
* **데이터 정규화 및 분석:** 센서별 출력 범위를 특정 임계값(Threshold) 기반으로 정규화하여, 데이터의 흔들림 속에서도 정확한 지문자를 판별하는 알고리즘을 적용했습니다. (※ 매핑 장비의 전압 임계값 판독 메커니즘과 일치)
* **시스템 통합 역량:** 하드웨어 센싱부터 실시간 데이터 파이프라인 구축까지 독자적으로 완료하여 장비 가동의 안정성을 증명했습니다.

👉 **[상세 프로젝트 보기 (Repository)](https://github.com/suhoank/High-Precision-Sign-Language-Translator-with-Sensor-Fusion)** | **[🎬 시연 영상 (YouTube)](https://youtu.be/Kg3Yly_6IG8)**

---

## 🖨️ 기구 설계 분석 및 주파수 응답 기반 공진 최적화 개조
> **System Integration | Resonance Data Analysis | Process Automation**

#### 📊 Hardware & Performance Comparison

| 구분 | 순정 KP3S (Baseline) | 하이브리드 개조 모델 (Improved) |
| :--- | :---: | :---: |
| **시스템 외형** | <img src="https://github.com/suhoank/kp3s-prusa-mini-mod/blob/main/Hardware/Images/KP3S.jpeg" width="350"> | <img src="https://github.com/suhoank/kp3s-prusa-mini-mod/blob/main/Hardware/Images/kp3s-prusa-mini-mod.jpg" width="350"> |
| **기구부 설계** | V-Slot 기반 보급형 캔틸레버 구조 | **Prusa Mini STEP 분석 기반** 강성 보완 이식 |
| **X축 공진 분석** | <img src="https://github.com/suhoank/kp3s-prusa-mini-mod/blob/main/Hardware/Images/kp3s_shaper_x.png" width="350"> | <img src="https://github.com/suhoank/kp3s-prusa-mini-mod/blob/main/Hardware/Images/kp3s-prusa-mini-mod_shaper_x.png" width="350"> |
| **Y축 공진 분석** | <img src="https://github.com/suhoank/kp3s-prusa-mini-mod/blob/main/Hardware/Images/kp3s_shaper_y.png" width="350"> | <img src="https://github.com/suhoank/kp3s-prusa-mini-mod/blob/main/Hardware/Images/kp3s-prusa-mini-mod_shaper_y.png" width="350"> |
| **제어 성능** | 고속 이동 시 진동(Ghosting) 발생 | **진동 감쇄 및 주파수 안정성 확보** |

#### 📝 Project Description
하드웨어 STL 파일 분석을 통해 시스템의 기계적 강성을 개선하고, Klipper 펌웨어를 활용해 제어 로직을 재구축한 프로젝트입니다. 특히 ADXL345 가속도 센서를 활용한 주파수 응답 분석을 실시하여, 시스템 구동 시 발생하는 진동 노이즈를 정량적으로 억제했습니다.

#### 🏆 Key Engineering Points
* **역설계 기반 기구부 통합:** 기구 설계 데이터를 정밀 분석하여 이종 장비의 핵심 파트를 최적화된 형태로 이식, 하드웨어의 물리적 강성을 개선했습니다.
* **공진 데이터 기반 제어 최적화 (Input Shaper):** * ADXL345 센서로 측정한 공진 주파수 데이터를 분석하여 MZV/EI 알고리즘을 적용했습니다.특정 주파수 대역의 피크(Power Spectral Density)를 효과적으로 억제하여 고속 구동 시의 신호 안정성을 확보했습니다. (※ 수술실 장비의 신호 노이즈 필터링 감각 배양)
* **센서 활용 데이터 보정:** BLTouch 센서를 적용하여 베드의 물리적 오차를 데이터화하고, 소프트웨어 보정 알고리즘을 통해 구동 오차를 최소화했습니다.
* **환경 변수 통제 자동화:** 챔버 온도 관리 및 출력 전 자동 예열/점검 시퀀스 매크로를 직접 설계하여 공정 안정성을 강화했습니다.

---

### 🧤 스위치 기반 에지 컴퓨팅 지문자 번역 시스템
> **Logical Classification | Bitmasking Logic | Embedded Edge Logic**

| 시스템 외형 (Switches) | 모바일 UI (TTS) |
| :---: | :---: |
| <img src="https://github.com/suhoank/Low-Cost-Switch-Sign-Translator/blob/main/Hardware/Images/Glove-Top-View2.jpg" width="350"> | <img src="https://github.com/suhoank/Low-Cost-Switch-Sign-Translator/blob/main//Mobile_App/Images/App_UI_종합설계.png?raw=true" width="350"> |

#### 📝 Project Description
하드웨어 구조를 효율화하여 시스템 안정성을 높인 경제형 지문자 번역기입니다. 외부 서버나 통신 연산에 의존하지 않고, MCU 내부에서 비트 연산을 통해 직접 데이터를 고속 분류(Classification)하는 독립형 시스템을 채택했습니다.

#### 🏆 Key Engineering Points
* **하드웨어 최적화 설계:** 스위치 레이아웃의 복합 배치를 통해 하드웨어 안정성을 높이면서도 20종 이상의 데이터 식별 기능을 안정적으로 구현했습니다.
* **비트 연산 기반 고속 알고리즘:** MCU 레지스터 데이터를 비트 시프트 및 마스킹 연산으로 처리하여 실시간 데이터 판별 로직을 직접 구현했습니다.
* **임베디드 에지 로직(Edge Logic):** 데이터 판별 로직을 장비 단에서 완결시켜 통신 부하를 줄이고 장비 자체의 독립적 응답 속도를 향상시켰습니다.
* **전용 패킷 통신 프로토콜:** 안정적인 데이터 전송을 위해 시작/종료 프레임(`<S>`, `<E>`)을 포함한 **Custom UART 프로토콜** 설계

👉 **[상세 프로젝트 보기 (Repository)](https://github.com/suhoank/Low-Cost-Switch-Sign-Translator)** | **[🎬 시연 영상 (YouTube)](https://youtu.be/u_X_YjnAQQs)**

---

## 📫 Contact & Links
* **GitHub:** [github.com/suhoank](https://github.com/suhoank)
* **Email:** [ksh29211@gmail.com]

---
<sub>© 2026 suhoank. All Rights Reserved.</sub>
