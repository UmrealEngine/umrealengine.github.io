---
layout: single
title: Python Syntax (1)
tag: python
author_profile: false
use_math: false
---

[^]: python 기초 DS

<style>
  textarea {
    background-color: #272822;
    border: 2px solid #272822;
    border-radius: 4px;
    color: #ffffff;
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
  u2 {
    text-decoration: underline;
    text-decoration-color: #ff0080;
  }
  u3 {
    text-decoration: underline;
    text-decoration-style: wavy;
    text-decoration-color: #ff0080;
    text-decoration-thickness: 2px;
  }
</style>

<br/>

<br/>

<br/>



<u2>ddd</u2>

📌 **파이썬 규칙**

1. 키워드 사용 x

   ```python
   1a = 1   #출력: error
   ```

2. 특수문자 _만 허용

3. 숫자 시작 x

   ```python
   1a = 1   #출력: error
   a2 = 1   #출력: 1
   ```

4. 공백 포함 x

   ```python
   people name = 1 #출력: error
   
   people_name = 1 #출력: 1 / 공백을 _로 교체하면 됨 약속임
   PeopleName = 1  #공백에 _를 주거나 대문자로 변경후 결합 하자는 약속
   ```

<br/>

<br/>

📚

**스네이크 케이스**

people_name = 1

공백을 _로 교체

<br/>

**캐멀케이스**

PeopleName

대문자로 변경 후 합침

<br/>

이렇게 하는 이유?

캐멀 케이스(대문자 시작) -> 클래스

스네이크 케이스(소문자 시작) -> **1.** 뒤에 괄호 o -> 함수 or  **2.** 뒤에 괄호 x -> 변수

<br/>

<br/>

<br/>

<br/>

📌 **/**

일반적으로

**정수 정수 = 정수** 라고 나오는데

`/` 이놈은 **소수**로 나옴

```python
4 / 2 #출력:2.0
```

> // (정수 나눗셈) 이렇게 해야 `#출력: 2` 로 나옴

<br/>

ex)

```python
10 / 3   #출력: 3.333333333
10 // 3   #출력: 3
10.0 // 3.0  #출력: 3.0  , 이건 안 떼주니깐 주의 , 근데 이놈도 소수 섞이면 소수로 출력
```

이렇게 나오니깐 주의

<br/>

<br/>

<br/>

<br/>

📌 **루트**

무엇을 제곱했을때, 이게 나옴 ?

<br/>

√4 = 2

```python
4 ** (1/2) #출력: 2.0
```

<br/>

3√8  

```python
8 ** (1/3) #출력: 2.0
```

<br/>

4√16

```py
16 ** (1/4) #출력: 2.0
```

<br/>

<br/>

<br/>

<br/>

📌 **input**()

```python
input("입력:")
```

<pre>
입력: (((여기에 입력창 뜸)))
</pre>

<br/>

`입력:`   에 `하이` 라고 입력 했다면

`input("입력:")`   -> `하이` 호출한 전체가 입력된걸로 바뀜

<br/>

```python
print(input("입력:"))    
```

<pre>
입력:하이
하이
</pre>

```python
a = input("입력:")
print(a)
```

<pre>
입력:하이
하이
</pre>

<br/>

input 함수의 호출에 어떤걸 입력하든 결과의 타입은 무조건 **문자열** 임

```python
a = input("입력:")
print(type(a))   

#출력: 입력:하이
#      <class 'str'>
    
b = input("입력:")
print(type(b)) 

#출력: 입력:1
#      <class 'str'>
```

<br/>

계산기를 만든다고 했을떄 `int()` 나 `float()`로 묶어 줘야함

```python
a = input("계산기1: ")
b = input("계산기2: ")

a = int(a)
b = int(b)

print(a + b)
```

<pre>
계산기1: 1
계산기2: 2
3   
</pre>
<br/>

<br/>

<br/>

<br/>

📚 **input을 사용해 inch -> cm 변환**

```python
a = input("ich 단위 숫자: ")

a= float(a) * 2.54

print(a,"cm")
```

```python
a = float(input("ich 단위 숫자: ")) * 2.54
print(a,"cm")
```

<br/>

<br/>

<br/>

<br/>

📌 **변수 교체 swap**

Q.  

```python
a = input("1번: ") #입력: aaaaaaaa  
b = input("2번: ") #입력: bbbbbbbb

print(a, b)

#????

print(a, b)
```

<pre>
aaaaaaaa bbbbbbbb
bbbbbbbb aaaaaaaa
</pre>

<br/>

첫번째 방법

```python
c = a
a = b
b = c
```

<br/>

두번쨰 방법

```python
a , b = b, a
```

<br/>

<br/>

<br/>

<br/>

📌 **format**

```py
a = "수"
b = 10

print("저의 이름은 {} 입니다, 나이는 {}입니다.".format(a , b))
```

<br/>

📚

```python
print("{:d}".format(11))
print("{:5d}".format(11))     # 5칸 공백
print("{:10d}".format(11))    # 10칸 공백
print("{:010d}".format(11))   # 0을 10칸 채움
```

<pre>
11
     11    
          11
000000000011
</pre>

<br/>

```python
print("{:f}".format(11))     #소수점 출력
print("{:.1f}".format(11))   #1번쨰 소수까지 출력
print("{:.1f}".format(11.111)) # 자동으로 반 올림함
```

<pre>
11.000000
11.0
11.1
</pre>

이런게 있구나 ~ 

필요할때 찾아서 사용하면됨



<br/>

<br/>

<br/>

<br/>

📌 **split**

```python
print("1 2 3 4".split(" "))
print("1-2-3-4".split("-"))
```

<pre>
['1', '2', '3', '4']
['1', '2', '3', '4']
</pre>

문자열 하나를 잘라서, 리스트에 여러개의 문자열을 만든다

<br/>

<br/>

<br/>

📌 **f 문자열**

```python
a = "수"
b = 10

print("저의 이름은 {} 입니다, 나이는 {}입니다.".format(a , b))
```

==

```python
a = "수"
b = 10

print(f"저의 이름은 {a} 입니다, 나이는 {b}입니다.")
```

<br/>

f 문자열은 여러줄 문자열에서도 사용 가능

```python
a = "안녕"
b = "hi"

print(f'''{a}
반갑
{b}
''')
```

<pre>
안녕
반갑
하이
</pre>

<br/>

```python
a = input("숫자1: ")
b = input("숫자2: ")

print("{} 와 {}을 더하면 {}이 나옵니다.".format(?????))
```

<pre>
2 와 1을 더하면 3이 나옵니다.
</pre>

그냥 `format(a, b, a+b)`라고 주면 xxx

input은 str 출력임 

```python
a = input("숫자1: ")
b = input("숫자2: ")

print("{} 와 {}을 더하면 {}이 나옵니다.".format(a, b, int(a)+int(b)))
```

<br/>

<br/>

<br/>

<br/>

📌 **파괴적, 비파괴적 연산**

```python
a = 1

a + 2

print(a)
```

<pre>
1
</pre>

`a = a + 2` 라고 할당을 안 해줬기 때문에

<br/>

<br/>

<br/>

<br/>

📌 **strip()**

문자열 양쪽에 공백을 제거

```python
a = "     \t\n      가           "

a = a.strip()

print(a)
```

<pre>
"가"
</pre>

<br/>

왼쪽의 공백 제거 : `lstrip()`

오른쪽 공백 제거: `rstrip()`

<br/>

<br/>

<br/>

<br/>

📌 **is00()**

is로 시작하는 함수들은 대부분 true, false

<br/>

ex)

```python
a = "가나다라마바"

print(a.isalpha(a))
```

<pre>
False
</pre>

<br/>

<br/>

<br/>

<br/>

📌 **find(), rfind()**

문자열 내에서 문자열이 어디에 있는지 탐색

<br/>

왼쪽부터 탐색: find() 

오른쪽부터 탐색: rfind()

```python
a ="가나다가나"
print(a.find("가")) #출력:0
print(a.rfind("가")) #출력:3
```

`find()` 왼쪽부터 탐색해서 제일먼저 탐색되는거 왼쪽부터 인덱스 번호

`rfind()` 오른쪽부터 탐색해서 제일먼저 탐색되는거 왼쪽부터 인덱스 번호

<br/>

```python
a ="가나다가나"
print(a.find("라")) #출력:-1
print(a.rfind("라")) #출력:-1
```

없는거 출력하면 `-1`

<br/><br/><br/><br/>

📌**in 연산자**

```python
print("가나" in "가나다라")
```

<pre>
True
</pre>

<br/><br/><br/><br/>

📌**True, false, or, and**

d

d

<br/><br/><br/><br/>

📌**True, false, or, and**



<br/>

📌list

<br/>

📑 **<u3>리스트 반대로 돌리기</u3>**

```python
a = [1, 2, 3, 4, 5]
print(a[::-1])
```

<pre>
[5,4,3,2,1,]
</pre>

<br/>

<br/>

**파괴적이다** : 연산 후 피연산자가 변형되는것

**비파괴적이다**: 변형 x / 원본과 결과 둘다 남기는거

<br/>

리스트와 관련된건 <u1>파괴적 연산 사용</u1>

<br/>

<br/>

​    📑**<u3>리스트 요소 추가</u3>**

```python
a = [1, 2, 3, 4]

a.append(10)      #가장 마지막에 요소 하나 추가
print(a) 💾출력: [1, 2, 3, 4, 10]

a.insert(0, 20)      #원하는 위치에 요소 하나 추가
print(a) 💾<u>출력</u>: [20, 1, 2, 3, 4, 10]

a.extend([5, 6, 7, 8])      #가장 마지막에 요소 여러 개 추가
print(a) 💾출력: [20, 1, 2, 3, 4, 10, 5, 6, 7, 8]
```

<br/>

<br/>

**<u2>a.extend</u2>**  vs  **<u2>a + []</u2>**

a.extend 는 파괴적 연산이라 원본에도 영향을 줌

a + [5, 6, 7, 8]은 원본에 영향 x

그래서

a = [1, 2, 3, 4] 

b = a + [5, 6, 7, 8]

이런식으로 가능

<br/>

<br/>

​    📑**<u3>리스트 요소 제거</u3>**

```python
a = [1, 2, 3]

del a[0]  #제거하고 싶은 인덱스 입력
print(a) 💾출력: [2, 3]


a.pop(0)    # 제거하고 싶은 인덱스 입력(입력하지 않았을떈 기본값 -1이 들어감)
print(a) 💾출력: [3]

a.remove(3)    # 제거하고 싶은 요소 입력
print(a) 💾출력: []
    
a.clear(0)    # 모든 요소 제거
print(a) 💾출력: []
```

<br/>

<br/>

​    📑**<u3>리스트 요소 정렬</u3>**

```python
a = [10 , 100, 3, 9 ,8 ,200]

a.sort()       #오름차순
print(a) 💾출력: [3, 8, 9, 10, 100, 200]

a.sort(reverse=True)       #내림차순
print(a) 💾출력: [200, 100, 10, 9, 8, 3]
```

<br/>

<br/>

​    📑**<u3>리스트 요소 확인</u3>**

```python
a = [10 , 100, 3, 9 ,8 ,200]

print(10 in a) 💾출력: True

print(99 in a) 💾출력: False

print(10 not in a) 💾출력: False
```

<br/><br/><br/>

📌**리스트 전개 연산자**

**<u2>*리스트</u2>**  <------ 리스트 앞에 * (곱하기 x)

<br/>

**<u3>(1) 리스트 내부</u3>**

```python
a = [1, 2, 3]
b = [*a,]       💻출력: [1, 2, 3]
c = [*a, *a]    💻출력: [1, 2, 3, 1, 2, 3]
```

비파괴적 연산이라 비파괴적인 형태로 사용하고 싶을떄 사용함

<br/>

**<u3>(2) 함수의 매개변수 위치</u3>**

```python
date = [2023, 05, 02]

print("{}년 {}월 {}일".format(*date))
```

<pre>
2023년 05월 02일
</pre>



<br/><br/><br/>

📌**딕셔너리**

<br/>

**</u2>{키 : 값, 키 : 값 ....}</u2>**

 ```python
 a = {"사과":100 , "배":300}
 
 for i in a:
     print(i)
 ```

<pre>
사과
배
</pre>

<br/>

```python
a = {"사과":100 , "배":300}

for i in a:
    print(i)
    print(a[i])
```

<pre>
사과
100
배
300
</pre>

<br/>

<br/>

📑**<u3>딕셔너리 값 변경</u3>**

```python
a = {"사과":100 , "배":300}

a["사과"] = "포도"
```

<pre>
{'사과': '포도', '배': 300}
</pre>

<br/>

<br/>

📑**<u3>딕셔너리 요소 추가</u3>**

```python
a["감자"] = 500
```

<pre>
{'사과': '포도', '배': 300, '감자': 500}
</pre>

<br/>

<br/>

📑**<u3>딕셔너리 요소 제거</u3>**

```python
del a["사과"]
```

<pre>
{'배': 300, '감자': 500}
</pre>

<br/>

<br/>

📑**<u3>딕셔너리 키의 존재 여부 확인</u3>**

```python
print("사과" in product)
```

<pre>
False
</pre>

<br/>

```python
print(a.get("사과"))
```

<pre>
None
</pre>

없을때는 `None` 출력

<br/>

```python
print(a.get("배"))
```

<pre>
300
</pre>

<br/>

<br/>

**<u3>++</u3>**

```python
print(f"{pet['name']}  {pet['age']}")
```

이런 코드 작성할때 안쪽까지  `" "`로 작성하면 이상하게 꼬임 `' '`  교체하기

<br/>

<br/>

📚

<pre>
장 20살
이 20살
강 20살
손 20살
전 20살
</pre>

```python
people = [
    {"name": "장", "age":20},
    {"name": "이", "age":20},
    {"name": "강", "age":20},
    {"name": "손", "age":20},
    {"name": "전", "age":20}
]


for person in people:
    print(f"{person['name']} {person['age']}살")
```

처음에 people에 0의 값이 per에 들어오는거니깐 `{person['name']}`이렇게 줘야함

<br/>

<br/>

📚 **문제**

<pre>
{1: 3, 2: 4, 6: 1, 8: 2, 4: 3, 3: 3, 9: 3, 5: 2, 7: 2}
</pre>

````python
num = [1, 2, 6, 8, 4, 3, 2, 1, 9, 5, 4, 9, 7, 2, 1, 3, 5, 4, 8, 9, 7, 2, 3]
count = {}
````

<br/>

```python
#요소의 출현 확인 코드
for number in num:
    count[number] = ""

print(count)
```

<pre>
{1: '', 2: '', 6: '', 8: '', 4: '', 3: '', 9: '', 5: '', 7: ''}
</pre>

<br/>

```python
for number in num:
    count[number] = 0      # 딕셔너리를 초기화 해줘야함

# 💻{1: 0, 2: 0, 6: 0, 8: 0, 4: 0, 3: 0, 9: 0, 5: 0, 7: 0}

#요소의 빈도 확인 코드

for number in num:
    count[number] += 1
```

나올때마다 +1씩 넣음

**<u2>요소 출현 + 요소 빈도</u2>** 를 합쳐야 원하는 값을 가져올 수 있음

<br/>

```python
num = [1, 2, 6, 8, 4, 3, 2, 1, 9, 5, 4, 9, 7, 2, 1, 3, 5, 4, 8, 9, 7, 2, 3]
count = {}

for number in num:
    if number not in counter:
        counter[number] = 0
    counter[number] += 1

print(counter)
```

![image-20230503095410462](../../../images/2023-04-29-Learning Python by Yourself copy/image-20230503095410462.png)

counter에 아무것도 없는데 +1을 할 수 없으니깐

0의 값을 미리 만들어 줘야함

![image-20230503095647667](../../../images/2023-04-29-Learning Python by Yourself copy/image-20230503095647667.png)

2의 값이 만들어져 있으면 

이렇게 바로 +1

<br/>

<br/>

📚

<pre>
sword : 불꽃의 검
armor : 풀플레이트    
</pre>

```python
character = {
    "name" : "기사",
    "level" : 12,
    "items" : {
        "sword" : "불꽃의 검",
        "armor" : "풀플레이트"
    },
    "skill" : ["베기", "세게베기", "아주 세게 베기"]
}
```

<br/>

```python
for key in character:
    if type(character[key]) is dict:
        for 키 in character[key]:
            print(f"{키} : {character[key][키]}")
```

![image-20230503103753955](../../../images/2023-04-29-Learning Python by Yourself copy/image-20230503103753955.png)

<br/>

<br/>

<br/>

📌 **범위와 반복문**

<br/>

📑**<u3>1개</u3>**

```python
rang(A)
```

0부터 A까지의 정수를 범위로 나열 , 

A는 포함 X

<br/>

```python
for i in range(10)
	print("hi")
```

특정 횟수만큼 반복하는 경우 많이 사용

<br/>

<br/>

📑**<u3>2개</u3>**

```python
rang(A, B)
```

A부터 B까지의 정수를 범위로 나열

B는 포함 X

<br/>

```python
for i in range(3)
	print(f"{i}번")
```

<pre>
1번
2번
3번
</pre>

반복 번수를 사용하는 경우 사용

<br/>

<br/>

📑**<u3>3개</u3>**

```python
rang(A, B, C)
```

A부터 B까지의 정수를 범위로 나열

B는 포함 X

C 만큼 건너 뜀

<br/>

```python
for i in range(0,10 + 1)
	print(f"{i}번")
```

`range(0,10 + 1)` == `range(0,11)`

0 ~ 10 까지 출력 

10을 포함하는걸 강조하고 싶어서 이렇게 쓰는거임

<br/>

```python
for i in range(3,-1, -1)
	print(f"{i}번")
```

<pre>
3번
2번
1번
</pre>

반대로 반독하는 경우

<br/>

<br/>

📑**<u3>반복문에  _ </u3>**

```python
for _ in range(3,-1, -1)
	print(f"{i}번")
```

그냥 똑같이 식별자임 다른거 없음

(옛날에 python에서는 반복변수를 사용하지 않을경우 _를 사용하는걸 권장했었음)

<br/>

<br/>

<br/>

📌 **등차수열**

![image-20230503121226434](../../../images/2023-04-29-Learning Python by Yourself copy/image-20230503121226434.png)

📑**<u3>일반항</u3>**

```python
n = x

a_n = 2 * n - 1
```

```python
n = 100

a_n = 2 * n - 1

print(a_n)
```

<pre>
99
</pre>

<br/>

a1 ~ a100 까지 나열 하고 싶음

```python
for n in range(1, 100 +1)
    a_n = 2 * n - 1
    print(a_n)
```

```python
n = 1

while n <= 100:
    a_n = 2 * n - 1
    print(a_n)
    n += 1
```

<br/>

a1 ~ a10 리스트

```python
a = []

for n in range(1, 10 +1):
    a_n = 2 * n - 1
    a.append(a_n)
    
print(a)
```

**<u2>Tip</u2>**

a_1 == 1

a_2 == 3

a[0] = 1

a[1] =3 

이렇게 햇갈리잖아

```python
a = [None]

for n in range(1, 10 +1):
    a_n = 2 * n - 1
    a.append(a_n)
    
print(a)
```

<pre>
[None, 1, 3, 5, 7, 9, 11, 13, 15, 17, 19]
</pre>

a[1] =1

a[2] =3

이러면 편함

<br/>

<br/>

<br/>

📑**<u3>점화식 </u3>**

이전 항을 기반으로 다음 항을 만드는 방법

![image-20230503123114053](../../../images/2023-04-29-Learning Python by Yourself copy/image-20230503123114053.png)

```python
a = [None]

for n in range(1, 10 +1):
    if n == 1:
        a_n = 1
    else:
        a_n = a[n-1] +2
    a.append(a_n)
    
print(a)
```

<br/>

<br/>

<br/>

📌 **reversed()**

<br/>

```python
print(list(reversed([1, 2, 3, 4, 5])))
```

<pre>
[5, 4, 3, 2, 1]
</pre>

<br/>

```python
print(list(reversed(range(0, 5))))
```

<pre>
[4, 3, 2, 1, 0]
</pre>

<br/>

38ㄱ

<br/>

<br/>

<br/>

📌 **while 반복문**

**<u2>for 반복문 -----> while 반복문</u2>**  구현 가능

**<u2>for 반복문 <---- while 반복문</u2>**  매우 어렵거나 불가능

<br/>

1. 특정 횟수만큼 반복 ---> **<u2>for 반복문</u2>**

   ex) 아이스크림 100개 먹어

   

2. 조건으로 반복 ---> <u2>while반복문</u2>

   ex) 돼지바만 먹어

   ​      재고가 다 떨어질떄까지 다 먹어

<br/>

<br/>



<br/>

📚 **출력** (while, input 활용)

<pre>
1번째 반복입니다.
> 종료하겠습니까?(y/n): 1 
<br/>
2번째 반복입니다.
> 종료하겠습니까?(y/n): n
<br/>
3번째 반복입니다.
> 종료하겠습니까?(y/n): y
반복문을 종료합니다.
</pre>

<br/>

```python
i = 0

while True:
    print(f"{i}번째 반복입니다.")
    i += 1

    a= input("> 종료하겠습니까?(y/n): ")
    if a in ["y", "Y"]
        print("반복 종료.")
        break
```

<br/>

<br/>



<br/>

<br/>

📌 **continue**

현재 반복을 넘어갈 때 사용

<br/>

📚 **출력**

```python
num = [1, 2, 3, 4, 5, 6, 7, 8]

?
```

<pre>
6
7
8
</pre>

<br/>

<br/>

✏ **answer 1**

```python
num = [1, 2, 3, 4, 5, 6, 7, 8]

for i in num:
    if i >= 6:
        print(i)
```

<br/>

✏ **answer 2**

```python
num = [1, 2, 3, 4, 5, 6, 7, 8]

for i in num:
    if i < 6:
        continue
    print(i)
```

