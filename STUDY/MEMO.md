## 강의 수강중 정리

### Map
> key / value 쌍으로 이루어진 자료형으로 리스트나 배열과는 다르게 

### 동시성

### Optional

### 람다식

### Test

> Test 시 순서는 상관이 없이 수행된다.
> @AfterEach 를 통해 테스트 종료마다 해당 메소드를 수행한다.
> 

## SPRING BOOT 2.x.x 와 3.0 차이점
> Java 17 이상 필요 <br/>
> GraalVM Native Image Support <br/>


섹션5
- 컨트롤러가 정적 컨텐츠보다 우선순위가 높음
- PostMapping 시 정의된 MemberForm 클래스를 받을 시 넘어옴 form 의 key 값에 맞춰 스프링에서 set 을 해줌
  - 이건 좀 신기하네.
- model addAttribute

섹션6
- OCP (개발-폐쇄 원칙)
  - 확장에는 열려있고 수정/변경에는 닫혀있음
- 스프링통합테스트
  - @SpringBootTest 어노테이션으로 스프링 컨테이너를 띄워서 통합테스트
  - @Transactional 어노테이션을통해 테스트 후 데이터 롤백을 지원
  - 단위 테스트
    - 순수 Java 코드를 통한 세부 단위 테스트
  - 통합 테스트
    - 스프링 컨테이너 및 DB 접근 등 통합적인 테스트
- JdbcTemplate
  - Jdbc 이용시의 반복적인 코드를 줄임
- JPA
  - application properties 설정
    - spring.jpa.hibernate.ddl-auto : 객체를 보고 테이브를 자동 생성옵션
  - JPA 는 자바표준 인터페이스
  - Hibernate 는 위 인터페이스의 구현체 중 하나
- ORM
  - 
- EntityManager
  - 
- JPA 의 모든 요청은 Transaction 하에 진행되어야함
- 쿼리 생성
  1. Method Naming (Spring JPA Data)
     - https://docs.spring.io/spring-data/jpa/docs/current/reference/html/#jpa.query-methods
  2. JPQL
  3. Criteria API
  4. QueryDSL

- AOP (관점 지향 프로그래밍)
  - 핵심 관심사항과 공통 관심사항의 분리
- Spring 에서의 AOP