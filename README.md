# px4gcs
PX4-KETI gcs

## PX4 implemented KETI GCS
This is an instruction for using KETI GCS + nCube_MUV + PX4 (+ Gazebo).

## 1. mode
**PX4**:manual-acro-offboard-stabilized-rattitude-altctl-posctl-auto:mission-auto:loiter-auto:rtl-auto:takeoff-auto:land-auto:precland

**Ardupilot**: stabilized-guided-poshold-auto-althold ~~~~

PX4의 경우, takeoff 명령 이후 hold (mavros에서는 AUTO:LOITER) 모드로 넘어감
goto의 경우, 쭉 hold 모드 유지
선회비행의 경우, Orbit (mavros에서는 POSCTL) 모드로 동작
리턴홈의 경우, Return (mavros에서는 AUTO.RTL) 모드로 동작


## 2. UDP
PX4는 자체적으로 UDP 포트 하나만 GCS용으로 열어놓은듯?
현재 nCube와의 통신은 **PORT1=14550**, **PORT2=18570** 으로 세팅
QGC,custom GCS 동시에 데이터 받을 수 있는지 테스트가 더 필요함


