스프링 빈과 의존관계
=================
컴포넌트 스캔과 자동 의존관계 설정

1. 컴포넌트 스캔 (생성자를 통한 스프링 빈 등록)

컴포넌트 스캔이 있으면 자동으로 객체를 생성한다.

>ex) @Controller, @Service, @repository
> 
>위 예들은 컴포넌트(@Component)를 포함하고 있으며 자동으로 스프링 빈으로 자동 등록된다.

```java
package hello.hellospring.controller;
import hello.hellospring.service.MemberService;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Controller;
@Controller
public class MemberController {
private final MemberService memberService;
@Autowired
public MemberController(MemberService memberService) {
this.memberService = memberService;
}
}
```

생성자에 @Autowired 가 있으면 스프링이 연관된 객체를 스프링 컨테이너에서 찾아서 넣어준다.

- 이렇게 객체 의존관계를 외부에서 넣어주는 것을 DI (Dependency Injection), 의존성 주입이라 한다.


2. 자바 코드로 직접 스프링 빈 등록하기

컴포넌트 스캔과 자동 의존관계 설정

```java
package hello.hellospring;
import hello.hellospring.repository.MemberRepository;
import hello.hellospring.repository.MemoryMemberRepository;
import hello.hellospring.service.MemberService;
import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;
@Configuration
public class SpringConfig {
@Bean
public MemberService memberService() {
return new MemberService(memberRepository());
}
@Bean
public MemberRepository memberRepository() {
return new MemoryMemberRepository();
}
}
```

개방-폐쇄 원칙(OCP, Open-Closed Principle)
- 확장에는 열려있고, 수정,변경에는 닫혀있다.
스프링의 DI (Dependencies Injection)을 사용하면
기존 코드를 전혀 손대지 않고, 설정만으로 구현 클래스를 변경할 수 있다.

>참고: 실무에서는 주로 정형화된 컨트롤러, 서비스, 리포지토리 같은 코드는 컴포넌트 스캔을 사용한다.
그리고 정형화 되지 않거나, 상황에 따라 구현 클래스를 변경해야 하면 설정을 통해 스프링 빈으로
등록한다.
> 
> 
> 주의: @Autowired 를 통한 DI는 스프링이 관리하는 객체에서만 동작한다.
> 스프링 빈으로 등록하지 않고 내가 직접 생성한 객체에서는 동작하지 않는다.