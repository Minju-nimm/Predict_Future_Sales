# 🛒 Predict_Future_Sales
다년간의 시계열 데이터를 분석하여, 특정 월의 상품 판매량을 예측하는 강건한 모델을 만드는 프로젝트입니다. 기존 수상작들의 코드를 참조하여 데이터 분석의 수준을 높여 생략되거나 미비했던 EDA 과정과 스케일링, 이상치 제거 등의 부수적인 전처리 과정을 추가하고 앙상블 모델을 사용함으로써 분석의 품질을 높이고자 했습니다. 

👉🏻 Kaggle Predict Future Sales 경진 대회 링크는 [이 곳](https://www.kaggle.com/c/competitive-data-science-predict-future-sales)을 눌러주세요.


🔎 프로젝트의 자세한 내용을 알고싶다면? [포트폴리오](링크)를 참고하세요!

<br>
</br>


## :family: 팀원 소개
|     :camera: |  Member	|             R & R   	|
|:-----:	|:-----:|:-------------------------------------------------------:	|
|     <img src="https://user-images.githubusercontent.com/119478998/228486556-2aa892ef-467a-45e7-9d8d-8c1608061d08.png" width = 130> |  김민주 <br> [@Minju-nimm](https://github.com/Minju-nimm) 	|      데이터 전처리 및 시각화 <br> Github, Notion 관리 <br> 모델링	|
|   <img src="https://user-images.githubusercontent.com/119478998/228737598-796b1bd7-cb2e-4cb6-8836-ca89c32b8851.png" width = 100> 	|   김기준 <br> [@AppleKimkijun](https://github.com/AppleKimkijun) 	|  데이터 전처리 및 시각화 <br> 피쳐 엔지니어링 |
|      <img src="https://user-images.githubusercontent.com/119478998/228737598-796b1bd7-cb2e-4cb6-8836-ca89c32b8851.png" width = 100>  |  고준성 <br> [@KO-JUNSUNG](https://github.com/KO-JUNSUNG) 	|      모델링 <br> Github, Notion 관리 <br> 피쳐 엔지니어링	|
|   <img src="https://user-images.githubusercontent.com/119478998/228737598-796b1bd7-cb2e-4cb6-8836-ca89c32b8851.png" width = 100> 	|   이한재 <br> [@]() 	|  하이퍼 파라미터 튜닝 <br> 모델링	|

<br>
</br>


## :computer: Installation

```bash
pip install -r requirements.txt
```
<br>
</br>

<div align="center">

![Pytorch](https://img.shields.io/badge/Pytorch-v1.13.1-orange?logo=Pytorch&style=plastic)
![NodeJS](https://img.shields.io/badge/Node.js-v18.14.2-339933?logo=node.js&style=plastic)
![react](https://img.shields.io/badge/react-v18.2.0-61dafb?logo=React&style=plastic)
![javascript](https://img.shields.io/badge/javascript-ES6-yellow?logo=javascript&style=plastic)

![Deepspeed](https://img.shields.io/badge/Deepspeed-v0.8.2+4ae3a3da-blue?logo=Deepspeed&style=plastic)
![Transformer](https://img.shields.io/badge/Transformer-v4.27.2-green?logo=Transformer&style=plastic)
![fastai](https://img.shields.io/badge/fastai-v2.7.11-orange?logo=fastai&style=plastic)

</div>

<br>
</br>

## 🔎 프로젝트에서 주목한 내용
### Log transformation
<img src = "https://user-images.githubusercontent.com/119478998/229987632-153e4bf9-4f1f-4c49-b0a2-ce4804fffd47.png" width="900" height="400" />

<br>
</br>

### Modeling
<img src = "https://user-images.githubusercontent.com/119478998/229986958-e272cef1-8d0e-48c0-9e58-38f21059f89a.png" width="900" height="400" />

<br>
</br>

- 스태킹/블렌딩 모델은 예측 변수 그룹의 예측을 집계해서, 최상의 개별 예측보다 더 나은 예측을 얻을 수 있는 원리로 작동
<img src = "https://user-images.githubusercontent.com/119478998/229987466-582a203b-d9ff-4066-9ac0-71634ab6e499.png" width="900" height="400" />

<br>
</br>

### Hyper parameters tuning : Optuna Library
<img src = "https://user-images.githubusercontent.com/119478998/229986581-84dee780-0fa8-4a4c-b1d5-576252cbb684.png" width="900" height="350" />

<br>
</br>

### Conclusion
<img src = "https://user-images.githubusercontent.com/119478998/229986143-0d5521c8-d033-4b9f-af28-46e68a65e4ae.png" width="900" height="400" />

<br>
</br>

## 📚 Reference
- https://www.kaggle.com/code/deinforcement/top-1-predict-future-sales-features-lightgbm
- https://www.kaggle.com/code/gordotron85/future-sales-xgboost-top-3/notebook

<br>
</br>

---
해당 프로젝트는 멀티캠퍼스 데이터 분석 및 웹 개발자 13회차의 실전 분석 프로젝트 4조 '고민기재'가 함께 기획하였습니다.
