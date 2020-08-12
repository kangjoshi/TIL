## use string carefully
_다른 자료형이 적절하다면 문자열 사용은 피하라._

문자열은 텍스트 표현과 처리에 걸맞도록 설계되었다. 지원이 훌륭하여 설계된 목적 이외의 용도로도 많이 활용되는 경우가 있다.

1. 문자열은 값 자료형을 대신하기에는 부족하다.
    - 키보드나 파일등 데이터를 통해서 들어올 때는 보통 문자열 형태이다. 데이터의 타입이 문자열일 경우에는 그대로 두면 되지만
숫자형이라면 int, float, BigInteger와 같은 수 자료형으로 변환해야한다. 만약 적당한 자료형이 없다면 새로 만들어야 한다.
1. 문자열은 enum 자료형을 대신하기에는 부족하다.
    - enum의 열거 자료형 상수를 이용하면 효과적이다.
1. 문자열은 혼합 자료형을 대신하기엔 부족하다.
    ```java
    // 구분자를 사용하여 혼합 자료형을 표현 각 필드를 사용하려면 느리고 오류 발생 가능성도 높다.
    String compoundKey = class + "|" + i.next();
    ```

더 좋은 자료형이 있거나 만들수 있다면 객체를 문자열로 표현하는 것은 피해야한다.

---
### Reference
조슈아블로크. _이펙티브자바2판_. 인사이트  