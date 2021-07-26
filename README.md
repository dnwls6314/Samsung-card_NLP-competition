# Samsung-card_NLP-competition
2021 SAMSUNG CARD NLP TASK competition

# 공모전 정보

---

- 홈페이지

[http://www.scic2021.com/](http://www.scic2021.com/)

- 주요 일정

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/87fa908d-edee-4d4e-a067-ece5ee850ea4/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/87fa908d-edee-4d4e-a067-ece5ee850ea4/Untitled.png)

# 사용 모델

### KcELECTRA-GCN

---

- ELECTRA representation을 Graph Convolutional Network의 feature matrix로 받는 모델
- 2021년 제안된 BertGCN 모델의 text encoder를 Bert가 아닌 ELECTRA로 대체

---

- [BERT에 대한 설명](https://www.notion.so/e806542ec7c14285842120d0c9efaa6f)
- BertGCN에 대한 설명
- ELECTRA에 대한 설명

→ 여기는 논문 읽고 정리한 내용 링크 추가할 거(건들 ㄴㄴ) ← 이거 뭐냐?

---

**Bert 대신 KcELECTRA를 쓰는 이유** 

![https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1299d1a5-2f85-42cc-8211-a278eb49c5dc/Untitled.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1299d1a5-2f85-42cc-8211-a278eb49c5dc/Untitled.png)

표1 한국어 텍스트 데이터에 대한 transformer NLP 모델 성능 비교 

- 본 task는 고객의 구어체에 가까운 `Korean review data`를 분류하는 문제이므로, 기존의 pretrained Bert 모델이 아닌 User-Generated Noisy text domain 데이터셋을 사전학습한 모델이 필요
- 표 1을 보면, Comment 데이터인 NSMC 데이터에 대해 `KcELECTRA`모델이 가장 높은 성능을 보임
- BertGCN 알고리즘에서 BERT의 역할은 단순히 문장 임베딩을 GCN의 입력으로 제공할 뿐이므로 이를 다른 모델로 바꾸어도 모델의 성능이 하락하지는 않을 것으로 판단하여 BERT를 `KcELECTRA`로 변경하기로 결정

# 회의 일지

---

[삼성카드 공모전 회의 일지](https://www.notion.so/964b33f48fed4bbd93b3ba4eabc97607)
