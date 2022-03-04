For(반복문)
=============
```java
public class For {
    public static void main(String[] args) {
        int total = 0;
        for(int i = 1; i <= 100; i++) {
//			if(i % 2 !=0) {
//				continue;       //continue를 만나면 아래쪽 반복문은 실행하지 않는다.
//			}
            total = total + i;
            if(i == 50) {
                break;
            }
        }
        System.out.println(total);
    }
}
```

for문은 구문 자체에 변수 초기화, 조건식, 증감식이 들어간다.

