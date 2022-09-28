# ✈️PlannerGram

## **00. 팀명**
### 🏋️‍♂️Man I-dle🏋️‍♂️

4명의 남자들만 모여 다소 프로젝트가 **딱딱** 할 수는 있지만  
  
어느 팀 부럽지 않은 **뚝딱**이들이 모였습니다.  
  
열정과 배움에 대한 열의만큼은 남들에게 **떵떵** 거릴수 있는 **Man I-dle 입니다.**

## **01. 팀원 명단 & 역할**

<br/>

-   **[김동현](https://github.com/soulchicken)** [BackEnd / Security / Web Publisher]
-   **[김영광](https://github.com/95Glory)** [BackEnd / Security / Open API]
-   **[김도현](https://github.com/thovy)**  [FrontEnd ]
-   **[이세운](https://github.com/Yiseun)** [DevOps]

<br/>

## **02. 기술 스택**

<br/>
<img src="https://img.shields.io/badge/REACT-61DAFB?style=flat&logo=react&logoColor=black"/> <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=JavaScript&logoColor=black"/>
</br> 
<img src="https://img.shields.io/badge/JAVA-83B81A?style=flat&logo=java&logoColor=white"/> <img src="https://img.shields.io/badge/Gradle-02303A?style=flat&logo=Gradle&logoColor=white"/> <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat&logo=Spring Boot&logoColor=white"/> <img src="https://img.shields.io/badge/Spring_Security-6DB33F?style=flat&logo=Spring Security&logoColor=white"/>
<img src="https://img.shields.io/badge/JSON_Web_Tokens-000000?style=flat&logo=JSON Web Tokens&logoColor=white"/> <img src="https://img.shields.io/badge/MariaDB-003545?style=flat&logo=mariadb&logoColor=white"/> <img src="https://img.shields.io/badge/Agile-EF2D5E?style=flat&logo=a-frame&logoColor=white"/> <img src="https://img.shields.io/badge/Figma-F24E1E?style=flat&logo=figma&logoColor=white"/> <img src="https://img.shields.io/badge/GIT-F05032?style=flat&logo=Git&logoColor=white"/> <img src="https://img.shields.io/badge/GitHub-181717?style=flat&logo=GitHub&logoColor=white"/> <img src="https://img.shields.io/badge/Notion-000000?style=flat&logo=Notion&logoColor=white"/> <img src="https://img.shields.io/badge/EC2-FF9900?style=flat&logo=Amazon EC2&logoColor=black"/> <img src="https://img.shields.io/badge/MUI-007FFF?style=flat&logo=MUI&logoColor=white"/>
<img src="https://img.shields.io/badge/Swagger-85EA2D?style=flat&logo=Swagger&logoColor=black"/>
<img src="https://img.shields.io/badge/Jenkins-D24939?style=flat&logo=Jenkins&logoColor=white"/>

<br/>

## **00. 협업방식**  
1. 애자일 프로세스  
    - check in / check out Ground Role 방식을 통한 멤버별 하루 과업량, 출/퇴근시간, 회고 등을 기록.
    * BackLog를 작성하여 프로젝트 총 소요 StoryPoint를 집계하여 개발 계획관리를 진행.
    * Sprint 작성하여 주 개발일정관리 진행.
    >  [Sprint]
    https://github.com/orgs/Manidle/projects/1
	    [Check in / Check out]
	    https://www.notion.so/4d5a322d0df74b0bb7cef51a44d88d0b?v=2d459594b7be4128b262b4607ba0c347
	    

2. GitHub
    * Git을 활용한 코드 형상관리.
    * 이슈Tab을 활용하여 팀원들간의 기술공유 및 Exception 공유.
    * Project Tab을 활용하여 BackLog, Sprint 틀 활용.

3. Notion
    * 주간 현황파악을 간단하게 볼 수 있는 주간현황 자료공유    
4.  Swagger
	* BackEnd / FrontEnd 개발자들과의 URI소통

6. Figma
    * 초기 화면단 WireFrame 작성당시 멤버들과의 화면단 구축 협업작업.


## **00. 프로젝트 주제**  

### **PlannerGram**

**PLAN**(여행계획) + **ER** + **GRAM**(통신수단, telegram)

유저들이 **여행코스를 작성**하고 나누는 **커뮤니티 서비스**

지역마다의 **숙소 / 관광지 / 기차표 / 렌트카 정보를** 얻어갈 수 있는 서비스를 제공  
<br/>

## **00. 도메인 관련 용어**

* **User(유저)** : 서비스를 이용하는 사용자.
* **Rentcar(렌트카)** : 차량을 일정기간 유상으로 대여하는 사업 및 그 사업을 통해 대여된 차량을 뜻한다
*  **Attraction(관광지)** : 관광, 여행, 유람에서 역사, 문화, 자연 경관 등의 관광자산을 가진 지역을 뜻한다.
*  **Stay(숙박)** : 여행자와 관광객들이 숙박을 할 수 있는 시설이 있는 업소이다.
* **TRAIN(기차)** : 사람을 실어나르는 여객차를 뜻한다.
* **Post(게시글)** : 여러 사람이 볼 수 있도록 서비스되는 서버에 유저(User)가 업로드 한 텍스트를 말한다.
* **REPLY(댓글)** : 서버에 업로드 된 게시글(POST)에 유저(USER)가 짧게 덧붙인 텍스트를 말한다. 

## **00. ERD (Entity Relationship Diagram)**
 ![image (3)](https://user-images.githubusercontent.com/92356170/192697493-85ff5f04-9b70-4ce2-9d39-882927148eb5.png)

<br/>



### **ATTRACTION** 테이블
| column          | data type   | 설명            |
| --------------- | ----------- | --------------- |
| attraction_id (PK)  | BIGINT        | 관광지 식별자     |
| name     | VARCHAR | 관광지 이름       |
| address   | VARCHAR     | 관광지 주소       |
| description     | VARCHAR | 관광지 소개글       |
| price    | INT         | 관광지 입장료   |
| likeCount | INT     | 관광지 좋아요 숫자 |
 
-  관광지에 관한 정보가 저장되는 테이블

<br/>

### **Attraction_Like** 테이블                                  
| column          | data type   | 설명                |
| --------------- | ----------- | ------------------- |
| attraction_like_id (PK) | BIGINT        | 유저가 좋아요 누른 관광지 식별자         |
| user_id    | BIGINT | 유저식별자     |
| attraction_id   | BIGINT | 관광지 식별자2 |

- Attraction(관광지)의 좋아요를 유저정보와 연결시켜주는 테이블.

<br/>

### **Board** 테이블
| column          | data type   | 설명            |
| --------------- | ----------- | --------------- |
| board_id (PK)  | BIGINT        | 게시판 식별자     |
| board_name     | VARCHAR | 게시판 이름       |

-  POST(게시글)을 하위 엔티티로 가지는 게시판 테이블

<br/>

### **PLATFORM** 테이블
| column          | data type   | 설명            |
| --------------- | ----------- | --------------- |
| platform_id (PK)  | BIGINT        | 플랫폼 식별자     |
| city_Code     | VARCHAR | 도시코드       |
| city_Name     | VARCHAR | 도시이름       |
| nodeId     | VARCHAR | 기차역코드       |
| nodeName     | VARCHAR | 기차역이름       |

-  기차(OPEN API) 역코드 변환 테이블

<br/>

### **POST** 테이블                                  
| column                    | data type   | 설명              |
| ------------------------- | ----------- | ----------------- |
| post_id (PK) | BIGINT        | 게시글 식별자       |
| user_id    | BIGINT | 유저 식별자 |
| board_id   | BIGINT | 게시판 식별자2 |
| title    | VARCHAR   | 제목 |
| contents    | VARCHAR   | 본문 |
| like_count    | INT   | 좋아요 숫자 |
| read_count    | INT   | 조회수 |
| boardName    | VARCHAR   | 게시판 이름(DTO) |
| nickname    | VARCHAR   | 작성자 닉네임(DTO) |
- BOARD(게시판)의 하위 엔티티, 게시글에 관한 정보를 담고 있는 테이블

<br/>

### **POST_ATTRACTION** 테이블                                  
| column                    | data type   | 설명              |
| ------------------------- | ----------- | ----------------- |
| post_attraction_id (PK) | BIGINT        | 참고된 관광지 식별자       |
| attraction_id    | BIGINT | 관광지 식별자 |
| post_id   | BIGINT | 게시글 식별자 |
| name(DTO)   | VARCHAR | 이름 |
| address(DTO)   | VARCHAR | 주소 |
| description(DTO)   | VARCHAR | 소개글 |
| price(DTO)   | INT | 입장료 |
| likeCount(DTO)   | INT | 좋아요 숫자 |

- POST(게시글)에 입력되는 정보

<br/>

### **POST_LIKE** 테이블                                  
| column                    | data type   | 설명              |
| ------------------------- | ----------- | ----------------- |
| post_like_id (PK) | BIGINT        | 유저가 좋아요 누른 게시글 식별자       |
| post_id    | BIGINT | 게시글 식별자2 |
| user_id   | BIGINT | 유저 식별자 |

- POST(게시글)의 좋아요와 유저정보를 연결해주는 테이블

<br/>

### **POST_RENTCAR** 테이블                                  
| column                    | data type   | 설명              |
| ------------------------- | ----------- | ----------------- |
| post_rentcar_id (PK) | BIGINT        | 참고된 렌트카 식별자       |
| rentcar_id    | BIGINT | 렌트카 식별자2 |
| post_id   | BIGINT | 게시글 식별자 |
| address(DTO)   | VARCHAR | 업체주소 |
| companyName(DTO)   | VARCHAR | 업체이름 |
| carSort(DTO)   | VARCHAR | 차량종류 |
| carName(DTO)   | VARCHAR | 차량이름 |
| likeCount(DTO)   | INT | 좋아요 숫자 |

- POST(게시글)에 입력되는 정보

<br/>


### **POST_STAY** 테이블                                  
| column                    | data type   | 설명              |
| ------------------------- | ----------- | ----------------- |
| post_stay_id (PK) | BIGINT        | 참고된 숙소 식별자       |
| stay_id    | BIGINT | 숙소 식별자 |
| post_id   | BIGINT | 게시글 식별자 |
| name(DTO)    | VARCHAR   | 이름 |
| address(DTO)    | VARCHAR   | 주소 |
| price(DTO)    | INT   | 1박당 가격 |
| checkIn(DTO)    | DATETIME   | 체크인 시간 |
| checkOut(DTO)    | DATETIME   | 체크아웃 시간 |
| likeCount(DTO)    | INT   | 좋아요 숫자 |
- POST(게시글)에 입력되는 숙소정보

<br/>

### **POST_TRAIN** 테이블                                  
| column                    | data type   | 설명              |
| ------------------------- | ----------- | ----------------- |
| post_train_id (PK) | BIGINT        | 참고된 기차 식별자       |
| post_id    | BIGINT | 게시글 식별자 |
| depplacename   | VARCHAR | 출발역 |
| arrplacename    | VARCHAR   | 도착역 |
| depplan    | VARCHAR   | 주소 |
| price(DTO)    | INT   | 1박당 가격 |
| checkIn(DTO)    | DATETIME   | 체크인 시간 |
| checkOut(DTO)    | DATETIME   | 체크아웃 시간 |
| likeCount(DTO)    | INT   | 좋아요 숫자 |
- POST(게시글)에 입력되는 정보

<br/>

### **RENTCAR** 테이블                                  
| column                    | data type   | 설명              |
| ------------------------- | ----------- | ----------------- |
| rentcar_id (PK) | BIGINT        | 렌트카 식별자       |
| address    | VARCHAR | 업체주소 |
| companyName   | VARCHAR | 업체이름 |
| carSort    | VARCHAR   | 차량종류 |
| carName    | VARCHAR   | 차량이름 |
| likeCount    | INT   | 좋아요숫자 |

- 렌트카에 관한 정보가 저장되는 테이블

<br/>

### **RENTCAR_Like** 테이블                                  
| column                    | data type   | 설명              |
| ------------------------- | ----------- | ----------------- |
| rentCar_like_id (PK) | BIGINT        | 유저가 좋아요 누른 렌트카 식별자       |
| rentcar_id    | BIGINT | 렌트카 식별자 |
| user_id   | BIGINT | 유저 식별자 |

- RENTCAR(렌트카)의 좋아요와 유저정보를 연결해주는 테이블

<br/>

### **REPLY** 테이블                                  
| column                    | data type   | 설명              |
| ------------------------- | ----------- | ----------------- |
| reply_id (PK) | BIGINT        | 댓글 식별자       |
| post_id    | BIGINT | 게시글 식별자 |
| user_id   | BIGINT | 유저 식별자 |
| contents    | VARCHAR   | 내용 |
| nickName(DTO)    | VARCHAR   | 작성자 닉네임 |

- POST(게시글)에 입력되는 댓글정보

<br/>



### **STAY** 테이블                                  
| column                    | data type   | 설명              |
| ------------------------- | ----------- | ----------------- |
| stay_id (PK) | BIGINT        | 숙소 식별자       |
| name    | VARCHAR | 이름 |
| address   | VARCHAR | 주소 |
| price    | INT   | 1박당 가격 |
| checkIn    | DATETIME   | 체크인 시간 |
| checkOut    | DATETIME   | 체크아웃 시간 |
| likeCount    | INT   | 좋아요 숫자 |

- 숙소에 관한 정보가 저장되는 테이블

<br/>

### **stay_like** 테이블                                  
| column                    | data type   | 설명              |
| ------------------------- | ----------- | ----------------- |
| stay_like_id (PK) | BIGINT        | 유저가 좋아요 누른 숙소 식별자       |
| stay_id    | BIGINT | 숙소 식별자2 |
| user_id   | BIGINT | 유저 식별자 |

- STAY(숙소)의 좋아요와 유저정보를 연결해주는 테이블

<br/>


### **USER** 테이블                                  
| column               | data type   | 설명              |
| -------------------- | ----------- | ----------------- |
| user_id (PK)    | BIGINT        | 유저 식별자       |
| username       | VARCHAR | 로그인 아이디         |
| password | VARCHAR         | 패스워드   |
| nickname  | VARCHAR         | 닉네임 |
| roles  | VARCHAR         | SECURITY권한 |

- 서비스 이용자들의 정보가 저장되는 테이블

<br/>

### **User_Info** 테이블                                  
| column                        | data type | 설명           |
| ----------------------------- | --------- | -------------- |
| user_info_id (PK) | BIGINT      | 유저 상세정보 식별자    |
| user_id        | BIGINT      | 유저 식별자 |
| profileImg        | VARCHAR      | 유저 프로필 사진 URL |
| email        | VARCHAR      | 유저 이메일 |

- 서비스 이용자들의 추가정보가 저장되는 테이블

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

- **👨김영광** : 

<br/>

## **00. 참고 자료** 
- [커밋 컨벤션 DOCS](https://udacity.github.io/git-styleguide/)
- [커밋 컨벤션 정리자료](https://overcome-the-limits.tistory.com/entry/%ED%98%91%EC%97%85-%ED%98%91%EC%97%85%EC%9D%84-%EC%9C%84%ED%95%9C-%EA%B8%B0%EB%B3%B8%EC%A0%81%EC%9D%B8-git-%EC%BB%A4%EB%B0%8B%EC%BB%A8%EB%B2%A4%EC%85%98-%EC%84%A4%EC%A0%95%ED%95%98%EA%B8%B0)
- [자바 컨벤션 DOCS](https://naver.github.io/hackday-conventions-java/)
- https://www.youtube.com/c/%EB%A9%94%ED%83%80%EC%BD%94%EB%94%A9
