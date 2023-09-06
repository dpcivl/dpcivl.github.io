---
title:  "[파이썬] 다중 상속"
excerpt: "공부하고 나니 내겐 필요없는 다중 상속..."

categories:
    - software

tags:
    - 파이썬 다중 상속
    - 다중 상속
    - C3 선형화
    - MRO

toc: true
toc_sticky: true

date: 2023-09-01
last_modified_at: 2023-09-01
---

# 다중 상속이란?  
간단히 말해서, **여러 개의 클래스로부터 기능을 상속받는 것**  
어떤 클래스가 하나 이상의 상위 클래스로부터 여러 가지 행동이나 특징을 상속받을 수 있는 것을 말한다.  
<br>
파이썬의 다중 상속은 C3 선형화(C3 Linearization) 또는 MRO(Method Resolution Order) 알고리즘을 사용하여 상속 순서를 결정한다.  
이러한 알고리즘을 사용하여서 <u>복잡한 상속 구조에서도 일관된 순서를 보장한다.</u>  
<br>

## Method Resolution Order(MRO)  
MRO는 상속 관계에서 어떤 메소드나 속성에 접근해야 할 때, 해당 메소드나 속성을 어느 클래스에서 찾아야 하는지 **순서를 정해준다.**  
<br>

### C3 선형화  
C3 선형화(C3 Linearization)는 클래스의 MRO를 결정하기 위한 알고리즘 중 하나이다.  
<u>파이썬에서는 MRO를 결정할 때, C3 선형화를 주로 사용한다.</u>  
<br>

> C3 선형화의 기본 원칙  

1. 자식 클래스를 부모보다 먼저 취한다.  
2. 부모 클래스의 순서는 클래스를 나열한 순서에 따라 달라진다.  
3. 다른 두 클래스에 공통된 부모가 있을 경우, 공통된 부모를 선택하기 전에 두 클래스를 먼저 선택한다.  

### ✅ 예제 코드  
```python
class A:
    def foo(self):
        print('A')

class B(A):
    def foo(self):
        print('B')

class C(A):
    def foo(self):
        print('C')

class D(B, C):
    pass

d = D()
d.foo()  # 출력은 'B', 왜냐하면 MRO에 따라 B가 C보다 먼저옴
```  
예제 코드에서 `D`의 MRO는 C3 선형화 알고리즘에 따라 <u>D, B, C, A 순으로</u> 정해진다.  
위의 코드의 MRO를 내 두 눈으로 직접 봐야 믿겠다 싶으면, `print(D.mro())`를 실행해서 나오는 클래스 순서를 확인하면 된다.  
<br>



- - -
> ### References  
> 1. [위키백과 다중상속](https://ko.wikipedia.org/wiki/%EB%8B%A4%EC%A4%91_%EC%83%81%EC%86%8D)
> 2. [[Python]다중상속](https://engineer-mole.tistory.com/196)