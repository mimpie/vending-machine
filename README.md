# vending-machine
놀러와요 개발의 숲 - 자판기 과제 리포지토리
# [과제] 자판기

# 🖥️ 요구 사항

요구 사항을 잘 읽고 어떤 기능을 구현해야 할 지에 대해 고민하세요!

---

안녕하세요 GDSC PKNU 입니다! 🙋‍♂️
이번 11월 25일에 GDSC PKNU에서는 부경대학교 학생들을 위해 정문에 **음료 자판기를 설치**하려고 합니다. 계절에 따라 학생들이 선호하는 차가운 음료와 따뜻한 음료를 다양하게 판매할 계획인데요.

GDSC PKNU 여러분들이 해당 자판기의 소프트웨어를 구현해주셨으면 합니다!

일반적인 자판기는 현금으로만 결제가 가능하지만, 학생들이 편리하게 이용할 수 있도록 카드 결제도 가능했으면 좋겠어요! 
(하지만, GDSC PKNU에서는 카드 결제 시에 10% 부가세를 포함하여 계산해야 해요. )

저희 GDSC PKNU에서 설치할 자판기는 **차가운 음료와 따뜻한 음료**를 제공할 예정인데
해당 음료의 종류와 가격을 아래와 같이 알려드려요!

**차가운 음료**

```
스프라이트 : 1,500원, 코카콜라 : 1,300원, 솔의눈 : 1,000원, 펩시 콜라 :1,100원
```

**따뜻한 음료**

```
TOP커피 : 1,800원, 꿀물 : 1,500원, 홍삼차 : 1,700원, 단팥죽 :2,100원
```

결제 방식은 현금과 카드로 가능하도록 하고자 합니다!

**현금 결제의 경우**, 초과되는 금액을 넣었을 때 거스름돈을 반환해야 합니다 !
(지폐나 동전을 최적으로 활용하여 거스름돈을 반환하는 방법을 고려해야 합니다.)

또한 ! 돈을 잘못 넣을 수 있기 때문에 **반환하는 기능**을 고려해서 만들어주시면 좋겠어요~

- 예시
    - ex)
    
    ```
    [현금 투입 : 1,000원]
    [1] 5만원권 
    [2] 1만원권 
    [3] 5천원권  
    [4] 1천원권  
    [5] 500원 동전
    [6] 100원 동전
    [0] 반환
    ```
    
    반환을 누르면 ‘[현금 투입 : 0원]’이 됩니다.
    
    ```
    [현금 투입 : 0원]
    [1] 5만원권 
    [2] 1만원권 
    [3] 5천원권  
    [4] 1천원권  
    [5] 500원  
    [6] 100원 
    ```
    

**카드 결제의 경우**, 부가세를 10% 부과하여 가격을 결제하면 좋겠어요!

 

# 🖼️실행 결과 예시

실행 결과 예시를 참고하여 최대한 요구 사항에 맞도록 구현해주세요!

---

<aside>
🔥 **현금 결제** / 결과 예시

- 현금 결제
    
    ```
    [어서와요! GDSC 음료 자판기]
    음료를 선택 해주세요!
    
    [1] 차가운 음료
    [2] 따뜻한 음료
    
    사용자 입력 > 1
    
    ------------------------------
    [차가운 음료]
    
    [1] 스프라이트 : 1,500원
    [2] 코카콜라 : 1,300원
    [3] 솔의눈 : 1,000원
    [4] 펩시 콜라 : 1,100원
    
    사용자 입력 > 1
    
    ------------------------------
    [결제 방식 선택]
    
    [1] 현금
    [2] 카드 (부가세 10% 적용)
    
    사용자 입력 > 1
    
    ------------------------------
    [현금 투입 : 0원]
    
    [1] 5만원권 
    [2] 1만원권 
    [3] 5천원권  
    [4] 1천원권  
    [5] 500원  
    [6] 100원 
    
    사용자 입력 > 4
    ------------------------------
    [현금 투입 : 1,000원]
    
    [1] 5만원권 
    [2] 1만원권 
    [3] 5천원권  
    [4] 1천원권  
    [5] 500원 동전
    [6] 100원 동전
    [0] 반환
    
    사용자 입력 > 4
    ------------------------------
    이용해주셔서 감사합니다.
    
    [주문 음료] 
    스프라이트
    
    [투입 금액]
    2,000원
    
    [잔돈] 
    500원 동전 : 1개
    ```
    
</aside>

<aside>
🔥 **카드 결제** / 결과 예시

- 카드 결제
    
    ```
    [어서와요! GDSC 음료 자판기]
    음료를 선택 해주세요!
    
    [1] 차가운 음료
    [2] 따뜻한 음료
    
    사용자 입력> 1
    
    ------------------------------
    [차가운 음료]
    
    [1] 스프라이트 : 1,500원
    [2] 코카콜라 : 1,300원
    [3] 솔의눈 : 1,000원
    [4] 펩시 콜라 : 1,100원
    
    사용자 입력 > 1
    
    -------------------------------
    [결제 방식 선택]
    
    [1] 현금
    [2] 카드 (부가세 10% 적용)
    
    사용자 입력 > 2
    
    -------------------------------
    이용해주셔서 감사합니다.
    
    [주문 음료] 
    스프라이트
    
    [결제 금액]
    1,650 원
    ```
    
</aside>

# 📌고려 사항

프로그래밍을 하면서 아래에 내용을 최대한 지키도록 노력해주세요!

---

<aside>
☝🏻 **고려 사항 목록**

1. 기능 요구 사항을 준수한다
2. 프로그래밍 요구 사항을 준수한다.
3. 커밋 컨벤션 을 준수하고자 노력한다. 
    
    [Conventional Commits](https://www.conventionalcommits.org/ko/v1.0.0/)
    
4. 언어는 구글 컨벤션을 준수하고자 노력한다.
    
    [Google Style Guides](https://google.github.io/styleguide/)
    
5. linter와 Code Formatter의 기능을 활용한다
6. 언어에서 제공하는 API 를 적극 활용한다
7. Pull Request를 보내기 전 브랜치 를 확인한다
8. PR을 한 번 작성했다면 닫지 말고 추가 커밋 한다
</aside>

# 추가 기능 요구사항

## 추가 기능 요구 사항

---

### 관리자 페이지

총 수익을 보여주는 관리자 페이지를 구현합니다.

관리자 페이지는 초기 화면에서 `admin`을 입력하여 접근 가능합니다.

**관리자의 권한 은 총 수익을 계산할 수 있고 음료를 추가 및 삭제, 가격 변경이 가능합니다.**

<aside>
💡 과제 **참조!**
- 위 예시 데이터는 구현의 편의를 위해 제공되는 정보이며, 요구사항(의도)을 만족시킨다면 **다른 형태의 요청 또는 UI**를 사용하여도 좋습니다.

- 사용자가 **잘못된 값을 입력할 경우에 대한 예외처리**를 반드시 해주셔야합니다.

- 위 제공된 UI는 예시이며**, 임의로** 생성 가능합니다.

- 명시되지 않은 조건은 자유롭게 개발하도록 합니다.

</aside>

- 관리자 - **음료 추가**
    
    ```
    [어서와요! GDSC 음료 자판기]
    음료를 선택 해주세요
    
    [1] 차가운 음료
    [2] 따뜻한 음료
    
    사용자 입력 > admin
    -------------------------------
    [관리자 페이지 - 음료 관리]
    
    [1] 음료 확인
    [2] 음료 추가
    [3] 음료 삭제
    
    admin 입력 > 2
    -------------------------------
    [관리자 페이지 - 음료 추가]
    
    [1] 차가운 음료
    [2] 따뜻한 음료
    
    admin 입력 > 1
    -------------------------------
    [관리자 페이지 - 음료 추가]
    
    음료 이름을 설정하세요
    
    admin 입력 > 토레타
    -------------------------------
    [관리자 페이지 - 음료 추가]
    
    음료 가격을 설정하세요
    
    admin> 1300원
    -------------------------------
    [관리자 페이지 - 추가완료]
    토레타 : 1300원 이(가) 추가 완료되었습니다.
    ```
    
- 관리자 - **음료 삭제**
    
    ```
    [어서와요! GDSC 음료 자판기]
    음료를 선택 해주세요
    
    [1] 차가운 음료
    [2] 따뜻한 음료
    
    사용자 입력 > admin
    -------------------------------
    [관리자 페이지]
    
    [1] 총 수익 확인
    [2] 음료 관리
    
    admin 입력 > 2
    -------------------------------
    [관리자 페이지 - 음료 관리]
    
    [1] 음료 확인
    [2] 음료 추가
    [3] 음료 삭제
    
    admin 입력 > 3
    
    -------------------------------
    [관리자 페이지 - 음료 삭제]
    
    [1] 스프라이트 : 1,500원
    [2] 코카콜라 : 1,300원
    [3] 솔의눈 : 1,000원
    [4] 펩시 콜라 : 1,100원
    [5] TOP커피 : 1,800원
    [6] 꿀물 : 1,500원
    [7] 홍삼차 : 1,700원
    [8]  단팥죽 :2,100원
    
    admin 입력 > 3
    
    -------------------------------
    [관리자 페이지 - 음료 삭제 완료]
    
    솔의눈 : 1,000원 이(가) 삭제되었습니다.
    ```
    
- 관리자 - **음료 확인**
    
    ```
    [어서와요! GDSC 음료 자판기]
    음료를 선택 해주세요
    
    [1] 차가운 음료
    [2] 따뜻한 음료
    
    사용자 입력 > admin
    -------------------------------
    [관리자 페이지]
    
    [1] 총 수익 확인
    [2] 음료 관리
    
    admin 입력 > 2
    -------------------------------
    [관리자 페이지 - 음료 관리]
    
    [1] 음료 확인
    [2] 음료 추가
    [3] 음료 삭제
    
    admin 입력 > 1
    
    -------------------------------
    [관리자 페이지 - 음료 확인]
    
    [차가운 음료]
    
    [1] 스프라이트 : 1,500원
    [2] 코카콜라 : 1,300원
    [3] 솔의눈 : 1,000원
    [4] 펩시 콜라 : 1,100원
    
    [1] TOP커피 : 1,800원
    [2] 꿀물 : 1,500원
    [3] 홍삼차 : 1,700원
    [4]  단팥죽 :2,100원
    ```
    
## 코드 리뷰시, 중점적으로 고려해야할 요구사항

---

- 1차 리뷰
    
    <aside>
    📌 1차 코드 리뷰시, 고려할 것들
    
    - 필드의 수를 줄이기 위해 노력한다
    - 비즈니스 로직과 UI 로직을 분리한다
    - 값을 하드 코딩하지 않는다
    - 발생할 수 있는 예외 상황에 대해 고민한다
    - 3항 연산자 사용 금지
    - 메서드는 최대한 한가지 기능만!
    </aside>
    
    ****
    
- 2차 리뷰
    
    <aside>
    📌 2차 코드 리뷰시, 고려할 것들
    
    - 객체의 상태 접근을 제한한다
    - 메서드의 길이가 15라인을 넘지 않도록 구현
    - indent(인덴트, 들여쓰기) depth를 3이 넘지 않도록 구현한다. 2까지만 허용한다.
        - 예를 들어 while문 안에 if문이 있으면 들여쓰기는 2이다.
        - 힌트: indent(인덴트, 들여쓰기) depth를 줄이는 좋은 방법은 함수(또는 메소드)를 분리하면 된다.
    - else 예약어를 쓰지 않는다.
        - 힌트: if 조건절에서 값을 return하는 방식으로 구현하면 else를 사용하지 않아도 된다.
        - switch/case도 허용하지 않는다.
    </aside>
---

[추가 기능 요구사항 ](%5B%E1%84%80%E1%85%AA%E1%84%8C%E1%85%A6%5D%20%E1%84%8C%E1%85%A1%E1%84%91%E1%85%A1%E1%86%AB%E1%84%80%E1%85%B5%20f970506f9df84b2f9fea35b5d175ef58/%E1%84%8E%E1%85%AE%E1%84%80%E1%85%A1%20%E1%84%80%E1%85%B5%E1%84%82%E1%85%B3%E1%86%BC%20%E1%84%8B%E1%85%AD%E1%84%80%E1%85%AE%E1%84%89%E1%85%A1%E1%84%92%E1%85%A1%E1%86%BC%202e558ae63d924e65a1188b30c667c1c7.md)
