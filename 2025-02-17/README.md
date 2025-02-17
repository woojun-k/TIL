## 목차

## Queue

- 큐
- 선형 큐
- 원형 큐
- 큐의 활용

### 큐(Queue)

줄, 줄을 서서 기다리다, 대기 행렬을 만든다

- 자료를 통로에 넣어 대기 줄과 같은 형태의 자료구조
- 선형 자료구조 (1:1)
- 선입선출(FIFO)
- `front`, `rear` 변수 활용

### 큐의 주요 연산

- 삽입`enQueue` : 큐의 맨 뒤쪽에 원소를 삽입
- 삭제`deQueue` : 큐의 맨 앞쪽에서 원서를 꺼내서 반환 ( 공백의 경우 예외 )
- 공백확인`Empty` : 큐가 비어 있는지 확인
- 포화확인`Full` : 큐가 가득 차 있는지 확인

### 선형 큐(Linear Queue)

배열을 사용하여 구현된 기본적인 큐

- 큐의 크기 -> 배열의 크기
- front: 큐에서 데이터를 제거하는 위치
- rear: 큐에서 데이터를 삽입하는 위치

#### 선형 큐(Linear Queue) - enQueue / deQueue

- 마지막 원소 뒤에 새로운 원소를 삽입
    ```
    enQueue(item) {
        if (isFull()) print("Queue_Full")
        else {
            rear <- rear + 1;
            Q[rear] <- item;
        }
    }
    ```
- 가장 앞에 있는 원소를 삭제
    ```
    deQueue(item) {
        if (isEmpty()) print("Queue_Empty")
        else {
            front <- front + 1;
            return Q[front];
        }
    }
    ```

#### 선형 큐(Linear Queue) - isEmpty() / isFull()

- 공백 상태: front == rear
    ```
    isEmpty() {
        if(front == rear) rear true;
        else return false;
    }
    ```

- 포화 상태: rear == n-1(n : 배열의 크기)
    ```
    isFull() {
        if (rear == n-1 ) return true;
        else return false;
    }
    ```

### 원형 큐(Circular Queue)

선형 큐의 공간 낭비 문제를 해결한 자료구조
- 논리적으로 처음과 끝이 연결하여 원형처럼 순환 동작하도록 만든 큐 (나머지 연산)
- front: 가장 먼저 들어온 데이터의 위치
- rear: 가장 최근에 들어온 데이터의 위치

#### 원형 큐(Circular Queue) - isEmpty() / isFull()

- 공백 상태 : front == rear

    ```
    isEmpty(){
        if(front == rear) return true;
        else return false;
    }
    ```

- 포화 상태: 삽입할 다음 rear의 위치 == 현재 front
(rear + 1) mod n = front

    ```
    isFull(){
        if((rear+1) mod n == front) return true;
        else return false;
    }
    ```

#### 원형 큐(Circular Queue) - enQueue(item) / deQueue()

- 마지막 원소 뒤에 새로운 원소를 삽입
    ```
    enQueue(item){
        if (isFull()) print("Queue_Full")
        else {
            rear <- (rear + 1) mod n;
            cQ[rear] <- item;
        }
    }
    ```

- 가장 앞에 있는 원소를 삭제
    ```
    deQueue() {
        if (isEmpty()) print("Queue_Empty")
        else {
            front <- (front + 1) mod n;
            return cQ[front];
        }
    }
    ```

### 큐의 활용

- Buffer
    - 데이터를 한 곳에서 다른 한 곳으로 전송하는 동안 일시적으로 데이터를 보관하는 메모리 영역
    - 버퍼링: 버퍼를 활용하는 방식 또는 버퍼를 채우는 동작을 의미

- 버퍼의 자료구조
    - 버퍼는 일반적으로 입출력 및 네트워크와 관련된 기능에서 이용
    - 입력과 출력이 순서대로 전달되어야 하므로 FIFO 방식의 자료구조인 큐가 활용됨

