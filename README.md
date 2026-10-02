# docs

프로젝트 공통 설계, 개발환경, 인터페이스 명세와 통합 시연 문서를 관리합니다.

## 레포 구성

| 레포 | 범위 |
| --- | --- |
| [`simulation`](https://github.com/capston1-irion/simulation) | PX4·Gazebo, 상태 생성, 브리지, MAVLink 수집 |
| [`ai`](https://github.com/capston1-irion/ai) | 공통 전처리·평가, 이상탐지 모델 2종 |
| [`ui`](https://github.com/capston1-irion/ui) | 별도 상태 모니터링과 AI 결과 표시 |
| `docs` | 공통 명세, 설치/실행 가이드, 통합 시연 |

## 문서 디렉터리

| 경로 | 역할 |
| --- | --- |
| `architecture/` | 파트별 책임과 시스템 구조 |
| `interfaces/` | 데이터 입력·출력 계약 |
| `setup/` | 팀 공용 설치·실행 가이드 |
| `demo/` | 통합 시연과 검증 기록 |

## 현재 범위

시뮬레이션 기반 배터리와 모터/ESC 4개의 실시간 이상 의심 구간을 선별하고 대상 부품을 표시합니다. 실제 하드웨어, 기업 운영 시스템 연동과 RUL/SOH 예측은 필수 목표로 두지 않습니다.

현재 레포는 문서 작성용 기본 구조입니다. 수행계획서 원본, 개인정보가 있는 문서와 기업 로그는 복사하지 않았습니다. 계획·임시 인터페이스와 실제 검증 결과를 구분해 기록합니다.

협업 방법은 [CONTRIBUTING.md](CONTRIBUTING.md)를 참고하세요.
