# **1주차**

## **목표**
자바 소스 파일(.java)을 JVM으로 실행하는 과정 이해하기.


### **JVM이란 무엇인가**
**Java Virtual Machine**, 자바 가상머신의 줄여서 부르는 용어
JAVA와 OS 사이에서 중개자 역할을 수행하여 OS와 상관없이 같은 코드로 같은 동작을 수행   

### **JVM 구성 요소**
- **Class Loader**
	- Runtime 시점에 클래스를 로딩하게 해주며 클래스의 인스턴스를 생성하면 클래스 로더를 통해 메모리에 로드하게 됩니다.
- **Runtime Data Areas**
	- JVM이 프로그램을 수행하기 위해 OS로 부터 별도로 할당 받은 메모리 공간을 말하며, 크게 5가지로 나눌 수 있음
	- PC Register, JVM stack, Native Methode Stack, Method Area, Heap
- **Execution Engine**
	- Load된 Class의 바이트코드를 실행하는 Runtime Module이 바로 실행엔진
	-  Class Loader를 통해 JVM 내의 Runtime Data Areas 에 배치된 바이트 코드는 실행엔진에 의해 실행되며, 실행 엔진은 자바 바이트 코드를 명령어 단위로 읽어서 실행합니다.  
	- 처음에는 인터프리터 방식으로 속도가 느린 단점이 있었지만, JIT complier 방식을 통해 이점을 보완

### **바이트코드란 무엇인가**
자바 바이트코드는 자바 가상 머신이 실행하는 명령어의 형태  
자바 바이트코드는 JVM만 설치되어 있다면 어느 운영체제에서도 실행 가능 (OS에 영향 X)


### **컴파일 하는 방법**
JAVA의 경로에서 .java파일을 javac라는 명령어를 이용하여 컴파일하고 실행 결과로 .class가 생성

    javac <옵션> <소스파일>

- 옵션 (추가중)
> -classpath (-cp) :
> 컴파일러가 컴파일 시 필요로하는 라이브러리나 클래스들의 경로를 지정해주는 옵션
> 컴파일 시, 다음과 같은 오류가 발생하면 classpath 옵션을 확인해보기
> > error: package ????.????? does not exist

### **실행하는 방법**
생성된 .class 파일을 다음과 같은 방식으로 실행

    java <옵션> <메인클래스>

### **JIT 컴파일러란 무엇이며 어떻게 동작하는지**
- **Just In Time**의 약자
- 실행 시점에 기계어로 변환된 코드를 저장해두고, 재사용시 저장된 코드를 재사용 하여 실행속도를 향상시키는 방법 
- 초기에는 선행 작업들로 느릴 수 있다.
 
### **JDK와 JRE의 차이**
- **JRE**
	- 자바실행환경(Java Runtime Environment)의 약자
	- JVM이 자바 프로그램을 동작시킬 때 필요한 라이브러리 파일 등을 가지고 있다.
- **jdk**
	- 자바개발도구(Java Development Kit)의 약자
	- JRE + 개발을 위한 도구들을 포함한다.

	