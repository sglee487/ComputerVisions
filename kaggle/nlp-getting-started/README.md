# Real or Not? NLP with Disaster Tweets
https://www.kaggle.com/c/nlp-getting-started<br>
Twitter에 올라온 글들로 실제 자연재해가 났는지 예측하는 내용입니다.

|파일|내용|
|:---:|:---:|
|[code/NLP custom.ipynb](https://github.com/sglee487/ComputerVisions/blob/master/kaggle/nlp-getting-started/code/NLP%20custom.ipynb)|데이터 정제, 훈련 및 예측|

<br>
사실 자연어쪽을 공부하지 않고 실습만 해서 이런식으로 동작하구나~ 하는 맥락을 알 수 있었습니다.<br>
문장을 각각 단어로 tokenize 하여 어떤 데이터들로 구성되어 있는지 시각화 하여 파악하고, https 링크나 이모티콘 등의 단어는 없애고, 오타는 spellchecker 모듈로 고친 뒤 각각의 단어들을 glove.6B.100d 로 임베딩하여 훈련을 수행하였습니다.
