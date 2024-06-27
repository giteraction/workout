# 운동기록 사이트 만들기

---

### <만들게 된 계기>

운동을 통해 멋진 몸과 자신감을 얻고 싶었지만 무계획적인 성향으로는 이러한 목적을 달성하기 어려웠습니다. 이를 타파하기 위해서는 체계적 운동이 필요함을 느꼈습니다. 

간단하게 메모장을 이용하여 “꾸준히 기록이라도 습관을 만들어보자”로 시작하였습니다. 이 때 기록하는 것 자체에도 의의와 동기부여를 얻기도 하였습니다


<img src="https://github.com/giteraction/workout/assets/95407727/82c083fb-1748-4cca-8258-bc730f958a8a" style="width:500px;">


하지만 쌓이기만 하는 과거의 데이터는 활용되지는 못한 점이 한계였습니다.

그리하여 이를 활용할 수 있는 데이터 분석 기록표를 만들 수 있겠다는 생각이 들었습니다.

---

### <준비사항>

먼저 사용하게 될 스택들과 요구 사항들을 개략적으로 나열 후 개발하면서 세부 사항을 다듬어가며 개발하고자하였습니다.

- 필요 스택
    - 서버 : Flask, mySQL, matplotlib
    - 서버↔클라이언트 : html, javascript, jinja, jquery, xhr
- 요구 사항
    - 프론트엔드
        - 운동 종목 기입 및 선택 인터페이스
        - 운동 세트수, 반복 횟수, 무게 등 기입 인터페이스
        - 식단 메뉴 기입 및 선택 인터페이스
        - 섭취 음식 중량 기입 인터페이스
        - 분석 결과 및 지침(일별,월별,분기별)
    - 백엔드
        - 클라이언트로부터 받은 데이터를 DB에 저장
        - DB로부터 가져온 데이터로 운동에 필요한 칼로리 계산(소모 칼로리)
        - DB로부터 가져온 데이터로 식단으로 얻게 되는 칼로리 계산(사용 가능 칼로리)
        - 영양 성분 계산
        - 사용자의 체중과 운동량, 영양 섭취 및 성분 균형 등을 고려한 계산 로직
    - ERD (개발 전)  
  
      <img src="https://github.com/giteraction/workout/assets/95407727/c87407e7-5e69-44dd-8b8d-599e61d43839" style="width:500px;">  
        
    - ERD (개발 후)  
        - USER 테이블 > 사용자의 체중, 운동 방향 및 빈도 컬럼으로 변경
        - FOOD 테이블 > 음식의 영양 성분을 담아둘 NUTRIENT 테이블 추가 (칼로리 및 단백질 계산을 위해)
        - EXERCISE 테이블 > 운동 종목 리스트 BODYBUILD 테이블 추가 (서버에서 전달하게끔 변경)
    
    <img src="https://github.com/giteraction/workout/assets/95407727/f48236e0-978a-4979-a12b-00cbb15d2396" style="width:500px;">  

---

### **<개발물 구성>**

1. 전체 구조 및 동작 시나리오 구상

<img src="https://github.com/giteraction/workout/assets/95407727/975900cf-0852-4b90-8b65-ec9fa2c3b9bb" style="width:500px;">
---

1. 인터페이스 디자인
<img src="https://github.com/giteraction/workout/assets/95407727/bbb66228-e0bd-4f74-a3d3-fa038222ce9b" style="width:500px;">

---

1. 서버 연동 및 테스트 
<img src="https://github.com/giteraction/workout/assets/95407727/ba4d5687-dfb6-4c11-8b04-f96f16628a82" style="width:500px;">
---

### <개발 과정 중 마일스톤 리스트>
<img src="https://github.com/giteraction/workout/assets/95407727/d09fa097-45b4-4e8e-85b6-2a39d6a38f78" style="width:500px;">


---

### <최종 완성>

- 사용자 설정
<img src="https://github.com/giteraction/workout/assets/95407727/0d401804-49ab-4b3b-a55f-4b518f6cec92" alt="사용자 설정" style="width:500px;">

- 운동 기록 저장
<img src="https://github.com/giteraction/workout/assets/95407727/47bdf292-ee82-464a-8a62-5282cd4e2707" alt="운동 기록 저장" style="width:500px;">

- 운동 기록보기
<img src="https://github.com/giteraction/workout/assets/95407727/730f000b-0799-4532-bffd-c7353de649a2" alt="운동 기록 보기" style="width:500px;">

- 새로운 운동 추가
<img src="https://github.com/giteraction/workout/assets/95407727/8b3b0263-67d4-48b5-877d-dac9fd25cc39" alt="새로운 운동 추가" style="width:500px;">

- 음식 기록 저장
<img src="https://github.com/giteraction/workout/assets/95407727/29f792c6-19f4-48f4-85f9-17b87b5b9041" alt="음식 기록 저장" style="width:500px;">

- 새로운 음식 추가
<img src="https://github.com/giteraction/workout/assets/95407727/ebc32e61-a7b7-4d20-bd9e-bf84fbe2bbfc" alt="새로운 음식 추가" style="width:500px;">

- 식단 기록 보기
<img src="https://github.com/giteraction/workout/assets/95407727/10dccb55-1a18-4360-b9b6-cd920a26145f" alt="식단 기록 보기" style="width:500px;">


---

### <후기>

코딩이 아직 서툴러서 시행착오가 있었지만 하나의 프로젝트를 완수하였음에 뿌듯함을 느낍니다.

데이터를 매차례 손으로 타이핑하다가 자동 처리되는 통쾌함이 그간의 어려움을 잊게해주는 것 같습니다.

GPT를 사용하여 뼈대 코드를 만들어 이어 붙이고 일부는 직접 손봐주는 것이 필요하였습니다. 

개발 과정 속에 어려움이 있었지만 결국 ‘구체적인 목표 아래 세분화된 요구사항 분배’ 있었기에 완성을 할 수 있었던 것 같습니다.

기능 체크를 하면서 기능에 연계되는 ‘이런 기능이 있으면 좋겠다’ 싶었고 

그것들을 구현하며 자연스레 결과물에 살을 붙일 수 있었던 점이 좋았습니다.

봐주셔서 감사합니다.
