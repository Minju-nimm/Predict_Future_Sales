# 🛒 Predict Future Sales
다년간의 시계열 데이터를 분석하여, 특정 월의 상품 판매량을 예측하는 강건한 모델을 만드는 프로젝트입니다. 기존 수상작들의 코드를 참조하여 데이터 분석의 수준을 높여 생략되거나 미비했던 EDA 과정과 스케일링, 이상치 제거 등의 부수적인 전처리 과정을 추가하고 앙상블 모델을 사용함으로써 분석의 품질을 높이고자 했습니다. 

👉🏻 Kaggle Predict Future Sales 경진 대회 링크는 [이 곳](https://www.kaggle.com/c/competitive-data-science-predict-future-sales)을 눌러주세요.


🔎 프로젝트의 자세한 내용을 알고싶다면? [포트폴리오](https://github.com/Minju-nimm/Predict_Future_Sales/blob/main/src/%EC%BA%90%EA%B8%80%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8_%EC%B5%9C%EC%A2%85_%ED%8F%AC%ED%8A%B8%ED%8F%B4%EB%A6%AC%EC%98%A4.pdf)를 참고하세요!

<br>
</br>


## :family: 팀원 소개
|     :camera: |  Member	|             R & R   	|
|:-----:	|:-----:|:-------------------------------------------------------:	|
|     <img src="https://user-images.githubusercontent.com/119478998/228486556-2aa892ef-467a-45e7-9d8d-8c1608061d08.png" width = 130> |  김민주 <br> [@Minju-nimm](https://github.com/Minju-nimm) 	|      데이터 전처리 및 시각화 <br> Github, Notion 관리 <br> 모델링	|
|   <img src="https://user-images.githubusercontent.com/119478998/228737598-796b1bd7-cb2e-4cb6-8836-ca89c32b8851.png" width = 100> 	|   김기준 <br> [@AppleKimkijun](https://github.com/AppleKimkijun) 	|  데이터 전처리 및 시각화 <br> 피쳐 엔지니어링 |
|      <img src="https://user-images.githubusercontent.com/119478998/230357145-bf7b0710-94b8-407b-b717-d0abcdc87b82.png" width = 150>  |  고준성 <br> [@KO-JUNSUNG](https://github.com/KO-JUNSUNG) 	|      모델링 <br> Github, Notion 관리 <br> 피쳐 엔지니어링	|
|   <img src="https://user-images.githubusercontent.com/119478998/230357125-816120d4-fa67-4c15-9194-4d0d2e0b0c2e.png" width = 140> 	|   이한재 <br> [@]() 	|  하이퍼 파라미터 튜닝 <br> 모델링	|

<br>
</br>


## 🔎 프로젝트에서 주목한 내용
### Log transformation
- 연속형 변수들에 대해서 분포를 확인, 정규성을 따르지 않는 변수들을 변환
- 예측모델을 적용할 때 통계적 이론을 바탕으로 구성, 예측모델은 데이터 분포가 정규분포를 따른다고 가정
- 데이터 분포를 안정화 시키기 위해서 보통 로그화나 정규화 방법을 이용

<img src = "https://user-images.githubusercontent.com/119478998/229987632-153e4bf9-4f1f-4c49-b0a2-ce4804fffd47.png" width="900" height="500" />

- item_price의 원래 분포형태는 정적 편포 형태
- 로그 변환을 시도한 결과 정규분포의 형태를 띄게 되었고, 왜도 절댓값도 크게 줄어 정규분포에 가깝다고 볼 수 있음
- item_cnt_day의 경우 로그 변환 전, 후로 그래프 형상에서는 큰 차이가 없어보였으나 왜도의 절댓값이 100에서 5로 크게 감소함

<br>
</br>

### Modeling
<img src = "https://user-images.githubusercontent.com/119478998/229986958-e272cef1-8d0e-48c0-9e58-38f21059f89a.png" width="900" height="400" />

<br>
</br>

- 스태킹/블렌딩 모델은 예측 변수 그룹의 예측을 집계해서, 최상의 개별 예측보다 더 나은 예측을 얻을 수 있는 원리로 작동
- 모델들의 장단점 및 예측 점수를 고려하여 스태킹을 최종 모델로 지정
<img src = "https://user-images.githubusercontent.com/119478998/229987466-582a203b-d9ff-4066-9ac0-71634ab6e499.png" width="900" height="400" />

<br>
</br>

### Hyper parameters tuning : Optuna Library
- 모델의 하이퍼 파라미터 튜닝으로 옵튜나 라이브러리를 사용
- 옵튜나 라이브러리는 하이퍼파라미터 튜닝에 쓰이는 최신 AutoML기법 중 하나
<img src = "https://user-images.githubusercontent.com/119478998/229986581-84dee780-0fa8-4a4c-b1d5-576252cbb684.png" width="900" height="350" />

<br>
</br>

### Conclusion
<img src = "https://user-images.githubusercontent.com/119478998/229986143-0d5521c8-d033-4b9f-af28-46e68a65e4ae.png" width="900" height="350" />

- 4번: quarter 변수를 추가하고, log 변환한 변수들을 추가한 경우 (1.24887로 좋지 못한 점수를 받음)
- Log 변환을 진행하면서 Feature를 많이 늘린 탓에 과적합 문제가 우려
- train data의 성능은 훌륭했으나 test data 예측 점수가 많이 낮아지는 문제 발생

<br>
</br>

## 📚 Reference
- https://www.kaggle.com/code/deinforcement/top-1-predict-future-sales-features-lightgbm
- https://www.kaggle.com/code/abubakar624/first-place-solution-kaggle-predict-future-sales/notebook
- https://www.kaggle.com/code/gordotron85/future-sales-xgboost-top-3/notebook
- https://medium.com/data-science-at-microsoft/introduction-to-feature-engineering-for-time-series-forecasting-620aa55fcab0
- https://www.kaggle.com/code/plarmuseau/forecast-log

<br>
</br>

---
해당 프로젝트는 멀티캠퍼스 데이터 분석 및 웹 개발자 13회차의 실전 분석 프로젝트 4조 '고민기재'가 기획하였습니다.
