# Process ID(PID)
운영체제가 각 프로세스를 구분하기 위해 부여하는 고유한 번호이다
(사람에게 주민번호가 있듯이, 프로세스마다 PID가 하나씩 존재한다)

### 특징
- 프로세스가 생성될 때 운영체제가 자동으로 부여한다
- 같은 시접에는 동일한 PID를 가진 프로세스는 존재하지 않는다
- 프로세스가 종료되면 PID는 나중에 다른 프로세스에서 다시 사용할 수 있다
- 운영체제는 PID를 이용해 특정 프로세스를 관리한다

### PID가 필요한 이유
운영체제는 수많은 프로세스를 동시에 실행한다
예를들어  
메모장, 크롬, 게임은 각각 하나 이상의 프로세스를 가지고 있다
운영체제는 이들을 구별하기 위해 PID를 사용한다

### PCB와 PID의 관계
프로세스마다 하나의 PCB가 존재한다  
PCB 안에는 프로세스를 관리하기 위한 다양한 정보가 저장되는데, 그중 하나가 PID이다  
```
PCB
├─ Process ID (PID)
├─ Process State
├─ Program Counter
├─ CPU Registers
├─ Scheduling Information
├─ Memory Information
├─ Open Files
└─ 기타 정보
```
PID는 PCB에 저장되는 정보 중 하나이다