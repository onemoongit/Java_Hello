# Course_2 : 자료구조 1

## stack
### 스택

- Stack : 처음에 문제를 제출할 때 혼자 작성한 코드
- Stack_2 : 조금 더 객체지향 방식으로 작성한 코드 ( 객체를 만들어 실행시켜야 한다.)
    - push 를 통해서 사이즈가 overflow 될때 생각해보기
    
## 괄호
### Bracket

- 스택을 이용해서 ( 를 만났을때는 push X , ) 를 만났을때는 pop 을 사용한다.
    - 중간에 pop을 할수 없는 경우를 생각해야 한다.
    - 결국 마지막에 empty가 된다면 제대로 작성이 된 것이다.
- 사실 굳이 스택을 사용 안해도 상관이 없다.
    - 현재 작성한 코드를 보면 숫자를 더하고 빼기만 해도 충분히 코드를 완성시킬 수 있다.
- 언제나 예외를 잘 생각해야 한다.

## 쇠막대기
### SteelStick

- 스택을 이용한 뒤 막대기가 생긴 경우 push 1
- 레이저를 쏠 때 모든 층의 막대기의 수가 +1
    - 레이저를 쏜 경우 스택의 모든 값에 +1

이 부분을 제대로 해결하면 된다. 인접한 쌍이 어떻게 되어있는 지를 확인한다.

총 4가지로 나뉠 수 있다. (( , )) , () , )( 각자의 상황에 맞춰서 케이스를 나눈 뒤 문제를 해결하자.

## 에디터
### Editor

- 처음에 문제는 풀었지만 시간 초과가 나타났다.
    - ArrayList.add 를 이용했는데 중간에 삽입한 경우 O(n)의 복잡도이기 때문이다.
- stack을 사용한다면 O(Constant)의 복잡도로 해결이 가능하다.
    - 핵심은 두개의 stack을 이용하는것 왼쪽 스택 , 오른쪽 스택
    - 커서를 기준으로 왼쪽 스택 오른쪽 스택을 나눠서 한쪽에서 푸시면 다른쪽은 팝 형식으로 진행한다.
    - 이렇게 되면 O(n) 복잡도가 아닌 O(Constant) 복잡도가 나오게 된다.
- 왜 stack 두개를 이용하면 좋을까?
    - 명령 하나당 커서의 이동이 1 만큼 이기 때문에 stack 으로 코드를 작성하기 편하다!

- 시간초과가 왜 나오지... 
 
 ## 큐
 ### Queue
 
 - 처음에 ArrayList 를 활용했지만 이미 구현되어있는 방식이므로 정석대로 다시 만들어보자
 
 