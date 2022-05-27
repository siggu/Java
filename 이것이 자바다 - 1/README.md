# 이것이 자바다 -1 개념정리
 - [Chapter 01 자바 시작하기](#Chapter-01-자바-시작하기)
 - [Chapter 05 참조 타입](#Chapter-05-참조-타입)
 - [Chapter 06 클래스](#Chapter-06-클래스)

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

<p align = "center"><img src = "https://user-images.githubusercontent.com/106001755/170723189-7fc96789-5fa5-4554-8043-ad8561f26b6e.png" width="400" height="300"></p>

### 6.1.2 객체의 상호작용












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


### 6.12 패키지
넘어감!(자연스럽게 배우는 내용이라서...)

### 6.13 접근 제한자
public, protected, 생략("default"라고 부른다), private

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
 - protected : 동일패키지의? 와? 자식클래스에만 허용
 - public : 다 허용
















</details>
