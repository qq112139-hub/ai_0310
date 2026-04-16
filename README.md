# 1. 이미지 다중 분류 모델 구성하기
- 딥러닝 기술 : google tensorflow (keras)
- 전처리 스케이링 : min-max scale
- 이미지 리사이징 : resize_with_pad (32*32 3channel 이미지)
- 훈련데이터 : cifar10
- 이미지 라벨 : ["airplane","automobile","bird","cat","deer","dog","frog","horse","ship","truck"]
- 이미지 한글라벨 : ["비행기", "자동차", "새", "고양이", "사슴", "강아지", "개구리", "말", "선박", "트럭"]
- 서비스 서버 : Flask
- 통신데이터 유형 : json / dict
- 특징 : Conv2D and MaxPOOL2D 사용으로 특성맵 추출과 풀링충을 거쳐 과대적합 방지  
## 디렉터리 구조  
<pre>
      디렉터리 구조:
      Portfolio (root)
       L ai model
           L ai_interface.py (모델인터페이스)
           L conv_ai.py (모델 로딩 및 분석기)
       L static
           L app
           L index.js (클라이언트 스크립트파일)
       L css
           L index.css (클라이언트 모양설정)
           L images (메인페이지 이미지 파일)
           L temp (예측 업로드 파일)
       L templates
           L index.html (메인페이지)
       L web_sercive.py (web route)
</pre>
