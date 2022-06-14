# 이것이 자바다 -1 개념정리
 - [Chapter 01 자바 시작하기](#Chapter-01-자바-시작하기)
 - [Chapter 05 참조 타입](#Chapter-05-참조-타입)
 - [Chapter 06 클래스](#Chapter-06-클래스)
 - [Chapter 07 상속](#Chapter-07-상속)
 
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

<p align = "center"><img src = "https://user-images.githubusercontent.com/106001755/170177138-5bb2e637-7e55-4e64-955a-cb539bb80f32.png" width="450" height="450"></p>

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

<p align = "center"><img src = "https://user-images.githubusercontent.com/106001755/170179296-7d3043be-cd8f-41e2-99f4-f42e8d0b7d51.png" width ="400" height="200"></p>

자바 프로그램을 개발하려면 우선 파일 확장명이 `.java`인 텍스트 파일을 생성하고 프로그램 소스를 작성한다. 이렇게 만들어진 파일을 `자바 소스 파일`이라고 한다. 작성 완료된 자바 소스 파일은 `컴파일러(javac.exe)`로 컴파일해야 한다. 컴파일이 성공되면 확장명이 `.class`인 `바이트 코드 파일`이 생성된다.

바이트 코드 파일은 완전한 기계어가 아니므로 단독으로 실행할 수 없고 JVM이 실행되어야 한다. JVM을 구동시키는 명령어는 `java.exe`이다.
> 주의할 점은 java.exe로 바이트 코드 파일을 실행할 때는 `.class` 확장명을 제외한 이름을 입력해야 한다.

java.exe 명령어가 실행되면 JVM은 바이트 코드 파일을 메모리로 로드하고, 최적의 기계어로 번역한다. 그리고 `main()` 메서드를 찾아 실행시킨다. 자바 소스 작성에서부터 실행까지의 과정을 도식화하면 다음과 같다.

<p align = "center"><img src = "https://user-images.githubusercontent.com/106001755/170181841-186f74c1-e0c4-4fdb-ab52-390a681191ea.png" width="550" height="200"></p>

---

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


## Chapter 05 참조 타입
<details markdown="1">
<summary>5.1 데이터 타입 분류</summary>

- 자바의 데이터 타입에는 크게 기본타입(원시 타입 : primitive type)과 참조 타입(reference type)으로 분류된다. 
> 기본 타입이란 정수, 실수, 문자, 논리 리터럴을 저장하는 타입을 말한다. 
> 참조 타입이란 객체(object)의 번지를 참조하는 타입으로 배열, 열거, 클래스, 인터페이스 타입을 말한다.

- 기본 타입을 이용해서 선언된 변수는 실제 값을 변수 안에 저장하지만, 참조 타입을 이용해서 선언된 변수는 메모리의 번지를 값으로 갖는다.
> 번지를 통해 객체를 참조한다는 뜻에서 참조 타입이라고 부른다.

예를 들어 int와 double로 선언된 변수 age와 price가 있고, String 클래스로 선언된 name과 hobby가 다음과 같이 선언되어 있다고 가정해보자.

```java
// 기본 타입 변수
int age = 25;
double price = 100.5;

// 참조 타입 변수
String name = "신용권";
String hobby = "독서";
```

메모리상에서 이 변수들이 갖는 값을 그림으로 표현하면 다음과 같다. 
> 변수가 스택 영역에 생성되고 객체는 힙 영역에 생성된다는 것만 알아두자.

<p align = "center"><img src = "https://user-images.githubusercontent.com/106001755/170263212-44d7b4a6-60b6-4c92-a529-fb3811a66dd3.png" witdh="450" height="300"></p>

int와 double 변수인 age와 price는 직접 값을 저장하고 있지만, String 클래스 변수인 name과 hobby는 힙 영역의 String 객체 주소 값을 가지고 있다. 주소를 통해 객체를 참조한다는 뜻에서 String 클래스 변수를 참조 타입 변수라고 한다.

</details>

<details markdown="1">
<summary>5.2 메모리 사용 영역</summary>  
<p align = "center"><img src = "https://user-images.githubusercontent.com/106001755/170264902-569f3029-432e-45da-98c4-262ce21f41a8.png" width="500" height="400"></p>


### 5.2.1 메서드(Method) 영역
- 메서드 영역에는 코드에서 사용되는 클래스(~.class)들을 클래스 로더로 읽어 클래스별로 런타임 상수풀(runtime constant pool), 필드(field) 데이터,메서드(method) 데이터, 메서드 코드, 생성자(constructor) 코드 등을 분류해서 저장한다. 
- 메서드 영역은 JVM이 시작할 때 생성되고, 모든 스레드가 공유하는 영역이다.

1. 힙(Heap) 영역
- 객체와 배열이 생성되는 영역이다.
- 힙 영역에 생성된 객체와 배열은 JVM 스택 영역의 변수나 다른 객체의 필드에서 참조한다. 
- 참조하는 변수나 필드가 없다면 의미 없는 객체가 되기 때문에 이것을 쓰레기로 취급하고 JVM은 쓰레기 수집기(Garbage Collector)를 실행시켜 쓰레기 객체를 힙 영역에서 자동으로 제거한다.

2. JVM 스택(Stack) 영역
- 각 스레드마다 하나씩 존재하며 스레드가 시작될 때 할당된다.  
- 변수가 이 영역에 생성되는 시점은 초기화가 될 때, 즉 최초로 변수에 값이 저장될 때 기본 타입 변수와 참조 타입 변수가 추가(push)되거나 제거(pop)된다.  
- 변수는 선언된 블록 안에서만 존재하고 블록을 벗어나면 스택에서 제거된다.


</details>

<details markdown="1">
<summary>5.3 참조 변수의 ==, != 연산</summary>  

- 기본 타입 변수의 ==, != 연산은 변수의 값이 같은지, 아닌지 조사
- 참조 타입 변수의 ==, != 연산은 동일한 객체를 참조하는지, 다른 객체를 참조하는지 조사
> 참조 타입 변수의 값은 힙 영역의 객체 주소이므로 결국 **주소 값을 비교**하는 것이 된다.
> 동일한 주소 값을 갖고 있다는 것은 동일한 객체를 참조한다는 의미이다.
>>( == 의 결과 : True, !=의 결과 : False)

<p align = "center"><img src = "https://user-images.githubusercontent.com/106001755/170266646-6a5d6a9e-68d1-4851-b629-ecc7080635f8.png" width="450" height="300"></p>

상기 그림에서 `refVar1`과 `refVar2`는 서로 다른 객체를 참조하고 있으므로 == 및 != 연산의 결과는 다음과 같다.

```java
refVar1 == refVar2 // 결과 : false
refVar1 != refVar2 // 결과 : true
```

`refVar2`과 `refVar3`는 동일한 객체2를 참조하고 있으므로 == 및 != 연산의 결과는 다음과 같다.

```java
refVar2 == refVar3 // 결과 : true
refVar2 != refVar3 // 결과 : false
```

</details>

<details markdown="1">
<summary>5.4 null과 NullPointerException</summary>  

- 참조 타입 변수는 힙 영역의 객체를 참조하지 않는다는 뜻으로 `null(널)` 값을 가질 수 있다. null 값도 초기값으로 사용할 수 있기 때문에 null로 초기화된 참조 변수는 스택 영역에 생성된다.

<p align = "center"><img src = "https://user-images.githubusercontent.com/106001755/170267700-bf82ee0a-7676-4dc5-83fd-3b9b5cc3bc68.png" width="450" height="160"></p>

참조 타입 변수가 `null` 값을 가지는지 확인하려면 다음과 같이 ==, != 연산을 수행하면 된다. 상기 그림에서 reVar1은 힙 영역의 객체를 참조하므로 연산의 결과는 다음과 같다.

```java
refVar1 == null // 결과값 : false
refVar1 != null // 결과값 : true
```

refVar2는 null값을 가지므로 연산의 결과는 다음과 같다.

```java
refVar2 == null // 결과값 : true
refVar2 != null // 결과값 : false
```

- 자바는 프로그램 도중에 발생하는 오류를 `예외(Exception)`라고 부른다. 
- `NullPointerException` 예외는 참조 타입 변수를 잘못 사용하면 발생한다. 
- 참조 타입 변수가 null을 가지고 있을 경우, 참조 타입 변수는 사용할 수 없다.
> 참조 타입 변수를 사용하는 것은 곧 객체를 사용하는 것을 의미하는데, 참조할 객체가 없으므로 사용할 수 없는 것이다.

```java
int[] intArray = null;
intArray[0] = 10; // NullPointerException
```

상기 코드에서 `intArray`는 배열 타입 변수이므로 참조 타입 변수이다. 그래서 null로 초기화가 가능하다. 이 상태에서 `intArray[0]`에 10을 저장하려고 하면 NullPointerException이 발생한다. intArray 변수가 참조하는 배열 객체가 없기 때문이다. 다른 코드를 보자

```java
String str = null;
System.out.println("총 문자수: " + str.lenth()); // NullPointerException
```

String은 클래스 타입이므로 참조 타입이다. 따라서 str 변수도 null로 초기화가 가능하다. 이 상태에서 String 객체의 length()라는 메서드를 호출하면 NullPointException이 발생한다. str 변수가 참조하는 String 객체가 없기 때문이다.

</details>

<details markdown="1">
<summary>5.5 String 타입</summary>

자바는 문자열을 `String` 변수에 저장하기 때문에 다음과 같이 String 변수를 우선 선언해야 한다.

```java
String 변수;
```

String 변수에 문자열을 저장하려면 큰 따옴표로 감싼 문자열 리터럴을 대입하면 된다.

```java
변수 = "문자열";
```

변수 선언과 동시에 문자열을 저장할 수도 있다.

```java
String 변수 = "문자열";
```

다음은 두 개의 String 변수를 선언하고 문자열을 저장한다.

```java
String name;
name = "신용권";
String hobby = "자바";
```

<p align = "center"><img src = "https://user-images.githubusercontent.com/106001755/170269979-2ea5e0c9-51b2-4d1f-9605-a3f10b8e0b25.png" width="400" height="350"></p>

- 사실 문자열을 String 변수에 저장한다는 말은 틀린 표현이다.
- 문자열이 직접 변수에 저장되는 것이 아니라, 문자열은 String 객체로 생성되고 변수는 String 객체를 참조한다.
- 위 그림을 보면 name 변수와 hobby 변수는 스택 영역에 생성되고, 문자열 리터럴인 "신용권"과 "자바"는 힙 영역에 String 객체로 생성된다. 그리고 name 변수와 hobby 변수에는 String 객체의 주소 값이 저장된다.

자바는 문자열 리터럴이 동일하다면 String 객체를 공유하도록 되어 있다. 다음과 같이 name1과 name2 변수가 동일한 문자열 리터럴인 "신용권"을 참조할 경우 name1과 name2는 동일한 String 객체를 참조하게 된다.

```java
String name1 = "신용권";
String name2 = "신용권";
```

<p align = "center"><img src = "https://user-images.githubusercontent.com/106001755/170270608-a04feb77-1d69-403f-925b-6bfafb72cc08.png" width="450" height="180"></p>

일반적으로 변수에 문자열을 저장할 경우에는 문자열 리터럴을 사용하지만, `new` 연산자를 사용해서 직접 String 객체를 생성시킬 수도 있다. new 연산자는 힙 영역에 새로운 객체를 만들 때 사용하는 연산자로 `객체 생성 연산자`라고 한다.

```java
String name1 = new String("신용권");
String name2 = new String("신용권");
```

이 경우 name1과 name2는 서로 다른 String 객체를 참조한다.

<p align = "center"><img src = "https://user-images.githubusercontent.com/106001755/170271133-23654e4f-8d8e-48c1-916f-5f2b8827a636.png" width="450" height="300"></p>

문자열 리터럴로 생성하느냐 new 연산자로 생성하느냐에 따라 비교 연산자의 결과가 달라질 수 있다. 동일한 문자열 리터럴로 String 객체를 생성했을 경우 == 연산의 결과는 true가 나오지만, new 연산자로 String 객체를 생성했을 경우 == 연산의 결과는 false가 나온다. == 연산자는 변수에 저장된 객체 번지가 동일한지를 검사하기 때문이다.

```java
String name1 = "신민철";
String name2 = "신민철";
String name3 = new String("신민철");
```

name1과 name2는 동일한 문자열 리터럴로 생성된 객체를 참조하기 때문에 name1 == name2의 결과는 true가 나온다. 그러나 name3는 new 연산자로 String 객체를 별도로 생성했기 때문에 name1 == name3은 false가 나온다. 동일한 String 객체이건 다른 String 객체이건 상관없이 문자열만을 비교할 때에는 String 객체의 `equals()` 메서드를 사용해야 한다. equals() 메서드는 원본 문자열과 매개값으로 주어진 비교 문자열이 동일한지 비교한 후 true 또는 false를 리턴한다.

```java
boolean result = str1.equals(str2);
```

```java
public class StiringEqualsExample {
  public static void main(String[] args) {
    String strVar1 = "신민철";
    String strVar2 = "신민철";
    
    if(strVar1 == strVar2) {
      System.out.println("strVar1과 strVar2는 참조가 같음");
    } else {
      System.out.println("strVar1과 strVar2는 참조가 다름");
    }
    
    if(strVar1.equals(strVar2)) {
      System.out.println("strVar1과 strVar2는 문자열이 같음");
    }
    
    String strVar3 = new String("신민철");
    String strVar4 = new String("신민철");
    
    if(strVar3 == strVar4) {
      System.out.println("strVar3과 strVar4는 참조가 같음");
    } else {
      System.out.println("strVar3과 strVar4는 참조가 다름");
    }
    
    if(strVar3.equals(strVar4)) {
      System.out.println("strVar3과 strVar4는 문자열이 같음");
    }
  }
}
```

실행 결과
```java
strVar1과 strVar2는 참조가 같음
strVar1과 strVar2는 문자열이 같음
strVar3과 strVar4는 참조가 다름
strVar3과 strVar4는 문자열이 같음
```

String 변수는 참조 타입이므로 초기값으로 null을 대입할 수 있따. null은 String 변수가 참조하는 String 객체가 없다는 뜻이다.
```java
String hobby = null;
```
다음 코드처럼 hobby 변수가 String 객체를 참조하였으나, null을 대입함으로써 더 이상 String 객체를 참조하지 않도록 할 수도 있다.
```java
String hobby = "여행";
hobby = null;
```
</details>

<details markdown="1">
<summary>5.6 배열 타입</summary>

### 5.6.1 배열이란?  
- 같은 타입의 데이터를 연속된 공간에 나열시키고, 각 데이터에 인덱스(index)를 부여해 놓은 자료구조이다.

<p align = "center"><img src = "https://user-images.githubusercontent.com/106001755/170281779-1334d0c8-6a8a-4e54-86fc-ae3d473ab247.png" width = "900" height="350"></p>

이렇게 성적을 배열로 만들면 성적의 평균값은 배열의 인덱스를 통해 for문으로 쉽게 구할 수 있다.
```java
int sum = 0;
for(int i=0; i<30; i++) {
  sum += score[i];
}
int avg = sum / 30;
```
- 배열은 같은 타입의 데이터만 저장할 수 있다.
> int 배열은 int 값만 저장 가능하고, String 배열은 문자열만 저장 가능하다.

- 한 번 생성된 배열은 길이를 늘리거나 줄일 수 없다.
> 만약 길이를 변경해야 한다면 새로운 배열을 생성하고 기존 배열 항목을 새 배열로 복사해야 한다.

---

### 5.6.2 배열 선언   
배열을 사용하기 위해선 배열 변수를 선언해야 한다. 배열 변수 선언은 다음과 같이 두 가지 형태로 작성할 수 있다.  
```java
타입[ ] 변수;                 타입 변수[];
```

대괄호 []는 배열 변수를 선언하는 기호로 사용되는데, 타입 뒤에 붙을 수도 있고 변수 뒤에 붙을 수도 있다. 타입은 배열에 저장할 데이터의 타입을 말한다.  
```java
int[] intArray;              int inArray[];  
double[] doubleArray;        double doubleArray[]; 
String[] strArray;           String strArray[];
```

배열 참조는 참조 변수에 속한다. 배열도 객체이므로 힙 영역에 생성되고 배열 변수는 힙 영역의 배열 객체를 참조하게 된다. 참조할 배열 객체가 없다면 배열 변수는 null 값으로 초기화될 수 있다.
```java
타입[] 변수 = null;
```
만약 배열 변수가 null 값을 가진 상태에서 변수[인덱스]로 값을 읽거나 저장하게 되면 NullPointException이 발생한다. 배열 변수는 배열을 생성하고 참조하는 상태에서 값을 저장하고나 읽어야 한다.

---

### 5.6.3 값 목록으로 배열 생성

배열 항목에 저장될 값의 목록이 있다면, 다음과 같이 간단하게 배열 객체를 만들 수 있다.
```java
데이터타입[] 변수 = { 값0, 값1, 값2, 값3, ... };
```
- 변수 선언과 동시에 값 목록 대입
<p align = "center"><img src = "https://user-images.githubusercontent.com/106001755/170288746-89cb8dc0-6bb1-4b5f-b2cb-754641c8bee2.png" width="500" height="150"></p>

- 변수 선언 후 값 목록 대입
```java
데이터타입[] 변수;
변수 = new 타입[] { 값0, 값1, 값2, 값3, ... };
```

중괄호 {}는 주어진 값들을 항목으로 가지는 배열 객체를 힙에 생성하고, 배열 객체의 번지를 리턴한다. 배열 변수는 리턴된 번지를 저장함으로써 참조가 이루어진다. 

[ ArrayCreateByValueListExample1.java ] 값 목록으로 배열 생성
```java
public class ArrayCreateByValueListExample1 {
  public static void main(String[] args) {
    int[] scores = { 83, 90, 87 };
    
    System.out.println("scores[0] : " + scores[0]);
    System.out.println("scores[1] : " + scores[1]);
    System.out.println("scores[2] : " + scores[2]);
    
    int sum = 0;
    for(int i = 0; i<3; i++) {
      sum += scores[i];
    }
    System.out.println("총합 : " + sum);
    double avg = (double) sum / 3;
    System.out.println("평균 : " + avg);
  }
}
```
값의 목록으로 배열 객체를 생성할 때 배열 변수를 이미 선언한 후에 다른 실행 문에서 중괄호를 사용한 배열 생성은 허용되지 않는다.
```java
타입[] 변수;
변수 = { 값0, 값1, 값2, 값3, ... }; // 컴파일 에러
```
배열 변수를 미리 선언한 후, 값 목록들이 나중에 결정되는 상황이라면 다음과 같이 `new 연산자`를 사용해서 값 목록을 지정해주면 된다. new 연산자 바로 뒤에는 배열 변수 선언에서 사용한 "타입[]"를 붙여주고 중괄호 {}에는 값들을 나열해주면 된다.
```java
변수 = new 타입[] { 값0, 값1, 값2, 값3, ... };
```
예를 들어 배열 names를 다음과 같이 생성할 수 있다.
```java
String[] names = null;
names = new String[] { "신용권", "홍길동", "김자바"};
```
메서드의 매개값이 배열일 경우에도 마찬가지이다. 아래와 같이 매개 변수로 int[] 배열이 선언된 add() 메서드가 있을 경우, 값 목록으로 배열을 생성함과 동시에 add() 메서드의 매개값으로 사용하고자 할 때는 반드시 new 연산자를 사용해야 한다.
```java
int add(int[] scores) {...}
----------------------------------
int result = add( {95, 85, 90} ); // 컴파일 에러
int result = add( new int[] {95, 85, 90} );
```
[ ArrayCreateByValueListExample2.java ] 값의 리스트로 배열 생성
```java
public class ArrayCreateByValueListExample2 {
  public static void main(String[] args) {
    int[] scores;
    scroes = new int[] { 83, 90, 87 };
    int sum1 = 0;
    for(int i=0; i<3; i++) {
      sum1 += scores[i];
    }
    System.out.println("총합 : " + sum1);
    
    int sum2 = add( new int[] {83, 90, 87} );
    System.out.println("총합 : " + sum2);
    System.out.println();
  }
  
  public static int add(int[] scores) {
    int sum = 0;
    for(int i=0; i<3; i++) {
      sum += scores[i];
    }
    return sum;
  }
}

}
```
실행 결과
```java
총합 : 260
총합 : 260
```

---

### 5.6.4 new 연산자로 배열 생성

값의 목록을 가지고 있지 않지만, 향후 값들을 저장할 배열로 미리 만들고 싶다면 new 연산자로 다음과 같이 배열 객체를 생성시킬 수 있다.

`타입[] 변수 = new 타입[길이];`

길이는 배열이 저장할 수 있는 값의 수를 말한다. new 연산자로 배열을 생성할 경우에는 이미 배열 변수가 선언된 후에도 가능하다.

`타입[] 변수 = null;`  
`변수 = new 타입[길이];`

다음은 길이가 5인 int[] 배열을 생성한다.

`int[] intArray = new int[5];`

자바는 intArrayu[0] ~ intArray[4]까지 값이 저장될 수 있는 공간을 확보하고, 배열의 생성 번지를 리턴한다. 리턴된 번지는 intArray 변수에 저장된다. 

<p align = "center"><img src = "https://user-images.githubusercontent.com/106001755/170704706-3e120194-af93-41db-a44e-ed2a3125a98b.png" width="700" height="300"></p>

- 타입별로 배열의 초기값

<p align = "center"><img src = "https://user-images.githubusercontent.com/106001755/170704927-ee9a4919-1e7a-4e43-add7-b99a4e26a294.png" width="400" height="300"></p>

---

### 5.6.5 배열 길이

배열의 길이간 배열에 저장할 수 있는 전체 항목 수를 말한다. 코드에서 배열의 길이를 얻으려면 다음과 같이 배열 객체의 length 필드를 읽으면 된다. 

```java
배열변수.length;
```

다음은 배열 intArray의 길이를 알아보는 코드이다.

```java
int[] intArray = {10, 20, 30};
int num = intArray.length;
```

length 필드는 읽기 전용 필드이기 때문에 값을 바꿀 수 없다.

```java
intArray.length = 10; // 잘못된 코드
```

배열의 length 필드는 for문을 사용해서 배열 전체를 루핑할 때 매우 유용하게 사용할 수 있다.

---

### 5.6.6 커맨드 라인 입력













</details>

## Chapter 06 클래스

<details markdown="1">
<summary>6.1 객체 지향 프로그래밍</summary>

- 어떤 제품을 만들 때, 부품을 먼저 개발하고 이 부품들을 하나씩 조립해서 완성된 제품을 만들 듯이, 소프트웨어를 개발할 때에도 부품에 해당하는 객체들을 먼저 만들고, 이것들을 하나씩 조립해서 완성된 프로그램을 만드는 기법을 객체 지향 프로그래밍(OOP : Object Oriented Programming)이라고 한다.

- 객체 지향이 나온 이유 : 하드웨어 부품처럼 재사용할 수 있는 방법이 없을까? 에서 시작했다.

### 6.1.1 객체란?

물리적으로 존재하고 추상적으로 생각할 수 있는 것 중에서 자신의 속성(상태)을 가지고 있고, 다른 것과 식별 가능한 것을 말한다.

자바에는 속성과 동작들을 각각 필드(field)와 메서드(method)라고 부른다.

<p align = "center"><img src = "https://user-images.githubusercontent.com/106001755/170723189-7fc96789-5fa5-4554-8043-ad8561f26b6e.png"></p>

---

### 6.1.2 객체의 상호작용

- 객체들은 서로 간에 기능(동작)을 이용하고 데이터를 주고 받는다.  
- 객체들 사이의 상호작용 수단은 메서드이다.
> 객체가 다른 객체의 기능을 이용하는 것이 바로 메서드 호출이다.

<p align = "center"><img src = "https://user-images.githubusercontent.com/106001755/170809488-d63ebdb0-a04e-4537-a378-3323bb143577.png" width="400" height="220"></p>

---

### 6.1.3 객체 간의 관계

객체는 개별적으로 사용될 수 있지만, 대부분 다른 객체와 관계를 맺고 있다. 

- 관계의 종류
  - 집합 관계 : 완성품과 부품의 관계
  - 사용 관계 : 객체 간의 상호작용(객체가 다른 객체의 메서드를 호출하는 것)
  - 상속 관계 : 상위(부모) 객체를 기반으로 하위(자식) 객체를 생성하는 관계

<p align = "center"><img src = "https://user-images.githubusercontent.com/106001755/170809599-5c8c2931-f628-428e-8a67-42438a3c14e2.png"></p>

---

### 6.1.4 객체 지향 프로그래밍의 특징

1. **Information Hiding(정보 은닉)** : 나의 상태(속성, 필드)는 나의 행위(동작, 메서드)로만 바꿀 수 있다.(제 3자가 나의 상태(속성)을 바꿀 수 없도록 접근 금지 시키는 것)
   > 나의 상태(속성)를 나의 행위(동작)으로만 바꿀 수 있도록 다른 행위(동작)의 접근을 막는 것
     
   > 접근 제한자를 이용해 정보 은닉이 가능하다.

2. **Encapsulation(캡슐화)** : 객체를 캡슐로 싸서 내부를 볼 수 없게 하는 것(어떤 객체가 그 객체를 가질 수밖에 없도록 상태(속성, 필드)와 행위(동작, 메서드)를 묶는 것)

3. **Inheritance(상속)** :  상위(부모) 객체의 필드와 메서드를 하위(자식) 객체에게 물려주는 것(반복된 코드의 중복을 줄여준다.)

4. **Polymorphism(다형성)** : 타입이지만 실행 결과가 다양한 객체를 대입할 수 있는 성질

<p align = "center"><img src = "https://user-images.githubusercontent.com/106001755/170810116-9ecff5c2-179c-40f5-974c-92db340c7fb2.png"></p>


</details>

<details markdown="1">
<summary>6.2 객체와 클래스</summary> 

- 예를 들어 사람들이 자동차를 이용하기 위해서는 공장에서 설계도를 보고 만들어야 한다. 객체 지향 프로그래밍에서도 마찬가지이다. 
- 메모리에서 사용하고 싶은 객체가 있다면 우선 설계도로 해당 객체를 만드는 작업이 필요한다. 자바에서는 설계도가 바로 **클래스(class)** 이다. 클래스에는 객체를 생성하기 위한 필드와 메서드가 정의되어 있다. 클래스로부터 만들어진 객체를 해당 클래스의 **인스턴스(instance)** 라고 한다. 
- 자동차 객체는 자동차 클래스의 인스턴스인 셈이다. 그리고 클래스로부터 객체를 만드는 과정을 인스턴스화라고 한다. 하나의 클래스로부터 여러 개의 인스턴스를 만들 수 있다.

```
객체 지향 프로그래밍 개발 3단계
1. 클래스 설계
2. 설계된 클래스를 이용한 객체 생성
3. 생성된 객체 이용
```
</details>

<details markdown="1">
<summary>6.3 클래스 선언</summary>  

- 자바 식별자 작성 규칙에 따라야 한다.

<p align = "center"><img src = "https://user-images.githubusercontent.com/106001755/170810621-f5c82315-f010-4a6b-812d-f311cffcdaed.png"></p>

- 자바 언어는 영어 대소문자를 다른 문자로 취급하기 대문에 클래스 이름도 영어 대소문자를 구분한다.
- 클래스 이름이 단일 단어라면 첫 자를 대문자로 하고 나머지는 소문자로 작성하는 것이 관례이다.
- 서로 다른 단어가 혼합된 이름을 사용한다면 각 단어의 첫 머리 글자는 대문자로 작성하는 것이 관례이다.
> Calculator, Car, Menber, ChatClient, ChatServer, Web_Browser


클래스 이름을 정했다면 "클래스이름.java"로 소스 파일을 생성해야 한다. 소스 파일 이름 역시 대소문자를 구분하므로 반드시 클래스 이름과 대소문자가 같도록 해야 한다. 소스 파일을 생성했다면 소스 파일을 열고 다음과 같이 클래스를 선언해준다.

```java
public class 클래스 이름 {

}
```

여기서 public class 키워드는 클래스를 선언할 때 사용하며 반드시 소문자로 작성해야 한다. 클래스 이름 뒤에는 반드시 중괄호 {}를 붙여주는데, 중괄호 시작({)은 클래스 선언의 시작을 알려주고 중괄호 끝(})은 클래스 선언의 끝을 알려준다. 다음은 Car 클래스를 선언한 것이다.

```java
public class Car {

}
```

일반적으로 소스 파일당 하나의 클래스를 선언하지만, 두 개 이상의 클래스 선언도 가능하다.

```java
public class Car {

}

class Tire {

}
```

두 개 이상의 클래스가 선언된 소스 파일을 컴파일하면 바이트 코드 파일(.class)은 클래스를 선언한 개수만큼 생긴다. 상기 코드를 컴파일하면 Car.class와 Tire.class가 각각 생성된다. **주의할 점은 파일 이름과 동일한 이름의 클래스 선언에만 public 접근 제한자를 붙일 수 있다.** 가급적 소스 파일 하나당 동일한 이름의 클래스 하나를 생성하는 것이 좋다.

</details>

<details markdown="1">
<summary>6.4 객체 생성과 클래스 변수</summary>  

- 클래스를 선언한 다음, 컴파일을 했다면(이클립스에서는 저장) 객체를 생성할 설계도가 만들어진 셈이다. 클래스로부터 객체를 생성하는 방법은 다음과 같이 new 연산자를 사용하면 된다.

```java
new 클래스();
```

- new는 클래스로부터 객체를 생성시키는 연산자이다. new 연산자 뒤에는 생성자가 오는데, 생성자는 클래스() 형태를 가지고 있다. 
- new 연산자로 생성된 객체는 메모리 힙(heap) 영역에 생성된다. 
- new 연산자는 힙 영역에 객체를 생성시킨 후, 객체의 주소를 리턴하도록 되어있다.
- 이 주소를 참조 타입인 클래스 변수에 저장해두면, 변수를 통해 객체를 사용할 수 있다.

```java
클래스 변수;
변수 = new 클래스();
```

클래스 변수 선언과 객체 생성을 한 개의 실행문으로 작성할 수도 있다.

```java
클래스 변수 = new 클래스();
```

다음 예제는 Student 클래스를 선언하고 StudentExample 클래스의 main() 메서드에서 Student 객체를 생성한다.

**[ Student.java ] 클래스 선언**

```java
public class Student {
}
```

**[ StudentExample.java ] 클래스로부터 객체 생성**

```java
public class StudentExample {
  public static void main(String[] args) {
    Student s1 = new Student;
    System.out.println("s1 변수가 Student 객체를 참조합니다.");
    
    Student s2 = new Student;
    System.out.println("s1 변수가 Student 객체를 참조합니다.");
  }
}
```
실행 결과
```java
s1 변수가 Student 객체를 참조합니다.
s1 변수가 Student 객체를 참조합니다.
```

Student 클래스는 하나지만 new 연산자를 사용한 만큼 객체가 메모리에 생성된다. 이러한 객체들은 Student 클래스의 인스턴스들이다. s1과 s2가 참조하는 Student 객체는 완전히 독립된 서로 다른 객체이다.

Student에 main() 메서드를 작성해서 라이브러리인 동시에 실행 클래스로 만들 수도 있다.

```java
public class Student {
  public static void main(String[] args) {
    Student s1 = new Student();
    System.out.println("s1 변수가 Student 객체를 참조합니다.");
    
    Student s2 = new Student();
    System.out.println("s2 변수가 또 다른 Student 객체를 참조합니다.");
  }
}
```
대부분의 객체 지향 프로그램은 라이브러리(부품 객체 및 완성 객체)와 실행 클래스가 분리되어 있다.
</details>

<details markdown="1">
<summary>6.5 클래스의 구성 멤버</summary>

### 6.5.1 필드

객체의 고유 데이터, 부품 객체, 상태 정보를 저장하는 곳이다. 선언 형태는 변수와 비슷하지만, 필드를 변수라고 부르지 않는다. 변수는 생성자와 메서드 내에서만 사용되고 생성자와 메서드가 실행 종료되면 자동 소멸한다. 하지만 필드는 생성자와 메서드 전체에서 사용되며 객체가 소멸되지 않는 한 객체와 함께 존재한다.

---

### 6.5.2 생성자

생성자는 new 연산자로 호출되는 특별한 중괄호 {} 블록이다. 생성자의 역할은 객체 생성 시 초기화를 담당한다. 필드를 초기화하거나, 메서드를 호출해서 객체를 사용할 준비를 한다. 생성자는 메서드와 비슷하게 생겼지만 클래스 이름으로 되어 있고 리턴 타입이 없다.

---

### 6.5.3 메서드

메서드는 객체의 동작에 해당하는 중괄호 {} 블록을 말한다. 중괄호 블록은 이름을 가지고 있는데, 이것이 메서드 이름이다. 메서드를 호출하게 되면 중괄호 블록에 있는 모든 코드들이 일괄적으로 실행된다. 메서드는 필드를 읽고 수정하는 역할도 하지만, 다른 객체를 생성해서 다양한 기능을 수행하기도 한다. 메서드는 객체 간의 데이터 전달의 수단으로 사용된다. 외부로부터 매개값을 받을 수도 있고, 실행 후 어떤 값을 리턴할 수도 있다.

<p align = "center"><img src = "https://user-images.githubusercontent.com/106001755/170898853-c7543996-3460-4b15-a9eb-315db2755b2f.png"></p>

</details>

<details markdown="1">
<summary>6.6. 필드</summary>

- 객체 고유의 데이터, 객체가 가져야 할 부품, 객체의 현재 상태 데이터를 저장하는 곳이다.

### 6.6.1 필드 선언

필드 선언은 클래스 중괄호 {} 블록 어디서든 존재할 수 있다. 생성자 선언과 메서드 선언의 앞과 뒤 어떤 곳에서도 필드 선언이 가능하다. 하지만 생성자와 메서드 중괄호 블록 내부에서는 선언될 수 없다. 생성자와 메서드 중괄호 블록 내부에 선언된 것은 모두 로컬 변수가 된다. 

타입은 필드에 저장할 데이터의 종류를 결정한다. 타입에는 기본 타입(byte, short, int, long, float, double, boolean)과 참조 타입(배열, 클래스, 인터페이스)이 모두 올 수 있다. 필드의 초기값은 필드 선언 시 주어질 수도 있고, 생략될 수도 있다. 다음은 올바르게 필드를 선언한 예를 보여준다.

```java
String company = "현대자동차";
String model = "그랜져";
String color = "검정";
int maxSpeed = 350;
int productionYear;
int currentSpeed;
boolean engineStart;
```

---

### 6.6.2 필드 사용

필드를 사용한다는 것은 필드값을 읽고, 변경하는 작업을 말한다. 클래스 내부의 생성자나 메서드에서 사용할 경우 단순히 필드 이름으로 읽고 변경하면 되지만, 클래스 외부에서 사용할 경우 우선적으로 클래스로부터 객체를 생성한 뒤 필드를 사용해야 한다. 그 이유는 필드는 객체에 소속된 데이터이므로 객체가 존재하지 않으면 필드도 존재하지 않기 때문이다.

<p align = "center"><img src ="https://user-images.githubusercontent.com/106001755/170852647-ffcdff67-f441-4493-81db-9fe6c6dcd142.png">,</p>

위 그림을 보면 Car 클래스의 speed 필드는 생성자와 메서드에서 변경이 가능하다. 사용 방법은 변수와 동일한데, 차이점은 변수는 자신이 선언된 생성자 또는 메서드 블록 내에서만 사용할 수 있는 반면 필드는 생성자와 모든 메서드에서 사용이 가능하다. 외부 Person 클래스에서 Car 클래스의 speed 필드값을 사용하려면 Car 객체를 우선 생성해야 한다.

```java
Car myCar = new Car();
```

myCar 변수가 Car 객체를 참조하게 되면, 도트(.) 연산자를 사용해서 speed 필드에 접근할 수 있다. 도트(.) 연산자는 객체 접근 연산자로 객체가 가지고 있는 필드나, 메서드를 사용하고자 할 때 사용된다. 다음 코드는 Car 객체의 speed 필드값을 60으로 변경하고 있다.

```java

myCar.speed = 60;

```

[ Car.java ] Car 클래스 필드 선언
```java
public class Car {
  // 필드
  String company = "현대자동차";
  String model = "그랜져";
  String color = "검정";
  int maxSpeed = 350;
  int speed;
}
```

[ CarExample.java ] 외부 클래스에서 Car 필드값 읽기와 변경
```java
public class CarExample { 
  public static void main(String[] args) {
    // 객체 생성
    Car myCar = new Car();
    
    // 필드값 읽기
    System.out.println("제작회사 : " + myCar.company);
    System.out.println("모델명 : " + myCar.model);
    System.out.println("색상 : " + myCar.color);
    System.out.println("최고속도 : " + myCar.maxSpeed);
    System.out.println("현재속도 : " + myCar.speed);
    
    // 필드값 변경
    myCar.speed = 60;
    System.out.println("변경된 속도 : " + myCar.speed);
  }
}
```

실행결과
```
제작회사 : 현대자동차
모델명 : 그랜져
색상 : 검정
최고속도 : 350
현재속도 : 0
변경된 속도 : 60
```

Car 클래스는 speed 필드 선언 시 초기값을 주지 않았다. 그러나 출력해보면 기본값이 0이 들어있는 것을 확인할 수 있다.

*예제*

[ Circle.java ] 반지름과 이름을 가진 Circle 클래스를 작성하고, Circle 클래스의 객체를 생성하라.
```java
public class Circle {
  int radius;                                  // 원의 반지름
  String name;                                 // 원의 이름
  
  public double getArea {                      // 메서드
    return 3.14 * radius * radius;
  }
  
  public static void main(String[] args) {
    Circle pizza;
    pizza = new Circle();                      // Circle 객체 생성
    // Circle pizza = new Circle();            // 한 줄로 선언 가능
    pizza.radius = 10;
    pizza.name = "자바피자";
    double area = pizza.getArea();
    System.out.println(pizza.name + "의 면적은 : " + area);
    
    Circle donut = new Circle();
    donut.radius = 2;
    donut.name = "자바도넛";
    area = donut.getArea();
    System.out.println(donut.name + "의 면적은 : " + area);
  }
}
```
</details>

<details markdown="1">
<summary>6.7 생성자</summary>

- 생성자는 new 연산자와 같이 사용되어 클래스로부터 객체를 생성할 때 호출되어 객체의 초기화를 담당한다.
- 객체 초기화란 필드를 초기화하거나 메서드를 호출해서 객체를 사용할 준비를 하는 것을 말한다.
> 생성자를 실행시키지 않고는 클래스로부터 객체를 만들 수 없다.

### 6.7.1 기본 생성자

모든 클래스는 생성자가 반드시 존재하며, 하나 이상을 가질 수 있다. 클래스 내부에 생성자 선언을 생략했다면 컴파일러는 다음과 같이 중괄호 {} 블록 내용이 비어있는 기본 생성자를 바이트 코드에 자동으로 추가시킨다.

```java
[public] 클래스() {

}
```

클래스가 public class로 선언되면 기본 생성자에도 public이 붙지만, 클래스가 public 없이 class로만 선언되면 기본 생성자에도 public이 붙지 않는다. 예를 들어 Car 클래스를 설계할 때 생성자를 생략하면 기본 생성자가 다음과 같이 생성된다.

<p align = "center"><img src = "https://user-images.githubusercontent.com/106001755/170852883-ffe6c6ea-adee-4176-8df3-f72a9046c352.png"></p>

그렇기 때문에 클래스에 생성자를 선언하지 않아도 다음과 같이 new 연산자 뒤에 기본 생성자를 호출해서 객체를 생성시킬 수 있다.

```java
Car myCar = new Car();
```

그러나 클래스에 **명시적으로 선언한 생성자가 한 개라도 있으면**, 컴파일러는 **기본 생성자를 추가하지 않는다.**

---

### 6.7.2 생성자 선언

기본 생성자 대신 생성자를 명시적으로 선언하려면 다음과 같은 형태로 작성하면 된다.

<p align = "center"><img src = "https://user-images.githubusercontent.com/106001755/170852936-b26a96e1-9844-4f38-90e7-5d5011bc0ae3.png"></p>

생성자는 메서드와 비슷한 모양을 가지고 있으나, 리턴 타입이 없고 클래스 이름과 동일하다. 생성자 블록 내부에는 객체 초기화 코드가 작성되는데, 일반적으로 필드에 초기값을 저장하거나 메서드를 호출하여 객체 사용 전에 필요한 준비를 한다.

매개 변수 선언은 생략할 수도 있고, 여러 개를 선언할 수도 있다. 매개 변수는 new 연산자로 생성자를 호출할 때 외부의 값을 생성자 블록 내부로 전달하는 역할을 한다. 예를 들어 다음과 가팅 Car 생성자를 호출할 때 세 개의 값을 제공한다고 보자.

```java
Car myCar = new Car("그랜져", "검정", 300);
```

두 개의 매개값은 String 타입이고 마지막 매개값은 int 타입인 것을 볼 수 있다. 세 매개값을 생성자가 받기 위해서는 다음과 같이 생성자를 선언해야 한다.

```java
public class Car {
  // 생성자
  Car(String model, String color, int maxSpeed);
}
```

클래스에 생성자가 명시적으로 선언되어 있을 경우에는 반드시 선언된 생성자를 호출해서 객체를 생성해야만 한다. 다음 예제를 보면 Car 클래스에 생성자 선언이 있기 때문에 기본 생성자 (Car())를 호출해서 객체를 생성할 수 없고 Car(Stirng color, int cc)를 호출해서 객체를 생성해야 한다.

[ Car.java ] 생성자 선언
```java
public class Car {
  // 생성자
  Car(String color, int cc) {
  }
}
```

[ CarExample.java ] 생성자를 호출해서 객체 생성
```java
public class CarExample {
  public static void main(Stirng[] args) {
    Car myCar = new Car("검정", 3000);
    //Car myCar = new Car(); (x) 기본 생성자를 호출할 수 없다.
  }
}
```

---

### 6.7.3 필드 초기화

- 클래스로부터 객체가 생성될 대 필드는 기본 초기값으로 자동 설정된다. 만약 다른 값으로 초기화를 하고 싶다면 두 가지 방법이 있다.
- 하나는 필드를 선언할 때 초기값을 주는 방법이고, 또 다른 하나는 생성자에서 초기값을 주는 방법이다.
- 필드를 선언할 때 초기값을 주게 되면 동일한 클래스로부터 생성되는 객체들은 모두 같은 데이터를 갖게 된다.

예를 들어 다음과 같이 Korean 클래스에 nation 필드를 선언하면서 "대한민국"으로 초기값을 준 경우, Korean 클래스로부터 k1과 k2 객체를 생성하면 각각 객채의 nation 필드에는 모두 "대한민국"이 저장되어 있다.

```java
public class Korean {
  String nation = "대한민국"
  String name;
  String ssn;
}

Korean k1 = new Korean();
Korean k2 = new Korean();
```

하지만 객체 생성 시점에 외부에서 제공되는 다양한 값들로 초기화되어야 한다면 생성자에서 초기화를 해야 한다. 위 코드에서 name과 ssn 필드값은 클래스를 작성할 때 초기값을 줄 수 없고 객체 생성 시점에 다양한 값을 가져야 한다. 따라서 생성자의 매개값으로 이 값들을 받아 초기화하는 것이 맞다.

```java
public class Korean {
  // 필드
  String nation = "대한민국"
  String name;
  String ssn;
  
  // 생성자
  public Korean(String n, String s) {
    name = n;
    ssm = s;
  }
}
```

아래 코드에서 "박자바", "김자바"는 매개 변수 n을 통해 전달되고, "011225-1234567", "930525-0654321"은 매겨 변수 s를 통해 전달된다. 이 값들은 각각 name 필드와 ssn 필드의 초기값으로 사용된다.

```java
Korean k1 = new Korean("박자바", "011225-1234567");
Korean k2 = new Korean("김자바", "930525-0654321");
```

[ Korean.java ] 생성자에서 필드 초기화
```java
public class Korean {
  // 필드
  String nation = "대한민국";
  String name;
  String ssn;
  
  // 생성자
  public Korean(String n, String s) {
    name = n;
    ssn = s;
  }
}
```

[ KoreanExample.java ] 객체 생성 후 필드값 출력
```java
public class KoreanExample {
  public static void main(String[] args) {
    Korean k1 = new Korean("박자바", "011225-1234567");
    System.out.println("k1.name : " + k1.name);
    system.out.println("k1.ssn : " + k1.ssn);
    
    Korean k2 = new Korean("김자바", "930525-0654321");
    System.out.println("k2.name : " + k2.name);
    System.out.println("k2.ssn : " + k2.ssn);
  }
}
```
출력결과
```
k1.name : 박자바
k1.ssn : 011225-1234567
k2.name : 김자바
k2.ssn : 930525-0654321
```

Korean 생성자의 매개 변수 이름은 각각 n과 s를 사용했다. 관례적으로 필드와 동일한 이름을 갖는 매개 변수를 사용한다. 이 경우 필드와 매개 변수 이름이 동일하기 때문에 생성자 내부에서 해당 필드에 접근할 수 없다. 왜냐하면 동일한 이름의 매개 변수가 사용 우선순위가 높기 때문이다. 해결 방법은 필드 앞에 "this."를 붙이면 된다. this는 객체 자신의 참조이다. this를 사용하여 Korean 생성자를 수정하면 다음과 같다.

```java
public Korean(String name, String ssn) {
  this.name = name;
  
  this.ssn = ssn;
}
```

---

### 6.7.4 생성자 오버로딩(Overloading)
- 생성자 오버로딩이란 매개 변수를 달리하는 생성자를 여러 개 선언하는 것을 말한다.

다음은 Car 클래스에서 생성자를 오버로딩한 예를 보여준다.

```java
public class Car {
  Car() { ... }
  Car(String model) { ... }
  Car(String model, String color) { ... }
  Car(String model, String color, int maxSpeed) { ... }
```

생성자 오버로딩 시 주의할 점은 **매개 변수의 타입의 개수 그리고 선언된 순서가 똑같을 경우 매개 변수 이름만 바꾸는 것은 생성자 오버로딩이라고 볼 수 없다.** 다음과 같은 경우에 해당한다.

```java
Car(String model, String color) { ... }
Car(String color, String model) { ... }  // 오버로딩이 아님
```

생성자가 오버로딩되어 있을 경우, new 연산자로 생성자를 호출할 때 제공되는 매개값의 타입과 수에 의해 호출될 생성자가 결정된다. 다음은 다양한 방법으로 Car 객체를 생성한다.

```java
Car car1 = new Car();
Car car2 = new Car("그랜저");
Car car3 = new Car("그랜저", "흰색");
Car car4 = new Car("그랜저", "흰색", "300");
```

다음 예제는 Car 생성자를 오버로딩해서 CarExample 클래스에서 다양한 방법으로 Car 객체를 생성하도록 했다.

[ Car. java ] 생성자의 오버로딩
```java
public class Car {
  // 필드
  String company = "현대 자동차";
  String model;
  String color;
  int maxSpeed;
  
  // 생성자
  Car() {
  }
  
  Car(String model) {
    this.model = model;
  }
  
  Car(String model, String color) {
    this.model = model;
    this.color = color;
  }
  
  Car(String model, String color, int maxSpeed) {
    this.model = model;
    this.color = color;
    this.maxSpeed = maxSpeed;
  }
}
```

[ CarExample.java ] 객체 생성 시 생성자 선택
```java
public class CarExmaple {
  public static void main(String[] args) {
    Car car1 = new Car();
    System.out.println("car1.company : " + car1.company);
    System.out.println();
    
    Car car2 = new Car();
    System.out.println("car2.company : " + car2.company);
    System.out.println("car2.model : " + car2.model);
    System.out.println();
    
    Car car3 = new Car();
    System.out.println("car3.company : " + car3.company);
    System.out.println("car3.model : " + car3.model);
    System.out.println("car3.color : " + car3.color);
    
    Car car4 = new Car();
    System.out.println("car4.company : " + car4.company);
    System.out.println("car4.model : " + car4.model);
    System.out.println("car4.color : " + car4.color);
    System.out.println("car4.maxSpeed : " + car4.maxSpeed);
  }
}
```

출력 결과
```java
car1.company : 현대자동차

car2.company : 현대자동차
car2.model : 자가용

car3.company : 현대자동차
car3.model : 자가용
car3.color : 빨강

car4.company : 현대자동차
car4.model : 자가용
car4.color : 빨강
car4.maxSpeed : 200
```

---

### 6.7.5 다른 생성자 호출(this())
- 생성자 오버로딩이 많아질 경우 생성자 간의 중복된 코드가 발생할 수 있다. 매개 변수의 수만 달리하고 필드 초기화 내용이 비슷한 생성자에서 이러한 현상을 많이 볼 수 있다.
- 이 경우에는 필드 초기화 내용은 한 생성자에만 집중적으로 작성하고 나머지 생성자는 초기화 내용을 가지고 있는 생성자를 호출하는 방법으로 개선할 수 있다.
- 생성자에서 다른 생성자를 호출할 때에는 this() 코드를 사용한다.

```java
클래스( [매개변수선언, ...] ) {
  this( 매개변수, ..., 값, ... );
  실행문;
}
```

this()는 자신의 다른 생성자를 호출하는 코드로 반드시 **생성자의 첫줄에서만 허용한다.** this()의 매개값은 호출되는 생성자의 매개 변수 타입에 맞게 제공해야 한다. this() 다음에는 추가적인 실행문들이 올 수 있다. 이 말은 호출되는 생성자의 실행이 끝나면 원래 생성자로 돌아와서 다음 실행문을 진행한다는 뜻이다. 

[ Car.java ] 다른 생성자를 호출해서 중복 코드 줄이기
```java
public class Car {
  // 필드
  String company = "현대자동차";
  String model;
  String color;
  int maxSpeed;
  
  // 생성자
  Car() {
  }
  
  Car(String model) {
    this(model, "은색", 250);
  }
  
  Car(String model, String color) {
    this(model, color, 250);
  }
  
  Car(String model, String color, int maxSpeed) {
    this.model = model;
    this.color = color;
    this.maxSpeed = maxSpeed;
  }
}
```

[ CarExample.java ] 객체 생성 시 생성자 선택
```java
public class CarExample {
  public static void main(Stirng[] args) {
    Car car1 = new Car();
    System.out.println("car1.company : " + car1.company);
    System.out.pritnln();
    
    Car car2 = new Car();
    System.out.println("car2.company : " + car2.company);
    System.out.println("car2.model : " + car2.model);
    System.out.println();
    
    Car car3 = new Car();
    System.out.println("car3.company : " + car3.company);
    System.out.println("car3.model : " + car3.model);
    System.out.println("car3.color : " + car3.color);
    System.out.println();
    
    Car car4 = new Car();
    System.out.println("car4.company : " + car4.company);
    System.out.println("car4.model : " + car4.model);
    System.out.println("car4.color : " + car4.color);
    System.out.println("car4.maxSpeed : " + car4.maxSpeed);
  }
}
```
</details>

<details markdown="1">
<summary>6.8 메서드</summary>

- 메서드는 객체의 동작에 해당하는 중괄호 {} 블록을 말한다. 증괄호 블록의 이름이 메서드의 이름이다. 메서들르 호출하게 되면 중괄호 블록에 있는 모든 코드들이 일괄적으로 실행된다. 메서드는 필드를 읽고 수정하는 역할도 하지만, 다른 객체를 생성해서 다양한 기능을 수행하기도 한다.
- 메서드는 객체 간의 데이터 전달의 수단으로 사용된다. 외부로부터 매개값을 받을 수도 있고, 실행 후 어떤 값을 리턴할 수도 있다.

### 6.8.1 메서드 선언

- 메서드 선언은 선언부(리턴타입, 메서드이름, 매개변수선언)와 실행 블록으로 구성된다. 메서드 선언부를 메서드 시그니처(signature)라고도 한다.

**리턴 타입**

- 리턴 타입은 메서드가 실행 후 리턴하는 값의 타입을 말한다.
- 메서드는 리턴값이 있을 수도 있고 없을 수도 있다.
- 메서드가 실행 후 결과를 호출할 곳에 넘겨줄 경우에는 리턴값이 있어야 한다.

예를 들어 전자계산기 객체에서 전원을 켜는 powerOn() 메서드와 두 수를 나누는 기능인 divide() 메서드가 있다고 가정해보자. divide() 메서드는 나눗셈의 결과를 리턴해야 하지만 powerOn() 메서드는 전원만 켜면 그만이다. 따라서 powerOn() 메서드는 리턴값이 없고, divide() 메서드는 리턴값이 있어야 한다고 봐야 한다. 리턴값이 없는 메서드는 리턴 타입에 void가 와야 하며 리턴값이 있는 메서드는 리턴값의 타입이 와야 한다. divide() 메서드의 결과가 double 값이라면 double을 리턴 타입으로 사용해야 한다.

```java
void powerOn() { ... }
double divide(int x, int y) { ... }
```

리턴값이 있느냐 없느냐에 따라 메서드를 호출하는 방법이 조금 다르다. 위의 두 메서드는 다음과 같이 호출할 수 있다.

```java
powerOn();
double result = divide(10, 20);
```

powerOn() 메서드는 리턴값이 없기 때문에 변수에 저장할 내용이 없다. 단순히 메서드만 호출하면 된다. 그러나 divide() 메서드는 10을 20으로 나눈 후 0.5를 리턴하므로 이것을 저장할 변수가 있어야 한다. 리턴값을 받기 위해 변수는 메서드의 리턴 타입인 double 타입으로 선언되어야 한다.

만약 result 변수를 int 타입으로 선언하게 되면 double 값을 저장할 수 없기 때문에 컴파일 에러가 발생한다.

```java
int result = divide(10, 20); // 컴파일 에러
```

리턴 타입이 있다고 해서 반드시 리턴값을 변수에 저장할 필요는 없다. 리턴값이 중요하지 않고, 메서드 실행이 중요한 경우에는 다음과 같이 변수 선언 없이 메서드를 호출할 수도 있다.

```java
divide(10, 20);
```

**메서드 이름**

메서드 이름은 자바 식별자 규칙에 맞게 작성하면 된다.

- 숫자로 시작하면 안되고, $와 _를 제외한 특수 문자를 사용하지 말아야 한다.
- 관례적으로 메서드명은 소문자로 작성한다.
- 서로 다른 단어가 혼합된 이름이라면 뒤이어 오는 단어의 첫머리 글자는 대문자로 작성한다.

다음은 잘 작성된 메서드 이름을 보여준다.

```java
void run() { ... }
void startEngine() { ... }
Stirng getName() { ... }
int[] getscores() { ... }
```

**매개 변수 선언**

매개 변수는 메서드가 실행할 때 필요한 데이터를 외부로부터 받기 위해 사용된다. 매개 변수도 필요한 경우가 있고 필요 없는 경우가 있다. 예를 들어 powerOn() 메서드는 그냥 전원만 켜면 그만이지만, divide() 메서드는 나눗셈을 할 두 수가 필요하다. 따라서 powerOn() 메서드는 매개 변수가 필요 없고, divde() 메서드는 매개 변수가 두 개 필요하다. 다음은 매개 변수가 있는 divide() 메서드 선언 예를 보여준다.

```java
double divide(int x, int y) { ... }
```

이렇게 선언된 divide() 메서드를 호출할 때에는 반드시 두 개의 int 값을 주어야 한다.

```java
double result = divide(10, 20);
```

호출 시 넘겨준 매개값인 10과 20은 해당 위치의 매개 변수인 x와 y에 각각 저장되고, 이 매개 변수들을 이용해서 메서드 블록을 실행하게 된다. 매개값은 반드시 매개 변수의 타입에 부합되는 값이어야 한다. divide() 메서드가 int 타입 매개 변수를 가지고 있다면 호출 시 매개값으로 int 값이나 int 타입으로 변환될 수 있는 값을 넘겨주어야 한다. 다음은 잘못된 매개값을 사용하여 컴파일 오류가 발생한다.

```java
double result = divide(10.5, 20.0);
```

10.5와 20.0은 double 값이므로 int 타입으로 변환될 수 없다. 하지만 다음 코드는 컴파일 오류가 발생하지 않고 정상적으로 실행된다. 매개값의 타입과 매개 변수의 타입이 달라도 자동 타입 변환이 되는 경우는 컴파일 오류가 생기지 않는다.

```java
byte b1 = 10;
byte b2 = 20;
double result = divide(b1, b2);
```

다음은 Calculator 클래스에서 powerOn(), plus(), divide(), powerOff() 메서드를 선언한 것이다.

[ Calculator.java ] 메서드 선언
```java
public class Calculator {
  
  // 메서드
  void powerOn() {
    System.out.println("전원을 켭니다.");
  }
  
  int plus(int x, int y) {
    int result = x + y;
    return result;
  }
  
  double divide(int x, int y) {
    double result = (double)x / (double)y;
    return result;
  }
  
  void powerOff() {
    System.out.println("전원을 끕니다.");
  }
}
```

---

### 6.8.2 리턴(return)문

- 메서드 실행을 중지하고 리턴값을 지정하는 역할을 한다.

**리턴값이 있는 메서드**

- 반드시 리턴문을 사용해 리턴값을 지정해야 한다.

```java
int plus(int x, int y) {
  int result = x + y;
  return result;
}
```

- return 문 뒤에 실행문은 올 수 없다.(조건식의 경우에는 조건에 따라 실행문을 작성할 수 있다.)

**리턴값이 없는 메서드**

- 메서드 실행을 강제 종료 시키는 역할을 한다.

---

### 6.8.3 메서드 호출

- 메서드는 클래스 내,외부의 호출에 의해 실행된다.
  - 클래스 내부 : 메서드 이름으로 호출
  - 클래스 외부 : 객체 생성 후, 참조 변수를 이용해 호출

**객체 내부에서 호출**

[ Calculator.java ] 클래스 내부에서 메서드 호출
```java
public class Calculator {
  int plus(int x, int y) {
    int result = x + y;
    return result;
  }
  
  double avg(int x, int y) {
    double sum = plus(x, y);  // 2. Calculator 클래스의 plus 메서드 호출
    double result = sum / 2;
    return result;
  }
  
  void execute() {
    doubel result = avg(7, 10);  // 1. double avg(int x, int y) 호출 
    println("실행결과 : " + result);  // 3. println(String message) 호출
  }
  
  void pritnln(String message) {
    System.out.println(message);
  }
}
```

**객체 외부에서 호출**

[ Car.java ] 클래스 외부에서 메서드 호출
```java
public class Car {
  
  // 필드
  int speed;
  
  // 생성자
  
  // 메서드
  int getSpeed() {
    return speed;
  }
  
  void keyTrunOn() {
    System.out.println("키를 돌립니다.");
  }
  
  void run() {
    for(int i=10; i<=50; i+=10) {
      speed = i;
      System.out.println("달립니다.(시속 : " + speed + "km/h)");
    }
  }
}
```

[ CarExample.java ] 클래스 외부에서 메서드 호출
```java
public class CarExample {
  public static void main(String[] args) {
    Car myCar = new Car();
    myCar.keyTrunOn();
    myCar.run();
    int speed = myCar.getSpeed();
    System.out.println("현재 속도 : " + speed + "km/h");
  }
}
```

출력 결과
```java
키를 돌립니다.
달립니다.(시속 : 10km/h)
달립니다.(시속 : 20km/h)
달립니다.(시속 : 30km/h)
달립니다.(시속 : 40km/h)
달립니다.(시속 : 50km/h)
현재 속도 : 50km/h
```

---

### 6.8.4 메서드 오버로딩

- 클래스 내에 같은 이름의 메서드를 여러 개 선언하는 것이다.
- 하나의 메서드 이름으로 다양한 매개값을 받기 위해 메서드 오버로딩을 한다.
- **오버로딩의 조건 : 매개변수의 타입, 개수, 순서가 달라야 한다.**

[ Calculator.java ] 메서드 오버로딩
```java
public class Calculator {
  // 정사각형의 넓이
  double areaRectangle(double width) {
    return width * width;
  }
  
  // 직사각형의 넓이
  doube areaRectangle(double width, double height) {
    return width * height;
  }
}
```

[ CalculatorExample.java ] 메서드 오버로딩
```java
public class CalculatorExample.java {
  public void main(String[] args) {
    Calculator myCalcu = new Calculator();
    
    // 정사각형의 넓이 구하기
    double result1 = myCalcu.arearectangle(10);
    
    // 직사각형의 넓이 구하기
    double result2 = myCalcu.areaRectangle(10, 20);
    
    // 결과 출력
    System.out.println("정사각형의 넓이 : " + result1);
    System.out.println("직사각형의 넓이 : " + result2);
  }
}
```

출력 결과
```java
정사각형의 넓이 : 100.0
직사각형의 넓이 : 200.0
```
</details>

<details markdown="1">
<summary>6.9 인스턴스 멤버와 this</summary>

- 인스턴스 멤버란?
  : 객체(인스턴스) 마다 가지고 있는 필드와 메서드
     > 이들을 각각 인스턴스 필드, 인스턴스 메서드라고 부름

- 인스턴스 멤버는 객체에 소속된 멤버이기 때문에 객체 없이는 사용할 수 없다.

[ Car.java ] 인스턴스 멤버와 this
```java
public class Car {
  // 필드
  Stirng model;
  int speed;
  
  // 생성자
  Car(String model) {
    this.model = model;
  }
  
  // 메서드
  void setSpeed(int speed) {
    this.speed = speed;
  }
  
  void run() { 
    for(int i=10; i<=50; i+=10) {
      this.setSpeed(i);
      System.out.println(this.model + "가 달립니다.(시속 : " + this.speed + "km/h)");
    }
  }
}
```

[ CarExample.java ] 인스턴스 멤버와 this
```java
public class CarExample {
  public static void main(String[] args) {
    Car myCar = new Car("포르쉐");
    Car youCar = new Car("벤츠");
    
    myCar.run();
    youCar.run();
  }
}
```

실행 결과

```java
포르쉐가 달립니다.(시속 : 10km/h)
포르쉐가 달립니다.(시속 : 20km/h)
포르쉐가 달립니다.(시속 : 30km/h)
포르쉐가 달립니다.(시속 : 40km/h)
포르쉐가 달립니다.(시속 : 50km/h)
벤츠가 달립니다.(시속 : 10km/h)
벤츠가 달립니다.(시속 : 20km/h)
벤츠가 달립니다.(시속 : 30km/h)
벤츠가 달립니다.(시속 : 40km/h)
벤츠가 달립니다.(시속 : 50km/h)
```
</details>

<details markdown="1">
<summary>6.10 정적 멤버와 static</summary>

- 정적(static) 멤버란?
  : 클래스에 고정된 필드와 메서드 - 정적 필드, 정적 메서드
  
- 정적 멤버는 클래스에 소속된 멤버이다.
  - 객체 내부에 존재하지 않고, 메서드 영역에 존재한다.
  - 정적 멤버는 객체를 생성하지 않고 클래스로 바로 접근해 사용한다.

### 6.10.1 정적 멤버 선언

다음은 정적 필드와 정적 메서드를 선언하는 방법을 보여준다.(필드 또는 메서드를 선언할 때 **static** 키워드를 붙인다.

```java
public class 클래스 {
  // 정적 필드
  static 타입 필드 [= 초기값];
  
  // 정적 메서드
  static 리턴 타입 메서드( 매개변수선언, ...) { ... }
}
```

필드를 선언할 때 인스턴스 필드로 선언할 것인가, 아니면 정적 필드로 선언할 것인가의 판단 기준은 객체마다 가지고 있어야 할 데이터라면 인스턴스 필드로 선언하고, 객체마다 가지고 있을 필요성이 없는 공용적인 데이터라면 정적 필드로 선언하는 것이 좋다.

```java
public class Calculator {
  String color;                 // 계산기별로 색깔이 다를 수 있다.(인스턴스 필드로 선언)
  static double pi = 3.141592;  // 계산기에서 사용하는 파이 값은 동일하다.(정적 필드로 선언)
```

메서드의 경우, 인스턴스 메서드로 선언할 것인가, 아니면 정적 메서드로 선언할 것인가의 판단 기준은 인스턴스 필드를 이용해서 실행해야 한다면 인스턴스 메서드로 선언하고, 인스턴스 필드를 이용하지 않는다면 정적 메서드로 선언한다.

```java
public class Calculator {
  Stirng color;                                         // 인스턴스 필드
  void setColor(String color) { this.color = color }    // 인스턴스 메서드
  static int plus(int x, int y) { return x + y; }       // 정적 메서드
  static int minus(int x, int y) { return x - y; }      // 정적 메서드
}
```

---

### 6.10.2 정적 멤버 사용

클래스 이름과 함께 도트(.) 연산자로 접근한다.

```java
public class Calculator {
  static double pi = 3.141592;
  static int plus(int x, int y) { ... }
  static int minus(int x, int y) { ... }
}
```

정적 필드 pi와 정적 메서드 plus(), minus()는 다음과 같이 사용할 수 있다.

```java
double result1 = 10 * 10 * Calculator.pi;
int result2 = Calculator.plus(10, 5);
int result3 = Calculator.minus(10, 5);
```

정적 필드와 정적 메서드는 원칙적으로는 클래스 이름으로 접근해야 하지만 다음과 같이 객체 참조 변수로도 접근이 가능하다.

```java
Calculator myCalcu = new Calculator();
double result1 = 10 * 10 * myCalcu.pi;
int result2 = myCalcu.plus(10, 5);
int result3 = myCalcu.minus(10, 5);
```

---

### 6.10.3 정적 초기화 블록
정적 필드는 다음과 같이 필드 선언과 동시에 초기값을 주는 것이 보통이다.

`static double pi = 3.14159;`

- **생성자에서 초기화 작업을 할 수 없다.** 생성자는 객체 생성 시에만 실행되기 때문이다.

- 자바는 정적 필드의 초기화 작업을 위해서 `정적 블록(static)`을 제공한다.

- **정적 블록은 클래스가 메모리로 로딩될 때 자동적으로 실행된다.(= 프로그램이 시작되자마자)** 정적 블록은 클래스 내부에 여러 개가 선언되어도 상관없다.
> 프로그램이 실행될 때 정적 블록은 자동적으로 실행된다.

- 클래스가 메모리로 로딩될 때 선언된 순서대로 실행된다.

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

---

### 6.10.4 정적 메서드와 블록 선언 시 주의할 점
- 정적 메서드와 정적 블록을 선언할 때 주의할 점은 객체가 없어도 실행된다는 특징 때문에, 이들 내부에 인스턴스 메서드를 사용할 수 없다.
- 객체 자신의 참조인 `this` 키워드도 사용이 불가능하다.
> static은 static 끼리 논다.

[ Car.java ] 정적 메서드와 블록 선언 시 주의할 점

```java
public class Car {
  int speed;
  
  void run() {
    System.out.println(speed + "으로 달립니다.");
  }
  
  public static void main(String[] args) {
    Car myCar = new Car();
    myCar.speed = 60;
    myCar.run();
  }
}
```

실행 결과
```java
60으로 달립니다.
```
---

### 6.10.5 싱글톤(Singleton)
- 하나의 어플리케이션 내에서 단 하나만 생성되는 객체(뒤로 미룸!)

</details>

<details markdown="1">
<summary>6.11 final 필드와 상수</summary>

### 6.11.1 final 필드
- 최종적인 값을 가지고 있는 필드 = 값을 변경할 수 없는 필드

<p align = "center"><img src = "https://user-images.githubusercontent.com/106001755/170189712-2f56e51c-f70c-4fac-82bd-8185d925aa5e.png"></p>

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

---

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

<details markdown="1">
<summary>6.12 패키지</summary>

디렉터리라고 이해

</details>

<details markdown="1">
<summary>6.13 접근 제한자</summary>

- public, protected, 생략("default"라고 부른다), private

접근 지정자의 목적
- 클래스나 일부 멤버를 **공개하지 않고** 다른 클래스에서 **접근하지 못하도록** 막음(**information hiding**)
- 최소한의 기능만 사용할 수 있도록 허용

```java
class A {      // 이렇게 감싸놓은 것이 캡슐화(관련된 정보를 하나로 묶어 놓는 것)


}
```

- 각 접근 제한자에 따른 클래스나 멤버의 공개 범위
  - private : 나 이외에는 허용 불가
  - 생략(default) : 같은 패키지의 클래스에만 허용
  - protected : 동일패키지와 자식클래스에만 허용
  - public : 다 허용

<p align="center"><img src="https://user-images.githubusercontent.com/106001755/173542304-0fe2636e-1b57-4280-9d0b-9dfb04cebd49.png"></p>

</details>

<details markdown="1">
<summary>6.14 Getter와 Setter 메서드</summary>

- 일반적으로 객체 지향 프로그래밍에서 객체의 데이터는 객체 외부에서 직접적으로 접근하는 것을 막는다.(**정보 은닉**)

- 객체 지향 프로그래밍에서는 **메서드를 통해서 데이터를 변경**하는 방법을 선호한다.

- 클래스를 선언할 때 필드(속성)는 반드시 private 접근 제한을 해야한다.

- Getter
  - 속성값을 읽기 위한 메서드
  - private 필드의 값을 리턴 하는 역할


- Setter
  - 속성값을 변경하기 위한 메서드
  - 외부에서 주어진 값을 필드 값으로 수정

> **정보 은닉**을 위해 꼭 필요하다.

</details>

<details markdown="1">
<summary>6.15 어노테이션</summary>

- 주석과 같은 의미

</details>

## Chapter 07 상속

<details markdown="1">
<summary>7.1 상속 개념</summary>

- 상속의 효과
  - 현실에서 상속은 부모가 자신에게 물려주는 행위를 말한다.
  - 객체 지향 프로그램에서도 부모 클래스의 **속성(필드)과 행위(메서드)** 를 자식 클래스에게 물려줄 수 있다.
  - 자식 클래스가 가지고 있는 속성과 행위가 더 많다.
  - 재사용과 같은 특징을 가지고 있다.
  - 객체 다형성 구현 가능

- 상속 대상 제한
  - 부모 클래스의 private 접근을 갖는 필드와 메서드
  - 부모 클래스가 다른 패키지에 있을 경우, default 접근을 갖는 필드와 메서드

```java
public class A {
  int field1;
  void method1() { ... }
}

public class B extends A {    // extends : 자식 클래스가 상속할 부모 클래스를 지정하는 키워드
  int field2;
  void method2() { ... }
}
```
상속을 해도 부모 클래스의 모든 필드와 메서드들을 물려받는 것은 아니다. 부모 클래스에서 private 접근 제한을 갖는 필드와 메서드는 상속 대상에서 제외된다.

- 자식 객체를 생성하면 부모 객체도 생성되는가?
  - 자식 객체를 생성(생성자를 호출)할 때는 부모 객체로부터 생성 후 자식 객체를 생성한다.
  
- 부모 클래스 = 슈퍼 클래스
- 자식 클래스 = 서브 클래스
</details>

<details markdown="1">
<summary>7.2 클래스 상속</summary>

</details>

<details markdown="1">
<summary>7.3 부모 생성자 호출</summary>

- 명시적인 부모 생성자 호출
  - 부모 객체를 생성할 때 부모 생성자를 선택해 호출

<p align="center"><img src="https://user-images.githubusercontent.com/106001755/172541577-55069f04-7144-4467-871e-6b36fe868e3e.png"></p>

  - **반드시 자식 생성자의 첫 줄에 위치**
  - 부모 클래스에 기본(매개변수가 없는) 생성자가 없다면 필수로 작성해야 한다.

</details>

<details markdown="1">
<summary>7.4 메서드 재정의(Override)</summary>

- 메서드 재정의(@Override)
  - 부모 클래스의 상속 메서드를 수정해 자식 클래스에서 재정의하는 것
  
  - 메서드 재정의 조건
    - 부모 클래스의 메서드와 동일한 시그니쳐를 가저야한다.

    - 접근 제한을 더 강하게 오버라이딩 불가
      - public을 default나 private로 수정 불가
      - 반대로 default는 public으로 수정 가능

```java
class B {
  public void M() {
    System.out.println("부모");
  }
}
class A extends B {

}
public class MainApp {
  public stataic void main(String[] args) {
    A objA = new A();
    objA.M();
  }  
} 
``` 
출력 결과 : 부모
 
```java
class B {
  public void M() {
    System.out.println("부모");
  }
}
class A extends B {
  public void M() {                 // 이때 M()은 부모에게 상속받은 것이다.
    System.out.println("자식");     // 자식 클래스에서 M()을 재정의 할 수 있다.(Override)
}
public class MainApp {
  public stataic void main(String[] args) {
    A objA = new A();
    objA.M();
  }
} 
``` 

출력 결과 : 자식

```java
class B {
  */public void M() {
    System.out.println("부모");
  }*/
}
class A extends B {
  public void M(String s) {
    System.out.println("자식");
}
public class MainApp {
  public stataic void main(String[] args) {
    A objA = new A();
    objA.M("나");
  }  
} 
```
출력 결과 : 자식(B에게서 상속받지 않았다.)

```java
class B {
  public void M() {
    System.out.println("부모");
  }
}
class A extends B {
  public void M(String s) {
    System.out.println("자식");
}
public class MainApp {
  public stataic void main(String[] args) {
    A objA = new A();
    objA.M("나");
  }  
} 
```

출력 결과 : 자식(이때, class A의 M()은 class B의 M(String s)와 전혀 다른 것이다. 따라서 둘은 상속 관계도 중복정의도 아니다(다른 클래스이기 때문)

- 중복정의(Overloading) -> **한 클래스 안에서** 메서드 이름 동일 + **매개변수의 순서, 개수, 타입이 달라야 한다.**
  >  프로토타입(public void M())는 동일, 시그니쳐(M()) 안은 달라야 한다.(책 보고 다시 작성)

- 재정의(Overriding) ->

- Override 어노테이션
  - 컴파일러에게 부모 클래스의 메서드 선언부와 동일한지 검사 지시

- 메서드 재정의 효과  
  : 부모 메서드는 숨겨지는 효과 발생
  : 재정의된 자식 메서드 실행
  
- 부모 메서드 사용(super)
  - 메서드 재정의는 부모 메서드를 숨기는 효과가 있다.
    - 자식 클래스에서는 재정의된 메서드만 호출한다.

  - 자식 클래스에서 수정되기 전 부모 메서드 호출 -> super 사용
    - super는 부모 객체 참조(this는 자신 객체 참조)

<p align="center"><img src="https://user-images.githubusercontent.com/106001755/172549270-4a27bb2b-8951-481c-82cc-5ab0e80429d7.png"></p>

</details>

<details markdown="1">
<summary>7.5 final 클래스와 final 메서드</summary>
 
- final 키워드는 클래스, 필드, 메서드 선언 시에 사용할 수 있다. final 키워드는 해당 선언이 최종 상태이고, 결코 수정될 수 없음을 뜻한다. 클래스와 메서드 선언 시에 final 키워드가 지정되면 상속과 관련이 있다.

### 7.5.1 상속할 수 없는 final 

- 클래스를 선언할 때 final 키워드를 class 앞에 붙이게 되면 이 클래스는 최종적인 클래스이므로 상속할 수 없는 클래스가 된다. 즉 final 클래스는 부모 클래스가 될 수 없어 자식 클래스를 만들 수 없다.

### 7.5.2 오버라이딩할 수 없는 final 메서드

- 메서드를 선언할 때 final 키워드를 붙이게 되면 이 메서드는 최종적인 메서드이므로 오버라이딩할 수 없는 메서드가 된다. 즉 부모 클래스를 상속해서 자식 클래스를 선언할 때 부모 클래스에 선언된 final 메서드는 자식 클래스에서 재정의할 수 없다는 것이다.

[ Car.java ] 재정의할 수 없는 final 메서드
```java
public class Car {
  // 필드
  public int speed;
  
  // 메서드
  public void speedUp() { speed = 1; }
  
  // final 메서드
  public final void stop() {
    System.out.println("차를 멈춤");
    speed = 0;
  }
}
```

[ SportsCar.java ] 재정의할 수 없는 final 메서드
```java
public class SportsCar extends Car {
  @Override
  public void speedUp() { speed += 10; }
  
  // 오버라이딩을 할 수 없음
  @Override
  pyublic void stop() {
    System.out.println("스포츠카를 멈춤");
    speed = 0;
  }
}
```
</details>

# 연습문제

<details markdown="1">
<summary>6장 연습문제</summary>

1. 객체와 클래스에 대한 설명으로 틀린 것은?

    (1) 클래스는 객체를 생성하기 위한 설계도(청사진)과 같은 것이다.
  
    (2) new 연산자로 클래스의 생성자를 호출하므로서 객체가 생성된다.
  
    (3) 하나의 클래스로 하나의 객체만 생성할 수 있다.
  
    (4) 객체는 클래스의 인스턴스이다.
    
<details markdown="1">
<summary>1번 정답</summary>
3. new 연산자를 호출하여 객체를 생성하는데, new 연산자를 여러 개 호출하면 여러 개의 객체를 생성할 수 있다.
</details>

2. 클래스의 구성 멤버가 아닌 것은?
    
    (1) 필드(field)
    
    (2) 생성자(constructor)
    
    (3) 메서드(method)
    
    (4) 로컬변수(local variable)

<details markdown="1">
<summary>2번 정답</summary>
4. 생성자와 메서드에서 사용된 변수이므로 아님
</details>

3. 필드, 생성자, 메서드에 대한 설명으로 틀린 것은?

    (1) 필드는 객체의 데이터를 저장한다.
    
    (2) 생성자는 객체의 초기화를 담당한다.
    
    (3) 메서드는 객체의 동작 부분으로, 실행 코드를 가지고 있는 블록이다.
    
    (4) 클래스는 반드시 필드와 메서드를 가져야 한다.

<details markdown="1">
<summary>3번 정답</summary>
4. 반드시 가질 필요는 없다.
</details>

4. 필드에 대한 설명으로 틀린 것은?

    (1) 필드는 메서드에서 사용할 수 있다.
    
    (2) 인스턴스 필드 초기화는 생성자에서 할 수 있다.
    
    (3) 필드는 반드시 생성자 선언 전에 선언되어야 한다.
    
    (4) 필드는 초기값을 주지 않더라고 기본값으로 자동 초기화된다.
    
<details markdown="1">
<summary>4번 정답</summary>
3. 블록 내에서 순서 상관 없이 선언할 수 있다.

```java
class 클래스 {
  int 필드1;
  
  생성자 { ... }
  
  int 필드2;
}
```
</details>

5. 생성자에 대한 설명으로 틀린 것은?

    (1) 객체를 생성하려면 생성자 호출이 반드시 필요한 것은 아니다.
    
    (2) 생성자는 다른 생성자를 호출하기 위해 this()를 사용할 수 있다.
    
    (3) 생성자가 선언되지 않으면 컴파일러가 기본 생성자를 추가한다.
    
    (4) 외부에서 객체를 생성할 수 없도록 생성자에 private 접근 제한자를 붙일 수 있다.

<details markdown="1">
<summary>5번 정답</summary>
1. 객체를 생성하려면 무조건 생성자 호출이 필요하다.
</details>

6. 메서드에 대한 설명으로 틀린 것은?

    (1) 리턴값이 있는 메서드는 리턴타입을 void로 해야 한다.
    
    (2) 리턴타입이 있는 메서드는 리턴값을 지정하기 위해 반드시 return 문이 있어야한다.
    
    (3) 매개값의 수를 모를 경우 "..."를 이용해서 매개변수를 선언할 수 있다.
    
    (4) 메서드의 이름은 중복해서 선언할 수 없다.
    
<details markdown="1">
<summary>6번 정답</summary>
4. 메서드의 이름은 중복해서 선언할 수 있다.(단 매개변수의 수, 타입, 순서를 다르게 해야 한다 = 메서드 오버로딩)
</details>

7. 메서드 오버로딩에 대한 설명으로 틀린 것은?

    (1) 동일한 이름의 메서드를 여러 개 선언하는 것을 말한다.
    
    (2) 반드시 리턴타입이 달라야 한다.
    
    (3) 매개변수의 타입, 수, 순서를 다르게 선언해야 한다.
    
    (4) 매개값의 타입 및 수에 따라 호출될 메서드가 선택된다.

<details markdown="1">
<summary>7번 정답</summary>
2. 반드시 리턴타입이 달라야 하는 것은 아니다.(리턴타입과 상관이 없다.)
</details>

8. 인스턴스 멤버와 정적 멤버에 대한 설명으로 틀린 것은?

    (1) 정적 멤버는 static으로 선언된 필드와 메서드를 말한다.
    
    (2) 인스턴스 필드는 생성자 및 정적 블록에서 초기화될 수 있다.
    
    (3) 정적 필드와 정적 메서드는 객체 생성없이 클래스를 통해 접근할 수 있다.
    
    (4) 인스턴스 필드와 메서드는 객체를 생성하고 사용해야 한다.
    
<details markdown="1">
<summary>8번 정답</summary>
2. 인스턴스 필드는 객체 안에 있는 필드이기 때문에, 객체 없이는 사용할 수 없다. 따라서 생성자(객체를 만듦) 안에서는 사용할 수 있지만, 정적 블록(클래스가 로딩될 때 자동으로 실행됨)에서는 사용할 수 없다.
</details>

9. final 필드와 상수(static final)에 대한 설명으로 틀린 것은?

    (1) final 필드와 상수는 초기값이 저장되면 값을 변경할 수 없다.
    
    (2) final 필드와 상수는 생성자에서 초기화 될 수 있다.
    
    (3) 상수의 이름은 대문자로 작성하는 것이 관례이다.
    
    (4) 상수는 객체 생성없이 클래스를 통해 사용할 수 있다.
    
<details markdown="1">
<summary>9번 정답</summary>
2. 상수는 생성자에서 초기화 될 수 없다. static final field이기 때문에 상수를 선언할 때 값을 주던지 정적 블록에서 초기화를 해야 한다. 객체를 만들 때 초기화를 한다는 의미이기 때문에 상수는 객체를 생성하기 전에 완성이 되어있어야 한다. 단순한 final 필드는 생성자로 초기화될 수 있다.
</details>

10. 접근 제한에 대한 설명으로 틀린 것은?

    (1) 접근 제한자는 클래스, 필드, 생성자, 메서드의 사용을 제한한다.
    
    (2) public 접근 제한은 아무런 제한 없이 해당 요소를 사용할 수 있게 한다.
    
    (3) default 접근 제한은 해당 클래스 내부에서만 사용을 허가한다.
    
    (4) 외부에서 접근을 하지 못하도록 하려면 private 접근 제한을 해야 한다.

<details markdown="1">
<summary>10번 정답</summary>
3. 해당 클래스 내부에서만 사용을 허가하는 접근 제한자는 private이다.
</details>

11. 다음 클래스에서 해당 멤버가 필드, 생성자, 메서드 중 어떤 것인지 괄호 안을 채우시오.

```java
public class Member {
  private String name;                                // 1.
  
  public Member(String name) { ... }                  // 2.
  
  public void setName(String name) { ... }            // 3.
}
```

<details markdown="1">
<summary>11번 정답</summary>

1. 필드

2. 생성자

3. 메서드
</details>

12. 현실 세계의 회원을 Member 클래스로 모델링하려고 한다. 회원의 데이터로는 이름, 아이디, 패스워드, 나이가 있다. 이 데이터들을 가지는 Member 클래스를 선언하라.
|데이터 이름|필드 이름|타입|
|:---:|:---:|:---:|
|이름|name|문자열|
|아이디|id|문자열|
|패스워드|password|문자열|
|나이|age|정수|

[ Member.java ]

```java
public class Member {
  // 작성 위치
}
```

<details markdown="1">
<summary>12번 정답</summary>

```java
public class Member {
  String name; 
  String id;
  String password;
  int age;
}
```
</details>

13. 위에서 작성한 Member 클래스에 생성자를 추가하려고 한다. 다음과 같이 Member 객체를 생성할 때 name 필드와 id 필드를 외부에서 받은 값으로 초기화하려면 생성자를 어떻게 선언해야 하는가?

```
Member user1 = new Member("홍길동", "hong");
Member user2 = new Member("강자바", "java");
```

[ Member.java ]

```java
public class Member {
  // 작성 위치
}
```

<details markdown="1">
<summary>13번 정답</summary>

```java
public class Member {
  String name; 
  String id;
  String password;
  int age;
  
  Member(String name, String id) {
    this.name = name;
    this.id = id;
  }
}
```
</details>

14. MemberService 클래스에 login() 메서드와 logout() 메서드를 선언하려고 한다. login() 메서드를 호출할 때에는 매개값으로 id와 password를 제공하고, logout() 메서드는 id만 매개값으로 제공한다. MemberService 클래스와 Login(), logout() 메서드를 선언해라.

(1) login() 메서드는 매개값 id가 "hong", 매개값 password가 "12345"일 경우에만 true로 리턴하고 그 이외의 값일 경우에는 false를 리턴하도록 해라.

(2) logout() 메서드의 내용은 "로그아웃 되었습니다."가 출력되도록 해라.

|리턴 타입|메서드 이름|매개 변수(타입)|
|:---:|:---:|:---:|
|boolean|login|id(String), password(String)|
|void|logout|id(String)|

[ MemberService.java ]

```java
public class MemberService {
  // 작성 위치
}
```

[ MemberServiceExample.java ]

```java
public class MemberServiceExample {
  public static void main(String[] args) {
    MemberService memberService = new Memberservice();
    boolean result = memberService.login("hong", "12345");
    if(result) {
      System.out.println("로그인 되었습니다.");
      memberService.logout("hong");
    } else {
      System.out.println("id 또는 password가 올바르지 않습니다.");
    }
  }
}
```

<details markdown="1">
<summary>14번 정답</summary>

[ MemberService.java ]
```java
public class MemberService {
  boolean login(String id, String password) {
    if(id.equals("hong") && password.equals("12345")) {
      return true
    } else {
        return false;
    }
  }
  void logout(String id) {
    System.out.println("로그아웃 되었습니다.");
  }
}
```

[ MemberServiceExample.java ]
```java
public class MeemberServiceExample {
  public static void main(String[] args) {
    MemberService memberService = new MemberService();
    
    boolean result = memberService.login("hong","12345");
    
    if(result) {
      System.out.println("로그인 되었습니다.");
      memberService.logout("hong");
    } else {
        System.out.println("id 또는 password가 올바르지 않습니다.");
    }
  }
}
```
</details>
