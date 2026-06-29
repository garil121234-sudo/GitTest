# Data 영역
프로그램이 실행되는 동안 계속 유지되어야 하는 데이터를 저장하는 메모리 공간  
**만들어지는 과정**  
1. 프로그램 실행
1. Code 영역 생성
1. Data 영역 생성
1. Heap 생성
1. Stack 생성(프로그램 종료 시 모두 사라진다)  

**데이터 영역에 저장되는 것**  
1. static 변수
1. static 필드
1. static 클래스의 데엍
1. 전역 변수(C#에는 없음)

**예시**
```C#
class Program
{
    static int count = 0;

    static void Add()
    {
        count++;
    }

    static void Main()
    {
        Add();
        Add();

        Console.WriteLine(count);
    }
}
```
Data영역에 저장하는 이유는 static 변수는 모든 함수가 같이 사용해야되기 때문  
출력은 2지만 count가 Stack에 있었다면 Add()가 끝날 때마다 사라졌을것이다
Data영역에 있기 때문에 2가 나올수있다
