김영한님의 [실전! 스프링 부트와 JPA 활용2 - API 개발과 성능 최적화](https://www.google.com/search?q=https://www.inflearn.com/course/%25EC%258A%25A4%25ED%2594%2584%25EB%25A7%2581%25EB%25B6%2580%25ED%258A%25B8-JPA-%25ED%2599%259C%25EC%259A%25A9-2/dashboard) 실습 코드 아카이브

---

### 💻 Development Environment

* Java 21
* Spring Boot 4.0.2
* Gradle
* Database: H2
* IDE: IntelliJ
* Tool: Postman (for API Testing)

### 🏆 실습 목표

* REST API 개발 시 엔티티를 직접 노출하는 문제점을 이해하고 DTO를 활용한 올바른 설계를 습득
* JPA 지연 로딩(Lazy Loading)으로 인한 N+1 성능 문제를 페치 조인(Fetch Join)으로 해결
* 컬렉션 조회 시 페이징 처리의 한계를 이해하고 `hibernate.default_batch_fetch_size` 등을 통한 최적화 방법 마스터
* OSIV(Open Session In View)의 동작 원리를 이해하고 실무 상황에 맞는 성능 최적화 전략 수립

### 📝 Curriculum

1. [**API 개발 기본**](https://mxxikr.github.io/posts/spring-boot-jpa-api-development-basics/)
  * 회원 등록, 수정, 조회 API 구축
  * 엔티티 직접 노출 시 발생하는 보안 및 스펙 결합 문제 분석과 DTO 변환 원칙 정립


2. [**API 개발 고급 - 준비**](https://mxxikr.github.io/posts/spring-boot-jpa-api-advanced-preparation/)
  * 지연 로딩 및 성능 최적화 테스트를 위한 주문, 배송, 상품 샘플 데이터 구축


3. [**API 개발 고급 - 지연 로딩과 조회 성능 최적화**](https://mxxikr.github.io/posts/spring-boot-jpa-api-lazy-loading-optimization/)
  * 다대일(N:1), 일대일(1:1) 관계에서 발생하는 N+1 문제 원인 분석
  * 페치 조인(Fetch Join)을 적용하여 단일 쿼리로 성능을 끌어올리는 방법
  * JPA에서 DTO로 직접 조회하여 네트워크 전송량을 최적화하는 전략 비교


4. [**API 개발 고급 - 컬렉션 조회 최적화**](https://mxxikr.github.io/posts/spring-boot-jpa-api-collection-query-optimization/)
  * 일대다(1:N) 컬렉션 조회 시 발생하는 데이터 중복(뻥튀기) 현상 이해
  * 페치 조인과 페이징을 함께 사용할 때 발생하는 메모리 초과 문제 분석
  * `default_batch_fetch_size` 설정을 통한 페이징 한계 돌파 및 IN 쿼리 최적화
  * 플랫 데이터 최적화 등 실무에서 활용하는 단계별 컬렉션 조회 최적화 전략 비교 및 마스터


5. [**API 개발 고급 - 실무 필수 최적화**](https://mxxikr.github.io/posts/spring-boot-jpa-api-osiv-optimization)
  * OSIV(Open Session In View)의 생명주기와 데이터베이스 커넥션 반환 시점 이해
  * 실무적인 관점(Command와 Query의 분리)에서 OSIV 활성화/비활성화 전략 선택


6. [**다음으로**](https://mxxikr.github.io/posts/spring-boot-jpa-spring-data-jpa-querydsl)
  * 실무 필수 기술인 스프링 데이터 JPA 및 QueryDSL의 필요성과 도입 배경 소개
