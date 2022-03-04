Operator(연산자 우선순위)
=============
```java
public class Operator3 {
    public static void main(String[] args) {
        int a = 5;
        int b = 10;
        int c = 15;

        System.out.println((a - b) * c); // 괄호 우선순위가 높고 그후 곱셈 우선순위

        System.out.println(a > b || b > 5); 비교연산자 > 이 논리연산자 || 보다 우선순위가 높다

        System.out.println(++a - 5); //산술연산자보다 단항연산자가 우선순위가 높다.
//      전위 연산자의 경우 ++이 먼저 실행되지만 후위연산자 a++의 경우는 a-5가 먼저 실행된 후 1을 증가시켜준다.

        System.out.println(a);
    }
}
```

괄호 연산자가 가장먼저 실행된 후
단항 > 산술 > 비교 > 비트 > 논리 > 삼항 > 대입 순으로 실행된다.
