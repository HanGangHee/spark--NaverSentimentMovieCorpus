spark--NaverSentimentMovieCorpus
================================

네이버 영화 댓글의 감성 데이터를 통해서 댓글로 감성을 예측해보는 모델을 만들어보자,

  0.분석 환경
  ----------
        1-1 하둡 클러스터(의사 분산모드)
         > version:2.9.0
         > master: yarn-client
         > memory: 11GB
        1-2 spark
         > version: 2.2.0
        1-3 zeppelin
         > version: 0.7.3


데이터 출처:https://github.com/e9t/nsmc (ratings.txt) 

1.분석 방법
----------
   * 1-1 결측값 제거
   * 1-2 training , test data classification(0.7 : 0.3)
   * 1-3 Tokenizer, hashingTF, LogisticRegression 적용
   >>명사, 동사, 명사 or 동사, 모든 형태소: 4가지 경우에 대해 모두 적용

2.코드 및 분석 결과 보기
-----------------------

  *[결측값 제거 및 training data에 대한 PipelineModel생성](https://www.zepl.com/UHMK7RFW2/spaces/SKIX7089H/fde3f1b5903245f08a4daf2f1ae4da8d)
   
  *[(동사, 명사, 모든 형태소, 동사 및 명사)에 대한 모델 평가](https://www.zepl.com/UHMK7RFW2/spaces/SKIX7089H/ed192cf60a484c219cd2f05a299d9ae0)
