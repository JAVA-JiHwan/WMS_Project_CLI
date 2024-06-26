
<h2>쇼핑몰 기반 창고관리 시스템(CLI방식)</h2>

<h3>프로젝트 목적</h3>
<ul>
<li>유저는 총관리자, 쇼핑몰관리자, 창고관리자, 주문고객 이렇게 4분류로 나뉜다.</li>
<li>주문고객이 상품을 주문하고 주문 상태에 따라 실시간으로 창고의 입출고 내역을 조회할 수 있다.</li>
<li>CLI방식으로 구현 후, Spring MVC 및 Mybatis적용해서 리펙토링한다. </li>
</ul>

---
<h3>팀원 소개</h3>

| 이름 |                                                                      업무 |
| --- | --- |
| 양성준  | ERD설계,Back-end 개발환경구성, GitHub관리,전체 개발관리  |
| 최문석  | 통합재고관리, 창고관리, 유즈케이스작성  |
| 백정훈 | 발주관리 |
| 문지환 | 상품관리 |
| 이도엽 | 주문관리 |
| 이다혜 | 배송관리 |

---
<h3>주요기능</h3>

- 상품관리 : 상품 등록 및 조회 관련 기능 처리
- 발주관리 : 발주관리 및 발주 관련 기능 처리
- 배송관리 : 배송준비된 상품에 대한 배송 처리
- 주문관리 : 주문 관리 고객 주문 처리 및 배송 연계
- 창고관리 : 발주 상품 입고 및 주문 상품 출고 자동화 관리
- 입/출고관리 : 발주와 주문에 따른 실시간 입/출고관리 (Trigger 적용)
  - 각 입/출고 상태는 대기/취소/확정으로 나뉜다.
- 통합재고관리 : 상품의 입/출고상태에 따라 실시간으로 재고조회 기능 처리

---
### 시연 영상

[여기를 클릭하시면 구현된 영상을 확인 가능합니다](https://www.youtube.com/watch?v=cJ7K8-btvWc)

---
### 사용기술

- JAVA : 전체적인 백엔드 JAVA 객체지향으로 구현
- MySQL : 관계형 데이터베이스로 데이터 저장 및 관리
- JDBC : Java 표준 API를 사용하여 MySQL과 연결하고, 쿼리를 통해 CRUD (Create, Read, Update, Delete) 작업 수행

---
### 주요기능 
![Class Diagram](src/image/주요기능.png)

---
### Class Diagram
![Class Diagram](src/image/Class다이어그램.png)

---
### ER Diagram
![ERDiagram](src/image/ER다이어그램.png)

---
### Usecase
![Usecase](src/image/유즈케이스.png)

---

## KPT (Keep, Problem, Try)

### Keep (유지할 점):

- **팀원 간의 협업 및 소통이 원활하게 이루어졌던 점**을 유지해야 합니다.
- **프로그램의 기본 기능인 주문 관리 및 창고 관리가 잘 구현되었다는 점**을 유지해야 합니다.
 
### Problem (문제점):

- **예외 처리 및 코드 패턴 변경이 필요한 부분**이 있습니다. 예외 상황에 대한 처리가 미흡하거나 코드의 가독성이 낮은 부분을 개선해야 합니다.
- **재고의 실시간 추적에 대한 기능이 미흡**하며, 특히 취소나 반품과 관련된 기능이 더 개선되어야 합니다.
- **유저와 관리자의 기능이 혼재되어 있어, 보다 신뢰성이 높은 프로그램을 구현하기 위해 기능을 분리해야 합니다.**
 
### Try (시도할 점):

- **예외 처리 및 코드 패턴 변경을 통해 코드의 안정성과 가독성을 개선**해야 합니다. 특히 예외 상황에 대한 명확한 처리 방법을 도입해야 합니다.
- **재고의 실시간 추적을 보다 효율적으로 구현하기 위해, 취소나 반품과 관련된 기능을 개선하고 실시간 데이터 업데이트를 강화**해야 합니다.
- **유저와 관리자의 기능을 분리하고, 각각의 역할에 맞는 보다 신뢰성이 높은 프로그램을 구현하기 위해 기능을 재정의**해야 합니다.




