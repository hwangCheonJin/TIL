Operator(삼항 연산자)
=============
```java
public class Operator5 {
    public static void main(String[] args) {
        int b1 = (5 < 4) ? 50 : 40;

        System.out.println(b1);

        int b2 = 0;
        if(5 < 4) {
            b2 = 50;
        }
        else {
            b2 = 40;
        }
        System.out.println(b2);
    }
}
```

위의 두 식은 같은 식이다.

아래의 if문을 삼항연산자로 표현하면 위의 식이 나온다.