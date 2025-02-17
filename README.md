# 🍽 회사 식단표 API 및 웹/모바일 앱 개발

## 📌 프로젝트 개요
회사의 식단표를 자동으로 크롤링하고, 이를 웹과 모바일 앱에서 확인할 수 있도록 하는 프로젝트입니다.  
현재 **FastAPI를 이용한 백엔드 개발이 완료**되었으며, 앞으로 **React 및 React Native를 활용한 프론트엔드 개발을 진행할 예정**입니다.

---

## 🏗 개발 진행 과정

### 1️⃣ FastAPI를 활용한 백엔드 개발 (완료 ✅)
- FastAPI를 이용하여 **회사 식단 데이터를 제공하는 API 개발**
- `BeautifulSoup`을 활용한 **웹 크롤링 기능** 구현
- **로컬 서버**에서 테스트 완료

### 2️⃣ API 엔드포인트 (현재 상태)
| 엔드포인트 | 설명 |
|-----------|------|
| `GET /` | API 상태 확인 |
| `GET /menu/week` | 이번 주 전체 메뉴 조회 |
| `GET /menu/day/{day}` | 특정 요일(월~금)의 메뉴 조회 |

🔹 **예제 요청 및 응답**  
`GET http://127.0.0.1:8000/menu/day/월`
```json
{
  "day": "월",
  "menu": {
    "한식": [
      "고기산적야채조림",
      "얼큰김치국",
      "들기름막국수",
      "아삭이고추양파무침",
      "깍두기/밥3종"
    ],
    "일품식": [
      "순살돈가스",
      "분모자떡볶이",
      "가쓰오장국",
      "열무김치/밥3종"
    ],
    "간편식": [
      "메뉴 중 1가지 선택",
      "1.수제샐러드",
      "2.떠먹는고구마케이크+견과류+음료1종",
      "3.치즈불고기버거+음료1종",
      "4.보틀선식set"
    ]
  }
}
