# 🚀 Crew Station

> 본 서비스는 여행자들이 연결되는 소셜 여행 플랫폼
> 여행 동행 모집, 지역 상품 판매, 여행 일기 작성을 한 곳에서 제공합니다.
> 여행자 간 교류와 거래가 이루어지는 통합 여행 플랫폼입니다.
> 함께 여행하고, 사고팔고, 기록하는 새로운 여행 경험을 만듭니다.

---

## 🎯 기획 의도

<img width="893" height="491" alt="Image" src="https://github.com/user-attachments/assets/62bbc22b-547c-4f73-9385-987955c1642c" />

<img width="892" height="497" alt="Image" src="https://github.com/user-attachments/assets/2e785061-087a-4c09-8021-0be51391ba9b" />

본 프로젝트는 청년층의 **사회적 고립 문제**와 **연대 부족**을 해결하고자 기획되었습니다.

주요 기획 배경은 다음과 같습니다:

1. **사회적 고립 완화**  
   청년들이 혼자 경험하는 여행이나 활동에서 **새로운 인간관계를 형성할 기회가 부족**하다는 문제를 발견했습니다.

2. **경제적 제약 완화**  
   청년들이 해외여행 등 다양한 경험을 하고 싶어도 **비용 부담으로 기회가 제한**되는 현실을 확인했습니다.

3. **안전하고 책임 있는 만남 필요**  
   기존의 여행 동행 방식에서는 **안전성과 신뢰성 부족**으로 범죄나 사고 위험이 존재한다는 점이 문제였습니다.

이에 따라, **안전한 플랫폼을 통해 청년들이 여행을 함께하고, 사회적 연결망을 확장할 수 있는 서비스**를 기획하게 되었습니다.

---

## 💡 기대 효과

<img width="1395" height="736" alt="Image" src="https://github.com/user-attachments/assets/66048866-0050-4afd-952b-4d2286b807b0" />

1. **경제적 부담 완화와 기회 형평성 제고**

    - 우리 서비스의 **크루원 모집 기능**을 통해 여행이나 활동 비용을 분담할 수 있어,  
      경제적 제약이 있는 청년도 다양한 경험을 누릴 수 있습니다.

2. **창업적 감각 함양**

    - 사용자가 해외에서 구한 상품을 **기프트에 올려 사고팔기**를 경험함으로써  
      소규모 비즈니스 운영 및 거래 경험을 쌓을 수 있습니다.

3. **콘텐츠 기반 성장**

    - **여행 다이어리 기록 공유**를 통해 개인 경험을 기록하고,  
      다른 사용자와 소통하며 **콘텐츠 기반의 성장 및 학습**이 가능합니다.

4. **심리적 안정감 제공**
    - 크루와 함께 활동하며 **역할을 수행하고 협력**함으로써  
      정서적 지지와 **심리적 안정감**을 얻을 수 있습니다.

---

## 🧰 프로젝트 사용 툴

-   **HTML Engine:** Thymeleaf
-   **Frontend:** Html, JavaScript, CSS
-   **Backend:** Spring Boot, Java
-   **Database:** PostgreSQL, Redis
-   **Infra:** AWS EC2, AWS IAM, AWS S3
-   **Tool:** VsCode, IntelliJ IDEA
-   **API:** Kakao Login, Kakao Map, Kakao 주소, SMTP Gmail API,REST API, Lombok, MyBatis, OAuth 2.0, Google Login, Boot Pay, Naver Login, JWT, Spring Security, CoolSMS, Swagger UI
-   **기타:** Git, GitHub, Slack, Postman, Sourcetree
-   **테스트:** JUnit5

---

## 🗂 ERD (Entity Relationship Diagram)

<img width="6222" height="6184" alt="Image" src="https://github.com/user-attachments/assets/6e275336-0946-4425-aae2-ccca73d4c320" />



## 👩‍💻 담당 업무

<img width="1629" height="327" alt="스크린샷 2025-11-03 오전 1 48 56" src="https://github.com/user-attachments/assets/d6812492-2581-46c3-8cd1-a8dac0e0a936" />


<br>▶ 메인페이지

-   메인 목록
-   헤더 (모바일, 웹)
-   푸터 (모바일, 웹)
-   알림

▶ 전체검색

- 통합검색

▶ 관리자

- 로그인
- 관리자 등록
- 관리자 메인
- 회원관리
- 회원관리 상세
- 크루동행 신고 목록
- 크루동행 신고 상세
- 공지사항 목록
- 공지사항 상세
- 공지사항 작성
- 배너관리
- 문의 목록
- 문의 상세/답변
- 결제관리
- 결제관리 상세


<br>

## 📊 QA 테스트

<img width="836" height="718" alt="스크린샷 2025-11-03 오전 1 32 43" src="https://github.com/user-attachments/assets/cdbc9612-701e-44bf-ae8f-78e851b76e43" />



## 🚨 오류 상황들

💥문제 상황

Caused by: java.lang.NullPointerException: Cannot invoke "String.hashCode()" because "" is null
at org.mybatis.spring.MyBatisSystemException:
### Error querying database.
Cause: java.lang.NullPointerException: Cannot invoke "String.hashCode()" because "" is null
### The error may exist in com/example/crewstation/mapper/member/MemberMapper.xml
### The error may involve com.example.crewstation.mapper.member.MemberMapper.findAdminMembers
### Cause: java.lang.NullPointerException: Cannot invoke "String.hashCode()" because "" is null


🔍 문제 원인
- DB에 저장된 member_gender 컬럼 값이 빈문자열('') 이라서 Enum(Gender) 매핑 과정에서 Enum.valueOf("")로 들어가서 목록이 안불러와지는 문제 발생
- DB값이 enum 정의에 없는 문자열이라서 NullPointerException이 발생

🛠️ 해결 방안
- 관리자 회원가입 시 gender가 비어 있을 경우 기본값을 넣도록 수정
<img width="1013" height="504" alt="스크린샷 2025-11-03 오후 7 38 14" src="https://github.com/user-attachments/assets/b95e8a39-73fd-4a43-a8df-843b690679d1" />








