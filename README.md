# 프리코스 3주차 - 로또

<br>

## 📌 개요

간단한 로또 발매기를 구현한다.

<br>

## ⚙️ 실행 결과 예시

```text
구입금액을 입력해 주세요.
8000

8개를 구매했습니다.
[8, 21, 23, 41, 42, 43]
[3, 5, 11, 16, 32, 38]
[7, 11, 16, 35, 36, 44]
[1, 8, 11, 31, 41, 42]
[13, 14, 16, 38, 42, 45]
[7, 11, 30, 40, 42, 43]
[2, 13, 22, 32, 38, 45]
[1, 3, 5, 14, 22, 45]

당첨 번호를 입력해 주세요.
1,2,3,4,5,6

보너스 번호를 입력해 주세요.
7

당첨 통계
---
3개 일치 (5,000원) - 1개
4개 일치 (50,000원) - 0개
5개 일치 (1,500,000원) - 0개
5개 일치, 보너스 볼 일치 (30,000,000원) - 0개
6개 일치 (2,000,000,000원) - 0개
총 수익률은 62.5%입니다.
```

---

## 📝 기능 목록

### 로또 구입 금액을 입력받는 기능

- [x] `구입 금액을 입력해 주세요.` 안내 메시지를 출력한다.
- [x] 사용자로부터 로또 구입 금액을 입력받는다.

<br>

### 당첨 번호를 입력받는 기능

- [x] `당첨 번호를 입력해 주세요.` 안내 메시지를 출력한다.
- [x] 사용자로부터 당첨 번호를 입력받는다.

<br>

### 보너스 번호를 입력받는다.

- [x] `보너스 번호를 입력해 주세요.` 안내 메시지를 출력한다.
- [x] 사용자로부터 보너스 번호를 입력받는다.

<br>

### 구입 금액을 관리하는 기능

- [x] 구입 금액의 유효성을 검사하는 기능
- [x] 구입 금액을 반환하는 기능

### 당첨 번호를 관리하는 기능

- [x] 당첨 번호의 유효성을 검사하는 기능
- [x] 당첨 번호는 쉼표 기준으로 분리하여 보관한다.
- [x] 당첨 번호를 반환하는 기능

### 보너스 번호를 관리하는 기능

- [x] 보너스 번호의 유효성을 검사하는 기능
- [x] 보너스 번호를 반환하는 기능


### 발행한 로또 수량 및 로또 번호를 출력하는 기능

- [x] 발행한 로또 수량을 출력한다.
- [x] 발행한 로또 번호를 출력한다. (번호는 오름차순으로 정렬)

<br>

### 로또 번호를 생성하는 기능

- [x] 로또 번호를 생성한다.
- [x] `Randoms.pickUniqueNumbersInRange(1, 45, 6)`를 사용한다.

<br>

### 로또를 발행하는 기능

- [x] `구입 금액 / 1,000` 만큼 로또를 발행한다.
- [x] 로또는 제공된 `Lotto` 클래스를 사용하여 구현한다.
  - `numbers` 이외의 필드는 추가할 수 없다.
  - `numbers`의 접근 제어자는 변경할 수 없다.
  - `Lotto`의 패키지는 변경할 수 있다.

<br>

### 로또 당첨 등수를 계산하는 기능

- [ ] 당첨 등수를 계산한다.

```text
1등: 6개 번호 일치 / 2,000,000,000원
2등: 5개 번호 + 보너스 번호 일치 / 30,000,000원
3등: 5개 번호 일치 / 1,500,000원
4등: 4개 번호 일치 / 50,000원
5등: 3개 번호 일치 / 5,000원
```

<br>

### 당첨 내역을 생성하는 기능

- [ ] 당첨 내역을 생성한다.

<br>

### 당첨 내역을 출력하는 기능

- [ ] 당첨 내역을 출력한다.
- [ ] 당첨 금액은 3자리마다 쉼표를 추가한다.

<br>

### 수익률을 계산하는 기능

- [ ] 수익률은 계산한다.

<br>

### 수익률을 출력하는 기능

- [ ] 수익률을 출력한다.
- [ ] 소수점 둘째 자리에서 반올림한다. (ex. 100.0%, 51.5%)
- [ ] 3자리 마다 쉼표를 추가한다. (ex. 10,000)

<br>

### 에러 문구를 출력하는 기능

- [ ] 예외 상황 시 에러 문구를 출력해야 한다.
- [ ] 단, `[ERROR]`로 시작해야 한다.

<br>

### 예외 발생 시

- [ ] `IllegalArgumentException`을 발생시킨다.
- [ ] 에러 문구 출력 후 그 부분부터 다시 입력을 받는다.


### 로또 예외 케이스
  - [x] 로또 번호가 6개 아닌 경우
  - [x] 로또 번호에 중복된 번호가 있는 경우
  - [x] 로또 번호가 1~45 사이의 정수가 아닌 경우


### 구입 금액 입력 예외 케이스
  - [x] 구입 금액이 숫자가 아닌 경우
  - [x] 구입 금액이 1,000원 미만인 경우
  - [x] 구입 금액이 1,000원 단위가 아닌 경우


### 당첨 번호 예외 케이스
  - [x] 당첨 번호가 6개가 아닌 경우
  - [x] 당첨 번호가 숫자가 아닌 경우
  - [x] 당첨 번호에 중복된 번호가 있는 경우
  - [x] 당첨 번호가 1~45 사이의 정수가 아닌 경우
  

### 보너스 번호 예외 케이스
  - [x] 보너스 번호가 숫자가 아닌 경우
  - [x] 보너스 번호가 당첨 번호에 이미 있는 경우
  - [x] 보너스 번호가 1~45 사이의 정수가 아닌 경우


### 입력 예외 케이스
  - [x] 입력이 빈 문자열인 경우

<br>

## 📝 프로그래밍 요구사항

_프로그래밍 요구사항은 구현 완료 후 위반되는 내용이 없는지 확인한다._

- [ ] 들여쓰기 깊이는 최대 2까지만 허용한다.
- [ ] 함수가 한 가지 일만 하도록 구현한다.
- [ ] 함수의 라인 수가 15라인을 넘지 않도록 구현한다.
- [ ] else 사용을 지양한다.
- [ ] Enum Class를 적용하여 프로그램을 구현한다.
- [ ] 값을 하드 코딩 하지 않는다.
- [ ] 구현 순서도 컨벤션에 따라 구현한다.
    - 속성, 생성자, 부 생성자, 함수, 동반 객체 순으로 작성한다.
- [ ] 변수 이름에 자료형은 사용하지 않는다.
- [ ] 구현한 기능에 대한 단위 테스트를 작성한다.
    - 단, UI 로직은 제외한다.

<br>