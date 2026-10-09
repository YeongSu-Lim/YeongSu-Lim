# 임영수 | Electronics Engineering

회로 해석·설계, 임베디드 제어, 디지털 시스템과 실환경 데이터 기반 문제 해결을 학습하고 구현해 왔습니다. 프로젝트의 목적, 본인 기여, 구현 범위와 검증 근거를 함께 기록합니다.

## 대표 프로젝트

### 1. AI 기반 보행자 후방 안전 보조 스마트 백팩

- **목적:** 후방 영상으로 접근 위험을 판단해 보행자의 상황 인식을 보조
- **본인 기여:** 접근 위험 판단 알고리즘 개선, 반복 야외 검증, 논문 제1저자
- **핵심 구현:** Raspberry Pi 5 · Hailo · Python, 객체 탐지·추적, Bounding Box 기반 TTC와 시간적 위험 판단
- **검증 결과:** 과거 자체 시험에서 통제 영상 약 95% → 보행 환경 50% 이하 → 개선 후 야외 약 85%. 현재 main·후속 업데이트의 성능 수치와는 구분

[저장소](https://github.com/YeongSu-Lim/Electronics-Engineering-Capstone-Design-1) · [TTC와 위험 판단](https://github.com/YeongSu-Lim/Electronics-Engineering-Capstone-Design-1/blob/3017b829014eaac35913cbde5793ea1bd3dc2542/docs/algorithm.md) · [검증 근거](https://github.com/YeongSu-Lim/Electronics-Engineering-Capstone-Design-1/blob/3017b829014eaac35913cbde5793ea1bd3dc2542/docs/validation.md) · [버전별 범위](https://github.com/YeongSu-Lim/Electronics-Engineering-Capstone-Design-1/blob/3017b829014eaac35913cbde5793ea1bd3dc2542/docs/versions.md)

상세 문서는 [Draft PR #1](https://github.com/YeongSu-Lim/Electronics-Engineering-Capstone-Design-1/pull/1)의 고정 커밋에 연결되어 있으며, 아직 main에 병합되지 않았습니다. 현재 main의 객체별 화면·콘솔 경고와 후속 자료의 주요 대상 선정·영상/CSV 기록·BLE용 공유 파일 구현을 구분합니다.

### 2. S32K144 기반 교육용 차량 전장 제어 시스템

- **목적:** 주행 제어·조향·클러스터 표시를 하나의 MCU에서 연동
- **본인 기여:** 클러스터·연료 경고등 직접 구현, 이후 가속 제어 로직 개발·시스템 통합 참여
- **핵심 구현:** Embedded C · GPIO · ADC · PWM · LPIT, 제어/표시 주기 분리와 FSM 기반 상태 제어
- **검증 범위:** 소스에서 주변장치 연결·호출 순서·표시/경고 조건 확인. 보드 실측 기록은 보완 필요

속도·거리·연료 경고는 교육용 모사이고, 상용 차량이나 전력 구동 회로 설계 경험을 뜻하지 않습니다.

[저장소](https://github.com/YeongSu-Lim/Microprocess-Design) · [클러스터 코드](https://github.com/YeongSu-Lim/Microprocess-Design/blob/main/seven_segment.c) · [가속·경고등 코드](https://github.com/YeongSu-Lim/Microprocess-Design/blob/main/motor.c) · [주기·핀맵·FSM](https://github.com/YeongSu-Lim/Microprocess-Design/blob/88e1d1b408318fcafbe39d3dd402ccfeee10a7d0/docs/architecture.md) · [검증과 한계](https://github.com/YeongSu-Lim/Microprocess-Design/blob/88e1d1b408318fcafbe39d3dd402ccfeee10a7d0/docs/validation.md)

상세 문서는 [Draft PR #1](https://github.com/YeongSu-Lim/Microprocess-Design/pull/1)의 고정 커밋에 연결되어 있으며, 아직 main에 병합되지 않았습니다.

### 3. Verilog 기반 Single-Cycle MIPS CPU

- **목적:** 명령어 실행을 위한 32비트 데이터 경로와 제어 구조 학습·구현
- **기여 범위:** 논리회로설계 프로젝트 경험. 세부 모듈별 본인 담당 범위는 보완 중
- **핵심 구현:** Verilog, ALU·레지스터 파일·메모리·PC·제어부, HI/LO 및 외부 예외 처리 경로
- **검증 범위:** RTL 구조 확인. 테스트벤치·명령어 메모리 파일·검증 로그가 없어 시뮬레이션 재현과 FPGA 성능 검증은 보완 필요

[저장소와 기술 설명](https://github.com/YeongSu-Lim/Logic-Circuit-Design) · [데이터 경로 통합 RTL](https://github.com/YeongSu-Lim/Logic-Circuit-Design/blob/main/TOP.v)

## 기술 경험

| 분야 | 경험 |
| --- | --- |
| 회로 해석·설계 | GPDK045 BGR, PVT Corner·Headroom·PSRR 분석 / OrCAD PSpice 회로 시뮬레이션 |
| 임베디드·제어 | C, S32K144, GPIO ISR, ADC, FTM PWM, LPIT, FSM, 기능 통합 |
| 디지털·반도체 설계 기초 | Verilog 데이터 경로·제어 로직, MOS 소자 동작점과 공정 Corner 검토 |
| 실환경 데이터 분석 | Python, 객체 크기 기반 TTC, 이동평균·시간적 조건, 반복 야외 검증 |
| 회로 실험 | 전자공학실험 수업에서 오실로스코프를 이용한 측정·보고서 작성 |

기술 목록은 프로젝트와 수업 경험을 나타내며, 모든 모듈의 단독 개발이나 산업 수준의 검증 완료를 뜻하지 않습니다. 팀 전체 결과와 개인 기여는 구분해 설명합니다.

## 학술 활동

2026년 한국정보기술학회 하계종합학술대회 대학생 논문경진대회 **우수논문상(동상)** · 논문 **제1저자**. 공개 가능한 논문·수상 증빙 링크는 보완 예정입니다. 수상 이력과 위험 판별 정확도의 시험 근거는 별도로 관리합니다.

## 추가 기술 문서 준비

**GPDK045 BGR 회로설계:** 기존 보고서의 설계 판단과 시뮬레이션 결과를 정리하고 있습니다. 자료의 공개 범위를 확인한 뒤 독립 저장소와 상세 문서를 연결할 예정입니다.

<!-- 링크 유지보수
스마트 백팩의 상세 문서 3개는 Draft PR #1의 검토 커밋에 고정한다.
PR 병합 및 대상 파일의 main 존재를 확인한 뒤 아래 경로에서만 ref를 변경한다.
저장소: YeongSu-Lim/Electronics-Engineering-Capstone-Design-1
변경 전: blob/3017b829014eaac35913cbde5793ea1bd3dc2542/
변경 후: blob/main/
대상: docs/algorithm.md, docs/validation.md, docs/versions.md
병합 확인 후 본문의 Draft PR 및 미병합 안내도 갱신한다.
Microprocess-Design의 docs/architecture.md와 docs/validation.md는 검토 커밋 88e1d1b408318fcafbe39d3dd402ccfeee10a7d0에 연결되어 있다.
MCU 문서 PR도 병합 전에는 검토 커밋 링크, 병합과 파일 존재 확인 후에는 main 링크를 사용한다.
BGR 저장소는 별도 생성 승인과 자료 공개 범위 확인 후에만 연결한다.
-->
