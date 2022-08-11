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
1byte = 4bit

byte   1byte (부호있는 정수값 저장 -128 ~ 127)
char   2byte (음수x)
short  2byte (음수o)
**int    4byte**
long   8byte


실수 타입
float  4byte
**double 8byte**
(+
둘의 차이는 메모리 크기
정밀도를 요하는 변수를 사용하려면 double
)

논리 타입
boolean 1byte

int -21억 ~ 21억

### 5.1 데이터 타입분류

데이터 타입에는 2가지가 있습니다
1. 기본타입(primitive type) - 직접 값을 가지고 있음
2. 참조타입(reference type) - 직접값을 가지고 있는게 아닌 주소값을 가지고 있음 

### 5.2 메모리 사용영역

jvm은 OS 에서 할당받은 메모리 영역(runtime data area)을 3영역으로 구분 

- 메소드 영역
jvm을 시작할때 생성
로딩된 클래스 바이트 코드 내용을 분석 후 저장, 모든 스레드가 공유


- 힙영역
jvm을 시작할때 생성
객체나 배열 생성시에 메모리가 할당된다.
GC에 의해 메모리가 정리된다.

- jvm 스택
지역변수가 할당되며, 메소드가 호출될때마다 frame을 스택에 추가하고, 메소드가 종료되면 frame을 제거한다.
쓰레드 별로 생성된다.

메모리사용영역 순서
java -> jvm 구동 
jvm 구동 (메소드영역, 힙영역이 생성됨)
메소드영역에 클래스파일 로딩
main 스레드 생성(스택에 스레드 생성)
main() 메소드 호출(jvm 스택에 main 프레임이 생성)
 String args; (힙영역에 생성)
main() 메소드가 끝나면 스택 메모리에서 제거

### 5.3 참조변수의 ==, != 연산

변수의 값이 같은지 다른지 비교

기본타입 : 변수의 값이 다른지 다른지 조사 
int v1 10;
int v2 100;
int v3 100;

v1 == v2 false
v1 != v3 true
v2 == v3 true


참조타입 : 동일한 객체를 참조하는지 다른 객체를 참조하는지 조사

String v1 = "a";
String v2 = "b";
String v3 = v2;

v1 == v2 false
v1 != v2 true
v2 == v3 true
v2 != v2 false

== : 참조값을 비교 !!!!

null은 참조타입의 변수에만 저장 가능
null로 초기화된 참조변수는 스택영역 생성 

### 5.5 String 타입 
String name1 = "j"; //100
String name2 = "j"; //100
같은값을 가진다면 같은 참조값을 가진다
name1 == name2 true

하지만 new 연산자를 이용한 String 객체생성을 하면 힙영역에 새로운 객체를 생성한다
String name1 = new String("j"); //100
String name2 = new String("j"); //200
name1 == name2 false

문자열이 같으냐 다르냐는 equals 를 활용한다. 
비교연산자가 아닌 equals 메서드를 활용하여 문자열을 비교한다.

name1.equals(name2) true


### 5.7 열거타입

열거타입 (enumeration Type)
한정된 값만을 갖는 데이터 타입
한정된 값은 열거 상수로 정릐 

열거 타입 선언 
public enum Week {
  MONDAY, TUESDAY, WEDNESDAY
}

열거 상수는 열거 객체로 참조한다.
열거 객체는 힙에 생성된다.
열거 상수는 메소드 영역에서 열거 객체를 참조한다.

- 열거 객체의 메소드
열거 객체는 열거 상수의 문자열을 내부 데이터로 가지고있다
열거 타입은 컴파일시에 java.lang.enum 클래스를 자동 상속한다. 

ordinal() 열거객체의 순번을 리턴
Week today = Week.SUNDAY;
int ordinal = today.ordinal();

### 6.1 객체 지향 프로그래밍










