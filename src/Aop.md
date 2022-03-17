Aop
=============
```java
package hello.hellospring.aop; 

import org.aspectj.lang.ProceedingJoinPoint;
import org.aspectj.lang.annotation.Around;
import org.aspectj.lang.annotation.Aspect;
import org.springframework.stereotype.Component;
import org.springframework.transaction.annotation.Transactional;


@Aspect
@Component
//@Transactional
public class TimeTraceAop {

    @Around("execution(* hello.hellospring..*(..))")
    public Object execute(ProceedingJoinPoint joinPoint) throws Throwable{
        long start = System.currentTimeMillis();
        System.out.println("START: " + joinPoint.toString());
        try{
            return joinPoint.proceed();
        }finally {
            long finish = System.currentTimeMillis();
            long timeMs = finish - start;
            System.out.println("END: " + joinPoint.toString() +" " + timeMs + "ms");
        }
    }
}
```
AOP는 핵심 관심사항과 공통 관심 사항을 분리한다.
위 예제에서는 핵심 관심사항은 hellospring아래있는 모든 메소드이며,
공통 관심 사항은 메소드들이 호출되고 실행되는데 걸리는 시간이다.

위 코드는 @Around를 이용해 경로를 설정해주고 hellospring아래있는
모든 메소드들이 호출되고 실행되는데 걸리는 시간을 ms단위로 구해주는 코드이다.

@component로 연결할때는 위 예제처럼 사용하면 되지만, @Bean으로 사용할 경우
위 코드 중 타겟을 설정해주는 코드가 아래 코드로 변경되어야 한다.
>@Around("execution(* hello.hellospring..*(..)) && !target(hello.hellospring.SpringConfig)")

아래 코드로 변환을 해주고 config에서 @Bean으로 TimeTraceAop를 등록해주면 된다.