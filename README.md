## Spring Data JPA + QueryDsl을 이용한 게시판

### 해당 프로젝트를 만들면서 배울수 있었던 점은 아래와 같습니다.

#### 1. 스프링부트 + Spring Data JPA

에전에 이클립스 IDE 환경에서 스프링 프레임워크와 SQL Mapper 프레임워크인 Mybatis를 이용하여 간단한 게시글과 댓글을 작성하는 사내 게시판을 만든적이 있습니다. 
그 당시에는 도메인과 VO 개념이 전혀 없었기 때문에 테이블에 해당 도메인에 매핑된 값만 넣는 CRUD 작업으로 게시판과 댓글 기능이 되는 그럴듯하게 동작하게 만드는데 포커를 맞추었었습니다. 그러다가 한동안 손을 두다가 스프링부트와 JPA를 접하면서 영속컨텍스트와 Querydsl을 배우면서 신세계를 접하였습니다. 테이블을 설계하는 시간보다 비즈니스 로직에 집중을 할 수 있었고, 이러한 이점은 전에 만들었던 게시판보다 더 객체지향적으로 게시판을 만들고, 빠르게 웹 어플리케이션을 구현할 수 있게 해주었습니다.


#### 2. 게시판를 JPA를 통한 재설계
이전에 만들었던 Mybatis 프레임워크 기반의 게시판 프로젝트는 테이블을 설계하는데 사실 많은 시간을 보내었고, 객체중심이 아니라 테이블 중심으로 설계를 하고 구현을 하였습니다. 하지만 스프링부트와 Spring Data JPA를 사용하면서 ORM 기술의 장점과 객체지향적인 코드 작성과 도메인과 VO, 뷰 템플릿에 보여줄 Response 객체까지 구현하여 유지보수성을 좀 더 쉽게 할 수 있도록 구현하면서 객체지향 설계에 대한 중요성을 조금이라도 알게 되었습니다.


#### 3. 사용한 기술 및 툴
- Spring Boot
- Spring Data JPA
- IntelliJ IDEA Ultimate 
- JAVA 8
- MySQL
- H2
- QueryDsl
- Postman(REST API 호출용)

#### 4. 프로젝트 실행환경
Lombok이 반드시 설치 되있어야 합니다.
* [IntellJ 설치 : [lombok] IntelliJ에 lombok(롬복) 설치](https://abettercode.tistory.com/72)
* [QueryDsl 설정: [QuertDsl] build.gradle 파일에 QueryDSL 설정](https://jojoldu.tistory.com/372)
* [QueryDsl 설정: [QuertDsl] pom.xml 파일에 QueryDSL 설정](https://webcoding-start.tistory.com/8?category=812502)

#### 5. 실행

```java
id 'io.spring.dependency-management' version '1.0.8.RELEASE' 
```

```
프로젝트 경로에 들어간 후
./gradleew bootjar
java -jar '실행파일명'.jar 수행
```



