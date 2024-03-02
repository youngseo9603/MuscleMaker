# 📈 Muscle-Maker
> ⚡A109 (서울 1반 9조)
>
> 운동 SNS
>
> 프로젝트 기간 : 2023.12.28 - 2024.02.16 (6주)

<br>

## :deciduous_tree: 프로젝트 개요

### 프로젝트 기간

-   기획 및 설계 :  2023.12.28 - 2024.01.15
-   프로젝트 개발 : 2024.01.15 - 2024.02.15

### 구성원

-   백엔드 4명
-   프론트엔드 2명

<br/>

## 👍 서비스 소개
- 운동과 식단을 서로 공유하는 운동 SNS 서비스입니다.
- 운동과 식단 피드를 올려 다른 사용자들과 공유할 수 있습니다.
- 운동과 식단 클럽에 참여하여 다른 사람들과 같이 운동/식단을 할 수 있습니다.
- 운동 루틴을 설정 할 수 있고, 다른 사람의 운동 루틴을 보고 가져올 수 있습니다.

<br/>

## 🔨 주요 기술 스택

### ✔️ Frontend

-   `Node`
-   `Next`
-   `React`
-   `TypeScript`

### ✔️ Backend

-   `Java`
-   `Spring Boot`
-   `Spring Security`
-   `Spring Data JPA`
-   `JWT`
-   `Gradle`

### ✔️ DB

-   `MySQL`

### ✔️ Deploy

-   `AWS EC2`
-   `Docker`
-   `Docker-compose`
-   `Nginx`
-   `Jenkins`

### ✔️ Communication

-   형상 관리 - `Gitlab`
-   이슈 및 스크럼 관리 - `Jira`
-   의사소통, 협업 - `Notion`, `Mattermost`
-   디자인 - `Figma`
  
<br>

## **📚 목차**  

1️⃣ [타겟층](#-타겟층)   
2️⃣ [주요 기능](#-주요-기능)  
3️⃣ [서비스](#-서비스)  
4️⃣ [실행방법](#-실행방법)  
5️⃣ [팀 구성](#-팀-구성)  
6️⃣ [기술 아키텍쳐](#-기술-아키텍쳐)  
7️⃣ [ERD 다이어그램](#-erd-다이어그램)  
8️⃣ [API 명세서](#-api-명세서)   

<br>

## 😮 타겟층
    ✔ 운동을 하며 동기부여 또는 소속감을 얻고자 하는 운동자들
    ✔ 운동을 하고 싶지만 어떠한 운동을 해야할지 고민하는 사람들
   
<br>

## 👍 주요 기능
|구분|기능|설명|비고|
|:---|:---|:---|:---|
|1|피드| - 피드 조회 / 등록 / 삭제 할 수 있다.<br> - 피드 댓글 작성할 수 있다.<br> - 피드에 좋아요를 할 수 있다.||
|2|추천| - 클럽을 추천 받을 수 있다. <br> - 유저를 추천 받을 수 있다.|클럽 -> 맴버순, 달성일순, 레벨순 <br>유저 -> 팔로워순, 유사 BMI순, 유사 골격근량순|
|3|루틴| - 일자별 루틴을 설정할 수 있다.<br> - 다른 사람의 루틴을 조회하고 나의 루틴으로 가져올 수 있다.||
|4|클럽| - 클럽에 가입 및 생성을 할 수 있다.<br> - 클럽에 피드를 작성할 수 있다.<br> - 클럽에 작성된 피드를 기준으로 클럽의 성공률, 경험치 성공일 수가 반영된다.||
|5|리포트| - 목표 체중, 골격근량, 체지방량을 설정할 수 있다.<br> - 주기별로 입력되는 체중, 골격근량, 체지방량을 이용해 시각화 자료를 제공한다.||
|6|팔로우| - 회원간 팔로우/팔로잉 기능을 제공한다.||
|7|알림| - 팔로우/팔로잉, 클럽, 댓글에 이벤트가 발생했을 때 알림을 제공한다.<br> - 알림을 통해 해당 위치로 바로 이동할 수 있다.|SSE를 활용 하여 구현|
<br>

# 서비스
## 📌 피드

 - 피드 조회 / 등록 / 삭제 할 수 있다.

 ![feedRegist](https://github.com/zsa332/Algorithms/assets/78728865/13361ee0-4288-4ca0-807f-3327282131f6)


 - 피드 댓글 작성할 수 있다.
 - 피드에 좋아요를 할 수 있다.

![feedFavoriteAndComment](https://github.com/zsa332/Algorithms/assets/78728865/8a38be3c-2cbb-4fea-92bb-6ecfedd66b56)


---

## 📌 - 추천

 - 클럽을 추천 받을 수 있다.
 - 유저를 추천 받을 수 있다.

![recommendClubAndUser](https://github.com/zsa332/Algorithms/assets/78728865/4816b410-59ca-4e41-a5e7-72098f68d87f)


---

## 📌 - 루틴

 - 일자별 루틴을 설정할 수 있다.

 ![routineSetting](https://github.com/zsa332/Algorithms/assets/78728865/de2ecf96-d35b-49c2-8be4-92b8e8ee3f64)


 - 다른 사람의 루틴을 조회하고 나의 루틴으로 가져올 수 있다.

![routineGet](https://github.com/zsa332/Algorithms/assets/78728865/a871c208-b7e8-468c-9c3d-d78524c1da11)


---

## 📌 - 클럽
 - 클럽에 가입 및 생성을 할 수 있다.
 
 ![clubRegister](img/club_1_.gif)

 - 클럽에 피드를 작성할 수 있고, 피드를 기준으로 클럽의 성공률, 경험치 성공일 수가 반영된다.

 ![writeClubFeed](img/club_2_.gif)
---

## 📌 - 리포트
 - 목표 체중, 골격근량, 체지방량을 설정할 수 있다.

 ![writeReport](img/report_1_.gif)
 
 - 주기별로 입력되는 체중, 골격근량, 체지방량을 이용해 시각화 자료를 제공한다.

 ![changeReport](img/report_2_.gif)

---

## 📌 - 팔로우
 - 회원간 팔로우/팔로잉 기능을 제공한다.

 ![follow](img/follow_1_.gif)

 ![following](img/follow_2_.gif)

---

## 📌 - 알림
 - 팔로우/팔로잉, 클럽, 댓글에 이벤트가 발생했을 때 알림을 제공한다.
 - 알림을 통해 해당 위치로 바로 이동할 수 있다.

 ![alarm](img/alarm.gif)

---



<br>

## 💾 실행방법

### [🔗 포팅 메뉴얼 바로가기]()
- exec 폴더 내 포팅 메뉴얼 참조


<br>

## 👬 팀 구성
<table>
  <tbody>
    <tr>
     <td align="center">
        <a href="https://github.com/JongJae2">
            <img src="https://avatars.githubusercontent.com/u/149658209?v=4" width="100px;" alt="팀원"/>
            <br />
            <sub><b>이종재</b></sub>
        </a>
        <br />
        <div>BE,FE</div>
      </td>
      <br/>
      <td align="center">
        <a href="https://github.com/youngseo9603">
            <img src="https://avatars.githubusercontent.com/u/22046916?s=400&v=4" width="100px;" alt="이영서"/>
            <br />
            <sub><b>이영서</b></sub>
        </a>
        <br />
        <div>Infra, Be</div>
      </td>
      <br/>
      <td align="center">
        <a href="https://github.com/zsa332">
            <img src="https://avatars.githubusercontent.com/u/78728865?v=4" width="100px;" alt="서성원"/>
            <br />
            <sub><b>서성원</b></sub>
        </a>
        <br />
        <div>Infra, BE</div>
      </td>
    </tr>
    <tr>
      <td align="center">
        <a href="https://github.com/dforce103">
          <img src="https://avatars.githubusercontent.com/u/139521803?s=400&v=4"
              width="100px;" alt="송찬의" />
          <br />
          <sub><b>송찬의</b></sub>
          </a>
          <br />
          <div>FE</div>
      </td>
      <td align="center">
        <a href="https://github.com/soyeonjwa">
            <img src="https://avatars.githubusercontent.com/u/81522548?v=4" width="100px;" alt="좌소연"/>
            <br />
            <sub><b>좌소연</b></sub>
        </a>
        <br />
        <div>FE, BE</div>
      </td>
      <td align="center">
        <a href="https://github.com/hello1334">
            <img src="https://avatars.githubusercontent.com/u/139297106?v=4" width="100px;" alt="전건휘"/>
            <br />
            <sub><b>전건휘</b></sub>
        </a>
        <br />
        <div>FE</div>
      </td>
    </tr>
  </tbody>
</table>

<br>

## ⚙ 기술 아키텍쳐
![image](https://github.com/zsa332/Algorithms/assets/78728865/458634de-a5b6-4d4a-8b37-bf8657165662)

<br>

## 💎 [ERD 다이어그램](https://www.erdcloud.com/d/5HtrrcsSCibroHX3k)
![image](https://github.com/zsa332/Algorithms/assets/78728865/9972bd5e-7713-47d8-a5f3-2b5b21a09476)

<br>

## 📘 [API 명세서](https://zesty-pheasant-3d2.notion.site/c72286b8426f46518d5b3f5d2484141e?v=7127dced354b4a31ba0433b9f466b599&pvs=4)
![image](https://github.com/zsa332/Algorithms/assets/78728865/c150aa48-5173-4afb-a392-ae2120ab4001)

![image](https://github.com/zsa332/Algorithms/assets/78728865/b36f22d5-140b-4077-b768-b5fa13247da6)

<br>

## 🍏[와이어프레임](https://www.figma.com/file/WCNg4xM6SWFmTKnQ8uZ3sB/Miracle-Maker?type=design&mode=design)
![image](https://github.com/zsa332/Algorithms/assets/78728865/a0243d0a-1f55-4fdf-aa34-3d4c604c6e75)
