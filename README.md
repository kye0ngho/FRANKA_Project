# FRANKA_Project
FRANKA

## VLA 로봇 제어 
```bash
# Robot : FRANKA
# Vision : YOLO
# Language : ?? 미정 , pi 0 , Octo 등 선택지 다수
# 현재 컴퓨터 스펙 : RTX 3050 하지만 4090 노트북 사용해서 돌릴예정
# Ros : Jazzy
```

```bash

#카메라 디바이스 번호부터 확인하기

ls -h /dev/video*

# 주의 진짜 카메라랑 무슨 메타 뭐시기 있는데 메타 뭐시기는 오류뜸
```



### 우선 Yolo 
```bash

#카메라 노드 불러오기
source /opt/ros/jazzy/setup.bash
ros2 run usb_cam usb_cam_node_exe --ros-args -p video_device:="/dev/video2"

# 미리 만들어둔 노드간 퍼블리시 ~ 해서 카메라와 통신
python yolo_test.py

# 시각화
source /opt/ros/jazzy/setup.bash
ros2 run rqt_image_view rqt_image_view

# 각각 다 다른 터미널에서 실행 및 Ros 는 가상환경 x 터미널로 실행

```

## 결과 사진

<img width="1166" height="867" alt="image" src="https://github.com/user-attachments/assets/c9121ac0-b05d-41b2-8ee2-6ee8e537dab4" />


