# spring-gift-enhancement

<br/>

# 1단계 - 상품 카테코리

## 요구 사항 정의

상품과 카테고리 간의 관계를 고려하여 카테고리 추가

구현한 기능에 대해 테스트를 실시

### 상품 카테고리
- 1차 카테고리만 있으며 2차 카테고리는 고려하지 않음
- 카테고리는 수정 가능
- 카테고리 예시
    - 교환권, 상품권, 뷰티, 패션, 식품, 리빙/도서, 레저/스포츠, 아티스트/캐릭터, 유아동/반려, 디지털/가전, 카카오프렌즈, 트렌드 선물, 백화점
- Request
    ```
    GET /api/categories HTTP/1.1
    ```
- Response
    ```
    HTTP/1.1 200
    Content-Type: application/json

    [
        {
            "id": 91,
            "name": "교환권",
            "color": "#6c95d1",
            "imageUrl": "https://gift-s.kakaocdn.net/dn/gift/images/m640/dimm_theme.png",
            "description": ""
        }
    ]
    ```

### 상품
- 상품 정보에 카테고리를 추가
- 항상 하나의 카테고리가 있어야 함

### 관리자 화면
- 상품 추가에 카테고리 선택란 추가