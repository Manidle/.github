# ✈️PlanerGram

 <br/>

## **00. 팀원 명단**

<br/>

-   **[김동현](https://github.com/soulchicken)** 
-   **[김영광](https://github.com/95Glory)** 
-   **[김도현](https://github.com/thovy)** 
-   **[이세운](https://github.com/Yiseun)** 

<br/>

## **00. 기술 스택**

<br/>
<img src="https://img.shields.io/badge/REACT-61DAFB?style=flat&logo=react&logoColor=black"/> <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=JavaScript&logoColor=black"/>  <img src="https://img.shields.io/badge/JAVA-83B81A?style=flat&logo=java&logoColor=white"/> <img src="https://img.shields.io/badge/Gradle-02303A?style=flat&logo=Gradle&logoColor=white"/> <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat&logo=Spring Boot&logoColor=white"/> <img src="https://img.shields.io/badge/Spring_Security-6DB33F?style=flat&logo=Spring Security&logoColor=white"/>
<img src="https://img.shields.io/badge/JSON_Web_Tokens-000000?style=flat&logo=JSON Web Tokens&logoColor=white"/> <img src="https://img.shields.io/badge/MariaDB-003545?style=flat&logo=mariadb&logoColor=white"/> <img src="https://img.shields.io/badge/Agile-EF2D5E?style=flat&logo=a-frame&logoColor=white"/> <img src="https://img.shields.io/badge/Figma-F24E1E?style=flat&logo=figma&logoColor=white"/> <img src="https://img.shields.io/badge/GIT-F05032?style=flat&logo=Git&logoColor=white"/> <img src="https://img.shields.io/badge/GitHub-181717?style=flat&logo=GitHub&logoColor=white"/> <img src="https://img.shields.io/badge/Notion-000000?style=flat&logo=Notion&logoColor=white"/> <img src="https://img.shields.io/badge/Docker-2496ED?style=flat&logo=Docker&logoColor=white"/> <img src="https://img.shields.io/badge/EC2-FF9900?style=flat&logo=Amazon EC2&logoColor=black"/> <img src="https://img.shields.io/badge/MUI-007FFF?style=flat&logo=MUI&logoColor=white"/>




<br/>

## **00. 협업방식**  
1. 애자일 프로세스  
    * check in / check out ground Role 방식을 통한 멤버별 하루 과업량, 출/퇴근시간, 회고 등을 기록.
    * BackLog를 작성하여 프로젝트 총 소요 StoryPoint를 집계하여 개발 계획관리를 진행.
    * Sprint 작성하여 주 개발일정관리 진행.

2. GitHub
    * Git을 활용한 코드 형상관리.
    * 이슈Tab을 활용하여 팀원들간의 기술공유 및 Exception 공유.
    * Project Tab을 활용하여 BackLog, Sprint 틀 활용.

3. Notion
    * 주간 현황파악을 간단하게 볼 수 있는 주간현황 자료공유
    * API명세서틑 통한 BackEnd / FrontEnd 개발자들과의 컨벤션 공유

4. Figma
    * 초기 화면단 WireFrame 작성당시 멤버들과의 화면단 구축 협업작업.


## **00. 프로젝트 주제**  

### **PlannerGram**

<br/>

## **00. 도메인 관련 용어**

- **👨 유저(User)** : 유저 어쩌고

## **00. 기능 명세**
[API DOCS](https://documenter.getpostman.com/view/21185842/UzBsHjMc) - PostMan API Documents

### 유저 관련기능
- 어쩌고 기능

## **00. ERD (Entity Relationship Diagram)**
 ![image](https://user-images.githubusercontent.com/85923524/175849491-49e9314f-71e7-43ea-aa76-f71a7243886d.png)

<br/>


### **Patient** 테이블
| column          | data type   | 설명            |
| --------------- | ----------- | --------------- |
| people_id (PK)  | LONG        | 고유 인덱스     |
| people_name     | VARCHAR(45) | 환자 이름       |
| people_gender   | TINYINT     | 환자 성별       |
| people_home     | VARCHAR(45) | 환자 주소       |
| people_phone    | INT         | 환자 전화번호   |
| people_isdanger | TINYINT     | 환자 위험군여부 |
 
-  환자 정보가 저장된다.
-  환자 정보의 매니저 정보가 없으면 등록 안된다.

<br/>

### **Manager** 테이블                                  
| column          | data type   | 설명                |
| --------------- | ----------- | ------------------- |
| manager_id (PK) | LONG        | 고유 인덱스         |
| manager_name    | VARCHAR(45) | 환자관리자 이름     |
| manager_phone   | VARCHAR(45) | 환자관리자 전화번호 |

- 매니저 정보가 저장된다.

<br/>

### **Hospital** 테이블                                  
| column               | data type   | 설명              |
| -------------------- | ----------- | ----------------- |
| hosipital_id (PK)    | LONG        | 고유 인덱스       |
| hosipital_name       | VARCHAR(45) | 병원 이름         |
| hosipital_patientnum | INT         | 병원 내 환자 수   |
| hosipital_roomlimit  | INT         | 병원 내 남은 병실 |

- 병원 정보가 저장된다.
- 환자들의 정보를 가지고 있다.

<br/>

### **Hospitalroom** 테이블                                  
| column                        | data type | 설명           |
| ----------------------------- | --------- | -------------- |
| hosipitalroom_roomnumber (PK) | LONG      | 고유 인덱스    |
| hosipitalroom_capacity        | LONG      | 병실 수용 인원 |

- 병실 정보가 저장된다.
- 병원 정보를 가지고 있다.
- 고위험군 환자들의 정보를 가지고 있다.

<br/>

### **Infectiontracking** 테이블                                  
| column                    | data type   | 설명              |
| ------------------------- | ----------- | ----------------- |
| infectiontracking_id (PK) | LONG        | 고유 인덱스       |
| infectiontracking_area    | VARCHAR(45) | 감염경로 방문지역 |
| infectiontracking_cause   | VARCHAR(45) | 감염경로 방문이유 |
| infectiontracking_date    | LOCALDATE   | 감염경로 방문날짜 |
- 감염환자 동선 및 장소 정보가 저장된다.
- 환자의 정보를 가지고 있다.

<br/>


### **Self_qurantine** 테이블                                  
| column                      | data type   | 설명             |
| --------------------------- | ----------- | ---------------- |
| self_qurantine_id (PK)      | LONG        | 고유 인덱스      |
| self_quarantine_people_name | VARCHAR(45) | 자가격리자 이름  |
| self_quarantine_date        | LOCALDATE   | 자가 격리 시작일 |
| self_quarantine_release     | LOCALDATE   | 자가 격리 해제일 |
- 자가격리자의 격리기간 정보가 저장된다.
- 환자의 정보를 가지고 있다.

<br/>

### **danger** 테이블                                  
| column              | data type | 설명                    |
| ------------------- | --------- | ----------------------- |
| danger_id (PK)      | LONG      | 고유 인덱스             |
| danger_care_date    | LOCALDATE | 고위험 환자 치료 시작일 |
| danger_care_release | LOCALDATE | 고위험 환자 치료 중단일 |

- 고위험군 환자의 격리기간 정보가 저장된다.
- 병실의 정보를 가지고 있다.
- 환자의 정보를 가지고 있다.

<br/>

## **00. 트러블 슈팅**
1. 무한 루프 : 테이블들을 서로 매핑해주는 과정에서 Entity를 return했을 때 객체 안에 다른 Entity를 return해주는 무한 순환 참조가 발생됨. **DTO패턴** 을 사용하여 Entity를 직접 참조하지 않고도 return할 수 있게 코드를 변경하여 무한 루프를 해결.   
2. 타입 에러 : 내장함수를 사용할때 타입이 불일치하여 사용 못하는 문재 발생하여
**.orElseThrow(Exception::new)** 을 사용하여 해결.   
3. 에러 관리 : 에러발생시 출력되는 에러문을 정확히 이해하지 못하는 현상 발생하여 **log**문을 따로 출력하여 에러문을 보기쉽게 관리 및 통제   
4. 인스턴스 서버 연결 : 각자의 로컬 서버로 데이터베이스를 관리하는 부분에서 서로 필요한 부분에 데이터가 안 들어가거나 테이블이 미완성 되는 문제를 해결하고자 하나의 인스턴스 서버로 하나의 데이터베이스를 여러 사용자가 이용을 하여 테이블의 부재를 방지.

<br/>

## **00. 느낀점**
- **👨김동현** : 

<br/>

- **👨김도현** : 
<br/>

- **👨이세운** : 
<br/>

- **👨김영광** : 프

<br/>

## **00. 참고 자료** 
- [커밋 컨벤션 DOCS](https://udacity.github.io/git-styleguide/)
- [커밋 컨벤션 정리자료](https://overcome-the-limits.tistory.com/entry/%ED%98%91%EC%97%85-%ED%98%91%EC%97%85%EC%9D%84-%EC%9C%84%ED%95%9C-%EA%B8%B0%EB%B3%B8%EC%A0%81%EC%9D%B8-git-%EC%BB%A4%EB%B0%8B%EC%BB%A8%EB%B2%A4%EC%85%98-%EC%84%A4%EC%A0%95%ED%95%98%EA%B8%B0)
- [자바 컨벤션 DOCS](https://naver.github.io/hackday-conventions-java/)
- https://www.youtube.com/c/%EB%A9%94%ED%83%80%EC%BD%94%EB%94%A9
