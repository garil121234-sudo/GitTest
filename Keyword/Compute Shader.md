# Compute Shader
GPU를 이용해서 그래픽을 그리는 것 외의 일반 계산 작업을 수행하는 프로그램  
  
**사용하는 곳**
* 게임 물리 계산
* AI
* 이미지 처리
* 대량 데이터 계산  
GPU를 사용해 한번에 많고 빠른 계산이 가능하다  
### Shader
GPU에서 실행되는 프로그램  
* Vertex Shader → 점(Vertex) 처리
* Pixel(Fragment) Shader → 픽셀 색상 처리
* Compute Shader → 일반 계산 처리  
  
 **목수 일로 비유하면**  
 CPU : 혼자서 못질 1000번  
 GPU : 1000명이 동시에 못질
 Compute Shader : 1000명에게 "못 하나씩 박아!"라고 지시하는 작업
