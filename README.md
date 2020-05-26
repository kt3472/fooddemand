## Food Demand forecasting Challenge


* About : https://datahack.analyticsvidhya.com/contest/genpact-machine-learning-hackathon-1/#About)
* Data description : https://datahack.analyticsvidhya.com/contest/genpact-machine-learning-hackathon-1/#ProblemStatement
* Forecasting target : num_orders
* Evaluation : 100 * RMSLE ( root of mean squared logarithmic error )

## 1. Objects
* 향후 10주간(146주 ~ 155주)의 식자재 수요 예측
 
## 2. Data Exploration

## 3. Model
* 앙상블 그래디언트 알고리즘인 [LightGBM](https://lightgbm.readthedocs.io/en/latest/index.html) 사용
* 참고 : [Gredient Boost](https://en.wikipedia.org/wiki/Gradient_boosting), [Ensemble](https://tensorflow.blog/파이썬-머신러닝/2-3-6-결정-트리의-앙상블/)


## 4. Parameter Tunning / feature engineering

## 5. Result
* final score = 52.6740812166, 
* 1,344팀 / 112위, 상위 8%

