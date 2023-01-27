## Spring 에서 쿼리를 작성하는 방법들

### Query Method (Spring JPA Data)
- Spring JPA DATA 가 제공하는 기능으로 메소드 이름을 통해 쿼리를 생성
- 메소드명에 조건절을 붙이는 형태로 간단히 작성 가능
- 하지만 조건이 많아지다보면 가독성이 떨어지는 단점이 있음
- 관련 레퍼런스 : https://docs.spring.io/spring-data/jpa/docs/current/reference/html/#jpa.query-methods

### JPQL
- 테이블이 아닌 객체를 검색하는 객체지향 쿼리
- SQL을 추상화하여 특정 데이터베이스에 의존하지 않음
- JPA 에 의해 SQL로 변환되어 수행

### Criteria API
- JPQL을 생성하는 빌더 클래스
- 자바코드로 JPQL을 작성할 수 있음
- 이에 컴파일단계에서 오류를 발견 가능
- 동적쿼리 작성에 유리하나 코드가 복잡하고 장황해짐. 직관적이지 못해 불편함
- 잘 안쓰는듯?

### QueryDSL
- 정적 타입을 이용해서 SQL 등의 쿼리를 생성해주는 프레임워크
- 자바코드로 JPQL을 작성할 수 있음
- 이에 컴파일단계에서 오류를 발견 가능
- 동적쿼리 작성에 유리
- Gradle 설정 및 사용법 등을 익혀야함
- 별도의 Q class 를 만들어 사용