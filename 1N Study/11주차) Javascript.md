- 2021/06/12 장태진 프로
- https://github.com/Ryze0323/boj/blob/master/js2.md

# Javascript

## loadsh
- js 유틸 라이브러리이다.

1) .head(array) : 배열의 첫번째 요소를 리턴
2) .assign(obj, obj ... ) : 오브젝트를 병합하는 함수

## merge, defaults, defaultsDeep
	
	- merge, assign 은 같은 필드를 마지막 값으로 덮어쓴다.
	- defaults, defaultsDeep 는 같은 필드면 덮어쓰지 않는다.

	### undefined
		- assign 은 undefined 도 덮어쓴다.
		- merge 는 undefined 는 덮어쓰지 않는다.
		- defaults,defaultsDeep 는 undefined 는 값이 없는 것으로 판단하여 덮어쓴다.

	## 배열
	- assign, defaults 는 배열도 값으로 인식하여 덮어쓴다.
	- merge, defaultsDeep 은 배열은 병합한다.

## get(object,path)
- path 의 object 에서 값을 가져온다.
- path 를 지정해줄 때는 a[0].b.c 와 같은 식으로 사용한다.

## map(collection, iterator)
- iterator 를 통해 collection 각 요소들을 뽑아 array 를 반환한다.
- key : value 형태로 넣어도 value 값을 뽑아 사용한다.
- 이상값의 경우, 배열에 NaN 이나 undefined 를 넣어서 반환해준다.

## forEach(collection, iterator)
- 첫번째 파라미터가 value, 두번째 파라미터가 key 이다.
- 배열의 경우, key 는 index 로 가져오고 key 값이 있을 경우 해당 값을 가져온다.

## filter(collection, 콜백함수)
- 콜백함수를 통해 뽑아낸 값이 true 일 경우에만 반환한다.
- return o.속성 / { '키' : 값 } / \['키' : 값] / '키' 로 사용할 수 있다.

## isEmpty
- 해당 필드가 비어있는지 여부를 리턴한다.
- 빈 String 은 true, 숫자는 무조건 true, 빈 오브젝트는 true, Boolean 은 true 를 리턴한다.

# ES6 문법 정리
- 다양한 웹 브라우저에서 자바스크립트가 공통되게 잘 작동되기 위한 표준 문법

## Arrows Function
1) () => { ... }
2) x => { ... } // 매개변수가 한개 인경우 소괄호 생략

- 함수 몸체 지정 방법도 동일하게 한줄의 구문이라면 중괄호를 생략 가능하다.
- 하지만, 객체 반환 시에는 한줄 반환 시 소괄호를 사용해야 한다.

- ex) x => x+x; () => ({a : 1 });

- arrow function 은 언제나 상위 스코프의 this 를 가리키며 이를 Lexical this 라고 부른다.
- var 을 선언하여 this 를 미리 넣어주어 사용하는 방법도 있다.
- 객체 내에서 this 를 사용하면 화살표 함수에서는 window 객체를 가리킬 수 있다.
- \`{$this.... }\` 를 사용해볼 수 있다.

## 모듈
- 애플리케이션을 구성하는 개별적 요소로 재사용 가능한 코드 조각

- 모듈 스코프 : 독자적 스코프를 사용하지 않고 전역 스코프를 공유하는 문제를 해결하고자 스코프를 따로 가져가낟.
- 같은 변수 명을 사용한 js 파일을 사용하면 해당 값을 덮어쓰게 되기 때문에 module 을 적용하는 것이 좋다.
- ex) script type="module" src="..."

### export / import
- export : 모듈의 식별자를 외부에서 사용할 수 있도록 함수
- import : 위에서 export 에서 공개한 식별자를 로드하는 키워드

- import { pi, square, Person } 
- import { pi, square, Person } from './lib.js';
- import \* as lib from './lib.js'; => lib.pi 와 같은 형태로 사용
- 이름 변경하여 import 도 가능하다.