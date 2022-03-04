TypeCasting(형변환)
=============

```java
public class TypeCasting {
    public static void main(String[] args) {
        int x = 50000;
        long y = x;
//		long y값이 int x보다 큰값이기 때문에 담을 수 있다.

        long x2 = 5;
        int y2 =(int) x2;
//		long x2의 값을 int y2로 담으려면 형변환이 필요하다.
    }
}
```

위 예제는 long 값이 int 보다 크다고 인식하기 때문에 y값에 x를 담을 수 있다.

long x2의 값이 int안에 들어갈 수 있다는것을 예상할 수 있기때문에 
강제로 int값으로 형번환 하여 y2안에 x2를 담아줄 수 있다.