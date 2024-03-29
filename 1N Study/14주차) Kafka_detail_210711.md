- 2021/07/11 장원용 프로

## Kafka
- 일반적인 MQ 시스템 ( ex, RabbitMq ) 는 데이터를 가져갈 때 삭제하게 되는데, Kafka 는 가져가더라도 삭제하지 않고 하루정도 보관 후 압축하는 방식으로 진행한다.
- 파티션은 분산처리를 위해 존재한다.
- 하나의 토픽에 데이터를 밀어넣을 때 병목 현상이 발생할 수 있어, 병렬로 밀어넣기 위해 존재한다.
- 데이터 순서가 중요할 경우, 파티션을 하나만 두어야 한다.
- 파티션이 여러개 있고, 해당 파티션에 따라 고객 속성을 구분하여 넣을 수 있다.

### Zookeeper
- 파티션에서 어느 offset(인덱스) 까지 읽었는지, 어느 부분부터 읽는지 등에 대한 관리를 하고있다.
- Kafka 는 Zookeeper 위에서 돌아간다.

## 실습
- 메시지를 토픽 단위로 보내기 때문에, 토픽을 먼저 생성한다.
- replication-factor : 파티션 복제본 개수
- 프로듀서와 컨슈머를 실행하여 실시간으로 토픽으로 이벤트를 추가하고 받을 수 있다.
- 메시지 전송 시 라운드 로빈을 통해 전달하다보니 받을 때는 순서가 꼬이게 된다.
- 하지만, 각 파티션 내의 데이터에는 순서가 보장된다.
- 파티션 간에는 데이터가 들어오는 속도 등에도 영향을 받기 때문에 파티션 간에는 데이터 순서가 보장되지 않는 것으로 봐야한다.

참고) Kafkacat

## 카프카 인증
- 토픽을 발행하고 구독을 해서 데이터를 컨슘받는다.
- 이 과정에서 서버에 인증을 걸 수 있다.
- sasl 은 어플리케이션 프로토콜로부터 인증을 받아야 그 층에서 접근이 가능하다.
- ssl 방식은 프로듀싱할 때 메시지를 암호화하고 컨슈밍 할때 메시지를 복호화하는 방식을 사용할 수 있다.

### https://wonyong-jang.github.io/kafka/2021/02/09/Kafka-basic-concept.html
### https://wonyong-jang.github.io/kafka/2021/02/10/Kafka-message-order.html