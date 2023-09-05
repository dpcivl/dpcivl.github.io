---
# 제목, 요약
title:  "[파이썬] getattr()에 대한 공부"
excerpt: "아주아주 기초적인 getattr()에 대한 공부"

# 카테고리, 태그
categories:
    - software
tags:
    - getattr
    - 파이썬 getattr

# 목차 설정
toc: true
toc_sticky: true

date: YYYY-MM-DD HH:MM:SS +09:00
---
# 개요  
**글 작성 시기 : 2023년 9월 5일**  
파이썬 코드 분석하다가 `getattr` 코드가 뭔지 몰라서 공부해봤다.  
<br>

# getattr()
파이썬의 내장 함수  
객체의 속성값을 동적으로 가져올 때 사용된다.  
<br>

## getattr() 기본 형태
```python
getattr(object, attribute_name[, default])
```  
- `object` : 속성값을 가져올 대상 객체
- `attribute_name` : 속성의 이름을 문자열로 가져온다.
- `default` : 해당 속성이 객체에 없을 경우 어떤 값을 내보낼지 정한다. 생략할 경우 `AttributeError` 발생  

<br>

## getattr() 예제 코드
```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

p = Person('John', 30)

# 정상적으로 속성 가져오기
print(getattr(p, 'name'))  # 출력: John

# 해당 속성이 없을 경우 AttributeError 발생
# print(getattr(p, 'address'))  # AttributeError: 'Person' object has no attribute 'address'

# default 값을 설정하여 해당 속성이 없을 경우 기본값 반환
print(getattr(p, 'address', 'Unknown'))  # 출력: Unknown
```  
<br>

`Person`이라는 클래스를 정의했다.  
name과 age라는 속성(attribute)이 있다.  
`Person`의 인스턴스인 `p`를 만들었고, 그 이후로는 `p`의 속성을 가져오는 내용이다.  

첫번째로는 `getattr(p, 'name')`이므로 `p`의 `name` 값인 *John*이 출력된다.  
두번째는 `getattr(p, 'address')`인데, `p`에 없는 속성이기 때문에 `AttributeError`가 뜬다.  
세번째는 `getattr(p, 'address', 'unknown')`이므로, 두번째와 같은 상황이지만 에러 메시지 대신 *unknown*을 반환한다.  