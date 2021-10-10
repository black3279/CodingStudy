2021/04/17
## 송명진 스터디

## 토비의 스프링 3.1
- 레거시에 레거시가 더해져 try catch 문이 복잡해지는 상황에서 중복을 제거하고 템블릿/콜백 패턴으로 설계한다.
- 템플릿이 파일을 열고 각 라인을 읽어올 수 있는 BufferedReader 를 만들어서 콜백에게 전달하고 최종결과만 템플릿에 전달한다.
- Callback 인터페이스 타입의 오브젝트를 실행한다.

### Template Method
- Callback 함수를 인터페이스로 구현하여 중복이 발생하는 부분을 제거한다.
- 제네릭으로 선언 시, 오브젝트 타입과 관계없이 작동하는 콜백 인터페이스를 구현가능하다.

https://app.gitbook.com/@rumblekat/s/weekendstudy/template-callback-pattern