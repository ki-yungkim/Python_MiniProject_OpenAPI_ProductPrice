# Python_2nd_Mini_OpenAPI
 
## 작성일 : 210930
## 김기영

 
## 활용 API https://www.data.go.kr/data/3043385/openapi.do

## 팀명 : 3팀 
## 팀원 : 김기영 김현진 박민재 한다예 
## 팀장 : 김기영 

## 주제 : 생필품 가격정보 
## 일정 : 210916 ~ 210929 (16, 17, 27, 28, 29 - 5일간)

## 사용 가능한 오퍼레이션 
    - 1. 상품정보 조회
    - 2. 판매점 정보 조회
    - 3. 생필품 가격정보 조회
    - 4. 생필품 가격 정보 기준 데이터 조회
    
## 구현 계획 중인 기능
- 공통 연구 주제 : 주소 활용 방안 탐색

- 1. 코드로 되어있는 것들 값 가져와서 출력 (4번 기능 값 이용)
- 2. 상품 분류별 정보(통계, 가격 변동률 등)
- 3. 판매점 이름으로 정보 검색 
- 4. 상품 가격 변동 그래프
- 5. 상품 가격 최고, 최소, 평균 출력
- 6. 상품 원플러스원 판매점 검색
- 7. 상품 할인 판매점 검색
- 8. 지역별 업체수
- 9. 목록에서 검색 기능
- 10. 할인 빈도 (할인 Y 갯수로)  
- 11. 원플러스원 빈도 (1+1 Y 갯수로)
- 12. 업태별 최저가 목록


## 진행 상황


### 210916
### 210917

### 210922
- getStandardInfoSvc를 standard_models.py 이름으로 정보 가져오기 성공
    - models/standard_models.py
    - templates/standard/ 이하 네개 .py 파일
    - route의 64번째 줄부터 getUT, getAL, getBU, getAR

- 1번 미션 진행 중   
- 생필품 목록 페이지에 코드로 되어있는 것들 기준 데이터 가져와서 알아볼 수 있는 형태의 데이터로 변환 완료
    - templates/product/goodList 수정 적용 (/product/goodInfoAll.html) 
    - 현재 상태 업로드 : 210922_김기영_생필품 목록 코드형 데이터 변환 처리.png

### 210923
- 코드로 되어있는 데이터들 처리 완료 (미션 1번)
- 날짜 입력 부분 달력 타입으로 변경
- 상품 아이디, 판매점 아이디와 날짜로 가격 검색하는 부분 이름으로 검색하는 기능 추가

- 상품 이름으로 검색하여 특정 날짜의 가격 평균, 최대, 최소 값 출력 기능 구현
- 상품 이름과 기준일, 비교일 입력하여 평균 가격, 최고값, 최저값 변동률 계산 기능 구현

### 210924
- 목록에서 검색 기능 기존 파일에 통합 
- 날짜 두개 입력하여 두 날짜 사이 기간 동안 가격 변동 출력 기능  
- 기존 최저가, 최고가 데이터에 해당하는 업체 내용 출력
- 날짜 두개 입력하여 가격 변동 출력하는 기능 활용 그래프 출력 기능

- 김기영 : 1, 2 완료, 12은 보류 
- 박민재 : 9 거의 완료, 5 기본 기능은 완료

## 진행 계획
- 김기영 : 추가 통계 데이터 구상 
- 박민재 : 9번 마무리, 4번을 2번 코드 참고하여 진행, 5번 최고값 최저값 판매점 정보 출력 기능 추가, 지역별 최저값 출력 기능 추가 
- 김현진 : 8번부터 진행
- 한다예 : 주말에 개별 미팅 

### 210927
# 3일차 진행
## 오전  
- 김현진 : 8.지역별 업체수, 지역 검색해서 업체 정보 출력
- 김기영 : 
    - 지역별 업체 수, 지역 검색하여 업체 정보 출력 기능 프로젝트에 병합
    - pie 그래프 그리는 방법과 그래프에서 한글 깨지지 않게 적용하는 방법 정립
    - 상품 할인 판매점 검색
- 한다예 : 판매점 이름으로 정보 검색
- 박민재 : matplotlib 기능 탐색

## 오후
- 주별 최저가 최고가 평균가 그래프 디자인
- 지역별 업체 수 파이 그래프 디자인 디자인
- 기능 정리 

# 완성한 기능

1. 상품 목록 조회
2. 상품 이름으로 검색
3. 판매점 목록 조회
4. 판매점 이름으로 검색
5. 판매점 주소로 검색
6. 판매점 지역별 업체 수 목록, 그래프 
7. 상품 이름과 날짜로 가격 검색
8. 상품 이름과 날짜로 할인 판매점 및 가격 검색
9. 상품 이름과 날짜로 해당 날짜의 평균가, 최고가, 최저가 검색
10. 두 날짜의 상품 가격 평균, 최고, 최저가 변동률
11. 기간(2달)내 가격 변동표, 그래프
12. 판매점 이름과 날짜로 가격 검색 

# 4일차 진행 예정 내용 
- 페이지 레이아웃 구성 
- 디자인 
### 210928
# 4일차 진행
## 오전 
### 디자인 아이디어, 적용
- 한다예 : 구글 스타일 센터 로고 + 상품 이름으로 검색창, 검색한 상품의 가격 변동 그래프 나올 수 있는지, 로고 디자인 편집
- 박민재 : Home 버튼 왼쪽으로, 조각페이지, 센터로 정렬 
- 김현진 : 테이블 정렬, 상세 주소 합치기, 로고 선정
- 김기영 : 부트스트랩 기본 구조 정립

- 기능 통합, 정리 완료, 디자인 완성 단계 
- 추가로 해보고 싶은 기능, 디자인 각자 진행 예정 
- 에러 처리 진행 예정

## 오후
- 김기영 : 화면정의서, 일정표 작성
- 한다예 : 발표 자료 작성
- 박민재 : 클래스, 액터 다이어그램 작성
- 김현진 : 디자인 점검 및 수정 
### 210929
# 5일차 진행
## 오전  
- 한다예 : 발표 자료에 업무분담 파트, 흐름도 추가
 
- 박민재, 김기영 : 시연용 데이터 정리 (날짜, 판매점, 상품 이름 등)  
              에러 캐치 -> 기존 버전은 백업하고 진행  
  
- 김현진 : 조각페이지 사용 방법 탐색 
    -> {% include 조각페이지.html %} 
    -> 페이지에 따라서 active 단어 위치가 바뀌게 
    
## 김기영 에러 발생 : DNS 에러 -> 공공 데이터 사이트가 안 들어가짐 

# 에러 처리 
## 메인페이지 
### 상품 이름으로 검색
- 없는 이름 입력시 빈 테이블 출력
- 날짜 입력하지 않을 시 빈 테이블 출력

# 시연용 데이터 정리 

# 참고문헌 
https://matplotlib.org/stable/index.html
https://ehclub.net/677
https://zephyrus1111.tistory.com/36
https://truman.tistory.com/103
https://wikidocs.net/141547
https://www.price.go.kr/tprice/portal/main/main.do

### 210929 
- 프로젝트 완성

### 210930 
- 프로젝트 발표