# mini-project-02
### 🏐 Machine Learning : 배구 승부 예측
* 🏆 목표 : 한국배구연맹 데이터를 활용하여 경기 결과 예측하는 머신러닝 모델 구축
* 📂 사용 데이터
  * 셀레니움을 활용하여 한국배구연맹 포털 [KOVO](https://www.kovo.co.kr/game/v-league/11141_game-summary.asp?season=017&g_part=201&r_round=1&g_num=2&) 경기 결과 크롤링
* 🗓 기간 : 2022-04-19 ~ 2022-04-20
* 👩‍💻 인원 : 5명(김한결 박서영 임민정 정유정 최유연) | [협업 툴 노션 사용](https://imdona.notion.site/mini-project-2-ML-0cde262f1c7e4342be54ab16a2f1b39b)

#### 1. 데이터 전처리·분석
* 현역 배구 선수님 인터뷰를 통한 도메인 이해
* 인터뷰 결과와 배구 승률 관련 논문 내용을 기반으로 데이터셋 추출
  - 참고 논문
    - [남자 프로 배구 경기 기록이 V-리그 시즌 승률에 미치는 영향](https://www.kci.go.kr/kciportal/ci/sereArticleSearch/ciSereArtiView.kci?sereArticleSearchBean.artiId=ART002440361)
    - [남자 프로배구 경기력 변인 분석에 관한 연구](https://m.earticle.net/Article/A362822)
* Feature Engineering
  - 선수 개인이 아닌 팀별 역량을 고려하기 위해 경기와 팀명을 기준으로 피쳐 생성 : 범실, 공격, 블로킹, 디그, 리시브
  - MVP : key player 참석 여부를 0과 1로 나타내는 피쳐 생성
    - 선정 기준 : 팀 내에서 득점이 가장 높은 선수

#### 2. 모델링
* 평가 지표 선정 : 분류(classification)의 평가 지표 중 정확도(Accuracy)로 선정
  - 선정 이유❓
    - 암 판단이나 스팸메일 분류처럼 승·패의 중요성의 차이가 없어 Recall(재현율) 이나 precision(정밀도)의 의미가 없음
    - 실제 사례 참고
      1. [타이타닉 생존자 분류](https://www.kaggle.com/c/titanic/overview/evaluation) : `정확도`
      2. [식물종류 판별](https://www.kaggle.com/c/herbarium-2020-fgvc7/overview/evaluation) : `F1 Score`
    - 정확도의 경우 예측하려고 하는 종속변수의 비율이 불균형할때 가치 하락
    - target의 비율을 고려해보았을 때 5:5로 균형 ➡️ 최종적으로 정확도(Accuracy)로 선정
* 활용 모델 : 다양한 모델을 비교·앙상블 진행하여 성능이 제일 좋은 것으로 선정(📂엑셀 파일 참고)
  0. auto ML(Automated Machine Learning) 성능을 기준으로 지정
  1. 단일 알고리즘 : Logistic Regression, Decision tree, KNN
  2. 앙상블 : Random Forest, Gradient Boost, LightGBM, Boosting - xgb, Voting, Stacking
  3. 최종 모델 : **Stacking**(Random Forest, Logistic Regression, KNN)
    - **Train score : 0.969| Test score : 0.992**

#### 3. 회고
* 추가 경기 결과를 크롤링하여 데이터의 양을 늘려 모델 성능 추가 테스트
* 컬럼을 재창출하고 오버피팅을 줄이려는 최적의 목표 달성
* 다양한 ML 모델을 직접 사용하고 시행착오 속에서 성장하는 Team JyGy

--- 
### 👀 발표자료 Preview
<img width="654" alt="gh1" src="https://user-images.githubusercontent.com/89832134/164351800-3654ddf2-f411-40e2-b1b1-5dc3d7a5c600.png">
<img width="654" alt="gh2" src="https://user-images.githubusercontent.com/89832134/164351816-ececc8c0-2316-4386-8ee0-ab148b8b872f.png">
<img width="654" alt="gh3" src="https://user-images.githubusercontent.com/89832134/164351829-f4506214-4480-44c8-85d5-0fa0e2a91f56.png">

