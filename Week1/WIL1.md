## 자바란?
객체 지향 언어로, 객체 지향 프로그래밍은 객체를 중심으로 프로그램을 작성하는 방법을 말한다.
## 자바의 특징
### 1. 간단하다

### 2. 객체 지향적이다.
숫자(int, float, long 등)나 논릿값(true, false)을 제외하면 거의 모두 객체로 구성된다.
실제로 자바는 Object 클래스에서 모든 클래스를 파생한다.

### 3. 인터프리터 언어이다.
자바는 컴파일 언어인 동시에 인터프리터 언어이다.
인터프리터 언어는 코드를 한 줄씩 작성하고 실행하여 결과를 바로 확인할 수 있다.

### 4. 강력하다.
포인터 연산을 지원하지 않는다. 즉, 잘못된 주소를 가리킬 가능성을 사전에 없앤 것이다.

### 5. 안전하다.
자바는 자료형 타입에 매우 민감하다. 따라서 일단 컴파일만 되면 실행할 때 오류 발생률이 다른 언어에 비해 현저히 낮다.

### 6. 플랫폼이 독립적이다.
자바의 실행 파일은 이진 코드(클래스)이므로 자바 런타임을 설치한 시스템에서는 어디서나 실행할 수 있다. 즉, 자바로 작성한 프로그램이라면 운영체제와 상관없이 어디서든 실행할 수 있다는 뜻이다. 왜냐하면 자바 프로그램은 가상 머신으로 실행되기 때문이다. 

### 7. 멀티 스레드를 지원한다.
멀티 스레드를 지원해서 프로그램 단위가 같은 스레드를 동시에 수행할 수 있다. 자바는 멀티 프로세서 하드웨어를 지원하도록 설계되었으므로 멀티 CPU 시스템에서 효율이 높다.

### 8. 동적이다.
자바 인터페이스를 이용하면 모듈을 갱신할 때 다른 모듈까지 모두 갱신할 필요가 없다. 인터페이스가 인스턴스 변수와 도구의 실행문을 모두 배제한 채 객체 간의 상호 작용을 정의하기 때문이다.

> [출처](https://wikidocs.net/199)


## 자바의 구조
```java
public class 클래스명 {

    /* 메서드 블록 */
    [public|private|protected] [static] (리턴자료형|void) 메서드명1(입력자료형 매개변수, ...) {
        명령문(statement);
        ...
    }

    /* 메서드 블록 */
    [public|private|protected] [static] (리턴자료형|void) 메서드명2(입력자료형 매개변수, ...) {
        명령문(statement);
        ...
    }

    ...
}
```
### 클래스 블록
클래스명은 소스 파일의 이름(예: 클래스명.java)과 똑같이 사용해야 한다. 그리고 클래스 블록은 여러 메서드 블록을 포함한다.

### 메서드 블록
```java
public class Sample {
    public static void main(String[] args) {
        (... 생략 ...)
    }
}
```
- public, private, protected가 오거나 아무것도 오지 않을 수 있다. public, private, protected는 메서드의 접근 제어자이다.   
- 또한 static 키워드가 올 수도 있고 오지 않을 수도 있다. static이라는 키워드가 붙으면 static 메서드가 된다. 메서드에 static 키워드가 붙으면 클래스 메서드가 되어 객체를 만들지 않아도 ‘클래스명.메서드명’ 형태로 호출할 수 있다.
- String[] args: 메서드의 매개 변수로, args 변수는 String[] 배열 자료형임을 의미한다. args는 argument의 줄임말로, 인수를 의미한다. args 대신 다른 이름을 사용해도 상관없다.

### 명령문
명령문은 메서드 블록 안에 있다.

* * *

## 객체 지향 프로그래밍
객체 지향에는 클래스, 객체, 인스턴스, 상속, 인터페이스, 다형성, 추상화 등의 많은 개념들이 존재한다.

### 클래스
- _보통 클래스는 특별한 경우가 아니라면 파일 단위로 하나씩 작성한다._   
- 클래스를 통해 객체를 만들 수 있다. 객체를 생성할 때 new 키워드를 사용한다.   
이렇게 클래스에 의해서 만들어진 객체를 인스턴스라고도 한다.
#### 객체와 인스턴스의 차이는?
Animal cat = new Animal() 이렇게 만들어진 cat은 객체이다. 그리고 cat이라는 객체는 Animal의 인스턴스이다. 인스턴스라는 말은 특정 객체(여기서는 cat)가 어떤 클래스(여기서는 Animal)의 객체인지를 관계 위주로 설명할 때 사용된다. 즉, ‘cat은 인스턴스’보다는 ‘cat은 객체’라는 표현이, ‘cat은 Animal의 객체’보다는 ‘cat은 Animal의 인스턴스’라는 표현이 훨씬 잘 어울린다.     

- 과자 모양을 찍어 내는 과자 틀을 클래스라고 한다면, 과자 틀에 의해 만들어진 과자들은 객체라고 할 수 있다.
- 클래스에서 선언된 변수를 *객체 변수*라고 한다.
- 객체끼리는 객체 변수의 값이 *독립적*으로 유지된다.

### 메서드
- 자바는 클래스를 떠나 존재하는 것은 있을 수 없기 때문에 자바의 함수는 따로 존재하지 않고 클래스 내에 존재한다. 즉, 클래스 내에서 사용되는 함수를 메서드라고 한다.
- 객체 변수에 값을 대입하는 방법에 사용된다.   
#### 매개변수와 인수
매개 변수는 메서드에 전달된 입력값을 저장하는 변수를 의미하고   
인수는 메서드를 호출할 때 전달하는 입력값을 의미한다.
- 메서드의 구조
```java
리턴자료형 메서드명(입력자료형1 매개변수1, 입력자료형2 매개변수2, ...) {
    ...    
    return 리턴값;  // 리턴자료형이 void 인 경우에는 return 문이 필요없다.
}
```
- 특별한 경우 메서드를 빠져나가고 싶다면 return을 단독으로 사용하여 메서드를 즉시 빠져나갈 수 있다. 이때, return 자료형은 void여야 한다.

###  값에 의한 호출과 객체에 의한 호출
- _메서드에 값(원시 자료형)을 전달하는 것과 객체를 전달하는 것에는 큰 차이가 있다._
- 메서드에 객체를 전달해야 메서드에서 객체 변수의 값을 변경할 수 있다.
#### 값에 의한 호출
```java
class Updater {
    void update(int count) {
    count++;
    }
}

class Counter {
    int count = 0;  // 객체변수
}

public class Sample {
    public static void main(String[] args) {
        Counter myCounter = new Counter();
        System.out.println("before update:"+myCounter.count);
        Updater myUpdater = new Updater();
        myUpdater.update(myCounter.count);
        System.out.println("after update:"+myCounter.count);
    }
}
```
출력값
```
before update:0
after update:0
```
#### 객체에 의한 호출
```java
class Updater {
    void update(Counter counter) {
        counter.count++;
    }
}

class Counter {
    int count = 0;  // 객체변수
}

public class Sample {
    public static void main(String[] args) {
        Counter myCounter = new Counter();
        System.out.println("before update:"+myCounter.count);
        Updater myUpdater = new Updater();
        myUpdater.update(myCounter);
        System.out.println("after update:"+myCounter.count);
    }
}
```
```
before update:0
after update:1
```
-> Sample.java 파일 내에 Sample, Updater, Counter라는 클래스 3개가 등장했다. 이와 같이 하나의 java 파일 내에는 여러 개의 클래스를 선언할 수 있다. 단, 파일명이 Sample.java라면 Sample.java 내의 Sample 클래스는 public으로 선언하라는 관례(규칙)가 있다.

### 상속
- 클래스 상속을 위해서는 *extends*라는 키워드를 사용한다.
- 부모 클래스로 만들어진 객체를 자식 클래스의 자료형으로는 사용할 수 없다.
- __오버라이딩__ : 부모 클래스의 메서드를 자식 클래스가 동일한 형태로 또다시 구현하는 행위, 즉 메서드 덮어쓰기이다.
- __오버로딩__ : 변경이 아닌 *추가*이다. 메서드의 입력 항목이 다른 동일한 이름의 메서드를 추가하는 행위이다.
- 자바는 다중상속을 지원하지 않는다.

### 생성자
- 생성자는 객체 변수에 값을 무조건 설정해야만 객체가 생성될 수 있도록 강제할수 있는 방법으로 사용된다.
#### 생성자의 규칙
```
1. 클래스명과 메서드명이 같다.
2. 리턴 타입을 정의하지 않는다(void도 사용하지 않는다.).
```
- 생성자는 객체가 생성될 때 호출된다. 즉, 생성자는 다음과 같이 new 키워드가 사용될 때 호출된다.
- 생성자가 다음과 같다면
```java
HouseDog(String name) {
    this.setName(name);
} 
```
다음과 같이 new 키워드로 객체를 만들 때 문자열을 전달해야만 한다.
```
HouseDog dog = new HouseDog("happy");   // 생성자 호출 시 문자열을 전달해야 한다.
```
#### 디폴트 생성자
- 생성자의 입력 항목이 없고 생성자 내부에 아무 내용이 없는 생성자이다.
- 만약 클래스에 생성자가 하나도 없다면 컴파일러는 자동으로 디폴트 생성자를 추가한다. 하지만 사용자가 작성한 생성자가 하나라도 구현되어 있다면 컴파일러는 디폴트 생성자를 추가하지 않는다.
- 예를 들어, new Dog()로 Dog 클래스의 객체가 만들어질 때의 디폴트 생성자는 Dog()이다.
#### 생성자 오버로딩
- 생성자 오버로딩을 통해 입력 항목이 다른 생성자를 여러 개 만들 수 있다.
```java
class HouseDog extends Dog {
    HouseDog(String name) {
        this.setName(name);
    }

    HouseDog(int type) {
        if (type == 1) {
            this.setName("yorkshire");
        } else if (type == 2) {
            this.setName("bulldog");
        }
    }
}

public class Sample {
    public static void main(String[] args) {
        HouseDog happy = new HouseDog("happy");
        HouseDog yorkshire = new HouseDog(1);
        System.out.println(happy.name);  // happy 출력
        System.out.println(yorkshire.name);  // yorkshire 출력
    }
}
```

### 인터페이스


### 다형성


### 추상 클래스


> [출처](https://wikidocs.net/156068)