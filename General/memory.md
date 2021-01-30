### 메모리 구조

- 프로그램이 실행되기 위해서 메모리에 로드가 되어야 한다 (프로세스)

- 프로그램에서 사용할 변수를 저장할 메모리도 있어야한다

- 메모리 구조 종류

  - 코드 영역 (프로그램 코드)
  - 데이터 영역 (전역 변수, 정적 변수)
  - 스택 영역 (지역변수, 매개변수)
  - 힙 영역 (사용자가 동적 할당)

    <img src="./images/memory.png" width="300px" height="250px"/>

> 코드 영역

- 실행할 프로그램의 코드가 저장되는 영역, 텍스트 영역이라고도 한다
- CPU는 코드 영역에 저장된 명령어를 하나씩 가져가서 처리한다

> 데이터 영역

- 프로그램의 전역 변수와 정적(static) 변수가 저장되는 영역이다
- 프로그램 시작과 함께 할당되고 프로그램이 종료되면 소멸한다

> 스택 영역

- 함수 호출과 관계되는 지역변수와 매개변수가 저장되는 영역
- 함수 호출과 함께 할당되고 함수가 종료되면 소멸한다
- 스택에 저장되는 함수의 호출 정보를 스택 프레임이라고 한다
- 메모리의 높은 주소에서 낮은 주소의 방향으로 할당된다
- 컴파일 시에 크기가 결정된다

> 힙 영역

- 사용자가 직접 관리할 수 있는(해야하는!) 영역
- 사용자에 의해 메모리 공간이 동적으로 할당되고 해제된다
- 메모리의 낮은 주소에서 높은 주소 방향으롤 할당된다
- 프로그램이 실행될 때까지 알수 없는 가변적인 양만큼 데이터 저장하기 위해 예약된 메인 메모리 영역
- 연결리스트, 트리, 그래프 처럼 동적인 특성 가진 자료구조에서 사용

### Heap vs stack

> stack

- 장점
  - 낭비되는 공간이 없음
  - 1명령 만으로 메모리 조작과 어드레스 조작 가능
- 단점
  - 크기에 한계가 있어 초과 삽입이 안된다
  - 유연성 부족

> heap

- 장점

  - 개체가 커서 스택 할당에 맞지 않는 경우 사용
  - 프로그램에 필요한 개체 개수나 크기 모르는 경우 사용가능

- 단점

  - 할당 및 해제 작업으로 속도 저하
  - 힙 손상 속도 저하 (이중 해제, 해제 후 블록 사용, 경계 벗어나 덮어쓰기)
  - 힙 경합 속도 저하 (두 개 이상의 스레드에서 동시에 데이터 엑세스 시도 시)

- 결론: 스택이 훨씬 빠르다

---

- 출처
  - [http://tcpschool.com/c/c_memory_structure](http://tcpschool.com/c/c_memory_structure)
  - [heap,stack](https://m.blog.naver.com/PostView.nhn?blogId=yoonjinym&logNo=30089450819&proxyReferer=https:%2F%2Fwww.google.co.kr%2F)