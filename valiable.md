## 변수 선언

```java
public class Java100 {
    public static void main(String[] args) {
        int a; //정수가 저장될 변수 a를 만들어라.
        a = 3; // (=) 은 같다라는 의미가 아닌, 3을 a라는 바구니에 "대입, 할당"해라.

    }
}
```

## 자바의 데이터타입(자료형)
1. 기본형 타입(Primitive Data Type)
    - 1byte = 8bit
    - 정수형 : byte(1byte), short(2), int(4), long(8)
    - 실수형 : float(4), double(8)
    - 문자형 : char(2) *문자열을 다루는 타입은 없다.
    - 논리형 : boolean(1) (true or false / 참 or 거짓)

2. 참조형 타입(Reference Data Type) : 위 기본형에 속하지 않는 데이터형들
    - 대표적인 것들 : 클래스(class), 배열(array), 인터페이스(interface), 문자열(String/immutable)
    - 참조형 변수의 특징 : 데이터가 저장된 메모리의 "주소" 값을 저장하는 변수이다.

### 기본형 타입 byte크기, bit크기 출력 코드
```java
public class Java100 {
    public static void main(String[] args) {
        // byte, short, int, long, char(1, 2, 4, 8, 2)
        System.out.println(Byte.BYTES); // 바이트 계산
        System.out.println(Byte.SIZE); // 비트 계산
        System.out.println(Short.BYTES);
        System.out.println(Short.SIZE);
        System.out.println(Short.MIN_VALUE) // -32768 
        System.out.println(Short.MAX_VALUE) // 32767
        // 2^16 = 65536 -> -32768 ~ 0 ~ 32767
        System.out.println((int)Character.MIN_VALUE) // 0 -> 문자형이라 음수값 x
        System.out.println((int)Character.MAX_VALUE) // 65535
    }
}
```

1. Wrapper class(래퍼 클래스) 
    - Byte, Short, Integer, Long, Float, Double, Character, Boolean
    - 8개의 기본 타입에 해당하는 데이터를 객체로 포장해주는 클래스
    - 각각의 타입에 해당하는 데이터를 인수로 전달받아, 해당 값을 갖는 객체로 만들어줌.
    - java.lang 패키지에 포함되어 제공된다.
