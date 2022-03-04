If문
=============
```java
public class If {
    public static void main(String[] args) {
        int x = 50;
        int y = 60;
        if(x < y) {
            System.out.println("x는 y보다 작습니다.");
        }

        if(x == y)
            System.out.println("x와 y는 같다");

        if(x == y) {
            System.out.println("x와 y는 같다.");
        }else if (x < y){
            System.out.println("x는 y보다 작다.");
        }else {
            System.out.println("x와 y는 다르다..");
        }

    }
}
```

IF문의 경우 값이 1줄 뿐이라면 중괄호를 생략할  수 있다.
else if구문의 경우는 여러개 붙여서 사용할 수 있지만, 가급적이면 많이 사용하지 않는게 좋다.