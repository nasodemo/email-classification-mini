# 메일 분류기 만들기 미니 프로젝트
---

## 개발 기한
8.10.

## 프로젝트 기획
8.8 : 데이터 다운 잋 데이터 셋 구분

8.9 : 이메일 데이터를 각 특성 백터로 구분하여 처리

8.10 : 하이퍼파라미터 추가 및 조정 => 성능 향상



p155 문제 4번 내용

 4.  스팸 분류기를 만들어보세요 (아주 도전적인 과제입니다 ).
 ●  아파치 스팸어새신Apache SpamAssassin 공공 데이터셋 ( https://homl.info/spamassassin )에서 스팸spam과 햄ham(스팸이 아닌 메일 ) 샘플을 내려받습니다.
 
 ●  데이터셋의 압축을 풀고 데이터 형식을 살펴봅니다.
 
 ●  데이터셋을 훈련 세트와 테스트 세트로 나눕니다.
 
 ●  각 이메일을 특성 벡터로 변환하는 데이터 준비 파이프라인을 만듭니다. 이 준비 파이프라인은 하나의 이메일을 가능한 단어의 존재 여부를 나타내는 (희소 ) 벡터로 바꿔야 합니다. 예를 들어 모든 이메일이 네 개의 단어 ‘Hello’, ‘how’, ‘are’, ‘you’만 포함한다면 ‘Hello you Hello Hello you’란 이메일은 벡터 [1, 0, 0, 1]([‘Hello’ 있음, ‘how’ 없음, ‘are’ 없음, ‘you’ 있음]을 의미 )로 변환되거나, 단어의 출현 횟수에 관심이 있다면 [3, 0, 0, 2]로 변환되어야 합니다.

●  준비 파이프라인에 이메일 헤더 제거, 소문자 변환, 구두점 제거, 모든 URLs 주소를 ‘URL’로 대체, 모든 숫자를 ‘NUMBER’로 대체, 어간stem 추출20(즉, 단어의 끝을 떼어냅니다. 이런 작업을 할 수 있는 파이썬 라이브러리가 있습니다) 등을 수행할지 여부를 제어하기 위해 하이퍼파라미터를 추가합니다
