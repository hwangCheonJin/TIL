Switch
=============
```java
public class Switch {
    public static void main(String[] args) {
//		switch, case, default, break
        int value = 2;
//		break문이 없을 경우 선택된 case부터 아래로 코드들이 실행되기 때문에 break문을 사용해야한다.
        switch(value) {
            case 1:
                System.out.println("1");
                break;
            case 2:
                System.out.println("2");
                break;
            case 3:
                System.out.println("3");
                break;
            default :
                System.out.println("그외 다른숫자.");
        }
        String str = "A";
        switch(str) {
            case "A":
                System.out.println("A");
                break;
            case "B":
                System.out.println("B");
                break;
        }
    }
}
```

Switch case 문에서 case별로 break문을 사용하여 case 값을 반환한 후 case문을 빠져나온다.

break문이 없을경우 선택된 case부터 아래구문으로 실행된다.

default는 if문의 else와 비슷한 기능을 한다. 선언된 값이 case중 없다면 default값이 나온다.

Switch case 문은 문자열도 반환이 가능하다.