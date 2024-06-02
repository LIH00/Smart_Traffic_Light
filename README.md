# Smart_Traffic_Light


## 환경설정

* [YOLOv8](https://github.com/ultralytics/ultralytics/blob/main/README.md)

Members
| Name           | Role |
|-------------------------------|---------------------------|
| 이인혁 | Project Member, 프로젝트를 총괄하고 망하면 책임진다. |
| 김용기 | Project Member, 마일스톤을 생성하고 프로젝트 이슈 진행상황을 관리한다. |

| Project Github | https://github.com/LIH00/Smart_Traffic_Light/edit/main/README.md |

# Project: 교통량에 따른 신호등 주기 조절

* OpenCV와 YOLO를 사용해 차량검출 후 교통량에 따른 신호 조절 
  
  
## High Level Design

flow chart:

```mermaid
flowchart TD
     A[카메라 또는 비디오 소스]  -->  B[객체 감지 및 분류: 차량 디텍션]
     B[객체 감지 및 분류: 차량 디텍션] --> C[신호 제어 알고리즘 및 시스템: 일정 차량 디텍션 시 신호 조절]
     C[신호 제어 알고리즘 및 시스템: 일정 차량 디텍션 시 신호 조절] -->  D[신호 제어 시스템 :신호 조절]
```     
-------------------

1. 카메라 또는 비디오 소스:

 
     -카메라나 비디오 소스로부터 영상을 획득합니다.

   
2. 객체 감지 및 분류:

 
     -객체 감지 및 분류 모델(YOLO 등)을 사용하여 차량을 디텍트합니다.

   
3. 신호 제어 알고리즘 및 시스템:


     -일정 수의 차량이 감지되면, 신호를 제어하기 위한 알고리즘과 시스템이 활성화됩니다.
   
     -알고리즘은 차량 수에 따라 신호등의 신호 주기를 늘리거나 줄이는 방식으로 실행합니다.

  
4. 신호 제어 시스템:

     -일정수의 차량이 감지되면 신호의 주기를 증가시키거나, 교통량이 줄어드는 경우에는 정상적인 실행을 위해 신호를 조절합니다.
   
## Clone code

* repository에 대한 code clone 방법

```shell
git clone https://github.com/LIH00/protectPJ.git
```

## Prerequite

* 프로잭트를 실행하기 위해 필요한 dependencies 및 configuration 설치 및 설정 방법

```shell
python -m venv .env
source .env/bin/activate
pip install -r requirements.txt
```

## Steps to build

* 프로젝트를 실행을 위해 빌드 절차 기술

```shell
cd ~/openvino_notebooks
source .env/bin/activate

git clone https://github.com/ultralytics/ultralytics.git
pip install yolov8
yolo predict

```

## Steps to run

* 프로젝트 실행방법에 대해서 기술
* project 폴더 다운로드
* .pt 모델 경로 설정 후 실행

```shell
model1 = YOLO('best.pt')

```


## Output

* 프로젝트 실행 화면    
  
![Alt text](sample.png)



## Appendix

* 참고 자료 및 알아두어야할 사항들 기술
  
* [OpenCV](https://github.com/opencv/opencv)
