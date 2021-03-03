## 피어세션 16:00 ~ 17:30

# 강의 관련 질문
- 6강 실습코드 설명 (p.48)에서 normalized_ratings!=0으로 처리를 해주는 부분
    - 강의에서는 둘 중에 영화를 한명이라도 관람하지 않았으면 제외해야 한다고 설명
    - 따라서 사용자의 ratings==0이면 제외해야 하는 것 아닌가 라고 생각
    - 그러나 sim(x,y)라는 공식에서 분자, 분모에 사용되는 경우의 수를 맞추기 위해서는 normalized_ratings 사용이 적절
    - 원점수에서 사용자 마다의 선호도를 제거해주는 것과 유사한 개념으로 판단
    - (질문게시판 or 조교님에게 질문) 왜 평균 평점이 0인 것도 제거해주는지

# 멘토링 추가 질문
- 추천시스템을 튜닝하기 위해서는 "충분한 데이터"가 쌓여야 함
    - 실제로 어느 만큼이 충분한 데이터의 양인지 의문
    - 원하는 데이터의 몇 퍼센트 정도가 쌓여야 튜닝을 시작하는지
    - 새로운 사용자, 새로운 데이터가 쌓였을 때 어떠한 방식으로 갱신하는지 (새로운 학습이 언제 시작하게 되는지)
- "논문을 구현한다"의 의미
    - 프레임워크만 사용해서 논문의 수식을 토대로 동작 가능한 모델을 설계하는지
- 잠재인수모형
    - 강의에서는 잠재인수모형을 협업 필터링과 독립적인 개념으로 설명
    - 다른 외부 자료에서는 잠재인수모형이 협업 필터링의 한 종류로 설명
- 잠재인수의 설정
    - 잠재인수를 크게 잡으면 연산량이 증가 -> 하이퍼파라미터를 설정하는 과정에서 연산량을 고려하는 부분은 없는지
    - RMSE 부분 외에는 어떤 부분을 참고하면 좋을지

# 특강 주차의 피어세션
- P stage 대비 실전 코딩 연습의 중요성
- torch에서 제공해주는 dataset을 활용해서 기초적인 모델 설계와 훈련/테스트를 수행해보자
    - 누리님: MNIST, 수업/대학원에서 수행했던 주제를 응용, Attention 활용
    - 지호님: CNN구조로 이미지 데이터셋 연습 (기존 연구하셨던 모바일 분야와 결합하기 좋을 것 같다)
    - 지영님: 기존에 하셨던 자연어 처리를 PyTorch로 수행 (성능에 대한 평가 부분을 추가)
    - 동현님: AlexNet, RestNet, YOLO 등 대표적인 CNN 모델로 이미지 데이터셋 연습 (하이퍼파라미터 연구)

# 누리님이 진행하셨던 연구 Presentation
- Graph 알고리즘에서 배웠던 Community Detection으로 Image Segmentation 수행
    - 학습데이터가 따로 필요하지 않은 알고리즘
    - 이미지 픽셀 간 연결되어 있는 weight는 거리와 밝기로 설정 (직접 설정 필요)
    - 이미지 픽셀 간 Edge가 적으면 결과가 좋지 않고, 많으면 소요되는 시간이 길다
    - Graph 알고리즘으로 이미지 데이터를 분석한 참신한 아이디어