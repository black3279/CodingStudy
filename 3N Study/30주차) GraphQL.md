## 20211212 송명진 프로
### https://github.com/RumbleKAT/graphQLStudy
- SQL 은 DBMS 에 저장된 데이터를 효율적으로 가져오는 것이 목표인 반면 GraphQL은 웹 클라이언트가 데이터를 서버로부터 효율적으로 가져오는 것이 목적이다.
- BFF(Backend for Frontend) 란 백엔드에 있는 서버가 각 서버의 데이터를 묶어서 화면단으로 넘겨주는 MSA 패턴이다.
- 웹 뿐만 아니라 모바일 등으로 다양화되면서 헤비 트래픽을 감당하기 위해 BFF 패턴이 쓰이게 되었다.
- BFF 패턴으로 GraphQL 이 많이 쓰이고 있다.
- Query 를 쓰면 Query Language Processer 가 Parsing 과 Validating 을 한다.
- 실제로 GraphQL 비즈니스 로직 코드가 들어가는 Resolver 에서 RDB 이든 NoSQL 이든 In memory DB 든 Resolver 를 구현하면 결과적으로 Output 은 JSON 으로 나온다.
- REST API 에 비하여 GraphQL 은 End point 가 하나로 통일되어 관리가 용이하다
- GraphQL 에서 쿼리는 읽는데 사용하고 뮤테이션은 데이터를 변조하는데 사용한다
- 여러 API 를 통해 조립함으로써 하나의 호출 수행으로 모든 데이터를 갖고 올 수 있으며 request/response 에 의존하는 의존도가 낮아진다.
- DBMS 에서는 SQL 작성하는 것과 달리 GraphQL 에선 이 과정을 리졸버에서 직접 구현해야 한다
  - 리졸버를 통해 DB 에서 데이터를 가져오거나 일반 파일이나 원격 데이터를 가져올 수 도 있다.
  - GraphQL 쿼리에는 각각의 필드마다 하나의 함수가 존재한다.
  - 이는 리졸버라고 하며 만약 리턴 값이 스칼라값(문자열이나 숫자같은 primitive 타입) 인 경우에는 실행이 종료된다.
  - 우리가 정의한 값일 경우에는 해당 타입의 리졸버를 호출한다.
  - 따라서, 연쇄적인 (재귀적으로) 호출이 가능하여 DBMS 관계에 대한 쿼리를 효율적으로 처리할 수 있다.
  - 리졸버 함수에는 내부적으로 DB쿼리가 존재하므로 쿼리에 맞게 필요한만큼 최적화해서 사용하고 로직은 비즈니스단에 작성한다.
