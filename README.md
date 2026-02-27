      김영한님의 [실전! Querydsl](https://www.inflearn.com/course/querydsl-%EC%8B%A4%EC%A0%84/dashboard?cid=324476) 실습 코드 아카이브

---

### 💻 Development Environment

* Java 21
* Spring Boot 4.0.3
* Gradle
* Database: H2
* IDE: IntelliJ

### 🏆 실습 목표

* 문자열이 아닌 자바 코드로 쿼리를 작성하여 컴파일 시점에 문법 오류를 잡는 타입 안전성(Type Safety) 확보
* 복잡한 동적 쿼리를 `BooleanBuilder`와 `Where` 다중 파라미터를 활용해 구조적으로 처리하는 노하우 체득
* 사용자 정의 리포지토리 패턴을 도입하여 스프링 데이터 JPA와 Querydsl을 역할에 맞게 분리하고 연동하는 아키텍처 설계
* 데이터 조회 쿼리와 Count 쿼리를 분리하는 페이징 처리 기법 및 `@QueryProjection`을 활용한 DTO 프로젝션 조회 기술 마스터

### 📝 Curriculum

1. [**프로젝트 환경설정**](https://mxxikr.github.io/posts/spring-boot-querydsl-project-setup/)
    * 스프링 부트 환경에서 Querydsl 라이브러리 및 빌드 환경(Q-Type 생성) 설정
    * H2 데이터베이스 연동 및 JPA 설정 동작 검증


2. [**예제 도메인 모델**](https://mxxikr.github.io/posts/spring-boot-querydsl-domain-model/)
    * 다대일(N:1) 관계를 가진 회원(Member)과 팀(Team) 엔티티 설계 및 데이터 세팅


3. [**기본 문법**](https://mxxikr.github.io/posts/spring-boot-querydsl-basic-syntax/)
    * Q-Type 생성 확인 및 JPQL과 Querydsl의 작성 방식 비교
    * 검색 조건, 정렬, 페이징 로직 구현
    * 집합, 조인(기본 조인, 페치 조인), 서브 쿼리, Case 문, 상수/문자 더하기 등 SQL 대응 문법 습득


4. [**중급 문법**](https://mxxikr.github.io/posts/spring-boot-querydsl-intermediate-syntax/)
    * 프로젝션(기본, DTO 반환) 처리 방식 및 `@QueryProjection` 활용
    * `BooleanBuilder`와 `Where` 다중 파라미터를 이용한 동적 쿼리 작성법 비교
    * 영속성 컨텍스트를 우회하는 벌크 연산 처리와 SQL function 직접 호출


5. [**실무 활용 - 순수 JPA와 Querydsl**](https://mxxikr.github.io/posts/spring-boot-querydsl-practical-usage/)
    * 순수 JPA 리포지토리에 Querydsl을 적용하여 기본 조회 및 동적 쿼리 로직 구현
    * Builder 방식과 Where 파라미터 방식을 적용한 데이터 조회 API 컨트롤러 개발


6. [**실무 활용 - 스프링 데이터 JPA와 Querydsl**](https://mxxikr.github.io/posts/spring-boot-querydsl-spring-data-jpa/)
    * 사용자 정의 리포지토리를 구축하여 스프링 데이터 JPA 인터페이스에 Querydsl 구현체 연결
    * 데이터 내용 쿼리와 전체 Count 쿼리를 분리하여 실행하는 Querydsl 페이징 컨트롤러 개발


7. [**스프링 데이터 JPA가 제공하는 Querydsl 기능**](https://mxxikr.github.io/posts/spring-boot-querydsl-spring-data-features/)
    * `QuerydslPredicateExecutor` 및 Web 지원 기능의 한계점 분석
    * `QuerydslRepositorySupport`의 내부 구조 분석 및 실무 요구사항에 맞춘 커스텀 Querydsl 지원 클래스 구현
