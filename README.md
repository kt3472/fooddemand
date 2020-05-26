# Food Demand forecasting Challenge


* About : https://datahack.analyticsvidhya.com/contest/genpact-machine-learning-hackathon-1/#About)
* Data description : https://datahack.analyticsvidhya.com/contest/genpact-machine-learning-hackathon-1/#ProblemStatement
* Forecasting target : num_orders
* Evaluation : 100 * RMSLE ( root of mean squared logarithmic error )

## 1. Objects
* 향후 10주간(146주 ~ 155주)의 식자재 수요 예측
 
## 2. Data Exploration & Preprocessing
* Data set : 1주 ~ 145주 동안의 식자재 주문 데이터(가격, 식자재아이디 등 9개 피쳐), 풀필먼트 정보데이터(지역코드, 센터코드 등 5개 피쳐), 식자재 정보데이터(식자재종류, 요리법 등 3개 피쳐)등 총 3개 Data set
* 결측치는 없으며, center_id, meal_id를 기준으로 3개 Data set을 Merge

## 3. Model
* Ensemble & Gredient 알고리즘인 [LightGBM](https://lightgbm.readthedocs.io/en/latest/index.html) 모델 사용
* 참고 : [Gredient Boost](https://en.wikipedia.org/wiki/Gradient_boosting), [Ensemble](https://tensorflow.blog/파이썬-머신러닝/2-3-6-결정-트리의-앙상블/)


## 4. Parameter Tunning / feature engineering
* 할인율, 할인율구간, 프로모션합계, sin-cos transform 등 생성   
* Grid search 를 통해 최적의 파라미터를 산출({'colsample_bytree': 0.4, 'min_child_samples': 5, 'num_leaves': 127'}

## 5. Results
* final score = 52.6740812166, 
* 2020/05/25 기준 1,344팀 / 112위, 상위 8%

