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
   (몇 차례 vscode를 사용하여 로컬에서 진행하고 결과를 확인하긴 했으나, 개선이 잘 되지 않았음. 이후 더 해볼 예정. 이때 사용한 코드를 업로드 하고 싶었으나 노트북 이상으로 백업 후 포멧 하는 과정에서 소실됨.)
---
### 과정
 + **데이터 수집**
   + Roboflow에서 다운받은 데이터셋을 구글드라이브에 마운트하여 사용함.
 + **모델링**
   + Yolov5 모델을 공식페이지에서 클론하여 불러옴.
   + 모델에 적용할 데이터셋의 경로 파일인 yaml 파일을 확인하고 학습데이터와 검증데이터를 변수로 정의.
   + 데이터 이미지 경로를 txt 파일로 저장하여 yaml 파일에 새롭게 정의하여 입력할 데이터셋의 세팅을 진행.
   + 사전학습 모델 Yolov5s를 사전학습모델로 사용하여 위에서 세팅한 yaml 파일로 모델 학습을 실시함.
 + **테스트 결과**
   + 모델학습 이후 테스트 데이터를 사용하는 과정에서 커스텀 설정할 수 있는 결과값을 세팅하여 탐지된 부분을 크롭하여 새롭게 폴더에 저장할 수 있도록 하여 데이터를 크롬과 논크롭 두가지로 확인할 수 있도록 함.
   + 거의 모든 데이터에 대해서 번호판 탐지를 성공하였고, 이후 easyOCR 라이브러리를 활용하여 크롭된 이미지에 대해서 인식을 시도했으나 제대로 인식하지 못함.
---
### 사용한 프로그래밍 언어 및 라이브러리
<img src="https://img.shields.io/badge/Python-yellow?style=flat"/> <img src="https://img.shields.io/badge/Yolov5-red?style=flat"/> <img src="https://img.shields.io/badge/cv2-blue?style=flat"/> <img src="https://img.shields.io/badge/easyOCR-lightgrey?style=flat"/> <img src="https://img.shields.io/badge/matplotlib-orange?style=flat"/>

---
### 데이터 정보 및 참고 사이트
 - **데이터**
   - Dataset : Korea Car Plate in roboflow.com(https://universe.roboflow.com/mmu-bkusm/-emfmu)
 - **참고 사이트**
   - Yolov5 : https://github.com/ultralytics/yolov5
