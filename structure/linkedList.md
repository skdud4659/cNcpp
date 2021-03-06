# 링크드 리스트
- '논리적인 순서'의 나열

## 그럼 배열과 리스트의 차이는 뭐지?
- 배열은 <b>'인덱스'</b>로 표현되는 <b>'순서'</b>가 배열 원소의 메모리 공간에서 물리적 의미를 의미
- 리스트는 어떤 정의에 의해 결정된 <b>'논리적인 순서</b>로, 원소들의 물리적인 저장 순서나 위치와 무관하게 원소들 간의 논리적인 순서만 유지한다.

## 리스트는 어떻게 구현하지?
### 포인터를 이용
- 원소값을 저장하는 공간과 다음 원소를 가리키는 위치 정보를 저장하는 공간을 같이 구현하는 방법
### 배열을 이용
- 배열을 만들어놓고 중간에 데이터를 삽입하려면 삽입하려는 위치 뒤에 있는 데이터를 다 한 칸씩 뒤로 밀고 삽입해야 한다는 단점이 존재
- 삭제할 때도 삭제하려는 위치 뒤에 있는 데이터를 한 칸씩 앞으로 당겨야 하는 단점
- 이러한 동작들은 원소의 수에 비례해서 프로그램 수행 시간을 엄청나게 증가시킬 수 있다.
> 따라서 일반적으로는 리스트는 포인터를 이용해서 구현함!!

## 기본 개념
### 노드
- 리스트의 원소(값)과 다음 원소를 가리키는 정보로 구성
- 데이터 요소인 값과 다음 원소를 지시하는 포인터로 구성된다.

![링크드리스트](https://miro.medium.com/max/1332/1*JG-58S8EMxVXrk7cKAaK8w.png)

### 링크드리스트 생성
```cpp
struct linked_list_node {
   // data
    int data;
   // pointer
    struct linked_list_node *link;
};
```

### 링크드리스트 삽입
![링크드리스트삽입](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FYN0nZ%2FbtqIsKtj5aH%2FWh5yiZ73POkR2o1PkNpCL0%2Fimg.png)
1. 메모리 공간을 할당받고 삽입할 내용을 저장하여 삽입할 노드를 생성한다.
2. 삽입할 노드의 링크 부분이 후행 토드가 될 노드를 가리키게 한다.
3. 삽입될 노드의 선행 노드가 될 노드의 링크 필드가 삽입할 노드의 주소를 가리키게 한다.

### 링크드리스트 삭제
![링크드리스트삭제](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FcheiRb%2FbtqIgfol0s5%2FnN4nBZ1EvILbK29mMUIcUk%2Fimg.png)
1. 삭제할 노드의 선행 노드의 링크 필드를 삭제할 노드의 후행 노드를 가리키게 한다.
2. 삭제할 노드를 메모리에 반환한다.