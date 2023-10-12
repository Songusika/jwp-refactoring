# 키친포스

## 요구 사항
### 상품
#### 상품
- 상품은 이름과 가격이 있다.
- 상품의 가격은 0원 이상이어야 한다.

### 메뉴
#### 메뉴 상품
- 메뉴 상품은 메뉴와 수량이 있다.
- 메뉴 상품은 특정 하나의 메뉴에 속할 수 있다.
- 메뉴 상품의 수량은 1 이상이어야 한다.

#### 메뉴
- 메뉴는 이름과 가격, 메뉴 상품 목록을 가지고 있다.
- 메뉴는 특정 하나의 메뉴 그룹에 속할 수 있다.
- 메뉴의 가격은 ∑((각 메뉴 상품 가격 * 각 메뉴 상품 수량) 이다.
- 메뉴의 가격은 1원 이상 이어야 한다.

#### 메뉴 그룹
- 메뉴 그룹은 이름을 가진다.
- 메뉴 그룹은 여러 메뉴를 가질 수 있다.

### 주문
#### 주문 상품
- 주문 상품은 메뉴와 해당 메뉴의 수량을 가진다.
- 주문 상품은 하나의 주문에 속할 수 있다.

#### 주문 상태
- 주문 상태는 '조리 중', '식사 중', '완료' 상태를 가진다.

#### 주문
- 주문은 주문 상태와 주문 시간, 주문 상품들을 가진다.
- 주문은 최소 한개 이상의 주문 상품을 가져야한다.
- 주문은 존재하지 않는 메뉴를 가진 주문 상품을 가질 수 없다.
- 주문은 특정 하나의 주문 테이블에 속해야한다.
- 주문 테이블이 빈자리일 경우 주문을 할 수 없다.
- 주문이 완료되면 주문 상태를 '조리 중"으로 변경한다.

### 테이블
#### 주문 테이블
- 주문 테이블은 손님의 수와, 빈자리 여부를 가잔다.
- 주문 테이블은 주문 상태가 '조리 중' 또는 '식사 중' 일 때 빈자리로 변경할 수 없다.
- 주문 테이블은 빈자리일 경우 손님 수를 변경할 수 없다.
- 주문 테이블은 특정 하나의 테이블 그룹에 속할 수 있다.

#### 테이블 그룹
- 테이블 그룹은 생성일, 주문 테이블들을 가진다.
- 테이블 그룹의 주문 테이블은 2 이상이어야 한다.
- 테이블 그룹은 생성 시 모든 주문 테이블이 빈자리여야 한다.
- 테이블 그룹은 주문 테이블 중 주문 상태가 '조리 중' 또는 '식사 중' 일 때 해제할 수 없다.


## 용어 사전

| 한글명 | 영문명 | 설명 |
| --- | --- | --- |
| 상품 | product | 메뉴를 관리하는 기준이 되는 데이터 |
| 메뉴 그룹 | menu group | 메뉴 묶음, 분류 |
| 메뉴 | menu | 메뉴 그룹에 속하는 실제 주문 가능 단위 |
| 메뉴 상품 | menu product | 메뉴에 속하는 수량이 있는 상품 |
| 금액 | amount | 가격 * 수량 |
| 주문 테이블 | order table | 매장에서 주문이 발생하는 영역 |
| 빈 테이블 | empty table | 주문을 등록할 수 없는 주문 테이블 |
| 주문 | order | 매장에서 발생하는 주문 |
| 주문 상태 | order status | 주문은 조리 ➜ 식사 ➜ 계산 완료 순서로 진행된다. |
| 방문한 손님 수 | number of guests | 필수 사항은 아니며 주문은 0명으로 등록할 수 있다. |
| 단체 지정 | table group | 통합 계산을 위해 개별 주문 테이블을 그룹화하는 기능 |
| 주문 항목 | order line item | 주문에 속하는 수량이 있는 메뉴 |
| 매장 식사 | eat in | 포장하지 않고 매장에서 식사하는 것 |
