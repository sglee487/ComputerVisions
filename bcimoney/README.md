# 이 프로젝트는...
https://bcimoney.xyz/ 라는 사이트가 있는데 광고를 보며 숫자를 입력하면 100원씩 준다는 사기 사이트입니다. 숫자를 자동 인식하여 입력해줍니다.

|파일|내용|
|:---:|:---:|
|[bcimoney.xyz 자동클릭 모델 학습.ipynb](https://github.com/sglee487/ComputerVisions/blob/master/bcimoney/bcimoney.xyz%20%EC%9E%90%EB%8F%99%ED%81%B4%EB%A6%AD%20%EB%AA%A8%EB%8D%B8%20%ED%95%99%EC%8A%B5.ipynb)|모델 설계, 학습|
|[bcimoney.xyz 자동클릭 모델 실행.ipynb](https://github.com/sglee487/ComputerVisions/blob/master/bcimoney/bcimoney.xyz%20%EC%9E%90%EB%8F%99%ED%81%B4%EB%A6%AD%20%EB%AA%A8%EB%8D%B8%20%EC%8B%A4%ED%96%89.ipynb)|모델 실행|
<br>

<img src="K-20200214-863954 t.png" alt="drawing" style="width:px;"/>
<br>
우선 3개의 숫자 그림이 떠있는 화면 위치에 스크린샷을 찍어 3등분을 합니다. 그 뒤 모델을 거쳐 숫자를 하나씩 읽어낸 뒤 결과를 배열에 저장하고, 키보드 입력 라이브러리를 이용해 입력합니다. 
<br><br>
완전히 처음부터 시작하니 의외로 데이터 수집부터 고민을 하였습니다. 단순 스크린샷을 찍더라도 png나 jpg로 찍어야 할지, rgb가 brg 로 순서가 바뀐다던가, 숫자가 알고보니 화면에서 몇 픽셀씩 좌우로 움직인다던가 하는 문제점이 있었고, 모델훈련쪽에선 overfitting과 underfitting 등의 문제가 나타났었습니다.
<br><br>
구글링해서 파일 포맷, 훈련 epoch를 조정하는 등으로 해결했지만 숫자 위치가 조금씩 바뀌어 나온다는 점, overfitting이 생각보다 쉽게 된다는 점에서 data argumentation의 중요성을 알게 되었습니다.
