# TCB(Thread Control Block)
운영체제가 하나의 스레드를 관리하기 위해 사용하는 정보(자료구조)이다  
운영체제는 스레드가 생성될 때마다 TCB를 만들고, 이 정보를 이용해 스레드를 실행하고 관리한다

### 필요한 이유
CPU는 동시에 여러 스레드를 실행하는 것처럼 보이기 위해
(실행, 대기, 종료)상태를 계속 바꾼다  
이때 운영체제는 어떤 스레드를 실행해야하는 알아야 하므로 스레드의 정보를 저장하는 공간이 필요하다  
그 공간이 바로 TCB이다

### TCB에 저장되는 정보
- Thread ID = (스레드 번호(ID))
- Thread State  = Ready, Running, Waiting 등의 상태
- Program Counter(PC) = 다음에 실행할 명령어 위치
- Register 값 = CPU 레지스터 값
- Stack Pointer(SP) = 스택의 현재 위치
- Priority = 스레드의 우선순위
- Scheduling 정보 = CPU 스케줄링 정보
- Thread Context = 문맥(Context) 정보

### 동작 과정
```
Thread A 실행 중

↓

CPU 시간이 끝남

↓

현재 레지스터 값을 TCB에 저장

↓

Thread B의 TCB에서 레지스터 값을 읽음

↓

Thread B 실행
```
운영체제는 TCB를 이용하여 문맥 교환을 수행한다

### PCB와의 관계
```
Process
 ├── PCB
 │
 ├── Thread1
 │      └── TCB
 │
 ├── Thread2
 │      └── TCB
 │
 └── Thread3
        └── TCB
```
프로세스 하나에는 PCB가 하나 있고, 그 안에 여러개의 스레드가 존재할 수 있으며
각 스레드마다 TCB가 하나씩 존재한다

### PCB와 TCB 차이
PCB | TCB
--- | ---
프로세스 관리 | 스레드 관리
프로세스당 1개 | 스레드당 1개
메모리 정보 포함 | 스택 정보 포함
파일 정보 포함 | 레지스터 정보 포함
프로세스 ID(PID)저장 | 스레드 ID(TID) 저장

### 게임으로 예시
프로세스가 하나라는 가정이면
```
게임(Process)
│
├── 렌더링(Thread)
├── 물리 계산(Thread)
├── 사운드(Thread)
└── 네트워크(Thread)
```
운영체제는
```
게임
 └── PCB

렌더링
 └── TCB

물리 계산
 └── TCB

사운드
 └── TCB

네트워크
 └── TCB
```
처럼 각각 관리한다