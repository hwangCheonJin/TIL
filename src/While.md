While(반복문)
=============
```java
public class While {
    public static void main(String[] args) {
//		int i = 0;
//
//		while(i<10) {
//			System.out.println(i);
//			i++; //i = i + 1;
//		}

        int total = 0;
        int i = 1;
        while(i<=100) {
            total = total + i;
            i++;
        }
        System.out.println(total);
    }
}
```

while문은 조건에 부합한다면 그문장을 계속 실행하는 것이다.

코드를 잘못짠다면 무한루프를 돌 수 있으니 조심해야한다.