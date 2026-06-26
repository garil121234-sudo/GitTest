# Process
process는 실행 중인 프로그램이다.(프로그램이 실행되는 순간 프로세스가 된다)  
자세하게 설명하면 컴퓨터에는 SSD, RAM이 있는데 프로그램은 SSD에 저장되어있고 
프로그램을 실행하면 RAM으로 올라가 CPU가 실행하게된다  

**Process를 실행하려면 여러가지가 필요하다
* 코드 (Code)
* 데이터 (Data)
* 메모리 (Heap)
* 스택 (Steak)
* 스레드 (Thread) 가 필요하다

**Process는 메모리가 따로있다**  
같은 프로그램을 실행해도 서로의 메모리가 달라서 직접 건드릴 수 없다.  

**Process 안에는 Thread가 있다**
process는 일종의 작업공간이고, 실제로 일 하는 것은 Thread이다
예를 들면 게임에서는
* Thread 1 : 화면 그리기
* Thread 2 : 소리 재생
* Thread 3 : 네트워크 통신 처럼 여러Threa가 동시에 일을 할 수 있다.  

