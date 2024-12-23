# PokemonPhoneBook

**목표**: Xcode에서 UIKit 프레임워크를 이용해서 스토리보드 혹은 코드베이스로 포켓몬 전화번호부를 만듭니다.

## 🌟 필수 구현 기능 (Levels 1-5)

- **Level 1**: `UILabel`, `UITableView`, `UIButton` 등을 이용해 테이블 뷰 만들기
- **Level 2**: `UIViewController`를 새로 추가하여 연락처 추가 화면을 구현하기(파일 이름: PhoneBookViewController.swift)
- **Level 3**: 상단 네비게이션 바 영역을 구현하기 (제목, 적용 버튼 등)
- **Level 4**: API를 연결하여 버튼을 눌렀을 때 랜덤한 이미지가 생성되도록 구현하기
- **Level 5**: 적용 버튼을 누르면 연락처 데이터(이름/전화번호/프로필 이미지)를 디스크에 실제 저장하도록 구현하기

## 💪 도전 구현 기능 (Levels 6-8)

- **Level 6**: 연락처를 추가한 후 메인화면의 연락처가 항상 이름 순으로 정렬되도록 구현하기
- **Level 7**: 테이블뷰의 셀을 클릭했을 때 `PhoneBookViewController` 페이지로 이동되도록 구현하기
- **Level 8**: 테이블뷰의 셀을 클릭해서 화면을 이동했을 때, 연락처 편집 페이지에서 실제로 기기 디스크 데이터에 Update가 일어나도록 구현하기

## 🔥 Challenge - 디테일 키우기

Level 1 ~ 8 까지 구현하고도 여유가 되시는 분들은 심화과정을 고민해보기

- 포켓몬의 덩치가 클 때, 이미지 영역을 벗어나는 경우가 있습니다. 이 때, 원 밖을 벗어나지 않도록 구현해 봅시다!!
- 연락처를 매우 많이 추가했을 경우(예: 20개 이상) 테이블 뷰 스크롤을 빠르게 내리면 이미지가 겹쳐 보이거나 텍스트가 제대로 노출되지 않는 문제가 있을 수 있습니다.
  - 이 문제는 `prepareForReuse`의 개념을 사용하면 해결할 수 있습니다
  - 구현은 못하더라도 개념 공부를 추천드립니다.
- 어떻게 구현하냐에 따라 메인화면의 우상단의 `추가` 버튼이 잘 클릭되지 않는 함정에 빠질 수 있습니다. 이걸 해결해 주세요!
- 연락처 앱에는 또 어떤 예외 사항이 있을지 스스로 고민해보며 자신만의 챌린지를 만들어 주세요!!

## 📜 구현 가이드

- 개발 프로세스 가이드
  - **`UIKit` 화면 구성 및 화면 전환**
    - 화면구성: `UITableView`, `UILabel`, `UITextView`, `UIButton`  활용
    - 화면전환: `친구 목록 페이지` → `연락처 추가 페이지`로 이동
    
  - **`URLSession` / `Alamofire` 복습**
    - 네트워크 통신을 이용해서 서버에서 랜덤 포켓몬 이미지를 불러옵니다.
    - 두 가지 방법으로 모두 개발해보면 좋은 연습이 됩니다.
    - 포켓몬 API: [포켓몬 API 링크](https://pokeapi.co/)

  - **`ViewController 생명주기` 개념**
    - 친구 목록 페이지에 진입할때마다 목록이 `이름순으로 정렬`되도록 합니다.
    
  - **`CoreData` / `UserDefaults` 활용**
    - 연락처 데이터를 `기기 디스크에 저장`합니다.
    - 두 가지 방법으로 모두 개발해보면 좋은 연습이 됩니다.

- **포켓몬 JSON Response 형태**
```swift
  // JSON Response 형태
  {
    "id": 25,
    "name": "pikachu",
    "height": 4,
    "weight": 60,
    "sprites": {
      "front_default": "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/25.png"
    }
  }
```

---

## 🎯 목표

- **기한**: 12월 12일 (목) 낮 12시까지 제출
- **제출물**:
  - 개인과제 결과물 제출 (GitHub 링크)
  - 트러블슈팅 TIL
  - 과제를 소개하는 README

## 🔗 과제 링크

- [Ch 3. 앱개발 숙련 주차 과제]([https://developer.apple.com/swift/](https://teamsparta.notion.site/Ch-3-1522dc3ef5148059b6c7f310f7b15966))
  
---
