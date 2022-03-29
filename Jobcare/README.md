# Dacon 잡케어 추천 알고리즘 대회


📌 소개
--
주어진 정형 데이터를 기반으로 개인별 맞춤형 컨텐츠 추천 모델링


🗓 개발기간
--
2022년 01월 03일 ~ 2022년 01월 17일 (14일)


🛠 프로젝트 사용기술
--
* Python3
* PyTorch
* Pandas
* Numpy
* Tabnet
* Scrapy
* Matplotlib
* Seaborn
* Google Colab



💡 프로젝트에서 진행한 내용
--
* Pandas, Matplotlib, Numpy를 활용해서 주어진 데이터를 EDA를 통해 2,3월에 컨텐츠열람한 횟수가 가장 많아서 채용시기와 겹친다고 판단함
* 전체적으로 어느 달에 몰리는 경향은 없는 것으로 보이고 주로 컨텐츠 열람 일자로는 6,13,20일이 많이 나타내고 있고 31일에는 다른 일자에 비해 많이 하락하는 경향이 보임
* LogisticRegression, RandomForestClassifier, BaggingClassifier등 3개의 모델을 Hard Voting으로 활용해서 0.6437으로 성능 개선
* 정형 데이터이기 때문에 적합한 딥러닝 모델이라고 생각하여 Job4파일을 PyTorch로 Tabnet을 적용해서 0.6202의 성능인 Baseline에서 0.6391으로 성능 개선했지만 HardVoting으로 작업한 성능보다 낮음


💡 자체 평가 및 보완 
--
* 다양한 모델의 결과를 비교해서 가장 많은 표를 얻는 클래스를 최종 예측값으로 정하는 Hard Voting 방식으로 적용해서 성능을 개선했지만 뚜렷하게 성능개선이 되지 않아서 아쉬운 경험이였습니다.
* Feature의 전처리 없이 raw한 데이터를 입력을 사용하고 Gradient Descent기반 최적화를 사용하여 End-to-End Learning을 가능하게하는 TabNet을 알게 되어 정형데이터에 접근하는 방법하나 알게 되었습니다.
