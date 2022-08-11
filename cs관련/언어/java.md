### java

https://www.youtube.com/watch?v=Sos11X7wy1M&list=PLVsNizTWUw7FPokuK8Cmlt72DQEt7hKZu

### 3절 자바 개발 환경 구축

Java SE 구현체 종류
- jdk(java development kit) = JRE + 개발도구
 : 자바 프로그램 개발하고 실행하기 위해 반드시 설치
- jre(java runtime environment) = JVM(가상의 운영체제) + 표준 클래스 라이브러리
 : 자바 프로그램을 실행하 경우 설치
 
 ### 4절 자바 프로그램 개발순서
 
.java 소스파일 작성 -> 컴파일(jdk가 제공해주는 javac.exe로 바이트코드 생성) -> jvm 구동명령어(java.exe)로 실행

자바는 2단계의 컴파일을 과정을 가진다
1. java -> class(바이트코드) 
2. class -> 완전한 기계어

각 운영체제에 맞는 JVM을 설치한다.

어떤운영체제에서든 우리는 개발을 하고 그걸 class 파일로 변경한 다음에 각 운영체제에 맞는 jvm이 완전한 기계어로 변경하여 프로그램을 실행한다ㅇ

### 2.1 변수(2)
리터럴 : 소스코드 내에서 직접 입력된 값
종류 : 정수리터럴, 실수리터럴, 문자리터럴, 문자열 리터럴...

정수 리터럴
소수점이 없는 정수 리터럴은 10진수로 간주한다. 

정수리터럴 타입 : byte, char, short, int, long

### 2.2 데이터 타입(1)
기본타입(primitive)

- 종류
정수 타입
byte   1byte
char   2byte
short  2byte
int    4byte
long   8byte


실수 타입
float  4byte
double 8byte

논리 타입
boolean 1byte


