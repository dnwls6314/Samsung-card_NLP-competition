# Samsung-card_NLP-competition
2021 SAMSUNG CARD NLP TASK competition

# 공모전 정보

---

- 홈페이지

[http://www.scic2021.com/](http://www.scic2021.com/)

- 주요 일정

![공모전 주요일정](https://github.com/dnwls6314/Samsung-card_NLP-competition/blob/main/image/%EA%B3%B5%EB%AA%A8%EC%A0%84%20%EC%A3%BC%EC%9A%94%EC%9D%BC%EC%A0%95.png)



# 사용 모델

### KcELECTRA-GCN

---

- ELECTRA representation을 Graph Convolutional Network의 feature matrix로 받는 모델
- 2021년 제안된 BertGCN 모델의 text encoder를 Bert가 아닌 ELECTRA로 대체

---

- [BERT에 대한 설명](https://www.notion.so/e806542ec7c14285842120d0c9efaa6f)
- BertGCN에 대한 설명
- ELECTRA에 대한 설명


---

**Bert 대신 KcELECTRA를 쓰는 이유** 

![NLP 모델 성능 비교](https://github.com/dnwls6314/Samsung-card_NLP-competition/blob/main/image/NLP%20%EC%84%B1%EB%8A%A5%EB%B9%84%EA%B5%90.png)

표1 한국어 텍스트 데이터에 대한 transformer NLP 모델 성능 비교 

- 본 task는 고객의 구어체에 가까운 `Korean review data`를 분류하는 문제이므로, 기존의 pretrained Bert 모델이 아닌 User-Generated Noisy text domain 데이터셋을 사전학습한 모델이 필요
- 표 1을 보면, Comment 데이터인 NSMC 데이터에 대해 `KcELECTRA`모델이 가장 높은 성능을 보임
- BertGCN 알고리즘에서 BERT의 역할은 단순히 문장 임베딩을 GCN의 입력으로 제공할 뿐이므로 이를 다른 모델로 바꾸어도 모델의 성능이 하락하지는 않을 것으로 판단하여 BERT를 `KcELECTRA`로 변경하기로 결정

# 회의 일지

---

[삼성카드 공모전 회의 일지](https://www.notion.so/964b33f48fed4bbd93b3ba4eabc97607)
