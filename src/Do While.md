Do While(반복문)
=============
```java
import java.util.Scanner;

public class dowhile {
    public static void main(String[] args) {
        int value = 0;
        Scanner scan = new Scanner(System.in);  //System으로부터 값을 입력받는 스캐너

        do {
//			반복할 문장
            value = scan.nextInt();
            System.out.println("입력받은 값:"+value);

        }while(value != 10);
        System.out.println("반복문 종료");
    }
}

```

while문은 조건에 부합하지 않을때 실행되지 않지만 

dowhile문은 무조건 한번은 실행된다.