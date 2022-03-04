Data Type
=============

```java
public class DataType {
public static void main(String[] args) {
boolean isFun = true;
System.out.println(isFun);

        char c = 'f';
        System.out.println(c);

        int x = 59;

        long bing = 3435343343L;

        float f = 32.4F;

        double d = 342535.3;
    }
}
```
>논리형
1. boolean : true 혹은 false값을 가진다.
>문자형 
1. char : ''를 사용하여 한글자를 표현할 수 있다.
>정수형
1. byte : -128 ~ 127 까지 표현 가능하다.
2. short : -32,768 ~ 32767 까지 표현 가능하다.
3. char : 0 ~ 65 까지 표현 가능하다.
4. int : -2147483648 ~ 2147483647까지 표현 가능하다.
5. long : int에서 표현되지 않는 값에서 사용한다.
>실수형
1. float : 2^31 ~ +2^31-1 범위까지 표현 가능하다.
2. double : float으로 표현할 수 없는 범위에서 사용한다.