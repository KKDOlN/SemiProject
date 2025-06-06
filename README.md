# SemiProject

# 요리 레시피 추천 사이트
![Image](https://github.com/user-attachments/assets/df3175f3-8ee2-4eea-9679-c8249d6695a5)
----------------------------------------------------
# 냉장고 속 재료 기반 맞춤형 레시피 제공
## 팀 프로젝트 소개
![프로젝트소개](https://github.com/user-attachments/assets/8b0bc40c-2505-4432-9268-5de467d17d64)
## 역할 분담
![역할분담](https://github.com/user-attachments/assets/ad960004-05c1-447a-973d-953805e883dd)
## 차별성
![차별성](https://github.com/user-attachments/assets/067ad8df-2ff8-4ddc-b152-36a5a9c2471c)

## 프로젝트 개발환경
- DB : Oracle 11g xe 버전 이용
- Intellij IDEA 이용
  
## 프로젝트 실행 환경 구축(로컬)
1. 오라클 11g 설치 및 application.properties의
```properties
# Oracle Connection Setting
spring.datasource.driver-class-name=oracle.jdbc.driver.OracleDriver
spring.datasource.url=jdbc:oracle:thin:@localhost:1521:xe
spring.datasource.username
spring.datasource.password
```
를 참고하여 로컬에 db 계정 생성
계정 생성 후 권한 부여 및 테이블 생성
테이블, 시퀀스 생성 및 데이터 삽입 스크립트

[ADD] db 스크립트 추가
- [A.ONEYO.sql](https://drive.google.com/file/d/1cSPpFyTk-KAC-y55RQNaak4GEStNA7by/view?usp=sharing)
  
# 1. 기술스택
![Oracle](https://img.shields.io/badge/Oracle-F80000?style=for-the-badge&logo=oracle&logoColor=white)
![java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white)<br>
![html5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white)
![java  Script](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)<br>
![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)
![Eclipse](https://img.shields.io/badge/Eclipse-FE7A16.svg?style=for-the-badge&logo=Eclipse&logoColor=white)
![Apache Tomcat](https://img.shields.io/badge/apache%20tomcat-%23F8DC75.svg?style=for-the-badge&logo=apache-tomcat&logoColor=black)

# 2. 프로젝트 구조
[프로젝트.PDF](https://drive.google.com/file/d/1arzy92_JuM-9a01Ubx2IDwtzkzLpSCXK/view?usp=sharing)

# 3. 프로젝트 후기
프로젝트에서 저는 레시피 등록, 수정, 검색, 그리고 회원과 비회원에 따른 레시피 추천 기능을 구현했습니다. 특히, 최소 1개 이상의 주재료 선택, 첨부파일 관리, 작성자별 검색 및 조회순 정렬 등 다양한 기능을 세밀하게 개발하며 백엔드 로직과 데이터베이스 연동 역량을 크게 향상시킬 수 있었습니다. 또한, 회원 마이냉장고 재료 기반 맞춤 추천 기능을 구현하면서 사용자 맞춤형 서비스 설계 경험도 쌓았습니다. 프로젝트 진행 과정에서 우선순위 설정과 팀원 간 원활한 소통의 중요성을 절실히 깨달았습니다. 문제 상황에서 적극적으로 의견을 교환하며 협력하는 과정이 개인 역량뿐 아니라 팀 전체 성과에 큰 영향을 미친다는 것을 느꼈습니다. 부족한 부분을 인지하고 개선하기 위해 꾸준히 노력할 수 있었으며, 어려운 부분을 도움 주신 팀원과 강사님께 깊이 감사드립니다. 향후에는 추천 알고리즘을 더욱 정교하게 개선하고, 사용자 경험을 높이기 위한 UI/UX 협업 역량을 강화하는 데 중점을 두겠습니다. 또한, 코드 리팩토링과 테스트 자동화를 통해 안정성과 유지보수성을 높이고자 합니다.

# 4. 주요기능 
### 레시피 
|기능명|상세|
|--|--|
|레시피 등록|관리자 또는 사용자가 레시피를 등록하는 페이지입니다. 최소 1개이상의 주재료를 선택해야하며, 부재료, 사진은 생략가능합니다. |
|레시피 수정| 자신이 작성한 레시피를 수정 합니다. 제목, 재료, 펌부파일, 내용을 수정가능합니다.|
|레시피 검색|레시피는 제목, 요리명, 작성자로 검색하고, 검색시엔 레시피들이 조회순으로 보여줍니다. 작성자로 검색 시 작성자의 레시피가 조회순으로 보여줍니다.|
|레시피 추천(비회원)|비회원은 메인페이지에 보여지는 추천 레시피 외에 자신의 재료로 레시피 추천 받는것이 불가하며, 레시피 검색만 가능합니다.|
|레시피 추천(회원)| 로그인한 회원의 경우 등록된 마이냉장고의 재료를 활용하여 만들 수 있는 레시피를 레시피 전체 리스트 조회시 추천받을수 있습니다|

# 5.화면 구현
### 레시피
### 비회원 로그인시 레시피 페이지
![recipeList.jsp](https://github.com/user-attachments/assets/8c709fb8-ea0c-4941-aeb8-f07d706b3fe2)
### 회원 로그인시 레시피 페이지
![recipeList.jsp](https://github.com/user-attachments/assets/8c709fb8-ea0c-4941-aeb8-f07d706b3fe2)
### 레시피 등록 페이지
![레시피 등록 페이지](https://github.com/user-attachments/assets/8615a2b0-4f7f-4870-90bb-9fc93b65c3ac)
### 레시피 목록 페이지
![recipeList.jsp](https://github.com/user-attachments/assets/267e770e-c232-4dc9-ae30-aa53650352d4)
### 레시피 상세 페이지
![레시피 상세 페이지](https://github.com/user-attachments/assets/1cca17db-d039-44c5-8da9-a616f7ceef12)
### 레시피 검색 페이지
![레시피 검색 페이지](https://github.com/user-attachments/assets/5747bf29-1b22-4d09-9495-d1a8534f45ed)


# 프로젝트 산출문서
- [기획보고서](https://drive.google.com/file/d/1Y3C14sBiMuAqhevhRxZlfjbmgGT4GhmF/view?usp=sharing)
- [요구사항정의서](https://drive.google.com/file/d/1RgoGpFdt7A6zdXNJZFLO3oyVxlTvvoMP/view?usp=sharing)
- [와이어프레임](https://drive.google.com/file/d/1drb5eNbOQtC9XqX8JaLTMBPpR8I4RiNi/view?usp=sharing)
- [DB설계](https://drive.google.com/file/d/1SE5tLfgGzGzj8OrBYAIF9nInZ62CDEUw/view?usp=sharing)
- [시퀀스 다이어그램](https://drive.google.com/file/d/1irW7kdzmYZ89WgiY9pEnN1GOeHFss63n/view?usp=sharing)
- [최종보고서](https://drive.google.com/file/d/15LTXkWCVk_EyxEJraH7CNYtN0ssnEkft/view?usp=sharing)
- [프로젝스 소스 DB](https://drive.google.com/file/d/1cSPpFyTk-KAC-y55RQNaak4GEStNA7by/view?usp=sharing)
- [시연영상](https://drive.google.com/file/d/1DTl3d_0OV_ZmpOyd2yzz-2jdzmypbnID/view?usp=sharing)
