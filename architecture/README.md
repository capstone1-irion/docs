# 시스템 구조

| 구간 | 책임과 경로 |
| --- | --- |
| 기본 비행제어 | 기존 PX4–Gazebo 경로 유지 |
| 모터 상태 | Custom Motor Plugin → Gazebo Transport → 별도 PX4 Motor Bridge → uORB `esc_status` → PX4 MAVLink |
| 배터리 상태 | 모터 부하 → Custom Battery Plugin → 외부 `BATTERY_STATUS` → PX4 외부 배터리 입력 → uORB `battery_status` → PX4 MAVLink |
| 분석·표시 | MAVLink 수집·시간정렬 → AI 추론 → 이상 시간/구간·대상 부품 → UI |

위 표는 구현 계획입니다. 실제 메시지·필드 지원은 선택한 버전과 실행 결과로 검증합니다. 기존 비행제어를 우회하거나 Gazebo 내부 고장 플래그를 모델 입력으로 전달하지 않습니다.
