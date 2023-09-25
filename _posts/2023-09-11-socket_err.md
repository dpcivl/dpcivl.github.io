---
# 제목, 요약
title:  "TypeError: an integer is required (got type str)"
excerpt: "파이썬으로 소켓 통신 구현할 때 자주 발생하는 에러"

# 카테고리, 태그
categories:
    - error
tags:
    - 파이썬 소켓 통신 에러

# 목차 설정
toc: true
toc_sticky: true

date: 2023-09-11
last_modified_at: 2023-09-11
---
파이썬으로 소켓 통신을 구현해보다가 아래와 같은 에러가 발생했다.  

![image](https://github.com/dpcivl/dpcivl.github.io/assets/95332280/ab927a79-4b39-4e4b-b61d-d34c62ae35dd)  

위와 같은 에러가 발생했을 때, **3가지 해결 방법**이 있다.  
<br>

# 포트 번호를 int 형으로 변경
```python
HOST = '127.0.0.1'
PORT = '30000'
```  

위와 같은 코드가 있다고 가정한다면, `HOST`는 맞게 입력해줬지만, `PORT`는 *int*가 아닌 *str*로 입력했음을 알 수 있다.  
port 값은 *int*형으로 전달해야 하기 때문에 아래와 같이 고쳐준다.  

```python
HOST = '127.0.0.1'
PORT = 30000
```  
<br>

# `send`나 `recv` 함수의 버퍼 크기를 문자열로 지정한 경우
> `send` 함수? `recv` 함수?  

## `send` 함수
`send` 함수는 서버나 클라이언트가 데이터를 전송할 때 사용된다.  
**전송하려는 데이터는 바이트 객체로 전달해야 한다.**  

## `recv` 함수
`recv` 함수는 서버나 클라이언트가 데이터를 수신할 때 사용된다.  
이 함수는 한 번에 수신할 수 있는 최대 바이트 크기를 argument로 전달해야 하며, 수신된 데이터를 바이트 객체로 반환한다.  

위의 내용을 토대로 잘못된 코드와 올바른 코드는 아래와 같다.  
```python
# 잘못된 예
data = conn.recv("1024")

# 올바른 예
data = conn.recv(1024)
```  
<br>

# `listen` 함수에 문자열을 전달한 경우
서버 측에서 클라이언트의 접속을 기다리는 `listen` 함수를 사용할 때도 *int*형으로 전달되어야 한다.  
```python
# 잘못된 예
s.listen("5")

# 올바른 예
s.listen(5)
```  
<br>

내가 겪은 에러는 위의 경우에서 **데이터를 바이트 객체로 보내지 않아서 발생**한 것으로 확인됐다.  