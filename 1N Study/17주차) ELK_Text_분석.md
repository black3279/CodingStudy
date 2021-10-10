## 2021/08/22 장원용 프로
# ELK Text 분석
## 1) Inverted Index
- 전통적인 RDBMS 에서 단어를 검색하는 경우 열을 한줄씩 찾아 내려가기 때문에 속도가 느리다
- 엘라스틱 서치는 데이터를 저장할 때 역 인덱스라는 구조를 만들어 저장한다
- 역 인덱스는 각 키워드(Term) 에 문서 id 를 맵핑하여 리스트로 가지고 있는 것이다
- 데이터가 늘어나는 경우에도 id 의 배열값이 추가되는 것이기 때문에 속도의 저하가 크지 않으며 이를 색인이라 표현한다

## 2) Text Analysis
- 텍스트 데이터가 입력되면 필요에 따라 특정 문자를 대치 또는 제거하는 캐릭터 필터를 거친다
- 다음으로 문장에 속한 단어들을 텀 단위로 분리하는 토크나이저를 거친다
  - 토크나이저는 반드시 1개만 적용이 가능하다
- 분리된 Term 들을 하나씩 가공하는 과정에 토큰 필터가 사용된다
  - 대소문자에 따라 단어가 다르게 색인될 수 있으므로 토큰필터 단에서 해당 병합을 해준다
  - 참고) snowball 토큰 필터, 동의어 필터

## 3) nori_tokenizer
- nori_tokenizer 를 사용하면 공백 분리 혹은 한글사전을 이용한 분리가 가능하다
  - user_dictionary : 사용자 사전 저장된 파일 경로
  - user_dictionary_rules : 사용자 정의 사전을 배열로 입력
  - decompound_mode : 합성어 저장방식
    - none : 완성된 합성어만 저장 (어근 분리하지 않음)
    - discard (디폴트) : 합성어를 분리하여 각 어근만 저장
    - mixed : 어근과 합성어 모두 저장
## 4) nori readingform (토큰필터)
- nori readingform 토큰 필터는 한자로 된 단어를 한글로 바꾸어 저장한다

### 추가 실습 관련 깃헙
- https://wonyong-jang.github.io/elk/2021/06/18/ELK-Elastic-Search-analyze-korean.html
- https://wonyong-jang.github.io/elk/2021/06/19/ELK-Elastic-Search-analyze-korean2.html