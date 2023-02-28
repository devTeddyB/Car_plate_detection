# Car Plate Detection and Recognition
Automatic License Plate Recognition(ALPR)
---
## 자동차 번호판 탐지 및 인식
### 설명
 - Computer Vision 과 Yolov5 모델을 학습하기 위한 목적으로, 자동차의 번호판을 탐지하고 번호를 인식하고 보여주기까지 진행하고자 함.
 - Roboflow 에서 제공되는 한국 자동차 데이터셋을 사용하였고, 데이터는 라벨링이 되어있는 상태.
 - 객체탐지에서 뛰어난 성능을 보이는 Yolov5의 s모델을 사전학습모델로 사용하여 진행하였음.
 - 번호판 탐지에는 잘 하나, 번호판을 크롭한 이후 이미지 화질 등의 이유로 번호를 인식하는 부분에서는 제대로 나타내지 못하는 결과를 보임.
 - 크롭한 번호판 이미지에 대하여 이미지 프로세싱을 통해 화질을 개선하고 기법들을 적용하여 숫자와 관련한 부분만 특징추출을 통해 인식할 수 있도록 시도해볼 예정.
---
### 과정
 + **데이터 수집**
 Roboflow에서 다운받은 데이터셋을 구글드라이브에 마운트하여 사용함.
 - 









## Dataset : Korea Car Plate in roboflow.com
#### https://universe.roboflow.com/mmu-bkusm/-emfmu
