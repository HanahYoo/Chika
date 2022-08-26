# 3조 Rhythm-of-Chika


## 1. 프로젝트의 목적 및 용도.
어린이들이 양치질을 꺼려하는 상황 속에서 부모들이 아이들에게 양치질 교육을 하는데 어려움이 있다.
구글의 오픈소스인 ‘mediapipe’를 활용해 양치하는 모습의 손 관절 데이터를 수집하고, 이를 통해 양치 부위를 예측하는 모델을 만들고자 했다. 
양치 부위 예측 모델을 게임에 적용하여 어릴 때부터 양치 습관을 올바르게 길러주는 에듀테인먼트 컨텐츠를 제작함으로써 양치질에 대한 아이들의 거부감을 해소할 수 있다.
효과 : 값비싼 전동칫솔을 구매하지 않고 카메라만으로 모든 구역을 구분할 수 있어 사용자들로 하여금 각 양치 부위를 정확히 그리고 꼼꼼히 닦도록 도와줄 수 있다.


## 2. 프로젝트 시작 방법 및 코드 설명
requirements.txt 
'''
 pip install -r requirements.txt
'''
데이터 수집 방법: collector_final.py를 실행시켜 400프레임 동안 (약 13초) 해당 양치 부위를 닦는다. 각 부위마다 numpy 배열 한 개씩 생성된다. 그리고 pause time(5초) 동안 다음 부위로 이동해 또 양치할 준비를 한다. 그렇게 해서 총 16개 부위를 닦고 배열들을 저장해서 총 100개의 세션을 쌓았다. 
 python collector_final.py로 데이터를 수집
데이터 전처리 및 모델 학습:
