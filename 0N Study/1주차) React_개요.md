[송명진 스터디] https://github.com/RumbleKAT/ReactStudy

Mosaic 브라우저가 브라우저의 시작
동적인 웹브라우저를 만들기위해 스크립팅 언어를 만듦
만들어진 동적인 언어 : Java Scheme 라는 언어
LiveScript 가 JavaScript 로 명명이 됨 ( Java 를 그때 많이 쓴다고해서 )
인터프리터 언어는 기계어가 아니라 소스코드를 바로바로 실행하는 방식, 중간에 잘못된게 있으면 에러를 그때그때 뱉는 방식이어서 컴파일러보다 더 빠르고 컴파일 단계가 필요없음
넷스케이프에서 1995 부터 익스플로러를 많이 쓰게 되었는데, 브라우저에서는 버전에 따라 호환성이 달라서 해당을 살펴볼 필요가 있음
Polyfill 은 크로스 브라우징을 지원하는 라이브러리이다.
Jscript 는 익스플로러사에서 쓰는 엔진이다.
학술단체에서 JS의 통합과 정리를 하고자 ECMAScript1 을 1997년에 정의함.
2000년 까지 인터넷 익스플로러가 대세이다가 2004년에 Firefox 가 ActionScript를 만들어서 출시했으나 모든 브라우저의 표준을 맞추지는 못함
2015년 2014년까지 넷스케이프, 인터넷 익스플로러, Firefox 가 대세이다가 2004년에 AJAX가 만들어짐.
AJAX 는 웹페이지의 속도가 상승되고 비동기 처리가 가능하며 서버에서 데이터만 제공하면 되므로 전체적인 코드량이 줄어든다.
파싱으로 인한 화면 깜빡임이 있었는데 AJAX 로 인해 유저 경험이 상승되었다.
하지만 히스토리 관리가 안되고 연속 데이터 요청 시 서버부하 증가 등 단점이 있었다.
이후에 JQuery 가 생겼다.
2015년에 생긴 ECMAScript6 는 6년 밖에 안됐으며 클래스, 람다 등을 제공하게 되었다.
TypeScript 는 일종의 JavaScript 버전에 따라서 버전호환을 지원하는 스크립트이다.
TypeScript 는 타입을 붙여주는데, JavaScript 의 경우 Object 자료형이 많아서 타입변환 시 발생하는 Side effect 를 TypeScript 에서는 보완할 수 있다.
Babel 은 JavaScript 컴파일러인데, 브라우저 호환성을 맞춰줄 수 있는 컴파일러이다.
크롬은 C++ 기반 V8 Javascript 엔진을 쓴다.
create-react-app 을 사용해서 리액트 프로젝트를 자동으로 만들어줄 수 있다.
크롬 데브툴즈에서 리액트 프로젝트가 생겼는지 확인하는 플러그인이 있는데 각 엘리먼트들이 호출되는 시간, 성능을 검사할 수 있다.
SPA ( Single Page Application ) : App.js 랑 앱테스트소스, 렌더링하는 ReactDOM, index 가 있는데 리액트는 js로 렌더링하여 구성한다.
SPA 에는 React, Angular, Vue 등이 있는데 클라이언트 사이드 렌더링하여 반응이 빠르다.
Next.js 는 리액트를 Server Side Rendering 으로 사용하기 위해 만들어졌다. 이를 사용하여 자바스크립트로 추가된 엘리먼트를 뿌려줄 수 있다.
Gatsby 라이브러리는 서버 사이드 렌더링을 지원하는 라이브러리이다.
Nuxt.js 는 뷰에서 서버 사이드 렌더링을 제공해주는 라이브러리이다.
Call Stack : 자바스크립트는 1개의 동시성을 다루는, 즉 단일 콜스택을 갖는다.
자바스크립트에서는 함수 호출이 스택형태로 쌓인 뒤, 상단부터 하나씩 리턴하는 방식으로 실행된다.
자바스크립트 엔진이 구동되면서 변수, 함수같은 정보가 메모리 힙에 저장되며 바라보는 곳이 없을 경우 프리시킨다.
비동기 함수는 큐에 저장되며 콜스택이 모두 실행된 후에 이벤트 큐가 실행된다.
동시성 모델에서 자바스크립트는 Non blocking 언어여서 비동기로 처리할 수 있으면 동시성을 최대한 높일 수 있게 작동한다.
콜스택 CPU 바운드 쪽 작업을 한 후, 이벤트 큐 DB 바운드 등의 응답을 받아서 콜스택이 작동한다.
스프링의 경우, DB 에서 값을 불러오는 동안 블로킹된다.
async & await : Premise 의 업그레이드 버전으로 블로킹으로 작동할 수 있도록 해준다.
리액트 JSX : Javascript + XML 로 이루어진 자체적인 언어
웹 브라우저에서 HTML 문서 렌더링 과정은 불러오기, 파싱, 렌더링 트리 만들기, CSS 결정, 레이아웃, 그리기 순서로 작동한다.
인덱스 트리에서 트리의 값이 바뀌면 자식 트리에 영향이 발생하는데, 리액트는 가상돔을 사용하여 자식 트리에 영향을 주지 않고 해당 변화점에만 연산이 생긴다.
자바스크립트에서는 === 까지 해야 자료형까지 비교하고 == 를 하면 값만 비교한다.
리액트 돔에서는 리액트 돔으로 한번 더 감싸서 XSS 공격을 방어할 수 있다.
리액트 돔 상에서는 엘리먼트끼리 깊은 비교가 아닌 얕은 비교를 하여 자식 트리와 비교를 하여 변화가 생겼는지 아닌지를 판단하여 연산이 빠르다.
리액트 라이프사이클 : 리액트 17 부터는 componentWillMount, componentWillUpdate, componentWillReceiveProps 라이프사이클이 deprecated 된다.
리액트 클래스 컴포넌트 : 헤더 컴포넌트를 만들때 컴포넌트를 상속받아 렌더 함수에서 태그를 리턴하는 방식이다.
최근 업무로 사용되는 Function 형태는 리액트 훅을 사용한다.
리액트 훅 : 예를 들어 변화를 주는 변수를 넣어서 새로운 상태 값을 정의하고 사용할 함수를 넣어서 표현한다.
원래같으면 클래스 컴포넌트 안에 Function 을 선언하고 setState 를 써서 코드가 길었는데, 함수형 리액트 훅을 사용하면 간결하게 표현이 가능하다.
이펙트 훅 : componentDidMount, componentDidUpdate 도 써야하는 것을 유즈 이펙트만 써서 컴포넌트를 가볍게 만들었다.
리듀서 : JS 기본 Function 중 배열에 있는 전체 값을 더해 새로운 value 로 리턴함.
리액트에서 리듀서는 이벤트 상태값과 액션들을 모아서, 액션의 타입 케이스 별로 상태 값을 리턴해준다.
리듀서를 사용할 것이라고 정의를 해놓으면 리듀서 안에서 상태 값을 바꿔서 전달을 해준다.
리듀서를 최근에 사용하는 이유는, 부모에서 자식으로 내려가는 데이터의 흐름 뿐만 아니라 자식에서 발생한 변화를 부모에게도 흘려주는 일괄적 관리를 위해 사용한다.
Redux 와 같은 역할이다.
리듀서는 Store 안에 있는 변수를 관리한다.
발행-구독 모델 : 카스카 등 비동기 메시징 패러다임이다. 구독을 누르고 나면 구독자에게 알림 메시지가 가는 것처럼 리듀스는 컴포넌트가 구독을 누르면 값이 변화했을때 구독자들에게 변화값을 전달해주는 것이다.
Redux-thunk : 디스패치 액션이 일어나고 끝났을 때 스토어에게 전달하는 비동기 과정을 도와줄 때 redux-thunk 를 사용한다
Redux-saga : 미들웨어에서 API 를 호출하고 비동기의 후처리 등 부가적인 기능들을 제공한다.
React-Redux : 리액트에서 만들지는 않았지만 대중적으로 사용되는 라이브러리이다.
createStore : Store 를 만들어준다, createStore(reducer) 와 같은 형태로 구독을 만들어준다.
리액트에서 Provider 라는 객체를 만드는데 App 을 상속하는 자식 컴포넌트들도 Store 에 접근하여 이를 상속한 자식끼리 서로의 상태값에 접근할 수 있다.
userReducer : 리액트 17버전 정도 부터 리액트 내부적으로 지원해주는 기능이다.
create-react : Velopert gitbook > 벨로퍼트와 함께하는 모던 리액트 참고

https://react.vlpt.us/
cf) Generator 문법, 유투브 라이브 강의 등