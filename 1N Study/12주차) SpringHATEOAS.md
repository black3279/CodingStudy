## 2021/06/19 송명진 프로

# Spring HATEOAS

## HATEOAS
- Hypermedia As The Engine Of Application State 의 약자로 REST 아키텍처의 한 구성요소
- 이 HATEOAS를 통해서 어플리케이션의 상태를 전이할 수 있는 메커니즘을 제공할 수 있다

- 카카오 헤어샵의 경우, 이벤트의 상황이나 스타일러에 따라 _links 에 다양한 태그를 붙여서 분기시키고 있다.

## 프로세스와 쓰레드
- 프로세스 간 통신은 IPC 를 사용하며 속도가 느린 반면에, 쓰레드는 같은 메모리를 공유하므로 쓰레드 간 통신속도가 빠르다

## Browser 아키텍처
- 브라우저는 한 탭마다 프로세스를 생성한다.
- 브라우저 프로세스는 어플리케이션의 chrome 부분 ( 주소표시줄, 앞으로 가기... ) 과 권한 부분을 처리한다.
- 렌더러 프로세스는 탭 안에서 웹 사이트가 표시되는 부분의 모든 것을 제어한다
- 플러그인 프로세스는 웹 사이트에서 사용하는 플러그인 을 제어한다.
- GPU 프로세스는 요청받은 내용을 그리기 때문에 별도 프로세스로 분리되어 있다.

## 다중 프로세스 아키텍처의 이점
- Chrome 이 렌더러 프로세스를 여러 개 사용한다
- 여러 프로세스에 나눠서 처리하는 방법은 보안과 격리에서 장점이 있다.
- 크롬은 한번에 호출할 수 있는 양이 정해져 있다
- chrome 67 부터는 iframe 에 별도의 렌더러 프로세스를 적용하도록 변경되었다

### https://github.com/RumbleKAT/WeekEndStudy/blob/main/spring-hateoas.md

### https://github.com/RumbleKAT/WeekEndStudy/blob/main/cpu-gpu-memory-and-multi-process.md