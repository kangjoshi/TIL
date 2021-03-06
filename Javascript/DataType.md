## Data type

### 데이터 타입의 종류
1. 기본형
    - number, string, boolean, null, undefined, Symbol 등이 있다.
    - 불변성
   
1. 참조형
    - object 하위에 array, function, date, Map, WeakMap, Set, WeakSet 등이 있다.
    - 기본적인 성질은 가변성, 불변 객체를 지원하는 라이브러리나 깊은 복사로 불변하게 사용 가능 
    - 객체 내부의 프로퍼티에 대한 변수 영역이 별도로 존재

### 변수 선언
- 변경 가능한 데이터가 담길 수 있는 공간
    ```javascript
    // 기본형
    var name; // 값을 할당하지 않았으므로 undefined이다.
    name = 'kang'; // 변수에 데이터 할당
  
    // 참조형
    var user = {
        name : 'kang',
        age : 32
    };
    user.age = 31; // 재할당
    ```
##### 변수 영역과 데이터 영역의 분리
- 데이터를 저장하기 위한 별도의 메모리 공간(데이터 영역)을 확보하여 데이터를 저장하고 저장된 주소를 (변수 영역)에 저장
- 메모리를 더욱 효율적으로 관리
    - 문자열의 크기는 가변적이다. 변수와 데이터 영역의 분리로 데이터 크기 증가시에도 변수 영역은 영향 받지 않음.
    - 중복된 데이터는 데이터 영역에 하나만 저장하여 중복성 데이터에 대한 메모리 효율성 증가

### undefined vs null
두 값은 값이 없다. '없음'을 표현하지만. 다른 부분이 있고 사용하는 목적 또한 다르다.
- undefined
    - 값을 대입하지 않은 변수
    - 객체 내부의 존재하지 않는 프로퍼티에 접근하려 할 때
    - return 문이 없거나 호출되지 않는 함수의 실행 결과
    - 즉 값이 존재하지 않을 때
- null
    - '없음'을 명시적 표현하기 위해 사용 (null로 값은 존재하는 것)
    
---
### Reference
정재남. _코어 자바스크립트_. 위키북스  
