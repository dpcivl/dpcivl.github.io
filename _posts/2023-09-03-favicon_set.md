---
# 제목, 요약
title:  "[깃허브 블로그] 깃허브 블로그 파비콘 설정"
excerpt: "깃허브 블로그에 파비콘을 설정해보자!!"

# 카테고리, 태그
categories:
    - blog
tags:
    - 깃허브 블로그 파비콘
    - minimal-mistakes 파비콘

# 목차 설정
toc: true
toc_sticky: true

date: YYYY-MM-DD HH:MM:SS +09:00
---
### 개요
**작성날짜 : 2023-09-03**

오늘은 minimal-mistakes에서 어떻게 파비콘을 설정하는지에 대해 구현해보고 글을 작성한다.  
사실 예전에 파비콘 설정을 했는데 계속 안 돼서 다시 구현하면서 글을 써보려고 한다.  
✅참고사항 : minimal-mistakes 테마에서는 바로 적용 가능하나, 다른 테마에서는 적용이 가능할지 모르겠다.  
<br> 

# 😎 파비콘 생성하기
## 파비콘 생성 사이트 접속
파비콘을 생성해주기 위해서 [Favicon Generator](https://realfavicongenerator.net/)에 접속한다.  
<br>

## 파비콘 이미지 업로드
![image](https://github.com/dpcivl/dpcivl.github.io/assets/95332280/e6f3a775-927f-4312-9c14-55def60c2cd2)  
접속하면 위와 같은 화면이 뜬다. `Select your Favicon image`를 눌러준다.  
파비콘 이미지는 본인이 준비한 이미지를 골라서 로드해주면 된다.  

나는 아래와 같이 내가 만든 허접한 마스코트인 handy로 준비했다.  
그림이 성공적으로 로드됐다면, `Continue with this picture`를 눌러준다.  

## html 코드 생성하기  
위의 과정을 거쳤다면, 다음 화면에서 데스크탑 브라우저를 위한 파비콘, iOS를 위한 파비콘 등등을 보여주는데 다 무시하고 맨 아래에 있는 `Generate your Favicons and HTML code`를 눌러준다.  

## 파비콘 설정하기
이 과정까지 잘 따라왔다면, 아래 화면이 표출될 거다.  
![image](https://github.com/dpcivl/dpcivl.github.io/assets/95332280/6e296f7b-b9cc-4c78-bafa-40cdeedf2be4)  

### 1. 파비콘 패키지 다운로드
화면에 보이는 1번 항목의 지침처럼 `Favicon package` 버튼을 눌러서 파비콘 패키지를 다운로드 받는다.  

### 2. 파비콘 패키지 압축 풀기
1번 과정에서 받은 압축 파일을 자신의 사이트 폴더에 압축 풀기를 해주면 된다.  
쉽게 생각해서, username.github.io 경로에 압축 풀기를 해주면 된다고 생각하면 된다.  
나같은 경우에는, dpcivl.github.io/favicon.ico가 가능하도록 압축 풀기를 진행했다.  

### 3. head/custom.html에 코드 적용하기
![image](https://github.com/dpcivl/dpcivl.github.io/assets/95332280/f3cb5431-c6df-48ea-a3d5-34389bc2fcb3)
*custom.html*에 들어가면 위와 같이 적용이 되어있을 거다. ~~font 적용 빼고...~~
저기 보면 `insert favicons`라고 하는 코멘트가 있는데 그 밑에 소스 코드를 넣으면 된다.  
아 소스 코드는 파비콘 사이트의 3번 항목에 있는 코드를 복붙해서 넣어주면 된다.  
> 혹시나 안 보인다면..??  

![image](https://github.com/dpcivl/dpcivl.github.io/assets/95332280/5feb3ad3-c869-4918-90dd-69c72862c2d6)  
`href`의 경로를 위의 사진처럼 변경해준다. (baseurl 항목 추가)  
여기까지 하면 파비콘 설정은 끝이 난 것이다.

### 추가) 파비콘 적용 확인
파비콘 적용은 로컬 환경에서는 확인이 힘드므로, 커밋 완료 후 사이트에서 확인을 해야 한다.  
커밋을 하고 난 후, 파비콘 패키지를 다운로드 받았던 페이지의 4번 항목 `Check your favicon` 버튼을 눌러서 확인을 하거나, 파비콘 생성기 사이트의 홈 화면에서 체크를 해줄 수도 있다.  

![image](https://github.com/dpcivl/dpcivl.github.io/assets/95332280/e30881ac-8211-4f4b-86b9-f470424f96a6)  
위와 같이 파비콘 체커에서 사이트 주소를 넣고 확인해주면, 다양한 환경에서 파비콘이 적용되고 있는지 확인할 수 있다. 

# 끝