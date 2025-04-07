## 목차

## Spring

### Spring Framework의 특징

- POJO(Plain Old Java Object) 방식의 프레임워크
- 의존성 주입을 통한 객체관계 구성
- 관점지향 프로그래밍(AOP, Aspect Oriented Programming)
- 제어 역전(IoC, Inversion of Control)
- 높은 확장성과 다양한 라이브러리

## Spring Container Build

### Spring IoC Container

- 스프링에서 핵심적인 역할을 하는 객체를`Bean`이라고 한다.
- Continer는 Bean의 인스턴스화 조립, 관리의 역할, 사용 소멸에 대한 처리를 담당한다.
    - BeanFactory:
        - 프레임워크 설정과 기본기능을 제공하는 컨테이너
        - 모든 유형의 객체를 관리할 수 있는 메커니즘 제공
    - ApplicationContext
        - BeanFactory 하위 인터페이스
        - 이벤트 처리, 국제화용 메세지 처리 등 다양한 기능 제공
    - WebApplicationContext
        - 웹 환경에서 Spring을 이용하기 위한 기능이 추가됨
        - 대표적인 구현 클래스로 XmlWebApplicationContext가 있음

### Spring configuration metadata

- 애플리케이션 작성을 위해 생성할 Bean과 설정 정보, 의존성 등의 방법을 나타내는 정보
- 설정정보를 작성하는 방법은 XML 방식, Annotation 방식, Java Config 방식이 있다.

### Bean Scope

- Bean 정의를 작성하는 것은 Bean 객체를 생성하는 것과 다르다
- Bean 범위를 정의해서 객체의 범위를 제어할 수 있다.
- Scopes  
    |Scope|설명|
    |---|---|
    |singleton|기본값, Spring IoC컨테이너에 대한 단일 객체 인스턴스|
    |prototype|빈을 요청할 때마다 새로운 인스턴스 생성|
    |request|HTTP Request 주기로 bean 인스턴스 생성|
    |session|HTTP Session 주기로 bean 인스턴스 생성|

## Spring DI

### Spring DI - XML

- 의존성 주입(생성자)
    - constructor-arg를 이용하여 의존성 주입
        ```xml
        <bean class="" id="">
            <constructor-arg ref=""></constructor-arg>
        </bean>
        ```
    - `<ref>`,`<value>`와 같이 하위 태그를 이용하여 설정/속성을 이용하여 설정

- 의존성 주입(생성자)
    - setter를 이용하여 의존성 주입
        ```xml
        <bean class="" id="">
            <property name="" ref=""></property>
        </bean>
        ```
    - `<ref>`,`<value>`와 같이 하위 태그를 이용하여 설정/속성을 이용하여 설정

### Spring DI - Annotation

- Bean 생성: `@Component`
    - 외에도 `@Service`, `@Controller`, `@Repository`의 Stereotype Annotaion 제공
    - `@Repository`, `@Service`, `@Controller`는 목적에 맞는 구체적인 사용을 위한 `@Component`의 확장
    - 생성 및 설정
        ```xml
        <context:component-scan base-package=""></context:component-scan>
        ```
- 의존성 주입: `@Autowired`
    - 생성자
    ```java
    @Autowired
    public Constructor(Class value){
        this.value = value;
    }
    ```
    - Setter
    ```java
    @Autowired
    public setSetter(@Qualifier("identifier")Class value){
        this.value = value;
    }
    ```
    - filed
    ```java
    @Autowired
    @Qualifier("identifier")
    private Class value;
    ```

### Spring DI - Java Config

- `@Configuration`
- `@ComponentScan(basePackages = {""})`