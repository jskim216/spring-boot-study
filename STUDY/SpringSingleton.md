## Spring 과 Singleton

### Singleton 패턴

- 객체의 인스턴스가 오직 1개만 생성되는 패턴
- 최초 생성 이후 호출된 생성자는 최초의 생성자가 생성한 객체를 리턴
- 장점
  - 불필요한 메모리 누수를 방지하고 하나의 인스턴스로 데이터 공유가 쉽다
- 단점
  - SOLID 원칙중 DIP 를 위반하고 OCP 또한 위반할 가능성이 높음
  - 멀티 쓰레드 환경에서 동시성 문제
  - 테스트가 어렵고 상속이 불가능
  - 유연성이 떨어짐

### Spring 의 Singleton

- Spring 은 직접 Singleton 형태의 오브젝트를 만들고 관리하는 기능을 제공 > Singleton Registry
- 이를 통해 Singleton 패턴의 단점을 보완
- 일반 자바 클래스를 싱글톤으로 활용할 수 있도록 지원
- 생성, 관계설정, 사용에 대한 제어권이 컨테이너에게 있기 때문에 일반 자바 클래스도 싱글톤으로 관리
- 객체지향적 설계와 디자인 패턴 적용이 가능

### 주의사항

- 기본적으로 Spring 은 멀티쓰레드 환경
- 상태정보를 내부에 가지고 있지않은 stateless 방식이어야함
- 즉, Thread-Safe 해야함

### 동시성 문제

- 멀티 쓰레드 환경에서 발생하는 문제로 여러 쓰레드가 동시에 동일한 자원에 접근하여 수정시 발생
- 싱글톤 객체에 단순 조회는 동시성 문제가 발생하지 않음
- 동일한 자원에 접근하여 수정을 할 때 발생
- 동시성 문제는 지역변수에서 발생하지 않음. 쓰레드마다 각 다른 메모리 영역이 할당 되기 때문.
- 동시성 문제를 해결하는 방법은 여러가지가 있으나 추후 천천히 알아봄..