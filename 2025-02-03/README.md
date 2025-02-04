## 목차

### [자료 구조](#자료-구조)
- [자료 구조의 분류](#자료-구조의-분류)
- [자료 구조의 선택 기준](#자료-구조의-선택-기준)

### [컬렉션](#컬렉션)
- [컬렉션 프레임워크](#컬렉션-프레임워크)
- [List 계열 컬렉션](#list-계열-컬렉션)
    - [ArrayList](#arraylist)
    - [LinkedList](#linkedlist)
    - [List 주요 메서드](#list-주요-메서드)
- [Set 계열 컬렉션](#set-계열-컬렉션)
    - [HashSet](#hashset)
    - [LinkedHashSet](#linkedhashset)
    - [TreeSet](#treeset)
    - [Set 주요 메서드](#set-주요-메서드)
- [Map 계열 컬렉션](#map-계열-컬렉션)
    - [HashMap](#hashmap)
    - [LinkedHashMap](#linkedhashmap)
    - [TreeMap](#treemap)
    - [Map 주요 메서드](#map-주요-메서드)
- [Stack](#stack)
    - [Stack 메서드](#stack-메서드)
- [Queue](#queue)
    - [Queue 메서드](#queue-메서드)
- [Deque](#deque)
    - [Deque 메서드](#deque-메서드)
- [정렬](#정렬)
    - [Comparatable 인터페이스](#comparable-인터페이스)
    - [Comparator 인터페이스](#comparator-인터페이스)
    


### 자료 구조

- 데이터에 효율적으로 접근하기 위해 선택되는 데이터의 조직 및 저장 형식
- 데이터 값들의 모음, 이들 간의 관계, 데이터에 적용될 수 있는 연산의 모음

#### 자료 구조의 분류
- 정적 자료 구조: 크기가 고정된 자료 구조
- 동적 자료 구조: 크기가 변할 수 있는 자료 구조

####  자료 구조의 선택 기준

- 데이터 접근 속도
- 메모리 사용 효율성
- 삽입 및 삭제의 효율성
- 순서 유지 여부
- 중복 데이터 허용 여부

### 컬렉션

- 컬렉션 프레임워크
- 정렬

#### 컬렉션 프레임워크

- 표준화된 데이터 구조와 이를 처리하기 위한 클래스 및 인터페이스의 집합
- 데이터를 동적 크기로 관리하고, 삽입, 삭제, 검색, 정렬 등을 효율적으로 처리할 수 있음
- 제네릭을 지원하여 타입 안전성 보장
- 표준화된 메서드 제공

#### List 계열 컬렉션

- 순서가 있는 데이터 집합
- 중복 데이터 허용
- 크기가 고정된 배열과 달리 크기가 동적으로 변함
- 구현 클래스
    - ArrayList
    - LinkedList
    - Vector

##### ArrayList

- 배열 기반의 구현
- 인덱스를 통한 접근이 빠름
- 데이터 삽입, 삭제가 빈번한 경우 성능 저하
- 데이터의 조회가 많고,  삽입/삭제가 적은 경우 유용

##### LinkedList

- 노드 기반의 구현
- 각 노드가 이전 노드와 다음 노드의 참조를 포함
- 데이터 삽입, 삭제가 빠름
- 데이터의 삽입/삭제가 많고 조회가 많이 없는 경우 유용

###### List 주요 메서드

- add(E e)
- add(Int index, E e)
- get(int index)
- set(int idex, E e)
- remove(int index)
- remove(Object o)
- size()
- isEmpty()
- contains(Object o)
- indexOf(Object o)
- clear()

#### Set 계열 컬렉션

- 중복 데이터 허용하지 않음
- 순서 보장하지 않음
- null 값 허용
- 데이터의 고유성을 보장하기 위해 사용
- 구현 클래스
    - HashSet
    - LinkedHashSet
    - TreeSet

##### HashSet

- 데이터의 저장 순서를 유지하지 않음
- HashMap 기반으로 동작 -> 빠른 추가, 삭제, 검색 가능
- null 값 하나 저장할 수 있음


##### LinkedHashSet

- 데이터의 저장 순서를 유지함
- LinkedHashMap 기반으로 동장 -> 빠른 추가, 삭제, 검색 가능
- 이중 연결 리스트를 이용하여 관리
- null 값 하나 저장할 수있음

##### TreeSet

- 데이터가 정렬된 상태로 유지
- 사용자의 정의 정렬이 필요한 경우 Comparator를 사용할 수 있음
- 내부적으로 이진 탐색 트리(R-B 트리)구조를 사용
- null 값 저장 불가

##### Set 주요 메서드

- add(E e)
- remove(Object o)
- size()
- isEmpty()
- contains(Object o)

#### Map 계열 컬렉션

- Key와 Value의 쌍으로 데이터를 저장하는 구조
- 키를 기준으로 값에 접근하여 키는 중복을 허용하지 않음
- 키를 활용하여 빠를 검색 가능
- 키 또는 값에 null 허용
- 구현 클래스
    - HashMap
    - LinkedHashMap
    - TreeMap

##### HashMap

- 데이터의 저장 순서를 유지하지 않음
- 내부적으로 Hash Table을 사용하여 데이터 저장 및 검색
- null 키를 하나 허용하며,  여러 개의 null 값을 허용
- 빠른 검색, 삽입, 삭제

##### LinkedHashMap

- 데이터의 저장 순서를 유지
- 내부적으로 Hash Table + 이중 연결 리스트를 사용하여 데이터 저장 및 검색
- null 키를 하나 허용하며, 여러 개의 null 값을 허용

##### TreeMap

- 키를 기준으로 정렬된 상태로 데이터를 유지
- 사용자 정의 정렬이 필요한 경우 Comparator를 사용
- 내부적으로 R-B 트리 기반으로 구현
- null 키는 허용하지 않음

##### Map 주요 메서드

- put(K key, V value)
- get(Object key)
- remove(Object key)
- containsKey(Object key)
- containsValue(Object value)
- keySet()
- values()
- isEmpty()
- size()

#### Stack

- 후입선출(LIFO) 구조
- Vector 기반으로 동작

##### Stack 메서드

- push(E item)
- pop()
- peek()
- isEmpty()
- size()

#### Queue

- 선입선출(FIFO) 구조
- 다양한 구현체 (LinkedList,  ArrayDeque)

##### Queue 메서드

- offer(E e)
- add(E e)
- poll()
- remove()
- peek()
- element()
- isEmpty()
- size()

#### Deque

- 양방향 큐
- ArrayDeque (배열 기반), LinkedList (연결리스트 기반)

##### Deque 메서드

- addFirst(E e)
- addLast(E e)
- removeFirst()
- removeLast()
- getFirst()
- getLast()
- isEmpty()
- size()

#### 정렬

- 요소들을 특정 기준에 맞추어 오름차순 또운 내림차순으로 배치 하는 것
- 순서를 가지는 Collection들만 정렬 가능
- 자바 제공 클래스
    - Collections의 sort()
    - 배열은 Arrays의 sort()

##### Comparable 인터페이스

- 객체의 기본 정렬 기준을 정의
- 클래스에 직접 구현
- compareTo(T o) 메서드를 구현하여 정렬 기준을 정의

```java
public interface Comparable<T> {
    public int compareTo(T o);
}
```

- 0: =
- 양수: >
- 음수: <

##### Comparator 인터페이스

- 별도의 정렬 기준을 정의
- 정렬 기준이 여러 개 필요한 경우 유용
- 클래스 외부에서 정렬 기준을 정의하며, 특정 필드나 사용자 정의 기준으로 정렬할 수 있음
- compare(T o1, T o2) 메서드를 구현하여 정렬 기준을 정의

```java
public interface Comparator<T> {
    int compar(T o1, T o2);
}
```

- 0: =
- 양수: >
- 음수: <

```java
Collections.sort(names, new StringLengthComparator());

Collections.sort(names, new Comparator<String>(){
    @Override
    public int compare(String o1, String o2) {
        return Integer.compare(o1.length(), o2.length());
    }
})

Collections.sort(names, (o1, o2)->{
    return Integer.compare(o1.length(), o2.length());
})
```