# 변수와 연산자
## 비트와 바이트
- 비트
  + 0과 1을 담을 수 있는 자리
- 바이트
  + 8비트
***
## 변수
- c언어에서는 변수를 통해 메모리에 접근해서 정보를 저장하거나 가져올 수 있다.
### 변수의 이름
- 원칙적으로 영어 대소문자, 숫자, 언더스코어의 조합만 가능하다.(a, my_name, myName123, _123abc...)
- 예약어 등 코드 내 특수한 목적이 있는 단어는 변수의 이름으로 사용할 수 없다.
- 동일한 이름의 변수명을 선언할 수 없다.
#### 적용하기
- 선언
  ```cpp
  int a;
  ```
- 대입 : 변수는 변하는 값이기 때문에 몇가지 사항을 제외하고는 다른 값으로 변경 할 수 있다.
  ```cpp
  a = 3; // 3
  a = 4; // 4
  ```
- 초기화 : 선언과 대입을 동시에 하는 것
  ```cpp
  int a = 3
  ```

### 자료형
- 변수에 담을 수 있는 자료의 형태(정수, 실수, 문자...)
- 정수
  + 정수의 사칙연산에서 결과도 정수이다.
  + 부호없는 정수 자료형의 경우 앞에 unsigned를 붙인다.
  > int (4바이트 = 32비트)   char (1바이트 = 8비트)   short   long   long long
- 실수
  + float
    * 실제 계산값과 printf의 값을 보면 컴퓨터가 소수를 처리하는 방식상 불가피하게 0.000001정도의 오차가 발생한다.(= 부동 소수점 오차)
    * 부동 소수점 오차를 줄이기 위해 정밀도가 두 배인 double 자료형을 쓰기도 한다.
  + double
- 진릿값
  + bool
- void
  + 자료형이 없다.

### sizeof
- 자료형 또는 변수의 크기를 알 수 있다.

### 형변환
- 변수에 서로 다른 자료형의 값을 대입하려고 할 때 발생한다.
- 정수와 실수의 나눗셈에서 실수가 하나라도 있으면 실수가 된다.
***
## 연산자
- 대입 연산자
  + =
  ```cpp
  a = a + 3 
  ```
    *복합 대입 연산자
    ```cpp
    a += 3
    ```
> 위 두 예시는 같은 뜻이다.
- 증감 연산자
  + 1씩 증감 : ++, --
- 비교 연산자
  + == / != / > / < / >= / <=
  + 참을 1/true, 거짓을 0/false으로 표현
- 논리 연산자
  + && / || / !

