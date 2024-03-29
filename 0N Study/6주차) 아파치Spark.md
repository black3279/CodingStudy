2021/04/17
## 장원용 스터디

- 분산 프로그래밍이란 큰 데이터를 여러 디스크로 나눠서 병렬로 액세스하여 빠르게 처리하는 방법이다.
- 하둡은 HDFS(Hadoop Distributed File System) 이라고 불리는 분산형 파일시스템에 데이터를 올린다.
- HDFS 와 맵 리듀스 프로그램을 하둡이라고 볼 수 있다.
- 데이터 처리 중간 과정 등도 DISK IO 를 기반으로 여러번 하므로 속도 측면에서 부담이 있다.
- 따라서, 배치성으로 데이터 처리를 하는 경우에는 적합하고 실시간성 데이터 처리에는 부적합하다.
- 따라서, 이러한 실시간성 데이터를 처리하는 아파치 스파크가 등장했다.

### 아파치 스파크
- 인메모리 (캐싱) 을 이용한다.
- 스파크는 자바, R, 파이썬, 스칼라로 개발할 수 있다.
- 스파크는 인메모리 기반으로 동작하기 때문에 반복처리 작업에서 하둡에 비해 속도가 약 100배 이상 빠르다.
- 인메모리 기반 툴의 경우, 휘발성 데이터므로 백업 플랜이 필요하다.

### Spark 구조
- 스파크는 마스터-슬레이브 구조로 실행되며, 여러 슬레이브에 시킨 작업의 값을 마스터가 받아 처리한다.
- Driver Program 이 Master, Worker Node 가 슬레이브가 되어 Task 작업을 처리한다.
- Cluster Manager 는 드라이버와 Worker Node 가 통신하며 일할 수 있도록 관리해준다.
- 스파크 클러스터는 생성 및 환경설정 (setMaster...) 을 한다.

### RDD (Resilient Distributed Datasets)
- RDD 는 회복력을 가진 분산 데이터 집합이다.
- 장애시 복구 계획 (Resilent) => RDD Lineage 참고
- 처리연산을 미뤄두었다가 한번에 처리하는 레이지 프로파게이션과 같은 방법으로 처리한다.
- 트랜스포메이션, 액션의 두가지 연산을 갖는다.

