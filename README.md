# 신한그룹 빅데이터 해커톤 (제 3회)
<img src="https://github.com/user-attachments/assets/0b11ed63-fa4b-42d6-b2cd-ca6f71c20433">
</br>

### 💻 Technology
***
![python](https://img.shields.io/badge/Python-14354C?style=for-the-badge&logo=python&logoColor=white)&nbsp; ![Visual Studio Code](https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white) &nbsp;<br>
![Selenium](https://img.shields.io/badge/-selenium-%43B02A?style=for-the-badge&logo=selenium&logoColor=white)&nbsp; ![Octopus Deploy](https://img.shields.io/badge/octopus%20deploy-0D80D8?style=for-the-badge&logo=octopusdeploy&logoColor=white) &nbsp;<br>
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white) &nbsp; ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white) &nbsp; ![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)&nbsp;<br>
<br>

### 📅 개발 기간
***
 - 2023-11-18 ~ 2024-01-27
<br>

### 📌 구현 과정

**1️⃣데이터 구축: 총 15759개 데이터** </br>
- 올리브영 사이트 웹 크롤링(제품,리뷰) 
- 제품 데이터: 제품명, 제품 브랜드, 가격, 카테고리, 총 리뷰 개수, 총 평점, 용량, 성분, 제품 이미지 (Selenium, Octoparse) 
- 리뷰 데이터: 제품명, 유저 아이디, 유저 타입, 점, 리뷰 날짜, 상세평점1-3, 리뷰 내용 (Selenium) 

**2️⃣ 데이터 전처리** </br>
- 평점 4,5점(긍정리뷰만) & 리뷰 개수 50개 이상 데이터 가져오기
- 리뷰 데이터 전처리 (특수문자, 띄어쓰기 제거)
 
**3️⃣ 키워드 추출**  </br>
- TextRank와 TF-IDF 이용
- KeyBert를 이용
- 각 방법을 통해 추출된 키워드를 비교하여 최종 키워드를 제품당 3~6개로 산출  

**4️⃣ 제품 군집화 및 라벨링** </br>
- 최종 키워드 원핫 인코딩
- 가져올 속성 선택 -> 제품명, 원가, 별점
- 원가 정규화(Min-Max 스케일링)
- KMeans 클러스터링 (elbow plot, silhouette score를 통해 군집개수 5개로 설정)
- 각 군집마다 1의 개수 비율(원핫인코딩 처리됨)을 통해 최종 클러스터의 키워드와 테마(과일)에 따라 라벨링
   
**5️⃣ 스모어 설문 사이트 사용하여 테스트** </br>
- 클러스터링 별 키워드를 기준으로 설문 문항 구상 / 답변마다 가중치(0-3) 부여
