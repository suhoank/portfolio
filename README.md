# 👨‍💻 안녕하세요, 임베디드 엔지니어 김수환입니다.

> **"하드웨어의 정밀함과 소프트웨어의 논리를 연결하는 엔지니어를 지망합니다."**
> 
> 실시간 데이터 처리와 센서 융합 기술을 통해 사용자 경험을 개선하는 솔루션을 개발합니다. 
> 회로 설계부터 펌웨어 최적화, 모바일 인터페이스 구현까지 시스템 전체 주기를 다루는 역량을 갖추고 있습니다.

---

## 🛠 Tech Stack

| Category | Skills |
| :--- | :--- |
| **Language** | ![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=white) |
| **Embedded** | **ATmega128(AVR)**, **UART Communication**, **ADC Data Mapping** |
| **Tools** | **AVR Studio 4**, **MIT App Inventor**, **GitHub**, **Git** |
| **Knowledge** | **Sensor Interface**, **Custom Communication Protocol**, **Data Normalization** |

---

## 🚀 Featured Projects

### 🧤 AVR 기반 실시간 지문자 번역 글로브 시스템
> **Embedded Control | Data Processing | Mobile Interface**

| 시스템 외형 (Hardware) | 핵심 로직 (Software) |
| :---: | :---: |
| <img src="https://github.com/suhoank/AVR-Sign-Language-Translator/blob/main/Hardware/Images/glove_top_view.jpg?raw=true" width="350"> | <img src="https://github.com/suhoank/AVR-Sign-Language-Translator/blob/main/Mobile_App/Images/App_UI_안녕_merged.jpeg?raw=true" width="450"> |

#### 📝 Project Description
4채널 플렉스 센서와 9축 AHRS 센서 데이터를 **ATmega128**로 처리하여, 스마트폰 앱을 통해 지문자를 실시간 텍스트 및 음성(TTS)으로 변환하는 시스템입니다.

#### 🏆 Key Engineering Points
* **센서 데이터 신뢰성 확보:** 1kΩ~34.5kΩ 부하 저항 실험을 통해 **Dynamic Range를 극대화**하여 인식 정확도 90% 달성
* **통신 프로토콜 설계:** 데이터 유실 방지를 위해 시작/종료 프레임(`<F>`, `<E>`)을 포함한 **Custom UART 패킷** 설계
* **알고리즘 구현:** 한글 오토마타 원리를 적용한 **자모음 결합 로직** 및 실시간 데이터 파싱 알고리즘 구축

* #### 🏆 Engineering Points
* **다중 센서 인터페이스 설계:** 4채널 Flex 센서(Analog)와 9축 AHRS(UART) 센서를 ATmega128에 통합하여 실시간 제스처 데이터 수집 환경 구축
* **데이터 정규화 및 분석:** 센서별 각기 다른 출력 범위를 특정 임계값(Threshold) 기반으로 **Data Normalization**하여, 손가락 굽힘 정도를 정밀하게 수치화
* **기기 간 전용 프로토콜 설계:** UART 통신 기반의 Custom 패킷 구조(`<F>...<E>`)를 정의하여 무선 환경에서도 왜곡 없는 실시간 데이터 전송 달성

👉 **[상세 프로젝트 보기 (Repository)](https://github.com/suhoank/AVR-Sign-Language-Translator)** | **[🎬 시연 영상 (YouTube)](https://youtu.be/Kg3Yly_6IG8)**

---

## 📫 Contact & Links
* **GitHub:** [github.com/suhoank](https://github.com/suhoank)
* **Email:** [suhoank@gmail.com]

---
<sub>© 2026 suhoank. All Rights Reserved.</sub>
