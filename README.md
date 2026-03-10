# 👨‍💻 안녕하세요, 임베디드 엔지니어 김수환입니다.

> **"하드웨어의 경제성과 소프트웨어의 논리를 연결하는 엔지니어를 지망합니다."**
> 
> 실무적인 센서 데이터 처리와 로우 레벨 최적화를 통해 실질적인 솔루션을 설계합니다. 
> 회로 설계부터 펌웨어 최적화,비용 최적화, 모바일 인터페이스 구현까지 폭넓은 개발 경험을 보유하고 있습니다.

---

## 🛠 Tech Stack

| Category | Skills |
| :--- | :--- |
| **Language** | ![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=white) |
| **Embedded** | **ATmega128(AVR)**, **Bitmasking & Bitwise Ops**, **UART/ADC Control** |
| **Tools** | **AVR Studio 4**, **MIT App Inventor**, **GitHub**, **Git** |
| **Knowledge** | **Cost Optimization**, **Custom Communication Protocol**, **Data Normalization** |

---

## 🚀 Featured Projects

## 🖨️ [Personal Project] KP3S 기반 Prusa Mini 기구 설계 이식 및 Klipper 펌웨어 최적화 개조
> **System Integration | Resonance Data Analysis | Process Automation**

#### 📊 Hardware & Performance Comparison

| 구분 | 순정 KP3S (Baseline) | 하이브리드 개조 모델 (Improved) |
| :--- | :---: | :---: |
| **시스템 외형** | <img src="https://github.com/suhoank/portfolio/blob/main/Images/kp3s_stock.jpg?raw=true" width="350"> | <img src="https://github.com/suhoank/portfolio/blob/main/Images/kp3s_mod.jpg?raw=true" width="350"> |
| **기구부 설계** | V-Slot 기반 보급형 캔틸레버 구조 | **Prusa Mini STEP 분석 기반** 강성 보완 이식 |
| **X축 공진 분석** | <img src="https://github.com/suhoank/portfolio/blob/main/Images/kp3s_shaper_calibrate_x_4.png?raw=true" width="350"> | <img src="https://github.com/suhoank/portfolio/blob/main/Images/kp3s_mini_shaper_x.png?raw=true" width="350"> |
| **Y축 공진 분석** | <img src="https://github.com/suhoank/portfolio/blob/main/Images/kp3s_shaper_calibrate_y_3.png?raw=true" width="350"> | <img src="https://github.com/suhoank/portfolio/blob/main/Images/kp3s_mini_shaper_y.png?raw=true" width="350"> |
| **제어 성능** | 고속 이동 시 진동(Ghosting) 발생 | **진동 감쇄 및 주파수 안정성 확보** |

#### 📝 Project Description
기존 KP3S의 기구적 한계를 극복하기 위해 Prusa Mini의 설계 데이터를 분석하여 핵심 기구부를 이식하고, Klipper 펌웨어를 통해 시스템을 재구축한 프로젝트입니다. 단순한 부품 교체를 넘어 ADXL345 가속도 센서를 활용한 주파수 응답 분석을 실시하였으며, 이를 통해 진동 억제 성능을 정량적으로 증명했습니다.

#### 🏆 Key Engineering Points
* **역설계 기반 기구부 통합:** Prusa Mini의 하드웨어 STEP 파일을 분석하여 KP3S 기구부에 최적화된 형태로 이식함으로써 기계적 강성을 개선했습니다.
* **공진 데이터 기반 제어 최적화 (Input Shaper):** * ADXL345 센서로 측정한 공진 주파수 데이터를 분석하여 MZV/EI 알고리즘을 적용했습니다.
    * 개조 전후 비교 분석 결과, 특정 주파수 대역의 피크(Power Spectral Density)를 효과적으로 억제하여 고속 출력 정밀도를 확보했습니다.
* **BLTouch를 활용한 정밀 레벨링:** BLTouch 센서를 적용하여 베드의 물리적 오차를 데이터화하고, 소프트웨어 보정 알고리즘을 통해 대형 출력물의 치수 정확도를 높였습니다.
* **환경 변수 통제 자동화:** 챔버 온도 관리 및 출력 전 자동 예열/점검 시퀀스 매크로를 직접 설계하여 공정 안정성을 강화했습니다.

---

### 🧤 [졸업논문] 스위치 매트릭스 기반 저가형 지문자 번역 시스템
> **Cost Optimization | Bitmasking Logic | Embedded Edge Computing**

| 시스템 외형 (Switches) | 제어 흐름 (Flowchart) |
| :---: | :---: |
| <img src="https://github.com/suhoank/Low-Cost-Switch-Sign-Translator/blob/main/Hardware/Images/Glove-Top-View2.jpg" width="450"> | <img src="https://github.com/suhoank/portfolio/blob/main/Images/flowchart.png?raw=true" width="350"> |

#### 📝 Project Description
고가의 플렉스 센서를 **풀업(Pull-up) 스위치**로 대체하여 제작 비용을 80% 이상 절감한 경제형 지문자 번역기입니다. **ATmega128** 내부에서 비트 연산을 통해 직접 지문자를 분류(Classification)하는 구조를 채택하여 시스템 효율을 극대화했습니다.

#### 🏆 Key Engineering Points
* **비용 최적화 설계(Cost-Effective Design):** 택트/옴론 스위치의 복합 배치를 통해 하드웨어 단가를 낮추면서도 20종 이상의 지문자 식별 기능 구현
* **비트 연산 기반 고속 알고리즘:** MCU 레지스터(`PINA`, `PINC`) 데이터를 비트 시프트 및 마스킹 연산으로 처리하여 실시간 분류 로직 직접 구현
* **임베디드 에지 로직(Edge Logic):** 데이터 판별 로직을 MCU단에서 완결하여 통신 부하를 줄이고 시스템 응답 속도를 향상
* **전용 패킷 통신 프로토콜:** 안정적인 데이터 전송을 위해 시작/종료 프레임(`<S>`, `<E>`)을 포함한 **Custom UART 프로토콜** 설계

👉 **[상세 프로젝트 보기 (Repository)](https://github.com/suhoank/Low-Cost-Switch-Sign-Translator)** | **[🎬 시연 영상 (YouTube)](https://youtu.be/u_X_YjnAQQs)**

---

### 🧤 복합 센서 융합 실시간 지문자 번역 글로브 시스템
> **Sensor Fusion | Data Normalization | Mobile Interface**

| 하드웨어 구성 (Sensors) | 모바일 UI (TTS) |
| :---: | :---: |
| <img src="https://github.com/suhoank/AVR-Sign-Language-Translator/blob/main/Hardware/Images/glove_top_view.jpg?raw=true" width="350"> | <img src="https://github.com/suhoank/AVR-Sign-Language-Translator/blob/main/Mobile_App/Images/App_UI_안녕_merged.jpeg" width="450" > |

#### 📝 Project Description
4채널 플렉스 센서와 9축 AHRS 센서 데이터를 **ATmega128**로 처리하여, 스마트폰 앱을 통해 지문자를 실시간 텍스트 및 음성(TTS)으로 변환하는 시스템입니다.

#### 🏆 Key Engineering Points
* **다중 센서 인터페이스 설계:** Flex 센서와 AHRS(UART) 센서를 통합하여 고정밀 제스처 데이터 수집 환경 구축
* **센서 데이터 신뢰성 확보:** 부하 저항 최적화 실험을 통해 **Dynamic Range를 극대화**하여 인식 정확도 향상
* **데이터 정규화 및 분석:** 센서별 출력 범위를 특정 임계값(Threshold) 기반으로 **Data Normalization**하여 지문자 판별 알고리즘 적용
* **시스템 통합 역량:** 하드웨어 센싱부터 모바일 TTS 출력까지 이어지는 전체 데이터 파이프라인 독자 구축

👉 **[상세 프로젝트 보기 (Repository)](https://github.com/suhoank/High-Precision-Sign-Language-Translator-with-Sensor-Fusion)** | **[🎬 시연 영상 (YouTube)](https://youtu.be/Kg3Yly_6IG8)**

---

## 📫 Contact & Links
* **GitHub:** [github.com/suhoank](https://github.com/suhoank)
* **Email:** [suhoank@gmail.com]

---
<sub>© 2026 suhoank. All Rights Reserved.</sub>
