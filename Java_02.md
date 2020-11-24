# **3주차**

## **목표**
자바에서 제공하는 다양한 연산자를 학습하세요

### **산술 연산자**
산술연산자는 사칙연산을 다루는 연산자이며, 두 개의 피연산자를 가지는 이항 연산자이다. 피연산자들은 왼쪽에서 오른쪽 방향으로 결합한다.

<산술연산자 표 그림>

<기본 결합방향 그림>

### **비트 연산자**
비트연산자는 비트 단위로 논리 연산을 할 때 사용하는 연산자로 왼쪽이나 오른쪽으로 전체 비트를 이동하거나, 1의 보수를 만들 때 사용한다.

<비트연산자 표>

<연산 과정 그림>

### **관계 연산자**
비교 연산자라고도 부르며, 결과로 true 혹은 false 값인 boolean 자료형으로 반환됨.

<관계 연산자 표>

### **논리 연산자**
and, or, not 세가지의 연산자가 있으며, 연산의 결과가 true 혹은 false 로 반환 된다.

### **instanceof**
객체 타입을 확인하는데 사용한다. 속성은 이항연산자이고 형변환 가능여부를 true / false 로 반환한다.  
주로 상속 관계에서 부모객체인지 자식객체인지 확인하는데 사용한다.

```java
public class InstanceofEx{
	public static void main(String[] args){
	A a = new A();
	B b = new B();
	
	System.out.println(a instanceof A);
	// true > a는 A객체이므로 형변환 가능
	System.out.println(b instanceof A);
	// true > b는 A의 자식객체이므로 형변환 가능

	System.out.println(a instanceof B);
	// false > a는 B의 부모객체이므로 형변환 불가능
	System.out.println(b instanceof B);
	// true > b는 B객체이므로 형변환 가능
	}
}

class A{}
class B extends A{}

```
<설명그림 추가>

### **assignment(=) operator**
값을 변수에 할당할 때 쓰는 연산자
<대입연산자? 할당연산자? 표 정리 추가>
```java
int a;
a = 10;
// a에 10을 할당
a += 10;
// a = a + 10;
a -= 10;
// a = a - 10;
```
### **화살표(->) 연산자**
람다표현식

### **3항 연산자**
- 단항 연산자
	- 대표적으로 부호연산자가 있다.
- 이항 연산자
- 삼항 연산자

### **연산자 우선 순위**
### **(optional) Java 13. switch 연산자**




