---
title: 01_Hexo
date: 2019-04-04 14:03:09
tags: Hexo
categories: Hexo
---
## HEXO 블로그 만들기

### 1. Node.js와 NPM 설치

+ Node.js

서버 사이드를 JavaScript로 구현할 수 있게 만든 런타임

+ NPM

Node.js기반의 모듈을 모아둔 집합

https://nodejs.org/ko/



---

### 2. Hexo 설치

```bash
$ npm install -g hexo-cli
```



---

### 3. 블로그 생성

생성할 폴더에 접근 후 

```bash
$ hexo init myBlog
$ cd myBlog
$ npm install
```

![1553361798946](https://user-images.githubusercontent.com/36959292/54869831-83756500-4de1-11e9-97e5-1f472870035f.png)

+ node_modules : 기본적인 node.js 모듈
+ scaffolds : 페이지를 구성할 기본 markdown 파일
+ source : 작성한 파일등 리소스
+ theme : 테마
+ .gitignore : github에 업로드 할때 제외할 파일 목록 정의
+ _config.yml : 블로그의 옵션 설정



---

### 4. github에 연동하기

자동으로 github에 업로드

+ github repo를 만들때 주소를 JHyunB.github.io 로 함 

+ _config.yml 파일 열고 아래처럼 수정

![1553362281981](https://user-images.githubusercontent.com/36959292/54869834-99832580-4de1-11e9-8c4d-fd21267cf69e.png)



+ 업로드하기 위한 모듈 설치

```bash
$ npm install hexo-deployer-git --save
```



+ hexo deploy 명령어 수행시 위에서 작성한 주소로 업로드



---

### 5. 포스트 생성

```bash
$ hexo new post first-post
```

source/_posts 경로에 myfirstpost.md 생성



---

### 6. 빌드

```bash
$ hexo generate 또는 hexo g
```

+ hexo g 가능
+ public 폴더가 생성됨

![1553362948919](https://user-images.githubusercontent.com/36959292/54869839-a9026e80-4de1-11e9-8f7f-5cac8c91eaf1.png)

+ 2019 : 포스트는 날짜별로 생성
+ css : 테마에 맞게 생성
+ index.html  : myfirstpost가 변경됨



---

### 7. 로컬 테스트

```bash
$ hexo server
```

+ 내장 서버를 구동 후  **http://localhost:4000**로 접속



---

### 8. github에 업로드

```bash
$ hexo deploy 또는 hexo d
```

+ hexo d 가능



---

### 9. 블로그 방문

+ 내장서버를 종료해도 https://jhyunb.github.io/로 접속가능



---

### 10. 테마적용

+ <https://hexo.io/themes/> 에서 원하는 테마 찾기

+ github에서 다운받아 theme폴더에 저장

  ![캡처](https://user-images.githubusercontent.com/36959292/55128335-8e6c2480-5156-11e9-8fb9-1fe599fe5929.PNG)

+ hexo _config.yml 파일 theme: 변경
+ 테마마다 추가 설정이 다를 수 있으므로 해당 테마 github 확인

---

### 11. Organization을 통한 여러 사용자의 포스팅

![cap7](https://user-images.githubusercontent.com/21974799/55216796-129ad680-5241-11e9-9990-2f04f394dce2.JPG)
+ 여러 사용자가 같은 프로젝트를 관리하기 위한 그룹 계정인 Organization을 생성 한다.

![cap1](https://user-images.githubusercontent.com/21974799/55216850-3e1dc100-5241-11e9-86ba-422e557ba3bb.JPG)
+ 올려진 서버를 clone해서 받은 뒤 (이후 pull을 통해서 항상 최신 버전으로 업데이트 한다.)

![cap2](https://user-images.githubusercontent.com/21974799/55216867-54c41800-5241-11e9-8d67-9f08f4651b7e.JPG)
![cap3](https://user-images.githubusercontent.com/21974799/55216911-71605000-5241-11e9-8e63-5f3c62d10122.JPG)
![cap4](https://user-images.githubusercontent.com/21974799/55216938-850bb680-5241-11e9-8011-763c8fe24a72.JPG)
+ 위와 같은 명령어를 쳐서 필요한 것들을 받고

![cap5](https://user-images.githubusercontent.com/21974799/55217019-b97f7280-5241-11e9-9ab2-a3c723454445.JPG)
![cap6](https://user-images.githubusercontent.com/21974799/55217018-b8e6dc00-5241-11e9-84df-c4d362ea53cf.JPG)
+ 포스팅 후 배포하면 된다. (로컬 서버를 통해서 제대로 됐는지 확인하고 commit - push를 해주자.)
