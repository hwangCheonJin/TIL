Constant(상수)
=============
```java
public class Constant {
    public static void main(String[] args) {
        int i;
        i = 5;

//      상수를 선언할때는 변수 앞에 final을 사용한다.
//		변수는 마지막 값이 저장되지만, 상수는 단하나의 값만 저장된다.
        final int J;
        J = 10;

//		J = 5;

        double circleArea;
        final double PI = 3.14159;
        circleArea = 3 * 3 * PI;

        final int OIL_PRICE = 1450;

        int totalPrice = 50 * OIL_PRICE;
        System.out.println(J);
        System.out.println(circleArea);
        System.out.println(totalPrice);
    }
}
```

상수를 선언할때는 변수앞에 final을 사용한다.
상수는 하나의 값만 가질 수 있으며, 보통 변치않는 값을 넣을때 사용한다.