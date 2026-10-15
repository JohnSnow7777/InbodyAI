# CONNECT InBody AI (`Bio-Vision Health Station v2.0`)

**주식회사 커넥트(Connect Corp.) × 스마일스퀘어 마이파크(MyPark Screen Park Golf)**  
약국·기업 건강관리실·스마트 경로당 및 전국 마이파크 매장에 설치되는 **차세대 5-Modal 비침습 AI 건강측정기기(`CONNECT InBody AI`)** 심층 기술 리서치 및 자체 개발 마스터플랜 레포지토리입니다.

- **Live Demo & Interactive Report**: [https://connectinbody.vercel.app/](https://connectinbody.vercel.app/)
- **GitHub Repository**: [https://github.com/JohnSnow7777/InbodyAI](https://github.com/JohnSnow7777/InbodyAI)

---

## 1. 핵심 아키텍처 (5-Modal Real-Science Sensor Fusion)

기존 중국산/OEM 양자공명자기분석기(QRMA) 핸드스틱의 유사과학 논란(단순 피부 저항 + 나이/성별 통계 더미 생성)을 100% 배제하고, 글로벌 반도체 제조사(Analog Devices, Texas Instruments, Melexis)의 **정통 임상급 생체신호 AFE 칩셋**과 커넥트 고유 **3D Physical AI 비전 엔진**을 결합했습니다.

1. **[비전 광학부]** 60fps RGB/IR 카메라 기반 **안면 rPPG (`TS-CAN`/`POS`) + 미세 두부 진동(`rBCG`) + 홍채 시선추적(`MediaPipe Iris` Anti-Saccade 경도인지장애 MCI 선별)**
2. **[전신 피지컬 AI부 (커넥트 독자 IP)]** 30초 무마커 3D 전신 기능 평가 (`MediaPipe Pose`/`RTMPose`/`Sports2D` + 커넥트 `RULA` 근골격 부하 엔진): 거북목(CVA), 어깨 회전 ROM, 하지 근력(5회 의자 일어서기 5xSTS), 외발서기 낙상 위험도(SLS)
3. **[음성 바이오마커부]** 20초 음성 발화 분석 (성대 떨림 Jitter/Shimmer 및 발화 휴지 구간 Pause → 치매·우울·직무 번아웃 스크리닝)
4. **[임상급 스마트 멀티센서 듀얼 핸드스틱 & 4전극 발판]**
   - **다주파수 BIA & 50kHz 세포막 위상각(Phase Angle)**: `Analog Devices AD5940` + `TI AFE4300`
   - **동기화 1-Lead 심전도(ECG) + 듀얼파장 PPG($\text{SpO}_2$) 기반 맥파전달시간(PTT) 무커프 혈압 추정**: `Analog Devices MAX86150`
   - **디지털 악력계(Grip Strength — AWGS 2025 근감소증 1차 지표)**: 50kg 스트레인게이지 로드셀 + `HX711` 24-bit ADC
   - **적외선 말초 체온 & 교감신경 땀샘 전도도(EDA)**: `Melexis MLX90614` + 내장 EDA 채널 + `ADuM1250` 의료급 디지털 절연
5. **[스마일스퀘어 마이파크 전국 거점 O2O 연동 (PHR × PSR)]**
   - 약국 정적 건강데이터(PHR)와 전국 마이파크(스크린 파크골프) 타석 1,800fps 스윙 운동데이터(PSR)를 결합한 **Check-to-Play (약국 → 마이파크) & Play-to-Care (마이파크 → 약국)** 양방향 순환 생태계

---

## 2. 하드웨어 제조원가 (BOM, 500대 양산 기준) 및 개발 기간

- **스마트 멀티센서 듀얼 핸드스틱 BOM**: 약 **$55 USD (약 76,000원)**
- **키오스크 전체 제조원가 (Total BOM)**:
  - **21.5" 약국 데스크형 (`Pharm-Desk`)**: 약 **$538 ~ $586 USD (약 74만 ~ 81만 원)**
  - **32" 매장·복지관 스탠드 풀패키지 (`Pro-Stand` / `Public-Care`)**: 약 **$663 USD (약 91.5만 원)**
- **총 개발 기간**: **4개월 (16주)**
  - **Phase 1 (1~4주차)**: 비전 rPPG/Iris + 3D Pose ROM/5xSTS + 음성 AI MVP
  - **Phase 2 (5~8주차)**: `AD5940` + `MAX86150` + `HX711` + `ADuM1250` 4층 절연 PCB 및 SUS316L 전극 금형
  - **Phase 3 (9~12주차)**: ECG-PPG PTT 혈압·위상각 보정, 약국 맞춤형 건기식 소분 RAG, 마이파크 앱 QR 연동
  - **Phase 4 (13~16주차)**: 주식회사 커넥트 단독 명의 KC인증·GS인증 1등급, 파일럿 실증 및 나라장터 1,980만 원 수의계약 등록
