## Day18 피어세션 15:30~17:00

- 조교님 멘토링
    1. 해밀턴 회로 탐색
    - 노드,엣지가 고정되어 있다고 가정하기 때문에 현실에 적용하기엔 괴리가 있다.
    - 음식배달 경로 탐색같은 경우 노드가 유동적이므로 다익스트라 같은 최단거리 찾는 알고리즘을 사용한다. \ 해밀턴 회로 탐색 문제는 NP-hard 문제여서 현업에서는 잘 사용하지 않는다.
    - 과거에 지하철 노선도를 기반으로 최단거리를 탐색할 때도 해밀턴 회로를 쓰지 않았다.

    2. 효율적인 논문 읽기 순서
    - 논문의 전반적인 흐름은 abstract, conclusion, future work에 담겨있다.
    - 모델의 핵심적인 구조를 파악하고 싶다면 figure를 유심히 보기.
    - 논문을 읽는 목적(선행연구 조사, 모델 차용 등)에 따라 집중해서 읽는 부분이 다르다.

    3. 캐글 데이터 vs 현업 데이터
    - 연구실에서 진행되는 과제들 중 전처리만을 목표로 하는 과제들도 존재함.
    - 특히 현업에서는 전처리를 많이 경험해볼수록 도움이 되지만, 크롤링은 선택 사항인 것 같다.
    - 저작권에 침해되지 않는 선에서 크롤링+전처리를 할 수 있으면 재밌는 데이터를 많이 다뤄볼 수 있을 것이다.

    4. 모델의 동작 원리를 얼마나 깊이 이해해야 하는가?
    - LSTM, GRU의 세부적인 구조(i,f,o,g gate)는 다 이해하지 못해도 괜찮다.
    - KL Divergence같은 개념은 알아야 하지만, VAE에 나오는 loss 증명까지 이해할 필요는 없다.
    - GAN과 VAE의 차이 정도 알고 넘어가면 좋을 거 같다.
    - 보통 모델을 가져다 쓰기 때문에 유명한 모델의 특징을 파악하는 게 중요하다. \
    (LSTM의 장단점, BERT의 특징, 기존 모델에서 어떤 변화를 주었는지 등)
    - 면접 준비 시 답변할 수 있을 정도로 전체적인 구조를 단순화해서 동작 원리를 이해하기

    5. 강의내용 질문
    - Day14 과제코드 (MNIST를 LSTM로 구현)
        - 28*28 데이터를 전부 다 입력받은 뒤 one-hot vector를 출력 -> many to one
        - 중간에 한 줄 뚫려있는 그 부분을 예측하는 것이 아니고 라벨(스칼라)을 예측하는 모델이다.
        - 중간에 한 줄 뚫려있어도 다 0으로 채워져있다고 생각하면 되므로 라벨을 예측하는 데 문제가 없다.
    
    - Day17 강의록 p.19
        - bias의 차원: 3x1 (hidden state vector의 차원과 같다.)


- 스몰토크
    - 지호님이 슬랙에서 뱅크샐러드 게시물을 읽고 위안을 얻었다며 꼭 읽어보라고 추천해주셨다!
    - 지영님 진로 고민 \
        알고리즘 코드 리뷰를 좋아해서 IT기업을 희망하지만 코테에 대한 두려움이 있다. \
        금융업계가 전공을 살리는 길이지만 보수적인 분위기와 잘 맞을지 걱정이다. \
        뱅크샐러드, 토스에 도전해봅시다! 화이팅:)
    - 코로나가 없었다면 지금쯤 뭘 하고 있었을지 계획했던 것들이 있나요? \
        누리님: 석사 졸업 후 한달 간 남미 여행. 현재 여행자금을 털어 파워앱등이가 되었다. \
        지영님: 아침 수영으로 하루를 활기하게 시작했으면 공부를 더 잘했을 것 같다. \
        지호님: 취뽀 후 미국여행 + EPL직관. 현재 이디야에 상주 중이다. \
        동현님: 코로나 덕분에 포스코와 부스트캠프를 모두 할 수 있었다ㅋㅋㅋ