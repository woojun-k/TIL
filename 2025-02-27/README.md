## 목차

## CSS

### 단위

- 절대단위: `px`, `pt`, `cm`, `mm`, `in`
- 상대단위: `%`, `em`, `rem`, `vw`, `vh`, `vmin`, `vmax`
- `auto`

### box model

- 모든 HTML 요소는 box 형태로 되어있음
- 모든 요소는 네모(박스모델)이고, 위에서부터 아래로, 왼쪽에서 오른쪽으로 쌓인다.

### layout

- float
    > float 속성은 박스를 어느 위치에 배치할 것인지를 결정하기 위해 사용(요소가 normal flow에서 벗어나 배치하도록 함)
    - none: 기본값
    - left: 요소를 왼쪽으로 띄움
    - right: 요소를 오른쪽으로 띄움

- clear
    > float 속성이 가지고 있는 값을 초기화 하기 위해 사용
    - left, right: 각각의 속성 값을 취소할 수 있음
    - both: 양쪽의 float 속성 값을 취소할 수 있음
    - none: 기본값

### Flexbox

- Flexible Box module은 인터페이스 내의 아이템 간 공간 배분과 강력한 정렬 기능을 제공하기 위한 1차원 레이아웃 모델로 설계
- 각각 아이템의 저마다의 높이를 가지고 있다면 flex는 자동으로 맞춰준다

#### Flexbox - 축

- Main Axis
- Cross Axis

#### Flexbox - 구성요소

- Flex Container
- Flex item

### Flex Container

- flexbox 레이아웃을 형성하는 가장 기본적인 모델

### Flexbox 속성

- `flex-direction`: row, row-reverse, column, column-reverse
- `flex-wrap`: nowrap, wrap, wrap-reverse
- `flex-flow`: row nowrap, column nowrap, row wrap
- `justify-content`: flex-start, flex-end, center, space-between, space-around, space-evenly
- `align-content`: flex-start, flex-end, center, space-between, space-around, space-evenly
- `align-items`: stretch, flex-start, flex-end, center, baseline
- `align-self`: stretch, flex-start, flex-end, center
    > 해당 속성은 컨테이너가 아닌 개별 아이템에 적용

### Flexbox 추가 속성

- `order`: item의 순서
- `flex-basis`: item의 초기 크기
- `flex-grow`: 여분의 공간 증가 비율
- `flex-shrink`: item 수용 공간이 부족할 때 축소 비율 지정
- `flex`: grow-shrink-basis 축약형
