Operator(산술 연산자)
=============
```java
public class Operator {
    public static void main(String[] args) {
        int i1 = -5;
        int i2 = +i1;
        int i3 = -i1;
        //+부호비트는 부호를 그대로, - 부호비트는 부호를 반대로 바꿔준다.

        System.out.println(i1);
        System.out.println(i2);
        System.out.println(i3);

        int i4 = ++i3;	// i3 = i3 + 1;
        System.out.println(i4);
        System.out.println(i3);
        int i5 = i3++;	// i3 = i3 + 1;
        System.out.println(i5);
        System.out.println(i3);

        int i = 5;
        int j = 2;

        System.out.println(i + j);
        System.out.println(i - j);
        System.out.println(i * j);
        System.out.println(i / (double)j);
        System.out.println(i % j);
    }
}
```

> 변수 앞에서 사용하는 부호비트
 
변수앞에서 + 부호비트는 부호를 그대로 유지
변수앞에서 - 부호비트는 부호를 반대로 바꿔준다.

증감식 ++i3의 경우 먼저 값을 더한 후 그 결과값을 i4에 넣어준다.

증감식 i3++의 경우 i3를 i5에 먼저 대입시킨 후 값을 더해준다.

그렇기 때문에 위 식에서의 i3의 값은 7, i4의 값은 6, i5의 값은 6이 된다.

산술연산자 +는 더하기, -는 빼기, *은 곱하기, /는 나누기, &는 값을나눈 나머지값이다.
위의 식에서 실수형으로 형변환을 해주지 않는다면 2라는 정수값이 나온다.