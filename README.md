# SPRING PLUS

---

스프링 플러스주차 개인 과제입니다.

주어진 코드를 요구사항에 맞게끔 수정하여 문제를 해결합니다.

과제 구현은 Lv2의 9.Spring Security 까지 진행했습니다.

+ Lv1 - 1에선 클래스 단위에 적용되어있던 트랜잭션을 메서드 단위로 각각의 용도에 맞는 트랜잭션을 적용하여 해결했습니다.


+ Lv1 - 2에선 User 엔티티에 nickname 필드를 추가하고, Jwt 관련 부분도 수정하여 토큰에서 닉네임을 추출할 수 있도록 수정했습니다.


+ Lv1 - 3에선 Repository에 동적 필터링을 적용하여 검색 기능을 구현했습니다.


+ Lv1 - 4에선 테스트코드는 예외 발생 상황을 가정하였는데, 기대하는 Http Code가 Ok였고, 이를 Bad Request로 수정하여 해결했습니다.


+ Lv1 - 5에선 AOP가 메서드 실행 전 동작해야하는데, @After어노테이션이 붙어있었고, 경로 또한 잘못 작성되어있었습니다. 따라서 @Before어노테이션으로 변경하고, 경로를 수정하여 해결했습니다.


+ Lv2 - 6에선 CascadeType을 ALL로 할지 PERSIST로 할지 고민하던 중 일정 삭제 시 담당자도 삭제되는것이 옳다고 생각해 ALL을 적용하여 해결했었습니다.
그러나 추후 CascadeType을 여러가지를 적용할 수 있다는 사실을 알게되었고, PERSIST와 REMOVE를 함께 적용하도록 변경하였습니다.


+ Lv2 - 7에선 Repository 쿼리문에 JOIN FETCH가 적용되도록 수정하여 해결했습니다.


+ Lv2 - 8에선 QueryDSL을 처음 사용해보았고, QueryDSL을 사용하는데에 약간의 어려움이 있었습니다. 우선 설정 클래스를 생성하여 JPAQueryFactory를 Bean으로 주입하는것부터 전용 Repository와 그 구현체를 만들지 않고 기존의 Repository 내에서 해결할 수 있는 방법이 없는지 시도하며 시행착오를 겪었고, 어째서 Repository를 분리하여 사용하는지와 같은 일련의 과정에 대한 궁금증이 있었습니다. 구글링 등을 활용해 정보를 찾아보며 궁금증을 해소하였고, 기존 JPQL구조의 메서드를 QueryDSL구조로 수정했습니다.

+ Lv2 - 9에선 기존의 JWT필터를  Spring Security를 사용하도록 수정하였습니다.


---

# 트러블슈팅 

---

[겪었던 트러블 내용](https://velog.io/@4ou_chan/Spring-%ED%94%8C%EB%9F%AC%EC%8A%A4%EC%A3%BC%EC%B0%A8-%EA%B0%9C%EC%9D%B8%EA%B3%BC%EC%A0%9C-%EC%A7%84%ED%96%89-%EC%A4%91-%EC%96%B4%EB%A0%A4%EC%9B%A0%EB%8D%98-%EB%B6%80%EB%B6%84)
