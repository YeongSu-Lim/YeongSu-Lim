# 임영수 | Electronics Engineering

회로 해석·설계, 임베디드 제어, 디지털 시스템을 학습하고 구현해 왔습니다. 코드와 실험 근거를 바탕으로 설계 판단과 문제 해결 과정을 기록합니다.

## 대표 프로젝트

### 1. AI 기반 보행자 후방 안전 보조 스마트 백팩

후방 영상의 객체 탐지·추적과 TTC(Time-To-Collision) 추정으로 보행자의 접근 위험 인식을 보조하는 팀 프로젝트입니다.

- **구현:** Raspberry Pi 5 · Hailo · Python, Bounding Box 기반 TTC, 이동평균과 시간적 위험 판단
- **본인 기여:** 접근 판단 알고리즘 개선·반복 야외 검증·논문 제1저자. 카메라 흔들림과 객체 자세 변화의 영향을 분석해 판단 기준 개선
- **결과:** 과거 자체 시험에서 통제 영상 약 95% → 보행 환경 50% 이하 → 개선 후 야외 약 85%. 현재 코드·후속 버전의 성능 수치와는 구분

[저장소](https://github.com/YeongSu-Lim/Electronics-Engineering-Capstone-Design-1) · [알고리즘과 문제 해결](https://github.com/YeongSu-Lim/Electronics-Engineering-Capstone-Design-1/blob/main/docs/algorithm.md) · [버전별 구현](https://github.com/YeongSu-Lim/Electronics-Engineering-Capstone-Design-1/blob/main/docs/versions.md) · [검증 근거와 과제](https://github.com/YeongSu-Lim/Electronics-Engineering-Capstone-Design-1/blob/main/docs/validation.md)

### 2. S32K144 MCU 기반 교육용 차량 전장 시스템

주행 제어·조향·클러스터 표시를 하나의 MCU에서 연동하는 팀 프로젝트입니다.

- **구현:** Embedded C · ADC · FTM PWM · LPIT · FSM, 제어 10ms와 한 자리 표시 갱신 0.05ms의 타이머 채널 분리
- **본인 기여:** 클러스터·연료 경고등 직접 구현, 가속 제어 로직 개발과 시스템 통합 참여
- **설계·확인:** 기능별 갱신 주기를 분리하고 입출력·공유 변수 인터페이스를 점검. 코드에서 ADC→속도 상한→PWM과 표시·경고 조건 확인

주기는 코드 설정값이며, 보드 실측과 상태·출력 제어의 추가 검증 범위는 상세 문서에 구분했습니다.

[저장소](https://github.com/YeongSu-Lim/Microprocess-Design) · [클러스터 코드](https://github.com/YeongSu-Lim/Microprocess-Design/blob/main/seven_segment.c) · [가속·경고등 코드](https://github.com/YeongSu-Lim/Microprocess-Design/blob/main/motor.c) · [아키텍처·핀맵·FSM](https://github.com/YeongSu-Lim/Microprocess-Design/blob/main/docs/architecture.md) · [구현과 기여](https://github.com/YeongSu-Lim/Microprocess-Design/blob/main/docs/implementation.md) · [검증과 개선 과제](https://github.com/YeongSu-Lim/Microprocess-Design/blob/main/docs/validation.md)

### 3. Verilog 기반 Single-Cycle MIPS CPU

32비트 데이터 경로와 명령어 제어 구조를 구현한 논리회로설계 프로젝트입니다.

- **구현:** ALU·레지스터 파일·메모리·PC·제어부 연결, HI/LO 연산과 CP0 외부 예외 처리 경로
- **기술 경험:** 명령어 인출부터 연산·메모리 접근·기록까지 RTL 구조 분석. 세부 모듈별 개인 담당 범위는 보완 예정
- **확인 범위:** 소스 구조 확인. 시뮬레이션 재현 조건과 미확보 증빙은 저장소에 정리

[저장소와 기술 설명](https://github.com/YeongSu-Lim/Logic-Circuit-Design) · [데이터 경로 통합 RTL](https://github.com/YeongSu-Lim/Logic-Circuit-Design/blob/main/TOP.v) · [시뮬레이션 준비와 검증 범위](https://github.com/YeongSu-Lim/Logic-Circuit-Design/blob/main/README.md)

## 기술 경험

| 분야 | 경험 |
| --- | --- |
| 회로 해석·설계 | GPDK045 BGR의 PVT Corner·Headroom·PSRR 분석, OrCAD PSpice 회로 시뮬레이션 |
| 임베디드·제어 | C, S32K144, GPIO ISR, ADC, FTM PWM, LPIT, FSM, 기능 통합 |
| 디지털·반도체 기초 | Verilog 데이터 경로·제어 로직, MOS 소자 동작점과 공정 Corner 검토 |
| 실환경 데이터 분석 | Python, 객체 크기 기반 TTC, 이동평균·시간적 조건, 반복 야외 검증 |
| 회로 실험 | 전자공학실험 수업에서 오실로스코프 측정·보고서 작성 |

팀 전체 구현과 개인 기여, 코드 분석과 실제 측정 결과를 구분해 기록합니다.

## 학술 활동

2026년 한국정보기술학회 하계종합학술대회 대학생 논문경진대회 **우수논문상(동상)** · 논문 **제1저자**  
「AI 기반 보행자 후방 안전 보조 스마트 백팩 개발」 — 공개 증빙 및 시험 근거는 [검증 문서](https://github.com/YeongSu-Lim/Electronics-Engineering-Capstone-Design-1/blob/main/docs/validation.md)에 구분합니다.
