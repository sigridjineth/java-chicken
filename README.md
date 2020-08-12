# java-chicken

### 기능 요구사항

- 치킨집 사장님이 사용하는 간단한 포스 (POS)프로그램을 구현한다.
- 주문등록, 결제하기, 프로그램 종료 기능을 가진다
- 메뉴 기본 정보가 주어지며 메뉴 번호, 종류, 이름, 가격을 가진다.
- 테이블 기본 정보가 주어지며 테이블 번호를 가진다.
- 한 테이블에서 주문할 수 있는 한 메뉴의 최대 수량은 99개 이다.
- 주문이 등록된 테이블은 결제가 이루어지기 전 까지 테이블 목록에 별도로 표시 한다
- 주문 내역에 대한 계산을 할 때는 결제 유형에 따라 할인율이 달라진다.
    - 치킨 종류 메뉴의 수량의 합이 10개가 넘는 경우 10,000원씩 할인된다.
        - 10개는 10000원할인, 20개는 20000원할인
    - 현금 결제는 5%할인 할인된 금액에서 한번더 할인 가능(중복가능)
- 주문, 혹은 결제가 불가능한 이유 출력 ⇒ 재 주문/ 재결제 가능하도록 구현
- 최종 결제 금액을 보여준다.

### 기능 구현 목록
- 포스 메뉴 선택 기능 (1번 : 주문등록, 2번 : 결제하기, 3번 : 종료)
- 주문 등록하기
    - 테이블 선택 기능
        - 선택 가능한 테이블의 범위를 넘어서는 경우 예외
    - 등록 할 메뉴 선택 기능
    - 수량 입력 기능 (입력 가능한 최대 수량 99)
    - 선택한 메뉴와 수량으로 음식 총 가격 계산 하는 기능
    - 주문이 등록 되면, 테이블 목록에 원화 표식 추가
    - 최종 계산 되기 전 까지, 주문 등록된 음식을 장바구니에 저장
- 결제하기 
    - 테이블 선택 기능
        - 주문이 등록된 테이블만 선택 가능 이외 테이블 선택시 예외 발생
    - 주문 내역 출력
    - 결제 수단 선택 기능 (1번 : 신용카드, 2번 : 현금)
    - 할인 금액 계산 
        - 현금 결제 시 5% 할인 (치킨할인과 중복할인 가능)
        - 치킨 종류 메뉴 10개 단위로 10000원씩 할인
    - 할인 된 최종 금액 계산
    - 결제 확인 및 최종 승인 시 메세지 출력
    - 해당 테이블에 원화 표식 제거
- 프로그램 종료
    - 종료 버튼뉴(3)이 눌러지기 전까지 계속 포스 메뉴 출력



### 프로그래밍 요구사항

- 자바 코드 컨벤션을 지키면서 프로그래밍한다.
- indent(인덴트,들여쓰기)depth를 3이 넘지 않도록 구현한다.2까지만허용한다.
- 3항 연산자를 쓰지 않는다.
- 함수(또는메서드)가 한 가지 일 만하도록 최대한 작게 만들어라.
- 함수(또는메서드)의 길이가 15라인을 넘어가지 않도록 구현한다.
- 함수(또는메서드)가 한 가지 일만 잘하도록 구현한다.
- else 예약어를 쓰지 않는다.
- public/protected/private/package 접근 제어자를 용도에 적합하게 사용해 구현한다.
- 함수(또는메소드)의 인자 수를 3개까지만 허용한다.4개 이상은 허용하지 않는다.
    - 단,생성자는 제외한다.
- src/main/java/Application의 main()을실행해프로그램을시작한다.
- Application의 main()에서구현을시작한다.
- Menu 클래스를 활용한다.
- Menu에 기본생성자를 추가할 수 없다.
- Menu의필드(인스턴스변수)를 추가할 수 없다.
- 단,기존필드(인스턴스변수)의 데이터 타입은 변경할 수 있다.
- 필드(인스턴스변수)의 접근 제어자는 private으로 구현해야 한다.
- MenuRepository클래스를 활용해 구현해야 한다.
- 데이터를 조회하는 DB역할을 한다.
- MenuRepository의 기존 코드는 수정할 수 없다.
  - 단,추가는가능하다
- Table 클래스를 활용해 구현해야 한다.
- Table에 기본 생성자를 추가할 수 없다.
- 필드(인스턴스변수)의 접근 제어자는 private으로 구현해야 한다
- TableRepository클래스를 활용해 구현해야 한다.
- 데이터를 조회하는 DB역할을 한다.
- TableRepository의 기존코드는 수정할 수 없다.
    - 단,추가는가능하다.
