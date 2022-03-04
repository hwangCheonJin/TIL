Array2(2차원 배열)
=============
```java
public class Array2 {

    public static void main(String[] args){
        int[][] array4 = new int[3][4];
        array4[0][1] = 10;

        int[][] array5 = new int[3][];
        array5[0] = new int[1];
        array5[0][0] = 10;

        int[][] array6 = {{1},{1,2},{1,2,3}};
        System.out.println(array6[0][0]);
        System.out.println(array6[2][2]);
    }

}

```

2차원 배열의 경우 중괄호 2개로 선언할 수 있다.

중괄호의 인덱스 값으로 각각 길이가 다른 2차원 배열을 선언할 수 있다.