# AME 자율주행 해커톤 대회
* 일시: 2025년 7월 9일(수) - 7월 11일(금)
* 장소: 서울 강남구 영동대로 513 3층 코엑스 C 홀
---
## 대회 참가 인원
* 주경호 / 2002.11.28 / 전산전자공학부 / 010-8723-5001 / 
* 이수민 / 2002.09.12 / 전자공학심화 / 010-2103-9076
* 최승원 / 2003.07.23 / 전산전자공학부 / 010-3258-4385
---
## 자율주행 대회 개요

* 주요 내용: 실제 코딩 기반으로 2팀이 동시에 출발하여 결승선을 먼저 통과
* 차량 조건: 자이트론 실습용 자율주행 모형차량 C모델

| 구분 | 세부내용 | 비고 |
| :------------: | :------------------------------: | :------------: |
| 프레임 | 1/12 크기 자동차 차체 프레임 (LWH 47*20*17cm) | - |
| SW | 리눅스 / ROS / 파이썬 프로그래밍 | - |
| 프로세서 모듈 | 라즈베리파이 4B 4G / RAM 4GB / SD카드 64GB | - |
| 센서 | IMU 관성센서, 카메라, 초음파센서, 무선랜 등 | - |

* 예선 트랙
<img src="image/track.png" width="600" height ="300">

***
## OS & Tool & Device
[![Linux](https://img.shields.io/badge/-Linux-FCC624?logo=Linux&style=flat-square&logoColor=black)](https://www.kernel.org)
[![Ros](https://img.shields.io/badge/-ROS-22314E?logo=Ros&style=flat-square&logoColor=white)](https://www.ros.org)
[![Ubuntu](https://img.shields.io/badge/-Ubuntu-E95420?logo=Ubuntu&style=flat-square&logoColor=white)](https://ubuntu.com)
[![Arduino](https://img.shields.io/badge/Arduino-00878F?logo=arduino&style=flat-square&logoColor=fff&style=plastic)](https://www.arduino.cc)
[![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=Python&logoColor=white)](https://www.python.org)
[![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)](http://pytorch.org)
[![RaspberryPi](https://img.shields.io/badge/-RaspberryPi-C51A4A?style=flat-square&logo=Raspberry-Pi)](https://www.raspberrypi.com)

* OS
>* Linux: 1991년 개발된 Unix 기반 오픈소스 운영체제로 Kernel과 SW 패키지로 구성되며, 현재 다양한 장치에서 사용되고 있다.
* Tool
>* ROS: 로봇 개발을 위해 tools, libraries 등을 제공하는 오픈소스 플랫폼이다.
>* Arduino: MCU 기반으로 만들어진 보드 및 오픈 소스 개발 환경(IDE)이다.
>* Ubuntu: Debian 기반의 오픈 소스 Linux 운영체제의 한 종류이다.
>* Python: 쉬운 문법,인터프리터, 객체지향, 다양한 라이브러리, 등의 특징으로 가장 맣이 사용되는 프로그래밍 언어 중 하나이다.
>* PyTorch: 파이썬 기반 오픈소스 딥러닝 프레임 워크로 컴퓨터 비전, 자연어 처리 등 다양한 인공지능 분야에서 활용되고 있다.
* Device
>* Raspberry:  리눅스 커널 기반의 개발이 가능한 보드로 임베디드, IoT 분야에서 사용된다.
>* IMU Sensor: 물체의 움직임, 기울기, 회전, 방향 등을 실시간으로 측정하여 파악하는 센서이다.
>* Ultrasound Sensor: 초음파를 이용하여 물체와의 거리를 측정하는 센서이다.
---
## 프로젝트 

**서론**
> 최근 자율주행 기술이 발전 되면서 자동차 산업에 새로운 혁신 적인 기술로 각광 받고 있다. 자율주행 기술은 인간의 개입 없이 외부 환경을 스스로 인식하고, 판단하여 원하는 목적지로 운송해주는 기술을 의미한다. 현재 자율주행은 총 0-5로 총 6단계로 구성되며 비자동화, 운전자 보조, 부분 자동화, 조건부 자동화, 고도 자동화, 완전 자동화에 해당하며 우리고 목표하는 것은 운전자의 개입이 없는 완전 자동화이다. 하지만 실제로 자율주행이 상용화 되는 부분에서 하드웨어 기술 부족과 소프트웨어 문제 등으로 인하여 구현에 어려움을 겪고 있으며, 안정적으로 운행 가능한 자율주행 시스템을 구현하는 것이 현재 우리의 핵심 과제이다.
AME 자율주행 대회에 참여하여 AI를 적용한 알고리즘과 IMU센서 및 초음파 센서 등을 활용하여 자율 주행 시스템을 구현하고자 한다. 핵심 목표로 신호등 인식 및 출발, 라바콘 주행, 차선 유지, 결승선 통과 총 4단계를 Linux 기반 오픈 소프트웨어 ROS 기반으로 안정적으로 자율주행 시스템을 구현하여, 자율주행 시스템의 근본적인 문제 해결에 다가서고자 한다.

**본론**
> 본 프로젝트에서 신호등 인식 출발,라바콘 주행, 차선 주행, 결승선 통과 4가지의 목표를 해결하기 위하여 ROS2 기반의 Python,PyTorch, OpenCV 등의 오픈소스를 적용하여  실시간 데이터 처리, 영상 분석을 딥러닝 기반으로 센서와 통신 가능한 자율주행 시스템을 구현하고자 한다.

설계를 위한 전반적인 방향은 카메라에 실시간으로 수신되는 영상 을 분석하여 차량이 실시간으로 전송되는 정보들을 ROS2 인터페이스에서 특정한 토픽을 구독하는 노드를 생성하고, OpenCV로 이미지를 변환하여 PyTorch에서 학습된 결과를 이용하여 다양한 기술들이 유기적으로 통합되어 정확성과 반응성을 충족하는 자율주행 시스템을 설계하고자 한다.
**결론**
> 본 프로젝트는 ROS2 기반을 바탕으로, 실시간으로 외부 환경을 인식한 정보를 통해 주행을 제어할 수 있는 자율주행 시스템을 구현하는 데 중점을 두었다. 신호등 인식, 라바콘 회피, 차선 유지, 결승선 통과라는 4가지 핵심 과제를 중심으로 카메라에서 획득한 영상 정보를 OpenCV로 처리하고, PyTorch 기반의 딥러닝 모델을 활용하여 정보를 처리를 수행한다.

결론적으로, 자이카를 이용하여 다양한 환경에서 유연하게 적응 및 안정적인 주행이 가능한 자율주행 시스템으로 자율주행 산업의 기술 바전에 기여하고자 한다.


---

