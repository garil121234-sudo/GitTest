# Heap 영역
프로그램이 실행 중에 필요한 데이터를 동적으로 저장하는 메모리 공간  

**Heap이 필요한 이유**
```c#
class Person
{
    public string Name;
    public int Age;
}
```
예를 들면 프로그램이 실행하기 전까진 몇 명이 만들어질지 모른다

```C#
Person p1 = new Person();
Person p2 = new Person();
Person p3 = new Person();
```
3명일수도있고
```C#
for(int i = 0; i < 10000; i++)
{
    new Person();
}
```
1만 명일 수도 있다
이처럼 실행 중에 개수가 결정되는 객체들을 저장하는 공간이 Heap이다  

**Heap에 저장되는 것들**
- Class
- Array
- String
- new로 생성한 객체들이 저장된다  

**Heap은 필요한 만큼 메모리를 할당받아 사용한다**

**Heap은 더 이상 사용하지 않는 객체가 되면
Garbage Collector이 나중에 제거한다**

**Heap은 참조형식이다**
```C#
Monster a = new Monster();
Monster b = a;
```
에서 메모리는
```
Stack

a ─────┐
       │
b ─────┘

      ▼

Heap

Monster
Hp = 100
```
a 와 b가 같은 Heap 객체를 참조(가리키기)떄문에 참조형식이라고 부른다  
a 와 b 둘중에 어느 값을 변경해도 같은 주소에 저장되기 때문에 같이 바뀐다  
