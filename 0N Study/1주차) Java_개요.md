[장원용 스터디]
https://wonyong-jang.github.io/java/2021/01/04/Java-Interface.html
https://wonyong-jang.github.io/java/2020/11/08/Java-JVM.html

.class 를 Class Loader 가 JVM 메모리에 적재
Execution Engine 이 실행
javac 를 통해 컴파일 java 로 실행
상위버전으로 컴파일후 낮은 버전으로 실행 시 에러
javac -source 옵션으로 특정버전으로 컴파일 할 수 있음
인텔리제이 shift 두번 바이트코드로 까볼수있음
javap -c 로 바이트코드 볼수있음
자바 8 부터 default static 메소드 추가
인터페이스에서는 static final , abstract 을 명시하지 않으면 자동으로 붙여서 컴파일한다.
interface 도 상속을 받을 수 있다, 메소드 명이 같고 리턴타입이 다르면 에러가 난다.
default 메소드를 사용하면 구현하고 싶은 클래스에만 구현하면 되어서 하위 호환성을 유지할 수 있다.
인터페이스에서 static 은 오버라이딩 불가
인터페이스 private 메소드도 캡슐화를 위해 나왔는데, private static 도 사용할 수 있다.
함수형 인터페이스의 경우 @FunctionalInterface 어노테이션을 붙여서 구현한다.
Constant Interface 상수만 리스트로해서 만드는 것이 좋다.