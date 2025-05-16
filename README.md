<h1 align="center"> <img src="https://github.com/user-attachments/assets/09a9e704-12f4-4fdc-aa73-a921de5e9432" alt="신한마크" width="30" height="30"> 신한그룹 빅데이터 해커톤 (제 3회) </h1>
<div align="center"> <img src="https://github.com/user-attachments/assets/0b11ed63-fa4b-42d6-b2cd-ca6f71c20433" alt="메인이미지" width="900"> </div>
</br>

## <img src="https://github.com/user-attachments/assets/09a9e704-12f4-4fdc-aa73-a921de5e9432" alt="신한마크" width="23" height="23"> 주제: 건강을 더하다 +he(the) 건강 서비스

**개발기간** </br>
 - 2024-10-07 ~ 2024-11-21
<br>

**참여인원**  </br>
|이름|직책|
|------|---|
| 김민지 | 팀리더 |
| 김용태 | 팀원|
| 박규리 | 팀원 |
| 원종철 | 팀원 | 
</br>

## ✨ 프로젝트 제안 배경(3C분석)
### 1. 시장(트렌드)분석: '건강' 키워드 선정 
### 2. 경쟁사 분석: 일상 속 맞춤형 고객 서비스 다수 
### 3. 자사 분석: 일상 속 간편한 육체 건강 서비스 부족 
</br>
  
## 🧑🏻‍💻 분석 및 모델링 과정
**1️⃣ 칼럼 추출**  </br>
+ 건강과 관련된 소비 데이터(의료, 스포츠)를 칼럼으로 추출 </br>
   
**2️⃣ 상관분석** </br>
+ 의료 데이터: 비율, 금액 상관성X </br>
+ 스포츠 데이터: 비율, 금액 상관성O / 골프장 상관성O </br>
   
**3️⃣ 피처 엔지니어링**  </br>
+ 이용금액과 이용비율을 곱해서 ‘1인당 소비 기대금액’ 칼럼 추출 </br>

**4️⃣ 이상치 처리**  </br>
+ 의료 데이터: 과도하게 큰 값 제외(보험사 관심 대상X) </br>
+ 스포츠 데이터: 과도하게 큰 값 제외X(보험사 관심 대상) </br>

**5️⃣ 군집 분석, 비율검정**  </br>
+ Elbow Method, Silhouette Analysis를 통한 최적의 군집개수(k) 선정 </br>
+ 군집별 고객군 연령대 분포 확인  </br>
+ 2번 클러스터를 기준으로 또 다시 군집분석 시행 </br>
+ 해당 군집의 보험 데이터 관련 특성 분석  </br>
</br>

## 🔍 결과물 설계
**해당 군집(20대, 건강관심)의 건강 보험 가입률 증진을 목표로 함**
+ 타겟층 확장(기존고객, 카드고객, 신규고객) </br>
+ 기존 신한 라이프 "마이 데이터" 서비스 개선방향 제시  </br>
</br>

## 💻 Technology
![python](https://img.shields.io/badge/Python-14354C?style=for-the-badge&logo=python&logoColor=white)&nbsp; ![Visual Studio Code](https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white) &nbsp;<br>
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white) &nbsp; ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white) &nbsp; ![SciPy](https://img.shields.io/badge/SciPy-%230C55A5.svg?style=for-the-badge&logo=scipy&logoColor=%white) &nbsp;<br> ![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black) &nbsp; ![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)&nbsp;<br>
</br>

