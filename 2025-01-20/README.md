## 목차
### [Java](#java)
### [통합 개발 환경 (Integrated Development Environment)](#통합-개발-환경-integrated-development-environment)
## [문법](#문법)
1. [주석](#주석)
2. [이론](#이론)
    - [변수(Variable)](#변수variable)
    - [자료형(Data Type)](#자료형data-type)
    - [연산자(Operator)](#연산자operator)
        1. [산술 연산자](#1-산술-연산자)
        2. [비교 연산자](#2-비교-연산자)
        3. [논리 연산자](#3-논리-연산자)
        4. [대입(복합) 연산자](#4-대입복합-연산자)
        5. [단항 연산자](#5-단항-연산자)
        6. [기타 연산자](#6-기타-연산자)
3. [제어문](#제어문)
    - [조건문(Conditional Statements)](#조건문conditional-statements)
    - [반복문(Loops)](#반복문loops)
    - [분기문(Branching Statements)](#분기문branching-statements)

## Java

- JVM (Java Virtual Machine)
- JRE (Java Runtime Environment)
- JDK (Java Development Kit)

## 통합 개발 환경 (Integrated Development Environment)

- Eclipse
- Spring Tools 4
- vscode
- etc..

## 문법

### 주석

- 한 줄 주석
    ```java
    // 주석 주석
    ```
- 여러 줄 주석
    ```java
    /*
        주석 주석
    */

- 문서 주석
    ```java
    /**
     * 주석 주석
    **/
    ```
    <i>메서드 사용 시 hint 표시 됨</i>

## 이론

### 변수(Variable)

- 정의
    - 컴퓨터 메모리의 데이터 저장소
    - 데이터에 이름을 부여하여 해당 데이터를 관리
    - 자료형에 따라 값 또는 참조 값을 저장
    - `=`를 통해서 CPU에게 연산 작업을 의뢰

- 규칙
    - 변수명은 대/소문자를 구분 (공백X)
    - 숫자로 시작할 수 없음
    - 특수문자 중 `$`,`_`만 사용가능
    - 자바 예약어를 사용할 수 없음
        - `public`,`private`,`import`,`for`,`if`,`etc...`
    - 의미를 담아서 지을 것 <i>readability</i>
    - 합성어의 경우 주로 `camelCase`표기법 사용

### 자료형(Data Type)

- Primitive Type
    - 변수 자체에 값(literal)이 저장됨
- Reference Type
    - 변수에 참조(reference, address)를 저장, 기본 값은 **null**

### 연산자(Operator)

- 연산자(operator): 계산이나 처리를 수행하는 기호
- 피연산자(operand): 해당 연산의 대상이 되는 값(또는 변수)
- 연산자가 여러 개 있을 때, 우선순위에 따라 계산 -> 모르면 소괄호() 쓰기

#### 종류
##### 1. 산술 연산자
- `+`
- `-`
- `*`
- `/`
- `%`

##### 2. 비교 연산자
- `==`
- `!=`
- `>`
- `<`
- `>=`
- `<=`
- `instanceof`

##### 3. 논리 연산자
- `&&`
- `||`
- `!`

##### 4. 대입(복합) 연산자
- `=`
- `+=`
- `-=`
- `*=`
- `/=`
- `%=`

##### 5. 단항 연산자
- `+`, `-`
- `++a`, `--a`
- `a++`, `a--`
- `!`
- `~`
- `(type)a`

##### 6. 기타 연산자
- `(조건) ? (참) : (거짓)`
- `new`
- `[인덱스]` - 배열 접근 연산자
- `.` - 객체 맴버 접근 연산자
- 비트연산자


## 제어문

### 조건문(Conditional Statements)

- if문
    ```java
    if (조건식) {
        // 조건식이 참(true)일 때 실행될 코드 블록
    }
    ```

- if-else문
    ```java
    if (조건식) {
        // 조건식이 참(true)일 때 실행될 코드 블록
    } else {
        // 조건식이 거짓(false)일 때 실행될 코드 블록
    }
    ```

- if - else if - else문
    ```java
    if (조건식1) {
        // 조건식1이 참(true)일 때 실행될 코드 블록
    } else if (조건식2) {
        // 조건식2가 참(true)일 때 실행될 코드 블록
    } else {
        // 모든 조건식이 거짓(false)일 때 실행될 코드 블록
    }
    ```

- switch 문
    ```java
    switch (변수) {
        case 값1:
            // 변수의 값이 값1과 일치할 때 실행될 코드 블록
            break;
        case 값2:
            // 변수의 값이 값2와 일치할 때 실행될 코드
            break;
        default:
            // 변수의 값이 모든 case와 일치하지 않을 때 실행될 코드
    }
    ```

### 반복문(Loops)

- for 문
    ```java
    for (초기화; 조건식; 증감식){
        // 코드
    }
    ```

- while 문
    ```java
    while (조건식) {
        // 코드
    }
    ```

- do-while 문
    ```java
    do {
        // 코드
    } while (조건식);
    ```
### 분기문(Branching Statements)

- `break`
- `continue`