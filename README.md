# mini-project-02
### ๐ Machine Learning : ๋ฐฐ๊ตฌ ์น๋ถ ์์ธก
* ๐ ๋ชฉํ : ํ๊ตญ๋ฐฐ๊ตฌ์ฐ๋งน ๋ฐ์ดํฐ๋ฅผ ํ์ฉํ์ฌ ๊ฒฝ๊ธฐ ๊ฒฐ๊ณผ ์์ธกํ๋ ๋จธ์ ๋ฌ๋ ๋ชจ๋ธ ๊ตฌ์ถ
* ๐ ์ฌ์ฉ ๋ฐ์ดํฐ
  * ์๋ ๋์์ ํ์ฉํ์ฌ ํ๊ตญ๋ฐฐ๊ตฌ์ฐ๋งน ํฌํธ [KOVO](https://www.kovo.co.kr/game/v-league/11141_game-summary.asp?season=017&g_part=201&r_round=1&g_num=2&) ๊ฒฝ๊ธฐ ๊ฒฐ๊ณผ ํฌ๋กค๋ง
* ๐ ๊ธฐ๊ฐ : 2022-04-19 ~ 2022-04-20
* ๐ฉโ๐ป ์ธ์ : 5๋ช(๊นํ๊ฒฐ ๋ฐ์์ ์๋ฏผ์  ์ ์ ์  ์ต์ ์ฐ) | [ํ์ ํด ๋ธ์ ์ฌ์ฉ](https://imdona.notion.site/mini-project-2-ML-0cde262f1c7e4342be54ab16a2f1b39b)

#### 1. ๋ฐ์ดํฐ ์ ์ฒ๋ฆฌยท๋ถ์
* ํ์ญ ๋ฐฐ๊ตฌ ์ ์๋ ์ธํฐ๋ทฐ๋ฅผ ํตํ ๋๋ฉ์ธ ์ดํด
* ์ธํฐ๋ทฐ ๊ฒฐ๊ณผ์ ๋ฐฐ๊ตฌ ์น๋ฅ  ๊ด๋ จ ๋ผ๋ฌธ ๋ด์ฉ์ ๊ธฐ๋ฐ์ผ๋ก ๋ฐ์ดํฐ์ ์ถ์ถ
  - ์ฐธ๊ณ  ๋ผ๋ฌธ
    - [๋จ์ ํ๋ก ๋ฐฐ๊ตฌ ๊ฒฝ๊ธฐ ๊ธฐ๋ก์ด V-๋ฆฌ๊ทธ ์์ฆ ์น๋ฅ ์ ๋ฏธ์น๋ ์ํฅ](https://www.kci.go.kr/kciportal/ci/sereArticleSearch/ciSereArtiView.kci?sereArticleSearchBean.artiId=ART002440361)
    - [๋จ์ ํ๋ก๋ฐฐ๊ตฌ ๊ฒฝ๊ธฐ๋ ฅ ๋ณ์ธ ๋ถ์์ ๊ดํ ์ฐ๊ตฌ](https://m.earticle.net/Article/A362822)
* Feature Engineering
  - ์ ์ ๊ฐ์ธ์ด ์๋ ํ๋ณ ์ญ๋์ ๊ณ ๋ คํ๊ธฐ ์ํด ๊ฒฝ๊ธฐ์ ํ๋ช์ ๊ธฐ์ค์ผ๋ก ํผ์ณ ์์ฑ : ๋ฒ์ค, ๊ณต๊ฒฉ, ๋ธ๋กํน, ๋๊ทธ, ๋ฆฌ์๋ธ
  - MVP : key player ์ฐธ์ ์ฌ๋ถ๋ฅผ 0๊ณผ 1๋ก ๋ํ๋ด๋ ํผ์ณ ์์ฑ
    - ์ ์  ๊ธฐ์ค : ํ ๋ด์์ ๋์ ์ด ๊ฐ์ฅ ๋์ ์ ์

#### 2. ๋ชจ๋ธ๋ง
* ํ๊ฐ ์งํ ์ ์  : ๋ถ๋ฅ(classification)์ ํ๊ฐ ์งํ ์ค ์ ํ๋(Accuracy)๋ก ์ ์ 
  - ์ ์  ์ด์ โ
    - ์ ํ๋จ์ด๋ ์คํธ๋ฉ์ผ ๋ถ๋ฅ์ฒ๋ผ ์นยทํจ์ ์ค์์ฑ์ ์ฐจ์ด๊ฐ ์์ด Recall(์ฌํ์จ) ์ด๋ precision(์ ๋ฐ๋)์ ์๋ฏธ๊ฐ ์์
    - ์ค์  ์ฌ๋ก ์ฐธ๊ณ 
      1. [ํ์ดํ๋ ์์กด์ ๋ถ๋ฅ](https://www.kaggle.com/c/titanic/overview/evaluation) : `์ ํ๋`
      2. [์๋ฌผ์ข๋ฅ ํ๋ณ](https://www.kaggle.com/c/herbarium-2020-fgvc7/overview/evaluation) : `F1 Score`
    - ์ ํ๋์ ๊ฒฝ์ฐ ์์ธกํ๋ ค๊ณ  ํ๋ ์ข์๋ณ์์ ๋น์จ์ด ๋ถ๊ท ํํ ๋ ๊ฐ์น ํ๋ฝ
    - target์ ๋น์จ์ ๊ณ ๋ คํด๋ณด์์ ๋ 5:5๋ก ๊ท ํ โก๏ธ ์ต์ข์ ์ผ๋ก ์ ํ๋(Accuracy)๋ก ์ ์ 
* ํ์ฉ ๋ชจ๋ธ : ๋ค์ํ ๋ชจ๋ธ์ ๋น๊ตยท์์๋ธ ์งํํ์ฌ ์ฑ๋ฅ์ด ์ ์ผ ์ข์ ๊ฒ์ผ๋ก ์ ์ (๐์์ ํ์ผ ์ฐธ๊ณ )
  0. auto ML(Automated Machine Learning) ์ฑ๋ฅ์ ๊ธฐ์ค์ผ๋ก ์ง์ 
  1. ๋จ์ผ ์๊ณ ๋ฆฌ์ฆ : Logistic Regression, Decision tree, KNN
  2. ์์๋ธ : Random Forest, Gradient Boost, LightGBM, Boosting - xgb, Voting, Stacking
  3. ์ต์ข ๋ชจ๋ธ : **Stacking**(Random Forest, Logistic Regression, KNN)
    - **Train score : 0.969| Test score : 0.992**

#### 3. ํ๊ณ 
* ์ถ๊ฐ ๊ฒฝ๊ธฐ ๊ฒฐ๊ณผ๋ฅผ ํฌ๋กค๋งํ์ฌ ๋ฐ์ดํฐ์ ์์ ๋๋ ค ๋ชจ๋ธ ์ฑ๋ฅ ์ถ๊ฐ ํ์คํธ
* ์ปฌ๋ผ์ ์ฌ์ฐฝ์ถํ๊ณ  ์ค๋ฒํผํ์ ์ค์ด๋ ค๋ ์ต์ ์ ๋ชฉํ ๋ฌ์ฑ
* ๋ค์ํ ML ๋ชจ๋ธ์ ์ง์  ์ฌ์ฉํ๊ณ  ์ํ์ฐฉ์ค ์์์ ์ฑ์ฅํ๋ Team JyGy

--- 
### ๐ ๋ฐํ์๋ฃ Preview
<img width="654" alt="gh1" src="https://user-images.githubusercontent.com/89832134/164351800-3654ddf2-f411-40e2-b1b1-5dc3d7a5c600.png">
<img width="654" alt="gh2" src="https://user-images.githubusercontent.com/89832134/164351816-ececc8c0-2316-4386-8ee0-ab148b8b872f.png">
<img width="654" alt="gh3" src="https://user-images.githubusercontent.com/89832134/164351829-f4506214-4480-44c8-85d5-0fa0e2a91f56.png">

---
### ๐ Directory Structure

๐ DA  

    ใด ๐ณ volleyball_preprocessing_final.ipynb  
    
๐ Dataset  

    ใด ๐ณ volleyball_raw.csv

๐ ML  

    ใด ๐ณ ensemble_random_forest.ipynb  
    
    ใด ๐ณ ensemble_stacking.ipynb  
    
๐ crawling  
