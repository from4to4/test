<h2>2021_PNU_BigDataAI_Project</h2>
팀명: Paul

팀원: 김은서, 차유빈, 윤석영, 문수인
# 

### 개요
1. 주제: 4.7 보궐선거 당선인 예측 및 분석과 2022년 대선 예측

2. 기간: 2021.03.08~2021.05.24

3. 기획의도: 단기간에 이루어지는 보궐선거의 경우 현 시점의 대중인식과 여론 방향이 선거결과에 큰 영향을 미칠 것이라 판단하여 당선인을 예측하고 더 나아가 2022년 대선 예측까지 예측해보았다

4. 개발과정: 데이터 수집 -> 데이터 전처리 -> 모델구축 <-> 데이터분석
# 

### 프로젝트 과정 설명

- 01_prediction_electionApril7_2021 : 
  - 키워드 '보궐선거'로 2020년 8월 30일부터 2021년 4월 7일까지의 뉴스기사 및 콘텐츠의 댓글을 수집 및 전처리 
  - 후보자를 예측하는 모델(모델1)과 감성분석 모델(모델2)를 개발하여 약 14만개의 데이터를 이용해 당선인 예측
- 02_analysis_electionApril7_2021:
  - 시기별 이슈 파악 : 각 후보자별 긍정-부정댓글 점유율 확인과 각 시기별 워드클라우드 생성
  - 2030표심 및 정치성향 분석: 2030세대를 특정하여 가중치를 둔 워드클라우드 생성과 KR-WordRank를 이용한 핵심 키워드 및 문장 추출
  - Word2Vec : 핵심 키워드와 연관성이 높은 단어를 추출하여 2030세대의 의견 파악
- 03_prediction_presidentialElection2022 :
  - 대선 예측
    - 대선 데이터 수집: 키워드 '대선 {후보자이름}'으로 2021년 3월 1일부터 2021년 5월 14일까지의 뉴스기사 및 콘텐츠의 댓글을 수집 및 전처리
    - 대선 데이터 분석:
      - 유망 후보자별 긍정률 예측 : 보궐선거 예측시 사용한 모델을 이용해 유력 후보자별 긍정률 예측
      - 테마주 : 유력 후보자별 테마주를 파악해 시장의 후보자에 대한 평가를 간접적으로 확인
  - 2030세대 특정 모델: 2030세대를 특정하는 분류모델 생성
- 04_Web: 유력 후보자별 긍정률과 각 후보자별 핵심 키워드 및 문장, 테마주, 2030세대의 의견 등을 제공하는 서비스
# 
### 개발 방향
대선 유망 후보자 별 수집한 데이터를 DB에 적재하고 이를 웹과 연동하여 준실시간으로 후보자별 긍정률과 핵심 키워드, 테마주 등 후보자에 대한 여론을 모니터링 할 수 있는 서비스 제공이 가능하다.
이를 필요로 하는 정당 혹은 정치인에게 제공하여 본인의 객관적인 여론 평가를 확인하고, 청년세대의 평가와 이슈를 파악해 2030세대의 지지기반을 얻기 위한 방향성을 제시할 수 있다.
