# Code 영역
프로그램의 실행 코드(명령어)가 저장되는 곳  
**예를 들자면**
``` C#
private static void Multiplay(int[] values)
{
    for(int i = values.Length-1; i >= 0; i--)
    {
        values[i] = values[i] * 10;
    }
}
```
실행이 되는 "Multiplay"함수는 Code 영역에 저장된다
```
int a = 10;
```
여기서  Code 영역에서 저장되는것은
a라는 변수를 저장하고 10을 넣는다 라는 명령만 저장된다  
값은 거의 안 들어간다(a = 10)이라는 데이터는 Stack에 저장된다