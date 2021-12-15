## 20211212 송명진 프로
### https://github.com/RumbleKAT/graphQLStudy
- SQL 은 DBMS 에 저장된 데이터를 효율적으로 가져오는 것이 목표인 반면 GraphQL은 웹 클라이언트가 데이터를 서버로부터 효율적으로 가져오는 것이 목적이다.
- BFF(Backend for Frontend) 란 백엔드에 있는 서버가 각 서버의 데이터를 묶어서 화면단으로 넘겨주는 MSA 패턴이다.
- 웹 뿐만 아니라 모바일 등으로 다양화되면서 헤비 트래픽을 감당하기 위해 BFF 패턴이 쓰이게 되었다.
- BFF 패턴으로 GraphQL 이 많이 쓰이고 있다.
- Query 를 쓰면 Query Language Processer 가 Parsing 과 Validating 을 한다.
- 실제로 GraphQL 비즈니스 로직 코드가 들어가는 Resolver 에서 RDB 이든 NoSQL 이든 In memory DB 든 Resolver 를 구현하면 결과적으로 Output 은 JSON 으로 나온다.