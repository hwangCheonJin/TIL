ForEach
=============
```java
public class forEach {
    public static void main(String[] args){
        int[] iarr = {10,20,30,40,50};

        for(int i = 0; i < iarr.length; i++){
            int value = iarr[i];
            System.out.println(value);
        }
        for(int value:iarr){
            System.out.println(value);
        }
    }
}

```

위 식은 for문을 forEach문으로 바꾼것이다.

:을 경계로 두 변수를 적어준다.

for(타입 값을 받아줄 변수 : 출력하고 싶은 자료구조)