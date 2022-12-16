<h1 align="center"> :sparkler::pretzel::honey_pot: HOTEL DAL-GO-NA :honey_pot::pretzel::sparkler: </h1>

- 수행 기간 : 2022. 12. 15.

- 제출일 : 2022. 12. 16.

- 발표일 : 2022. 12. 16.

---

## 💁‍♂️ 프로젝트 소개

### 📃 시나리오

```
일본 모 대학을 군휴학한 한국인 대학생 유정호 씨(22세).
그는 전역 후 얼마간의 짜릿한 공백기를 마치고 복학을 앞둔 상태이다.
다시 시험과 과제의 늪에 빠질 자신을 위로하기 위해, 그는 Hotel-DalGoNa(서울 중구 명동8길 229-7)에 투숙하기로 예약했다.
예약 당일, 그는 택시를 타고 호텔 Lobby의 Entry에 도착했다.
택시에서 내리자마자 DoorMan Kim이 그를 Reception으로 안내했다.
Reception에서 상시 대기 중인 Manager Park은 그에게 예약 여부를 확인하고 체크인을 도왔다.
이후 그가 투숙할 동안 서비스를 책임질 Bell-Boy Jeong을 호출했다.
Jeong은 그를 Room(객실)까지 안내했다.
```

### 📚 구성

- `PACKAGE` ***common***
  - 호텔과 연관성이 비교적 낮고 보편적인 클래스를 담은 패키지
  - `CLASS` ***Person*** : 사람에 관하여 정의함
  - `CLASS` ***Guest*** : 손님에 관하여 정의함
  - `CLASS` ***Employee*** : 직원에 관하여 정의함

- `PACKAGE` ***place.lobby.entry***
  - 직원이 호텔 입구에서 고객을 응접하는 클래스를 담은 패키지
  - `CLASS` ***DoorMan*** : 고객을 응접하는 직원에 관하여 정의함

- `PACKAGE` ***place.lobby.reception***
  - 직원이 호텔 프론트에서 고객의 예약 확인, 접수, 체크인/체크아웃을 돕는 클래스를 담은 패키지
  - `CLASS` ***Manager*** : 고객의 예약 확인, 접수, 체크인/체크아웃을 돕는 직원에 관하여 정의함
  - `CLASS` ***Reservation*** : 고객의 예약에 관하여 정의함
  - `CLASS` ***Reception*** : 고객의 접수에 관하여 정의함

- `PACKAGE` ***place.lobby.room***
  - 객실 특성 및 직원이 고객을 객실까지 안내하는 클래스를 담은 패키지
  - `CLASS` ***BellBoy*** : 고객을 객실까지 안내하는 직원에 관하여 정의함
  - `CLASS` ***Room*** : 객실 특성에 관하여 정의함
  
---

## 🎁 common

- `CLASS` ***Person***
  - `FIELD` `PRIVATE` ***name*** : 성명
  - `FIELD` `PRIVATE` ***age*** : 나이; 1~150세
  - `FIELD` `PRIVATE` ***gender*** : 성별; M(남성), W(여성)
  - `FIELD` `PRIVATE` ***nationality*** : 국적; K(한국), J(일본), C(중국), S(스페인어권), E(영어권 및 기타)
  - `CONSTRUCTOR` ***Person*** : name, age, gender, nationality를 파라미터로 받음
  - `Getter` : name, age, gender, nationality를 확인함
  - `Setter` : name, age, gender, nationality를 재정의함
    
- `CLASS` ***Guest***
  - extends Person
  
- `CLASS` ***Employee***
  - extends Person

---

## 🎁 place.lobby.entry

- `CLASS` ***DoorMan***
  - extends Employee
  - `METHOD` ***helloGuestDoorMan*** : 고객을 entry에서 reception까지 안내하는 행위

---

## 🎁 place.lobby.reception

- `CLASS` ***Manager***
  - extends Employee

- `CLASS` ***Reservation***
  - `METHOD` ***enrollReservation*** : 손님이 호텔을 예약하는 행위
    - 내부적으로 `CLASS` ***Guest***의 `Setter` 작동함

- `CLASS` ***Reception***

---

## 🎁 place.lobby.room

- `CLASS` ***BellBoy***
    - extends Employee
    - `METHOD` ***helloGuestBellBoy*** : 고객을 reception에서 room까지 안내하는 행위

- `CLASS` ***Room***
  - `FIELD` ***roomNumber*** : 객실번호
  
  - `FIELD` ***roomTypeBed*** : 침대 종류
    - single
    - double
  
  - `FIELD` ***roomTypeBath*** : 샤워실 종류
    - showerbooth
    - bathtub
  
  - `FIELD` ***roomTypeView*** : 전망 종류
    - city
    - mountain
    - ocean
  
---

## 👭 WORKMATE

👩 [**김가람**](https://github.com/kim-garam)

👩 [**김효정**](https://github.com/410am)

🧑 [**왕재준**](https://github.com/jayarnim)

---
