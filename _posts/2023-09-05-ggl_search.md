---
# 제목, 요약
title:  "[깃허브 블로그] 블로그 구글 노출, 네이버 노출, 빙 노출"
excerpt: "내 블로그를 모두에게 알리자!"

# 카테고리, 태그
categories:
    - trial
tags:
    - 깃허브 블로그 구글 노출
    - 깃허브 블로그 네이버 노출
    - 깃허브 블로그 빙 노출

# 목차 설정
toc: true
toc_sticky: true

date: 2023-09-05
last_modified_at: 2023-09-05
---
**작성 날짜 : 2023년 9월 5일**  

깃허브 블로그를 포털사이트에 노출시키려면 몇 가지 설정이 필요하다.  
구글 노출을 위해서는 구글 서치 콘솔,  
네이버 노출을 위해서는 네이버 서치 어드바이저,  
그 외에 다음, 빙(Bing)에도 노출 시켜줄 수 있는데,  
해당 글에서는 구글, 네이버, 빙 노출까지 시키는 방법에 대해 작성한다.  

# 구글 서치 콘솔
[구글 서치 콘솔 사이트](https://search.google.com/search-console/welcome)  
위 링크를 눌러서 구글 서치 콘솔에 접속한다.  

![image](https://github.com/dpcivl/dpcivl.github.io/assets/95332280/cd7bfc5d-d41d-4e67-9f24-c37dac0397bc)  
위의 그림처럼 오른쪽 항목인 URL접두어 항목에 자신의 깃허브 블로그 주소를 적어주고 다음 단계를 진행한다.  
<br>

## 구글 - 사이트 소유권 확인
![image](https://github.com/dpcivl/dpcivl.github.io/assets/95332280/dcc748c4-40ac-478b-b16d-6f1667f70553)  
구글이 권장하는 확인 방법은 html 파일을 다운해서 루트 디렉토리에 업로드해주는 것이다.  
다운로드 받은 파일을 루트 디렉토리에 업로드해주자.  

**🖐 푸쉬하고 나서 시간이 좀 걸린 후 확인이 되니까 참고!!**  

![image](https://github.com/dpcivl/dpcivl.github.io/assets/95332280/51fc5184-4726-44be-bf3b-fd8581059098)  
커밋하고 나서 안된다고 다시 돌아가지 말고 <u>시간을 두고 소유권 확인을 눌러주도록 하면 된다.</u>  
<br>

## 구글 - 사이트맵 제출  
소유권 확인했다고 끝이 아니라 **sitemap을 설정해줘야 한다.**  

> sitemap이 뭐야?  

웹사이트의 구조와 구성 요소들(페이지나 문서 등)을 표현한 목록  

![image](https://github.com/dpcivl/dpcivl.github.io/assets/95332280/084d1b6b-166d-4968-9648-f8990d734fa6)  
소유권 확인이 끝나면 좌측 사이드바에 Sitemaps라는 탭이 있다.  
탭을 누르면 *새 사이트맵 추가*라는 항목이 있는데, 여기에 자신의 url 뒤에 `sitemap.xml`만 적어서 *제출*을 눌러주면 된다.  
제출된 사이트맵 목록이 뜰텐데, **상태가 성공으로** 뜬다면, 다음 단계로 넘어가면 된다.  
<br>


# 네이버 서치 어드바이저
[네이버 서치 어드바이저 들어가기](https://searchadvisor.naver.com/console/board)  

네이버 노출을 위해 위의 링크를 눌러서 네이버 서치 어드바이저로 들어가준다.  

## 네이버 - 사이트 등록
위의 링크에 접속했다면, 사이트 등록 화면이 보일 거다.  
여기에 자신의 블로그 주소를 입력해주면 된다.  
<br>

## 네이버 - 사이트 소유확인
![image](https://github.com/dpcivl/dpcivl.github.io/assets/95332280/7f3663a5-7d58-435f-98e2-5063f9d4fe87)  
들어가보니까 구글 서치콘솔에서 했던 것처럼 html 파일 업로드 방식을 권장한다고 나와있다.  
이것 또한 단계대로 html 확인 파일을 다운로드하고, 루트 디렉토리에 업로드 해준 뒤 소유 확인을 해주자.  

이 과정 역시 커밋하고 푸쉬한 뒤 시간이 좀 지나서 소유 확인이 가능하다 🙂  
![image](https://github.com/dpcivl/dpcivl.github.io/assets/95332280/698aceb2-7405-4ca3-9e29-55aad0e4d765)  
<br>

## 네이버 - 사이트맵 제출
소유 확인을 한 후 사이트 목록에 있는 나의 블로그 사이트 주소를 클릭해서 들어간다.  

![image](https://github.com/dpcivl/dpcivl.github.io/assets/95332280/ed697d5a-3a42-413a-a3eb-9caea3ac845b)  
위의 사진처럼 사이트맵 제출을 누르고 아까 구글 서치콘솔에 해줬던 것과 같이 sitemap.xml을 제출하면 네이버도 완료됐다.  

마지막은 빙 검색인데, 내 블로그는 개발 블로그라서 *빙에도 노출이 되면 사람이 오지 않을까?* 해서 등록하는 거라 빙에 굳이 노출시켜서 블로그 품질 저하될 가능성을 높이고 싶지 않다면 여기까지만 하면 된다.   

# 마이크로소프트 빙 웹 마스터 도구
[Bing 웹 마스터 도구 접속하기](https://www.bing.com/webmasters)  

위의 링크를 타고 Bing 웹 마스터 도구로 들어간다.  

![image](https://github.com/dpcivl/dpcivl.github.io/assets/95332280/a4e096e7-550d-45bd-8e81-127085e675bf)  

위의 화면처럼 뜨는데 구글 서치콘솔 인증을 이미 마쳤으니까 왼쪽의 *가져오기*를 이용해서 쉽게 가져와보자.  
*가져오기* 버튼을 누르면 **구글 서치콘솔을 등록했던 계정으로 로그인하고 연동만 해주면** 아래와 같은 화면이 보인다.  

![image](https://github.com/dpcivl/dpcivl.github.io/assets/95332280/5683d306-354d-4283-8827-69a6922b332f)  
겁나 간단하다..!! 👍👍  
해당 화면의 우측 하단에 *가져오기* 버튼이 있는데 그걸 누르면 설정이 완료된다.  

## 빙 - 사이트맵 제출
구글 서치콘솔에서 가져오기를 했다면 사이트맵도 자동으로 제출되어 있다.. ~~개꿀~~  

![image](https://github.com/dpcivl/dpcivl.github.io/assets/95332280/9dd2fea8-e4a3-4165-bc8c-7042505e7cd0)

- - -
> References  
> 1. [Google 검색 엔진과 애널리틱스 등록하기](https://devinlife.com/howto%20github%20pages/google-search-console-and-analytics/)