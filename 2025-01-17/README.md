## 목차
### [Java](#java)
1. [Data Type](#data-type)
    - [Primitive Data Type](#primitive-data-type-기초-자료형)
    - [Type Casting](#type-casting-형변환)
2. [Operators](#operators)
3. [Conditional](#conditional)
    - [if](#conditional---if)
    - [Switch](#conditional---switch)
4. [Loop](#loop)
    - [for](#loop---for)
    - [while](#loop---while)

# Java 

## Data Type

### Primitive Data Type (기초 자료형)

|Type|keyword|Range|
|---|---|---|
|논리형|boolean|true, false|
|문자형|char|16비트 유니코드, 0 ~ 65536|
|정수형|byte<br>short<br>int<br>long|8비트, -128 ~ 127<br>16비트, -32,768 ~ 32,767<br>32비트, -2,147,483,648 ~ 2,147,483,647<br>64비트, -9223372036854775808 ~ 9223372036854775807|
|실수형|float<br>double|32비트, IEEE 754-1985표준<br>64비트, IEEE 754-1985표준|

### Type Casting (형변환)

- Automatic promotions (implicit Type Casting)
    - 작은 크기의 타입은 큰 크기의 타입으로 자동으로 형변환 된다.
    - 정수형은 실수형으로 자동형변환 된다.
        - long var = 100;
        - float fvar = var;
        - int kvar = 'A';

- Explicit Type Casting
    - 큰 크기의 타입을 작은 크기의 타입으로 변경할 경우
    - 실수형을 정수형의 타입으로 변경할 경우
    - identifier = (target_type) value;
        - float fvar = 100;
        - long var = (long)fvar;

## Operators

|우선순위|연산자|연산대상|연산내용|
|---|---|---|---|
|1|[ ]<br>.<BR>++, --<br>+, -<br>~<br>!<br>new<br>(type)|모든 데이터형<br>레퍼런스<br>정수형<br>정수형, 실수형<br>정수형<br>논리형<br>레퍼런스형<br>모든데이터형|배열요소 지정<br>객체 멤버 지정<br>값 증가, 값 감소<br>부호에 사용<br>비트 반전<br>논리 반전<br>객체 생성<br>캐스팅 연상자|
|2|*, /, %|정수형, 실수형|곱셈, 나눗셈, 나머지|
|3|+, -|정수형, 실수형|덧셈, 뺄셈|
|4|<<, >>, >>>|정수형|비트단위 좌우 이동, 비트 비부호화 우이동|
|5|<, <=, >, >=|정수형, 실수형|값 대소 비교|
|6|==, !=|기본 데이이터형|값 비교|
|7|&|정수형, 논리형|비트 AND, 논리 AND|
|8|^|정수형, 논리형|비트 XOR, 논리 XOR|
|9|\||정수형, 논리형|비트 OR, 논리 OR|
|10|&&|논리형|조건 AND|
|11|\|\||논리형|조건 OR|
|12|? :|논리형, 모든 데이터형|조건 삼항|
|13|=<br>*=, %=, +=, -=, <<=, >>=, >>>=, &=, ^=, \|=|변수, 모든 데이터형|대입/할당 연산|


## Conditional
### Conditional - if

``` java
if ( boolean_expression ) {
    Statements
    ..
}
```

``` java
if ( boolean_expression ) {
    Statments
    ..
} else {
    Statements
    ..
}
```

``` java
if ( boolean_expression ) {
    Statments
    ..
} else if ( boolean_expression ) {
    Statements
    ..
} else {
    Statements
    ..
}
```
### Conditional - switch

``` java
switch ( expr ) {
    case 값1:
        statements;
        break;

    case 값2:
        statements;
        break;

    case 값3:
        statements;
        break;

    default:
        statements;
}
```

## Loop

### Loop - for
``` java
for ( init_expr; boolean_testexpr; alter_expr ) {
    Statments or block;
    ..
}
```

``` java
for ( type item : items ) {
    Statments or block;
    ..
}
```

### Loop - while
``` java
while ( boolean ) {
    Statement or block;
    ...
}
```
``` java
do {
    Statement or block;
    ...
} while ( boolean );
```

- `continue`   
- `break`   
- `label:`
    - `break label;`
    - `Continue label;`

