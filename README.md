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

1. **API 개발 기본**
   * 회원 등록, 수정, 조회 API를 직접 개발하며 엔티티 직접 노출의 문제점 분석
   * 엔티티를 외부에 노출하지 않고 별도의 DTO(Data Transfer Object)로 변환하여 응답하는 원칙 정립


2. **API 개발 고급 - 지연 로딩과 조회 성능 최적화**
   * 주문 조회 V1: 엔티티를 직접 노출할 때 발생하는 양방향 연관관계 문제(`@JsonIgnore`)
   * 주문 조회 V2: 엔티티를 DTO로 변환했지만 여전히 발생하는 지연 로딩 N+1 문제 확인
   * 주문 조회 V3: **페치 조인(Fetch Join)**을 적용하여 쿼리 1번으로 조회 성능 최적화
   * 주문 조회 V4: JPA에서 DTO로 바로 조회하여 SELECT 절을 최적화하는 방법


3. **API 개발 고급 - 컬렉션 조회 최적화**
   * 컬렉션 조회 V1~V2: 일대다(`1:N`) 관계 조회 시 데이터 뻥튀기 현상과 N+1 문제
   * 컬렉션 조회 V3: `DISTINCT`를 사용한 중복 제거와 페치 조인 최적화
   * 컬렉션 조회 V3.1: **페이징과 한계 돌파** - `default_batch_fetch_size`를 활용한 최적화
   * 컬렉션 조회 V4~V6: JPA에서 DTO 직접 조회, 플랫 데이터 최적화 등 다양한 전략 비교


4. **API 개발 고급 - 실무 필수 최적화**
   * **OSIV**(Open Session In View)의 동작 원리와 DB 커넥션 유지 전략 분석
   * 성능과 커맨드/쿼리 분리(CQS) 관점에서 OSIV를 끄고 켜는 전략적 선택
   * 복잡한 쿼리를 다루기 위한 스프링 데이터 JPA와 Querydsl 소개