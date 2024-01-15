## 💳 CARD SERVICE (카드 실적 분석 시스템)

이 프로젝트는 KB IT's Your Life 4기 미니 프로젝트로 개발된 간단한 Java 기반의 카드 실적 분석 시스템입니다. 사용자가 다양한 회사의 각 카드로 결제를 하면 해당 지출 내역을 기반으로 간단한 분석을 수행하고 사용자에게 보여줍니다.


## 🗓️ PERIOD
2023년 8월 3일 ~ 8월 4일 (2일간)


## 🤝 Member
- 강유석 (https://github.com/kangyuseok)
- 강태섭(https://github.com/KSEOP)
- 박서희 (https://github.com/seohee99)
- 조원형 (https://github.com/JoWonHyeung)

  
## ⚙️ STACKS

### ✔️ Environment 
![Eclipse IDE](https://img.shields.io/badge/Eclipse%20IDE-2C2255.svg?&style=for-the-badge&logo=Eclipse%20IDE&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032.svg?&style=for-the-badge&logo=Git&logoColor=white)
![GitHub](https://img.shields.io/badge/github-181717?style=for-the-badge&logo=github&logoColor=white)

### ✔️ Development
![Java](https://img.shields.io/badge/JAVA-007396?style=for-the-badge&logo=java&logoColor=white)

### ✔️ Database
![Oracle](https://img.shields.io/badge/Oracle-F80000.svg?&style=for-the-badge&logo=Oracle&logoColor=white)

### ✔️ Communication
![Notion](https://img.shields.io/badge/Notion-181717.svg?&style=for-the-badge&logo=Notion&logoColor=white)


## 🔧주요 기능 

- 카드 및 회원 관리:
  - 카드 정보 등록, 조회, 수정, 삭제 (CRUD)
  - 회원 정보 등록, 조회, 수정, 삭제 (CRUD)

- 결제 기능:
  - 카드 결제 시 사용 내역 저장

- 소비 이력 관리:
  - 소비 이력 조회

- 분석 기능:
  - 기간별 소비 분석
  - 카테고리별 소비 분석
  - 총 합계 계산
  - 회원 등급 확인

    
## 작업 내용

- ✔️작업 방식
  - 모든 팀원이 전체 구조를 정확히 파악한 뒤 구현하는 것을 목표로 하여 설계는 회의를 통해 함께 진행하되, 기능은 나누어 진행
    
- ✔️역할
  - 강유석 — CRUD 기능
  - 강태섭 — 데이터 관련 작업
  - 박서희 — 결제 기능, 회원 등급 기능
  - 조원형 — 조회 기능, 분석관련 기능 

- ✔️변경사항
<table>
<tbody>
  <tr>
    <th>변경 항목</th>
    <th>기존 내용</th>
    <th>문제 확인</th>
    <th>변경 내용</th>
  </tr>
  <tr>
    <th>DB modeling</th>
    <td>회사이름(pk), 주소를 가진 Company 존재</td>
    <td>Company 클래스, DB의 존재 의미와 역할 상실 확인</td>
    <td>Company 클래스 및 테이블 제거</td>
  </tr>
  <tr>
    <th>JAVA - Class MyDate</th>
    <td>Mydata 클래스 제작 및 활용
(YYYY/MM/DD)</td>
    <td>오라클 insert 시 데이터 타입 오류 발생.</td>
    <td>- 컨벤셔널하고 안전한 Java - Oracle 데이터타입 호환 형태 조사 후 MyData 클래스 제거. <br>
    - String ‘YYYY-MM-DD’ 으로 다룬 후 ValueOfDate() 
으로 변환하는 로직 구현</td>
  </tr>
  <tr>
    <th>JAVA - isExist()</th>
    <td>- 기존 customer의 ssn 유무를 확인하는 isExist만 있었음 <br>
- getCustSsn() 을 인자로 받아 확인함.</td>
    <td>중복 되는 카드 번호 등록 SQL 쿼리 오류 발생.</td>
    <td>isExist(//)는 cust 또는 card 객체 인자를 받는(오버로딩) 형태로 변경됨. </td>
  </tr>
  <tr>
    <th>알고리즘</th>
    <td>특정 금액(10만원) 이상 금액 소비 검색 시 이분탐색 적용 계획</td>
    <td>이분탐색의 기능과 필터의 목적이 부합하지 않음</td>
    <td>버블정렬을 이용해 필터된 검색결과 출력하는 것으로 변경 </td>
  </tr>
  <tr>
    <th>JAVA - Identifier</th>
    <td>RegisterDAO</td>
    <td>카드 및 회원정보 수정 기능을 갖고 있으나 불명확한 identifier</td>
    <td>InfoHandlerDAO로 변경</td>
  </tr>
  </tbody>
</table>

## 📄산출물

<table>
  <tbody>
    <tr>
      <td align="center"><img src= "https://github.com/KB-MiniProject/Card_Service/assets/53520867/4266cc07-63b7-44d2-b3bb-262a973edaf1" width=500px;" alt=""/><br /><sub><b> Usecase Diagram </b></sub><br /></td>
      <td align="center"><img src= "https://github.com/KB-MiniProject/Card_Service/assets/53520867/009da63e-717c-4278-afed-87b0955a744e" width=500px;" alt=""/><br /><sub><b> Front UI </b></sub><br /></td>
    </tr>
    <tr>
      <td align="center"><img src= "https://github.com/KB-MiniProject/Card_Service/assets/53520867/ffe21c90-8011-4e35-9fa5-1be5aa1350fd" width=500px; alt=""/><br/><sub><b> Class Diagram </b></sub><br/></td>
      <td align="center"><img src= "https://github.com/KB-MiniProject/Card_Service/assets/53520867/3f80baaa-744f-435b-a834-0a965157d802" width=500px;" alt=""/><br /><sub><b> DB Modeling </b></sub><br/></td>
    </tr>
  </tbody>
</table>

## 📂전체 구조
<pre>
📦src
 ┣ 📂com
 ┃ ┣ 📂card
 ┃ ┃ ┣ 📂algorithm
 ┃ ┃ ┃ ┗ 📂test
 ┃ ┃ ┃ ┃ ┗ 📜AlgorithmTest.java
 ┃ ┃ ┣ 📂dao
 ┃ ┃ ┃ ┣ 📂impl
 ┃ ┃ ┃ ┃ ┣ 📜InfoHandlerDAOImpl.java
 ┃ ┃ ┃ ┃ ┗ 📜ServiceDAOImpl.java
 ┃ ┃ ┃ ┣ 📜InfoHandlerDAO.java
 ┃ ┃ ┃ ┗ 📜ServiceDAO.java
 ┃ ┃ ┣ 📂exception
 ┃ ┃ ┃ ┣ 📜DuplicateSSNException.java
 ┃ ┃ ┃ ┣ 📜InvalidTransactionException.java
 ┃ ┃ ┃ ┗ 📜RecordNotFoundException.java
 ┃ ┃ ┣ 📂test
 ┃ ┃ ┃ ┗ 📜Test.java
 ┃ ┃ ┣ 📂util
 ┃ ┃ ┃ ┗ 📜MyDate.java
 ┃ ┃ ┣ 📂vo
 ┃ ┃ ┃ ┣ 📜Card.java
 ┃ ┃ ┃ ┣ 📜Company.java
 ┃ ┃ ┃ ┣ 📜Cust.java
 ┃ ┃ ┗ ┗ 📜Purchase.java
 ┣ 📂config
 ┃ ┣ 📜.gitignore
 ┗ ┗ 📜ServerInfo.java
</pre>
