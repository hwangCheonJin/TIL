SpringDataJpa
=============
```java
package hello.hellospring.repository;

import hello.hellospring.domain.Member;
import org.springframework.data.jpa.repository.JpaRepository;

import java.util.Optional;

public interface SpringDataJpaMemberRepository extends JpaRepository<Member, Long>, MemberRepository {
    @Override
    Optional<Member> findByName(String name);
}

```

SpringDataJpa는 interface로 만들어주며, springframework에 있는 JpaRepository를 호출하여 사용한다.

JpaRepository에는 기본적인 쿼리문이 작성되어있어 따로 구현 클래스를 만들어줄 필요가 없으며,
위 예의 findByName처럼 현업에서 예상 불가능한 쿼리문은 따로 선언해준다.

복잡한 동적 쿼리는 Querydsl을 사용하여 작성하고, 이 조합으로 해결하기 어려운 쿼리는
JPA가 제공하는 네이티브 쿼리를 사용하거나 JdbcTemplate을 사용하여 작성한다.
