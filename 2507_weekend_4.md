### 오늘 배운 것

#### Arrays.toString()
: Arrays.toString()은 Java에서 배열의 내용을 사람이 읽을 수 있도록 문자열로 변환해주는 유틸리티 메서드

🔹 특징
* 배열 값이 진짜 String으로 바뀌는 게 아니라 문자열로 표현만 되는 것
  
📌 왜 쓰냐면?
배열을 그냥 출력하면 메모리 주소가 나옴
```java
int[] arr = {1, 2, 3};
System.out.println(arr); // [I@15db9742 ← 주소값
```
Arrays.toString()을 사용하면 보기 좋은 형태로 출력됨
```java
System.out.println(Arrays.toString(arr)); // [1, 2, 3]
```

🔍 예제 
```java
import java.util.Arrays;

public class Main {
    public static void main(String[] args) {
        int[] numbers = {1, 2, 3, 4, 5};

        System.out.println(numbers);                  // [I@15db9742
        System.out.println(Arrays.toString(numbers)); // [1, 2, 3, 4, 5]
    }
}
```
</br></br>

#### 동적 인스턴스
: 동적 인스턴스란 자바에서 new 키워드를 사용해 실행 중(runtime)에 생성되는 객체

* "동적" → 실행 중에 생성
* "인스턴스" → 클래스에서 만든 실제 객체

🔹 특징
* new 키워드를 사용해 힙(Heap) 메모리에 생성됨
* 각 객체는 독립된 상태(state) 를 가짐

🔍 예제
```java
class Dog {
    String name;
}

public class Main {
    public static void main(String[] args) {
        Dog d = new Dog();     // 동적 인스턴스 생성
        d.name = "Happy";
    }
}
```
