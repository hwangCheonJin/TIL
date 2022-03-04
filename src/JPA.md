JPA
==========

>spring.jpa.show-sql=true
> 
-JPA가 생성하는 SQL을 출력한다.

>spring.jpa.hibernate.ddl-auto=none
>
-JPA는 테이블을 자동으로 생성하는 기능을 제공하는데 none 를 사용하면 해당 기능을 끈다.

실무에서는 ddl-auto는 대부분 none값을 사용한다.
create 를 사용하면 엔티티 정보를 바탕으로 테이블도 직접 생성해주지만, 
보통은 테이블을 직접 구성하여 사용하기 때문에 사용하지 않는다.

*JPA는 테이블 대상이 아닌 엔티티를 대상으로 쿼리를 작성한다
그렇기 때문에 아래와 같이 코드가 다르다.*

*JPA EntityManager 선언부*
```java
public class JpaMemberRepository implements MemberRepository {
private final EntityManager em;
public JpaMemberRepository(EntityManager em) {
this.em = em;
}
```

*JPA 회원가입 코드*
```java
public Member save(Member member) {
em.persist(member);
return member;
}
```

*JPA id를 이용한 검색*
```java
public Optional<Member> findById(Long id) {
Member member = em.find(Member.class, id);
return Optional.ofNullable(member);
}
```

*JPA 회원목록 불러오기*
```java
public List<Member> findAll() {
return em.createQuery("select m from Member m", Member.class)
.getResultList();
}
```

*JPA name을 이용한 검색*
```java
public Optional<Member> findByName(String name) {
List<Member> result = em.createQuery("select m from Member m where
m.name = :name", Member.class)
.setParameter("name", name)
.getResultList();
return result.stream().findAny();
}
}
```


