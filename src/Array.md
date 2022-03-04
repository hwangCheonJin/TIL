Array(배열)
=============
```java
public class Array {
    public static void main(String[] args) {
        int[] array1 = new int[100];

        array1[0] = 50;
        array1[10] = 100;

        int[] array2 = new int[] {1,2,3,4};

        int[] array3 = {1,2,3,4};

        System.out.println(array3[3]);
        int value = array3[0];

        System.out.println(value);
    }
}

```

배열은 0번째 인덱스부터 사용한다.

배열 1,2,3,4를 선언했다면 0,1,2,3번째 인덱스에 각각의 값이 들어간다.