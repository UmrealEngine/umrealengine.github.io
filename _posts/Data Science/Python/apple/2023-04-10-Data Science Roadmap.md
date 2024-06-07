---
layout: single
title: Python Syntax
tag: Data Science Roadmap
author_profile: false
use_math: false
date: 2023-04-10
---

[^]: python 기초 DS

<style>
  textarea {
    background-color: #272822;
    border: 2px solid #272822;
    border-radius: 4px;
    color: #ffffff; /* 글자 색상 추가 */
    padding: 5px;
  }
  textarea:focus {
    border-color: #555;
    outline: none;
  }
  .code-wrapper {
    padding: 16px;
    border-radius: 8px;
  }
</style>
<br/>

<br/>

<br/>

📌

문자열 "2" 

정수형 2

소수형 2.0

모두 다른거

<br/>

<br/>

<br/>

<br/>

📌함수 

```python
def 인사():         
	print("hi")
	print("hello")
    
인사()
```

<pre>
hi
hello
</pre>

def == 함수

인사() == 함수 이름

print("hi"),print("hi") == 실행값

<br/>

<br/>

<br/>

<br/>

📌 **1개 파라미터**

```python
def 인사(day):
	print(day)
	print("hi")
	print("hello")

인사(10)
```

<pre>
10
hi
hello
</pre>

**10** -> 인사(**day**) -> print(**day**)

<br/>

<br/>

<br/>

<br/>

📌 **파라미터 여러개**

```python
def sum(a, b, c):
    (a + b + c)
    
sum(1, 2, 3)
```

<pre>
6
</pre>

<br/>

<br/>

<br/>

<br/>

📌 **return**

```python
def test(x, y):
    return x * y       # 함수를 실행하고 return 옆에 값을 가죽으로 남겨라 

test(3, 4)        # 3이 x로 들어가고 4는 y로 들어간 후 return으로 내려간 후 실행 -> x * y -> 3*4가 남는거 
print(test(3, 4) + test(1, 2))
```

<pre>
12
14
</pre>
<br/>

<br/>

<br/>

<br/>

📌 **숫자형**

```python
#덧셈
print(2 + 3)
#소수 덧셈
print(2.0 + 3.0)

#뺄셈
print(2 - 3)
#소수 뺄셈
print(2.0 - 3.0)

#곱셈
print(2 * 3)
#소수 곱셈
print(2.0 * 3.0)

#나머지
print(5 % 2)
#소수 나머지
print(5.0 % 2.0)

#거듭제곱 
print(2 ** 3)
#소수 거듭제곱
print(2.0 ** 3.0)

#나누기
print(4 / 2) #출력 2.0     정수 나눗셈이라도 소수로 나옴
print(4.0 / 2)

# floor division(버림 나눗셈 == 몫만 남김)

print(3 // 2)
print(3 / 2)

#버림 나눗셈도 하나라도 소수형이면 소수형으로 결과값이 나옴
print(5.0 // 2.0)
print(5.0 // 2)


#round (반올림)

print(round(3.123456))

print(round(3.23456, 2)) #소수 두번째 자리 반올림 하고 싶은 경우
```

<pre>
5
5.0
-1
-1.0
6
6.0
1
1.0
8
8.0
0.6666666666666666
2.0
1
1.5
2.0
2.0
3
3.23
</pre>

정수 정수  == 정수

소수 소수 == 소수

정수 소수 == **소수**

<br/>

<br/>

<br/>

<br/>

📌 **문자열**

```python
print("안녕하세요 저는 \"su\" 입니다")
```

`\ "`  이렇게 쓰면 따옴표로 인식



<br/>

<br/>

<br/>

<br/>

📌 **형 변환**

**int** 정수
**float** 소수
**str** 문자형

<br/>

```python
print(int(1) + int(2)) #출력: 3.0
print(str(1) + int(2)) #출력: 12
```

<br/>

```python
price = 700
print("물건의 가격은" + price + "임") # xxxxx

price = 700
print("물건의 가격은 " + str(price) + " 임") #출력: 물건의 가격은 700 임
```

<br/>

<br/>

<br/>

<br/>

📌  **format**

```py
price = 700
quantity = 3

print("오늘 커피 가격은 " + pricer + "에" + quantity + "개" +" 를 드립니다.")
```

price , month , quantity 는 정수형이라 다른 문자형이랑 합쳐지지 않음

<br/>

```python
print("오늘 커피 가격은 " + str(pricer) + "에" + str(quantity) + "개" +" 를 드립니다.")
```

이렇게 하기엔 너무 번거롭

<br/>

```py
print("오늘 커피 가격은 {}에 {}개를 드립니다.".format(price, quantity))
```

<pre>
오늘 커피 가격은 700에 3개를 드립니다.
</pre>

**format**을 활용하여 이런식으로 가능 

<br/>

```python
Example = "오늘 커피 가격은 {}에 {}개를 드립니다."
print(Example.format(price, quantity))
```

이렇게도 가능 

<br/>

<br/>

🧩

```python
print("{}, {} ,{} 안녕".format("a", "b", "c")) 


print("{2}, {1} ,{0} 안녕".format("a", "b", "c"))
```

<pre>
a, b ,c 안녕
c, b ,a 안녕
</pre>

<br/>

<br/>

🧩

```python
print("{}년도엔 {}살 입니다".format(2023, 3.11111111))
```

<pre>
2023년도엔 3.11111111살 입니다
</pre>

<br/>

`:.3f`

f == 소수

.2 == 소수점 세번쨰에서 반올림 하라

:.0f 정수 

```python
print("{}년도엔 {:.0f}살 입니다".format(2023, 3.11111111)) 
```

<pre>
2023년도엔 3살 입니다
</pre>

<br/>

<br/>

<br/>

<br/>

📌 **f-string**  (format의 새로운 방식)

```python
price = 700
name = "딸기스무디"

print(f"{name}의 가격은 {price} 입니다")

print("{}의 가격은 {} 입니다".format(name, price))
```

<pre>
딸기스무디의 가격은 700 입니다
딸기스무디의 가격은 700 입니다
</pre>

<br/>

<br/>

<br/>

<br/>

💻

```python
wage = 2  # 시급 (1시간에 2달러)

exchange_rate = 1234.56  # 환율 (1달러에 1234.56원)
```

<br/>

<br/>

<pre>
나는 1시간에 4달러 받는다.    
</pre>

```python
print("나는 {}시간에 {}{} 받는다.".format(1, wage * 2, "달러"))

print(f"1 시간에 {wage*2}달러 받는다.")
```

---> 

f-string에서 {}를 유지한채로 하려먼 아예  이렇게 바꿔야할듯

```py
wage = 2 
exchange_rate = 1234.56
hour = 1

print(f"나는 {hour}시간에 {wage*2}달러 받는다.")
```

<br/>

<br/>

<pre>
나는 1시간에 2469.12원 받는다.    
</pre>

```python
print("나는 {}시간에 {}원 받는다".format(1, wage * exchange_rate))
print(f"나는 1시간에 {wage * exchange_rate}원 받는다")
```

<br/>

<br/>

<pre>
나는 2시간에 4938.24원 받는다. #소수 두번쨰
</pre>

```python
print("나는 {}시간에 {:.2f}원 받는다.".format(2, wage * 2 * exchange_rate))
print(f"나는 2시간에 {wage * 2 * exchange_rate:.2f}원 받는다.")
```

<br/>

<br/>

<br/>

<br/>

📌 **True,False**

<br/>

① <span style=" background: linear-gradient(to top, #9acfc9 100%, transparent 10%)"><span style="color:black">and</span></span>

a = True

b = True

a and b -> True

<br/>

a = True

b = False

a and b -> False

<br/>

a =False

b = False

a and b -> False

> 모두 True 일때만 True

<br/>

<br/>

② <span style=" background: linear-gradient(to top, #9acfc9 100%, transparent 10%)"><span style="color:black">or</span></span>

> 하나라도 참이면 Ture

<br/>

<br/>

③ <span style=" background: linear-gradient(to top, #9acfc9 100%, transparent 10%)"><span style="color:black">not </span></span>

반대로 만들어 준다?

<br/>

ex) 

not 딸기는 과일이다(True)

-> 딸기는 과일이 아니다 (False)

<br/>

not 딸기는 육류이다(False)

->딸기는 육류가 아니다(True)

<br/>

<br/>

🧩

`?=`      <- 같지 않다

```python
print(1 ?= 1)
```

<pre>
False
</pre>

<br/>

<br/>

🧩

```python
a = 5


print(a == 4 or not (a > 2 or a < 3))
```

<pre>
False
</pre>

> ㅡㅡㅡㅡㅡㅡㅡㅡㅡ
>
> a > 2   ----> True
>
> a<3  -----> False
>
> True or False  ---> True
>
> not True  ------> False
>
> ㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡ
>
> a == 4   ----> False
>
> ㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡㅡ
>
> False or False  -------> False

<br/>

<br/>

<br/>

<br/>

📌 **=**

`=`는 수학적 의미인 같다 라는 뜻이 아님

오른쪽의 값을 왼쪽으로 지정해주는 기호임 

```python
a = 10

a = a + 3 
```

<pre>
13
</pre>

> a 가 +3 됬다 ~ 라는 뜻으로 알면 될듯

<br/>

<br/>

<br/>

<br/>

📌 **return 역활**

1. 가죽남김(값을 돌려줌)
2. 함수를 끝냄

```python
def test(x):
    print("start")
    return x + x
    print("end")
    
    
print("aaaaaa")
print(test(3))
print("bbbbbb")
```

<pre>
aaaaaa
start
6
bbbbbb
</pre>


리턴즉시 함수를 끝냄

<br/>

<br/>

<br/>

<br/>

📌📌📌📌📌 **return** vs **print**

<br/>

**print**는,

그저 값을 **출력**할 뿐, 컴퓨터가 이 값을 가지고 무얼 하진 못한다.

변수가 어떤 값을 가지는지 사용자 측에서 편하게 보기 위함이지 함수에는 전혀 영향을 끼치지 않는다.

<br/>

**return**은,

함수가 값을 **반환**하는 가장 주된 방법이다.

모든 함수는 어떠한 값을 return하며, 이 return(혹은 yield)이 명시되어 있지 않은 경우에는 None을 return한다.

이 반환된 값은 다른 함수에서 사용될 수 있으며 변수에 저장될 수도 있다.

<br/>

함수내에 return 이 정의되어 있지 않거나,

 return 을 실행할 수 없는 경우

 파이썬은 내부적으로 함수의 가장 마지막 줄에 return None 이 있다고 가정하고 None 을 반환

<br/>

```python
def print_square(x):
    print(x * x)

print(print_square(3))
```

함수를 중첩해서 사용할 경우 괄호 안의 함수를 먼저 실행한 다음 그 바깥의 함수를 실행

그러므로 

1.print_square(3) - >def ~~~ print(x * x)  #출력: 9 -> 9 출력 

2.괄호안의 함수가 실행되고 없으니 print(none) 이 들어가 있게됨 

3.그러므로 출력이 9, none 이런식으로 나온다

<br/>

근데 이제 **return**은 **가죽**을 남긴다고 했잖슴 그러니깐

```python
def print_square(x):
    return x * x

print(print_square(3))
```

1. print_square(3)  ->  def~~  return 3 * 3 = 9  -> print_square(3)이 가죽인 9를 남김
2. print(print_square(3)) -> print(9)

> 참고:https://potettangee.github.io/Python-Basic-Syntax-ap-1/

<br/>

<br/>

<br/>

<br/>

📌 **옵셔널 파라미터** 

기본값(default value)을 설정하여 파라미터에 값을 전달하지 않아도 기본값으로 설정된 값이 할당되도록 하는 파라미터

```python
def m(name, price, Spiciness="강"):
    print("주문할 메뉴는 {}입니다".format(name))
    print("가격은 {} 짜리로 주시고".format(price))
    print("맵기는 {} 부탁드려요".format(Spiciness))


m("떡볶이", 500, "하")  # 값 설정
m("떡볶이", 1)  # 값 설정 x
```

> 옵셔널 파라미터는 마지막에 와야함 
>
> m("떡볶이", 1)
>
> m("떡볶이", 500, "하")  
>
> 이렇게 하면 오류남

<br/>

<br/>

<br/>

<br/>

📌 **syntactic sugar**

```py
a = a + 1
a += a 

a = a - 1
a -= 1
```

이런식으로 줄여서 쓸 수 있음 , 나머지도 다 가능

<br/>

```python
3 -= 3  #xxxxxxxx
```

정수는 불변 자료형

이런건 아님

<br/>

<br/>

<br/>

<br/>

📌 **scope** (변수 사용 가능한 범위)

```python
def m():
    x = 2
    print(x)
    
m()
print(x)
```

<pre>
2
error
</pre>

> 함수내에서 정의한 변수는 로컬변수라고 부르고 함수 내에서만 사용 가능한 변수임



<br/>

<br/>

```python
x= 1

def m():
    x = 2
    print(x)
    
m()
print(x)
```

<pre>
2   #로컬변수꺼 가져옴 / 로컬변수가 먼저임
1   #글로벌 변수꺼 가져옴
</pre>

`x= 1` 요놈은 글로벌 함수, 전체 사용 가능

<br/>

<br/>

```python
y= 1

def m():
    x = 2
    print(x + y + 3)
    
m()
print(y)
```

<pre>
6
1
</pre>

<br/>

<br/>

```python
def test(x):
    return x + x

print(test(1))
```

파라미터도 사실 로컬변수

<br/>

<br/>

<br/>

<br/>

📌 **상수**

```python
PRICE = 300

def Information(a)
	return a + b
```

바꾸지 않을 설정 값 = **상수** 

-> 모두 대문자로 표현해야함 

코드의 가독성을 높일 수 있고, 상수 값이 다른 변수와 구분되어 보다 명확하게 표현됨

<br/>

수정을 못하진 않음, 근데 바꾸지 않을꺼라는 약속을 하는거임

<br/>

<br/>

<br/>

<br/>

🧩

```python
def test(number):
    return bool(1 in number)

print(test(1))
print(test(2))
print(test(3))
print(test(11))
print(test(111))
```

<pre>
Error
</pre>

정수형이나 소수형은 in 연산자를 사용하여 직접 요소를 찾을 수 없음

```python
def test(num):
    return bool('1' in str(num))

print(test(1))
print(test(2))
print(test(3))
print(test(11))
print(test(111))
```

<pre>
True
False
False
True
True
</pre>

> 하지만 문자열, 리스트, 튜플, 딕셔너리 등의 컬렉션 타입에 대해서는 in 연산자를 사용하여 해당 요소가 있는지 확인할 수 있음

<br/>

<br/>

<br/>

<br/>

📌 **while 반복문**

<br/>

```python
while 조건(불린값):
    반복 실행
```

조건 **true** -> 수행 부분 **실행** -> 조건부분 **true** -> 수행부분 **실행** -> 조건부분 **false** -> **끝**

<br/>

ex) 5번만 출력을 하고 싶을때

```python
x = 1
while x <= 5:
    print("hello world")
    x += 1
```

반복문 될때마다 x의 값이 1씩 증가하게 됨 

그러다가 x가 6이 되면  `x <= 5`의 값이 False가 되니깐 반복문이 종료됨

<br/>

ex) 1 ~ 100까지 출력 

```python
x = 1

while x <= 100:
	print(x)
	x += 1
```

이렇게 주면 

x= 1이 먼저 print가 되고

x+1이 뒤에 되니깐 1~100까지만 출력됨 

그런데

```python
x = 1

while x <= 100:
	x += 1
	print(x)
```

이렇게 주면 2~101까지 출력됨 

왜? 

`100 <= 100` **True**

`100 + 1 = 101`

`print(101)`

이렇게 되니깐

<br/>

처음에 print가 먼저 오는 코드는

```python
x = 1

while x <= 100:
	print(x)
	x += 1
```

`100 <= 100` **True**

`print(100)` 이 된다음

100 + 1 = 101 이 되는거니깐

`101 <= 100` **False**

바로 걸러짐

<br/>

🚀 **while 중첩 문제**

**Q.** 1 * 1 = 1  .....  9 *9  출력값이 나오도록 코드를 짜라

```python
a = 1

while a <= 9:
    b = 1
    while a <= 9:
        print("{} * {} = {}".format(a, b, a * b))
        a += 1
    a += 1
```

> while 내부에서 false 나오기 전 까지 뻉뻉이 한다는것만 좀 더 신중하게 생각했음 쉽게 했을듯

<br/>

<br/>

<br/>

<br/>

📌 **break**

<br/>

while의 False 상관없이 while문 탈출

```python
a = 1

while a <= 5:
    print(a)
    a += 1
    break
```

<pre>
1
</pre>

<br/>

<br/>

<br/>

<br/>

📌 **continue**

```python
a = 1

while a <= 100:
	a += 1
    
    if a % 2 == 0:
    	continue
    print(a)
```

이렇게 입력하면 

2의 배수일떄는 print로 넘어가지 않고 바로 조건부분으로 돌아가기 때문에

<pre>
3
5
7
...
</pre>

이런식으로 출력이 나오게 된다

<br/>

<br/>

<br/>

<br/>

📌 **if, else**

<br/>

```python
if 조건(불린):
    실행
else:
    실행
```

ex)

```python
clock = 15

if clock >= 10:
	print("밥")
else:
    print("공부")
```

<br/>

<br/>

<br/>

<br/>

📌 **elif**

if  + else  합친거 

코드를 조금 더 간단하게 하기 위해서 

```python
if 90 < x:
    print("1등급")
else:
    if 80 < x:
        print("2등급")
    else:
        if 70 < x:
            print("3등급")
        else:
            print("4등급")
```

이 코드를 elif로 대체 가능

````python
if 90 < x:
    print("1등급")
elif 80 < x:
	print("2등급")
elif 70 < x:
	print("3등급")
else:
	print("4등급")
````

좀더 복잡하게

```python
def grade(one, two):
    grade = one + two
    if grade > 90:
        print("1등급")
    elif grade > 80:
        print("2등급")
    elif grade > 70:
        print("3등급")
    else:
        print("4등급")

grade(10, 71)
```



<br/>

<br/>

<br/>

<br/>

📌 **list**

```python
a = [1, 2, 3, 4]

print(a[0:3]) 
```

<pre>
[1, 2, 3]
</pre>

<br/>

리스트 값 바꾸기

```python
a = [1, 2, 3, 4]

a[0] = 222

print(a)
```

<pre>
[222, 2, 3, 4]
</pre>

<br/>

<br/>

🧩  **list 함수**

<br/>

리스트 안에 총 몇개 있는지

```python
a = []
len(a)
```

<br/>

값 추가 (가장 우측에 들어감)

```python
a.append(1) #[1]
a.append(2) #[1, 2]
```

<br/>

삭제

```python
b = [1, 2, 3, 4, 5, 6, 7, 8, 9]

del b[1]  # n번째 삭제 , [1, 3, 4, 5, 6, 7, 8, 9]
```

<br/>

원하는 위치에 값 삽입

```python
a.insert(0, 99)  # 0번쨰에 99를 삽입 한다 # [99, 3, 4, 5, 6, 7, 8, 9]
```

<br/>

<br/>

🧩  **list 정렬**

```python
a = [1, 4, 6, 2, 3]

new_a = sorted(a)  #오름차순 [1, 2, 3, 4, 6]
new_a = sorted(a, reversed=True) #내림차순 [6, 4, 3, 2, 1]
print(a) # [1, 4, 6, 2, 3]

#sorted는 기존의 값을 건들이지 않음, 새로운 리스트를 만듬


print(a.sort())  #출력: none  #sort는 따로 출력을 하는게 아니라 본래꺼 정렬만 시킴

print(a) #출력:[1, 2, 3, 4, 6] #a.sort()를 하고 print(a)를 해주면 본래께 정렬된걸 볼 수 있다.
```



`sorted`      <---- 기존꺼를 안 걸들이고, 새로운걸 정렬 후 리턴해줌

`sort`      <----  기존 리스트를 정렬 시킴, 따로 리턴은 없어서 따로 기존 리스트를 print 해줘야 확인 가능  
