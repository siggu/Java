# 이것이 자바다 -1 개념정리
 - [01. 자바 시작하기](#Chapter-01-자바-시작하기)

## Chapter 01 자바 시작하기

<details markdown="1">
<summary>1.1 프로그래밍 언어란?</summary>

- 컴퓨터가 이해하는 언어 ≠ 인간이 이해하는 언어 ( `서로 이해할 수 없다.` )
  > 둘 사이를 이어주는 다리 역할이 필요하다!  
  
---

- 프로그래밍 언어는 고급 언어와 저급 언어로 구분된다.
  - 고급 언어 : 컴퓨터와 대화할 수 있도록 만든 언어 중에서 사람이 쉽게 이해할 수 있는 언어
  
  > 컴퓨터가 바로 이해할 수 없어서 `컴파일(compile)` 과정을 통해 기계어로 변환한 후 컴퓨터가 사용한다.
  
  - 저급 언어 : 기계어에 가까운 언어  
  
  > 사람이 쉽게 이해할 수 없기 때문에 배우기 까다롭다.

---
- 일반적으로 프로그래밍 언어는 `C, C++, 자바(Java)`는 모두 고급 언어에 속한다.
- 이 언어들로 작성된 내용을 소스(source)라고 부르고, 이 소스는 컴파일러(compiler)라는 소프트웨어에 의해 기계어로 변환된 후 컴퓨터에서 실행할 수 있게 된다.

> 프로그램(program)이란 컴퓨터에서 특정 목적을 수행하기 위해 프로그래밍 언어로 작성된 소스를 기계어로 번역한 것을 말한다.
</details>

<details markdown="1">
<summary>1.2 자바란?</summary>

### 1.2.1 자바 소개  
- 1995년 썬 마이크로시스템즈(Sun Microsystems)에서 자바(Java)언어를 발표.
- 가전 제품에서 사용될 목적으로 고안된 오크(oak) 언어에서 시작.
- 1999년부터 단 한 번의 작성으로 모든 곳에서 실행 가능한 유일한 언어로 웹 어플리케이션 구축용 언어로 급부상.
---  
### 1.2.2 자바의 특징
**1. 이식성이 높은 언어**
> 이식성 : 서로 다른 실행 환경을 가진 시스템 간에 프로그램을 옮겨 실행할 수 있는 것
  
- 자바 언어로 개발된 프로그램은 소스 파일을 다시 수정하지 않아도, `자바 실행 환경(JRE : Java Runtime Environment)`이 설치되어 있는 모든 운영체제에서 실행 가능하다.  

**2. 객체 지향 언어**  
- 프로그램을 개발하는 기법으로 부품에 해당하는 객체들을 먼저 만들고, 이것들을 하나씩 조립 및 연결해서 전체 프로그램을 완성하는 기법을 `객체 지향 프로그래밍(OOP : Object Oriented Programming)`이라고 하고, 이때 사용되는 언어를 객체 지향 언어라고 한다.
> 자바는 100% 객체 지향 언어이다(하지만 자바로 객체 지향 언어를 이용하지 않으면, 객체 지향 프로그램이 아니다).  

**3. 함수적 스타일 코딩을 지원**
- 자바는 함수적 프로그래밍을 위해 `람다식(Lanbda Expresstions)`을 자바 8부터 지원한다. 람다식을 사용하면 컬렉션의 요소를 필터링, 매핑, 집계 처리하는데 쉬워지고, 코드가 간결해진다.  

**4. 메모리를 자동으로 관리**
- 자바는 개발자가 직접 메모리에 접근할 수 없도록 설계되었으며, 메모리는 자바가 직접 관리한다. 객체 생성 시 자동적으로 메모리 영역을 찾아서 할당하고, 사용이 완료되면 `쓰레기 수집기(Garbage Collector)`를 실행시켜 자동적으로 사용하지 않는 객체를 제거시켜준다.

**5. 다양한 어플리케이션 개발 가능**
- 자바는 윈도우, 리눅스, 유닉스, 맥 등 다양한 운영체제에서 실행되는 프로그램을 개발할 수 있다.   

**6. 멀티 스레드(Mulit-Thread)를 쉽게 구현 가능**
- 하나의 프로그램이 동시에 여러 작업을 처리해야 할 경우와 대용량 작업을 빨리 처리하기 위해 서브 작업으로 분리해서 병렬 처리하려면 멀티 스레드 프로그래밍이 필요하다. 자바는 스레드 생성 및 제어와 관련된 라이브러리 API를 제공하고 있기 때문에 실행되는 운영체제에 상관없이 멀티 스레드를 쉽게 구현할 수 있다.   

**7. 동적 로딩(Dynamic Loading)을 지원**
- 어플리케이션이 실행될 때 모든 객체가 생성되지 않고, 객체가 필요한 시점에 클래스를 동적 로딩해서 객체를 생성한다.   

**8. 막강한 오픈소스 라이브러리**
- 자바는 오픈소스(Open Source) 언어이기 때문에 자바 프로그램에서 사용하는 라이브러리 또한 오픈소스가 넘쳐난다. 검증된 오픈소스 라이브러리를 사용하면 개발 기간을 단축하면서 안전성이 높은 어플리케이션을 쉽게 개발할 수 있다.   
---

### 1.2.3 자바 가상 기계(JVM)  
- 자바 프로그램은 완전한 기계어가 아닌, 중간 단계의 바이트 코드이기 때문에 이것을 해석하고 실행할 수 있는 가상의 운영체제가 필요하다. 이것이 `자바 가상 기계(JVM : Java Virtual Machine)이다.
- JVM은 실 운영체제를 대신해서 자바 프로그램을 실행하는 가상의 운영체제 역할을 한다.
  > 운영체제별로 프로그램을 실행하고 관리하는 방법이 다르기 때문에 운영체제별로 자바 프로그램을 별도로 개발하는 것보다 운영체제와 자바 프로그램을 중계하는 JVM을 두어 자바 프로그램이 여러 운영체제에서 동일한 실행 결과가 나오도록 설계한 것이다.

- 바이트 코드는 모든 JVM에서 동일한 실행 결과를 보장하지만, JVM은 운영체제에 종속적이다.(운영체제에 맞는 JVM이 설치되어야 한다)

<p align = "center"><img src = "https://user-images.githubusercontent.com/106001755/170177138-5bb2e637-7e55-4e64-955a-cb539bb80f32.png" width="300" height="400"></p>

<div align = "center">
JVM, 자바 프로그램의 실행 단계
</div>
</details>

<details markdown="1">
<summary>1.3 자바 개발 환경 구축</summary>
</details>

<details markdown="1">
<summary>1.4 자바 프로그램 개발 순서</summary>

### 1.4.1 소스 작성에서부터 실행까지  
자바 프로그램을 개발하려면 다음과 같은 순서로 진행해야 한다.

<p align = "center"><img src = "https://user-images.githubusercontent.com/106001755/170179296-7d3043be-cd8f-41e2-99f4-f42e8d0b7d51.png" width ="300" height="200"></p>

자바 프로그램을 개발하려면 우선 파일 확장명이 `.java`인 텍스트 파일을 생성하고 프로그램 소스를 작성한다. 이렇게 만들어진 파일을 `자바 소스 파일`이라고 한다. 작성 완료된 자바 소스 파일은 `컴파일러(javac.exe)`로 컴파일해야 한다. 컴파일이 성공되면 확장명이 `.class`인 `바이트 코드 파일`이 생성된다.

바이트 코드 파일은 완전한 기계어가 아니므로 단독으로 실행할 수 없고 JVM이 실행되어야 한다. JVM을 구동시키는 명령어는 `java.exe`이다.
> 주의할 점은 java.exe로 바이트 코드 파일을 실행할 때는 `.class` 확장명을 제외한 이름을 입력해야 한다.

java.exe 명령어가 실행되면 JVM은 바이트 코드 파일을 메모리로 로드하고, 최적의 기계어로 번역한다. 그리고 `main()` 메서드를 찾아 실행시킨다. 자바 소스 작성에서부터 실행까지의 과정을 도식화하면 다음과 같다.

<p align = "center"><img src = "https://user-images.githubusercontent.com/106001755/170181841-186f74c1-e0c4-4fdb-ab52-390a681191ea.png" width="550" height="200"></p>

### 1.4.2 프로그램 소스 분석
자바 실행 프로그램은 반드시 `클래스(class)` 블록과 `main() 메서드(method)` 블록으로 구성되어야 한다. 메서드 블록은 단독으로 작성될 수 없고 항상 클래스 블록 내부에서 작성되어야 한다.
- 클래스 : 필드 또는 메서드를 포함하는 블록
- 메서드 : 어떤 일을 처리하는 실행문들을 모아 놓은 블록

```java
public class Hello {
  public static void main(String[] args) {
   System.out.println("Hello, welcome to the java world!");
   }
  }
}
```

`Hello`가 클래스 이름이고, 그 다음에 있는 중괄호({)부터 그와 짝을 이루는 중괄호(})까지가 클래스 블록이다.

<p align = "center"><img src = "https://user-images.githubusercontent.com/106001755/170183347-22b6cb80-ef56-4160-b213-79a7f70ca2b9.png" width="500" height="150"></p>

- 클래스 이름은 소스 파일명과 대소문자가 일치해야 한다.
- 숫자로 시작할 수 없다.
- 공백을 포함해서는 안 된다.

메서드는 클래스처럼 이름과 블록을 가진다. `main`이 메서드 이름이고, 중괄호({)부터 그와 짝을 이루는 중괄호(})까지가 메서드 블록이다.

<p align = "center"><img src = "https://user-images.githubusercontent.com/106001755/170183958-493542d8-4cc0-4581-b77e-d7735c50440b.png" width="500" height="150"></p>




</details>

<details markdown="1">
<summary>6.10 인스턴스 멤버와 this</summary>
### 6.10.3 정적 초기화 블록
정적 필드는 다음과 같이 필드 선언과 동시에 초기값을 주는 것이 보통이다.

`static double pi = 3.14159;`

- **생성자에서 초기화 작업을 할 수 없다.** 생성자는 객체 생성 시에만 실행되기 때문이다.

- 자바는 정적 필드의 초기화 작업을 위해서 `정적 블록(static)`을 제공한다.

- **정적 블록은 클래스가 메모리로 로딩될 때 자동적으로 실행된다.(= 프로그램이 시작되자마자)** 정적 블록은 클래스 내부에 여러 개가 선언되어도 상관없다.
> 프로그램이 실행될 때 정적 블록은 자동적으로 실행된다.

- 클래스가 메모리로 로딩될 때 선언된 순서대로 실행된다.

### 6.12 패키지
넘어감!(자연스럽게 배우는 내용이라서...)

### 6.13 접근 제한자
public, protected, 생략("default"라고 부른다), private

접근 지정자의 목적
- 클래스나 일부 멤버를 **공개하지 않고** 다른 클래스에서 **접근하지 못하도록** 막음(**information hiding**)
- 






```java
public static TelevisionExample {
  public static void main(String args[]) {
    System.out.println(Television.info);
    }
  }
}

public class Television {
  static String company = "Samsung";
  static String model = "LCD";
  static String info;
  
  static {
    info = company + "-" + model;
  }
}
```

### 6.10.4 정적 메서드와 블록 선언 시 주의할 점
- 정적 메서드와 정적 블록을 선언할 때 주의할 점은 객체가 없어도 실행된다는 특징 때문에, 이들 내부에 인스턴스 메서드를 사용할 수 없다.
- 객체 자신의 참조인 `this` 키워드도 사용이 불가능하다.
> static은 static 끼리 논다.

### 6.10.5 싱글톤(Singleton)
- 하나의 어플리케이션 내에서 단 하나만 생성되는 객체(뒤로 미룸!)

## 6.11 final 필드와 상수
### 6.11.1 final 필드
- 최종적인 값을 가지고 있는 필드 = 값을 변경할 수 없는 필드

<p align = "center"><img src = "https://user-images.githubusercontent.com/106001755/170189712-2f56e51c-f70c-4fac-82bd-8185d925aa5e.png" width="300" height="450"></p>

final 필드의 초기값을 줄 수 있는 방법은 두 가지 밖에 없다.

1. 필드 선언 시에 주는 방법

2. 생성자에서 주는 방법


[ Person.java ] final 필드 선언과 초기화
```java
public class Person {
  final String nation = "Korea";  // 생성자 초기화를 해줘야 한다.
  final Stirng ssn;
  String name;
  
  public Person(Stirng ssn, String name) {
    this.ssn = ssn;
    this.name = name;
  }
}
```

[ PersonExample.java ] 필드 테스트
```java
public class PersonExample {
  public static void main(String[] args) {
    Person p1 = new Person("123456-1234567", "계백");
    
    System.out.println(p1.nation);
    System.out.println(p1.ssn);
    System.out.println(p1.name);
    
    //p1.nation = "usa";
    //p1.ssn = "654321-7654321";
    p1.name = "을지문덕";
  }
}
```

출력 결과
```java
Korea
123456-1234567
계백
```

### 6.11.2 상수(static final)
일반적으로 불변의 값을 상수라고 부른다. final 필드는 한 번 초기화되면 수정할 수 없는 필드라고 했다. 그렇다면 final 필드를 상수라고 불러도 되지 않을까? 하지만 final 필드를 상수라고 부르진 않는다. 불변의 값은 객체마다 저장할 필요가 없는 공용성을 띄고 있으며, 여러 가지 값으로 초기화될 수 없기 때문이다. final 필드는 객체마다 저장되고, 생성자의 매개값을 통해서 여러 가지 값을 가질 수 있기 때문에 상수가 될 수 없다.

pi = 3.141592... // 변하지 않는 값(상수)  
누군가 pi가 몇이냐 했을 때 "3"이라 하면 변한 것이다.

```java
Person p1 = new Person("3.14", "PI1");
Person p2 = new Person("3", "PI2");

p1.printPi();
p2.printPi();
```

상수는 static이면서 final이어야 한다. static final 필드는 객체마다 저장되지 않고, 클래스에만 포함된다. 그리고 한 번 초기값이 저장되면 변경할 수 없다.

그냥 final은 상수가 아니고, static final ~ 하면 상수가 된다.(static은 하나밖에 없기 때문)

클래스 변수(필드)는 클래스당 하나만 가지고 있다.(클래스 안에서 하나씩 가지고 있다는 뜻)





</details>
