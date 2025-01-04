# 📲 SocialHub

> ## 🔍 목차
> 1. [서비스 소개](#-서비스-소개)
> 2. [R&R 및 주요 소스 코드](#-rr)
> 3. [프로젝트 일정](#-프로젝트-일정)
> 4. [프로젝트 환경](#%EF%B8%8F-프로젝트-환경)
> 5. [API 명세서](#-api-명세서)
> 6. [ERD](#%EF%B8%8F-erd)
> 7. [협업 및 커뮤니케이션](#%EF%B8%8F-협업-및-커뮤니케이션)
> 8. [Github Issue & Jira 를 통한 Task 트래킹 관리 (WBS)](#%EF%B8%8F%EF%B8%8F-github-issue--jira-를-통한-task-트래킹-관리-wbs)
> 9. [Discord를 활용한 소통 및 PR 알림 봇](#-discord를-활용한-소통-및-pr-알림-봇)
> 10. [트러블 슈팅](#-트러블-슈팅)
> 11. [고민한 흔적](#-고민한-흔적)
> 12. [디렉토리 구조](#%EF%B8%8F-디렉토리-구조)


<br/>

## 📋 서비스 소개
- 해시태그를 기반으로 `인스타그램`, `스레드`, `페이스북`, `트위터(X)` 등
복수의 SNS에 게시된 게시물 중 해시태그가 포함된 게시물들을 하나의 서비스에서 확인할 수 있는
**통합 Feed 어플리케이션의 API 서버**입니다.

<br/>

## 🧑🏻‍💻 R&R
| 담당자       | 담당 업무                                                 |
|:--------------:|----------------------------------------------------------|
| [오예령](https://github.com/ohyeryung) | 게시물 기능 구현 (등록, 수정, 삭제, 검색)                  |
| [**유리빛나**](https://github.com/ryuneng)     | **게시물 기능 구현 (목록 조회, 상세 조회, 좋아요, 공유)**       |
| [김유현](https://github.com/youhyeoneee)       | 통계 기능 구현 (서비스 및 컨트롤러, 단위 테스트)           |
| [김은정](https://github.com/fkznsha23)| 사용자 기능 구현 (로그인, 계정 중복 확인)                  |
| [김효진](https://github.com/hyojin52)       | 통계 기능 구현 (서비스 및 레포지토리, 스웨거)              |
| [배서진](https://github.com/bsjin1122)       | 사용자 기능 구현 (회원가입, 이메일 인증, 회원정보 수정)         |

### 담당 업무 소스 코드
1. <a href="https://github.com/ryuneng/socialhub/blob/dev/src/main/java/com/allclear/socialhub/post/controller/PostController.java">Controller 코드 보기</a>
2. <a href="https://github.com/ryuneng/socialhub/blob/dev/src/main/java/com/allclear/socialhub/post/service/PostServiceImpl.java">Service 코드 보기</a>
3. <a href="https://github.com/ryuneng/socialhub/blob/dev/src/main/java/com/allclear/socialhub/post/repository/querydsl/PostRepositoryImpl.java">Repository 코드 보기</a>
4. <a href="https://github.com/ryuneng/socialhub/blob/dev/src/test/java/com/allclear/socialhub/post/controller/PostControllerTest.java">주요 테스트 코드 보기</a>

<br>

## 🗓 프로젝트 일정
<img src="https://github.com/user-attachments/assets/1016fba4-e0c2-4858-b21d-636e56523120" alt="image" width="90%">
</details>

<br>
<br>

## 🛠️ 프로젝트 환경

| Stack                                                                | Version            |
|:----------------------------------------------------------------------:|:-----------------:|
| ![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white)  | Spring Boot 3.3.x |
| ![Gradle](https://img.shields.io/badge/Gradle-02303A.svg?style=for-the-badge&logo=Gradle&logoColor=white)    | Gradle 8.8       |
| ![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)    | JDK 17           |
| ![MySQL](https://img.shields.io/badge/mysql-4479A1.svg?style=for-the-badge&logo=mysql&logoColor=white)       | MySQL 8.0        |
| ![Redis](https://img.shields.io/badge/redis-%23DD0031.svg?style=for-the-badge&logo=redis&logoColor=white)    | Redis 6.0        |

<br>

## 📄 API 명세서
 > 자세한 명세는 🔗<a href="https://documenter.getpostman.com/view/20456478/2sAXjGcDg4">여기 (POSTMAN API 명세)</a>를 클릭해 확인해주세요!

| 도메인 | 기능명               | Http Method | API Path                       | 인증 | 담당자        |
|--------|----------------------|-------------|--------------------------------|------|---------------|
| 게시물 | 게시물 목록 조회      | `GET`         | /api/posts                     | `O`    | [유리빛나](https://github.com/ryuneng)        |
| 게시물 | 게시물 상세 조회      | `GET`         | /api/posts/{postId}            | `O`    | [유리빛나](https://github.com/ryuneng)        |
| 게시물 | 게시물 좋아요         | `POST`        | /api/posts/{postId}/like       | `O`    | [유리빛나](https://github.com/ryuneng)        |
| 게시물 | 게시물 공유           | `POST`        | /api/posts/{postId}/share      | `O`    | [유리빛나](https://github.com/ryuneng)        |

<br>

## ⛓️ ERD
<img width="1417" alt="image" src="https://github.com/user-attachments/assets/ac5359a2-566e-4f82-91e6-5d2c615b9a71">

<br>
<br>

## 🗣️ 협업 및 커뮤니케이션

<details>
<summary>문서화 작업</summary>
<div markdown="1">
    <div style="flex justify-content-center">
        <img src="https://github.com/user-attachments/assets/17ced01a-a322-4538-b3ea-8484adaa411f" width="45%">
        <img src="https://github.com/user-attachments/assets/8e747e76-3e9f-4903-8e54-b6f7a9f79ac7" width="45%">
    </div>
</div>
</details>

<br/>

## 🏃‍♀️‍➡️ Github Issue & Jira 를 통한 Task 트래킹 관리 (WBS) 

<details>
<summary>개발일정 관리</summary>
<div markdown="1">
    <img src="https://github.com/user-attachments/assets/71d9340d-98a7-4ffc-aa05-05367b8544c6" width="90%">
    <div style="flex justify-content-center">
        <img src="https://github.com/user-attachments/assets/589e3eee-997d-48a8-adb9-18fb3dd9045a" align="center" width="40%">  
        <img src="https://github.com/user-attachments/assets/11a9b040-a855-4533-bbe8-d3cc63240b01" align="center" width="40%">  
    </div>
</div>
</details>

<br/>

## 🤖 Discord를 활용한 소통 및 PR 알림 봇 

<details>
<summary>소통 및 PR 알림 확인</summary>
<div markdown="1">
    <img src="https://github.com/user-attachments/assets/6a051e1d-58d4-4779-a7b8-1a1b6725671f">
    <img src="https://github.com/user-attachments/assets/16f92c8c-6b92-45b7-8d83-95f1d47d0fb1" width="50%">
</div>
</details>

<br>

## 💥 트러블 슈팅
- DB에 저장된 데이터에 따라 테스트 결과가 달라지는 문제 - <a href="https://github.com/ryuneng/socialhub/wiki/DB%EC%97%90-%EC%A0%80%EC%9E%A5%EB%90%9C-%EB%8D%B0%EC%9D%B4%ED%84%B0%EC%97%90-%EB%94%B0%EB%9D%BC-%ED%85%8C%EC%8A%A4%ED%8A%B8-%EA%B2%B0%EA%B3%BC%EA%B0%80-%EB%8B%AC%EB%9D%BC%EC%A7%80%EB%8A%94-%EB%AC%B8%EC%A0%9C"> WIKI 이동 </a>
- 테스트 실행 순서에 따라 일부 테스트가 실패하는 문제 - <a href="https://github.com/ryuneng/socialhub/wiki/%ED%85%8C%EC%8A%A4%ED%8A%B8-%EC%8B%A4%ED%96%89-%EC%88%9C%EC%84%9C%EC%97%90-%EB%94%B0%EB%9D%BC-%EC%9D%BC%EB%B6%80-%ED%85%8C%EC%8A%A4%ED%8A%B8%EA%B0%80-%EC%8B%A4%ED%8C%A8%ED%95%98%EB%8A%94-%EB%AC%B8%EC%A0%9C"> WIKI 이동 </a>
- QueryDSL 사용 중 발생한 문제 - <a href="https://github.com/ryuneng/socialhub/wiki/QueryDSL-%EC%82%AC%EC%9A%A9-%EC%A4%91-%EB%B0%9C%EC%83%9D%ED%95%9C-%EB%AC%B8%EC%A0%9C"> WIKI 이동 </a>

<br>

## 🤔 고민한 흔적
- JPA 엔티티의 식별자 변수명 - <a href="https://github.com/ryuneng/socialhub/wiki/JPA-%EC%97%94%ED%8B%B0%ED%8B%B0%EC%9D%98-%EC%8B%9D%EB%B3%84%EC%9E%90-%EB%B3%80%EC%88%98%EB%AA%85"> WIKI 이동 </a>
- 게시물 목록 응답 DTO의 생성 및 수정 시간 필드 타입 (LocalDateTime vs String) - <a href="https://github.com/ryuneng/socialhub/wiki/%EA%B2%8C%EC%8B%9C%EB%AC%BC-%EB%AA%A9%EB%A1%9D-%EC%9D%91%EB%8B%B5-DTO%EC%9D%98-%EC%83%9D%EC%84%B1-%EB%B0%8F-%EC%88%98%EC%A0%95-%EC%8B%9C%EA%B0%84-%ED%95%84%EB%93%9C-%ED%83%80%EC%9E%85-(LocalDateTime-vs-String)"> WIKI 이동 </a>
- ERD 게시물 조회 테이블의 필요성 - <a href="https://github.com/ryuneng/socialhub/wiki/ERD-%EA%B2%8C%EC%8B%9C%EB%AC%BC-%EC%A1%B0%ED%9A%8C-%ED%85%8C%EC%9D%B4%EB%B8%94%EC%9D%98-%ED%95%84%EC%9A%94%EC%84%B1"> WIKI 이동 </a>

<br>

## 🗂️ 디렉토리 구조
<details><summary>디렉토리 구조</summary>

```text
C:.
│   .env
│   .gitignore
│   build.gradle
│   docker-compose.yml
│   settings.gradle
├───.github
│   ├───ISSUE_TEMPLATE
│   └───workflows
├───build
└───src
    ├───main
    │   ├───java
    │   │   └───com
    │   │       └───allclear
    │   │           └───socialhub
    │   │               ├───common
    │   │               ├───post
    │   │               └───user
    │   └───resources
    └───test
        ├───java
        │   └───com
        │       └───allclear
        │           └───socialhub
        └───resources
```

<br>
    
```text
📦socialhub
 ┣ 📂common
 ┃ ┣ 📂config
 ┃ ┃ ┣ 📜ConverterConfig.java
 ┃ ┃ ┣ 📜JpaConfig.java
 ┃ ┃ ┣ 📜RedisConfig.java
 ┃ ┃ ┣ 📜SwaggerConfig.java
 ┃ ┃ ┗ 📜WebSecurityConfig.java
 ┃ ┣ 📂converter
 ┃ ┃ ┣ 📜StringToStatisticTypeConverter.java
 ┃ ┃ ┗ 📜StringToStatisticValueConverter.java
 ┃ ┣ 📂domain
 ┃ ┃ ┗ 📜Timestamped.java
 ┃ ┣ 📂exception
 ┃ ┃ ┣ 📂handler
 ┃ ┃ ┃ ┗ 📜GlobalExceptionHandler.java
 ┃ ┃ ┣ 📜CustomException.java
 ┃ ┃ ┣ 📜ErrorCode.java
 ┃ ┃ ┗ 📜ErrorResponse.java
 ┃ ┣ 📂provider
 ┃ ┃ ┗ 📜JwtTokenProvider.java
 ┃ ┗ 📂util
 ┃ ┃ ┣ 📜DateUtil.java
 ┃ ┃ ┗ 📜TokenUtil.java
 ┣ 📂post
 ┃ ┣ 📂common
 ┃ ┃ ┣ 📂hashtag
 ┃ ┃ ┃ ┣ 📂domain
 ┃ ┃ ┃ ┃ ┣ 📜Hashtag.java
 ┃ ┃ ┃ ┃ ┗ 📜PostHashtag.java
 ┃ ┃ ┃ ┣ 📂repository
 ┃ ┃ ┃ ┃ ┣ 📜HashtagRepository.java
 ┃ ┃ ┃ ┃ ┗ 📜PostHashtagRepository.java
 ┃ ┃ ┃ ┗ 📂service
 ┃ ┃ ┃ ┃ ┣ 📜HashtagService.java
 ┃ ┃ ┃ ┃ ┗ 📜HashtagServiceImpl.java
 ┃ ┃ ┣ 📂like
 ┃ ┃ ┃ ┣ 📂domain
 ┃ ┃ ┃ ┃ ┗ 📜PostLike.java
 ┃ ┃ ┃ ┣ 📂dto
 ┃ ┃ ┃ ┃ ┗ 📜PostLikeResponse.java
 ┃ ┃ ┃ ┗ 📂repository
 ┃ ┃ ┃ ┃ ┗ 📜PostLikeRepository.java
 ┃ ┃ ┣ 📂response
 ┃ ┃ ┃ ┗ 📜StatisticQueryResponse.java
 ┃ ┃ ┣ 📂share
 ┃ ┃ ┃ ┣ 📂domain
 ┃ ┃ ┃ ┃ ┗ 📜PostShare.java
 ┃ ┃ ┃ ┣ 📂dto
 ┃ ┃ ┃ ┃ ┗ 📜PostShareResponse.java
 ┃ ┃ ┃ ┗ 📂repository
 ┃ ┃ ┃ ┃ ┗ 📜PostShareRepository.java
 ┃ ┃ ┗ 📂view
 ┃ ┃ ┃ ┣ 📂domain
 ┃ ┃ ┃ ┃ ┗ 📜PostView.java
 ┃ ┃ ┃ ┗ 📂repository
 ┃ ┃ ┃ ┃ ┗ 📜PostViewRepository.java
 ┃ ┣ 📂controller
 ┃ ┃ ┣ 📜PostController.java
 ┃ ┃ ┗ 📜StatisticController.java
 ┃ ┣ 📂domain
 ┃ ┃ ┣ 📜Post.java
 ┃ ┃ ┣ 📜PostType.java
 ┃ ┃ ┣ 📜SearchByType.java
 ┃ ┃ ┣ 📜StatisticType.java
 ┃ ┃ ┗ 📜StatisticValue.java
 ┃ ┣ 📂dto
 ┃ ┃ ┣ 📜PostCreateRequest.java
 ┃ ┃ ┣ 📜PostDetailResponse.java
 ┃ ┃ ┣ 📜PostListResponse.java
 ┃ ┃ ┣ 📜PostPaging.java
 ┃ ┃ ┣ 📜PostResponse.java
 ┃ ┃ ┣ 📜PostUpdateRequest.java
 ┃ ┃ ┣ 📜StatisticRequestParam.java
 ┃ ┃ ┗ 📜StatisticResponse.java
 ┃ ┣ 📂repository
 ┃ ┃ ┣ 📂querydsl
 ┃ ┃ ┃ ┣ 📜PostRepositoryImpl.java
 ┃ ┃ ┃ ┗ 📜PostRepositoryQuerydsl.java
 ┃ ┃ ┗ 📜PostRepository.java
 ┃ ┗ 📂service
 ┃ ┃ ┣ 📜PostService.java
 ┃ ┃ ┣ 📜PostServiceImpl.java
 ┃ ┃ ┣ 📜StatisticService.java
 ┃ ┃ ┗ 📜StatisticServiceImpl.java
 ┣ 📂user
 ┃ ┣ 📂controller
 ┃ ┃ ┗ 📜UserController.java
 ┃ ┣ 📂domain
 ┃ ┃ ┗ 📜User.java
 ┃ ┣ 📂dto
 ┃ ┃ ┣ 📜UserEmailRequest.java
 ┃ ┃ ┣ 📜UserInfoUpdateRequest.java
 ┃ ┃ ┣ 📜UserInfoUpdateResponse.java
 ┃ ┃ ┣ 📜UserJoinRequest.java
 ┃ ┃ ┣ 📜UserLoginRequest.java
 ┃ ┃ ┗ 📜UserResponse.java
 ┃ ┣ 📂exception
 ┃ ┃ ┗ 📜DuplicateUserInfoException.java
 ┃ ┣ 📂repository
 ┃ ┃ ┣ 📜EmailRedisRepository.java
 ┃ ┃ ┗ 📜UserRepository.java
 ┃ ┣ 📂service
 ┃ ┃ ┣ 📜EmailService.java
 ┃ ┃ ┣ 📜EmailServiceImpl.java
 ┃ ┃ ┣ 📜UserService.java
 ┃ ┃ ┗ 📜UserServiceImpl.java
 ┃ ┗ 📂type
 ┃ ┃ ┣ 📜EmailType.java
 ┃ ┃ ┣ 📜UserCertifyStatus.java
 ┃ ┃ ┣ 📜UsernameDupStatus.java
 ┃ ┃ ┗ 📜UserStatus.java
 ┗ 📜SocialhubApplication.java
``` 
</details>
