---
layout: single
title: Web Crawler
tag: Web Crawler
author_profile: false
use_math: false
typora-root-url: ../
---

[^]: python 기초 DS

<h3 style="font-size: 8px; margin-top: -45px; font-color: #434343;">
  <a href="https://potettangeeeeeeeeeeeeeeeeeeeeeeeee.github.io/Python/" style="text-decoration: none; color: #3c3c3c; background-color: #f8f9fa; border-radius: 20px; padding: 5px 10px; display: inline-block;">
    <img src="../images/ImgFile/bf.png" style="height: 12.33px; width: auto; margin-top: -4px; vertical-align: middle;" alt="Python 이미지">
    Python / Web crawler & Automation
  </a>
</h3>


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
    text-decoration-thickness: 3px;
  }
  u3 {
    text-decoration: underline;
    text-decoration-style: wavy;
    text-decoration-color: #ff0080;
    text-decoration-thickness: 3px;
  }
</style>





<br/>
<br/>

📌 **Web Crawer**

<br/>

```python
pip install request
```

```python
pip install bs4
```

터미널을 열어서 라이브러리 설치

<br/>

<br/>

```python
import requests
from bs4 import BeautifulSoup
```

`import requests` == 웹사이트 접속을 도와주는 라이브러리

`from bs4 import BeautifulSoup` ==  HTML 웹문서 분석 도와주는 라이브러리.

<br/>

<br/>

```python
import requests
from bs4 import BeautifulSoup

#data = requests.get("URL")
data = requests.get("https://www.upbit.com/trends")
print(data)
```

<pre>
&#60;Response [200]&#62;
</pre>

200 뜨면 정상적으로 가져온거

<br/>

```python
print(data.status_code) 
```

웹페이지에 제대로 접속되고 있냐 라고 물어보는거, 

정상 == 200

비정상 == 400 or 500

<br/>

```python
print(data.content)
```

이렇게 하면 html 다 긁어오는데 , 깨져서 보이는 문제가 있음

<br/>

<br/>

```python
import requests
from bs4 import BeautifulSoup

data = requests.get("https://www.upbit.com/trends")

bdata = BeautifulSoup(data.content, "html.parser") 
```

<u2>BeautifulSoup</u2> 안에 넣어서 깔끔하게 정리

<br/>

<br/>

<img src="../images/2023-04-30-Web Crawer (AP)/image-20230430162349079-1682841029052-2.png" align="left"><br/>

```python
#print(pdata.find_all("태그명",속성명))

print(bdata.find_all("span",id="_quant"))
```

<pre>
[ &#60;span class="tah p11" id="_quant"&#62;18,139,558 &#60;/span&#62;]
</pre>

이렇게하면 찾은 결과를 리스트로 출력해줌

<br/>

```python
print(bdata.find_all("span",id="_quant")[0])
```

<pre>
&#60;span class="tah p11" id="_quant"&#62;18,139,558 &#60;/span&#62;
</pre>

이렇게 해서 리스트 벗기기도 가능

<br/>

```python
print(bdata.find_all("span",id="_quant")[0].text)
```

<pre>
18,139,558
</pre>

텍스트만 꺼낼 수 도 있음

<br/>

<br/>


<img src="../images/2023-04-30-Web Crawer (AP)/image-20230430162349079-1682841029052-2.png" align="left"><br/>

근데 이제 만약 id말고 class로 찾고 싶다 ?

```python
print(bdata.find_all("span",class_="tah")[0].text)
```

이렇게 언더바 추가해 줘야함

그리고 "tah p11" 이렇게 띄어써져있으면 클래스 명이 두개인거

<br/>

태그에 부여된 **id**는 **<u2>유니크</u2>**

태그에 부여된 **class**는 **<u2>중복</u2>** 가능

<br/>
<br/>
<br/>

**<u3>하나씩 해체되어 있을떄</u3>**

![image-20230501141755997](/../../images/2023-04-30-Web Crawer (AP)/image-20230501141755997.png)

이렇게 글자가 하나씩 해체되어 있어도

그냥

```python
print(bdata.find_all("span",class_="no_up")[0].text)
```

일케 하면 됨

<br/>

<br/>

**<u3>class, id가 없을떄</u3>**

![image-20230501142129361](/../../images/2023-04-30-Web Crawer (AP)/image-20230501142129361.png)

```python
import requests
from bs4 import BeautifulSoup

#data = requests.get("URL")
data = requests.get("https://www.upbit.com/trends")

bdata = BeautifulSoup(data.content, "html.parser") 

print(bdata.find_all("span",id="_quant")[0])
```

<br/>

```python
print(bdata.find_all("em")[0])
```

그냥 이렇게 하면 되는데 그럼 em이 너무 많음

<br/>

```python
bdata.select(".f_up")
```

`class = "f_up"` 을 찾는 코드

class를 찾을떄는 **<u2>.</u2>**

<br/>

```python
bdata.select("#f_up")
```

id를 찾을떄는 **<u2>#</u2>**

근데 이대로는 이 전에 했던것 보다는 자세한게 아님 

```python
print(bdata.find_all("span",id="_quant")[0].text)
```

이 코드와 똑같이 할려면 

```python
bdata.select("span#f_up")
```

<br/>

```python
bdata.select("span")
```

```python
bdata.select("td")
```

아무것도 없이 쓰면 태그명 검색

<br/>

![image-20230501142129361](/../../images/2023-04-30-Web Crawer (AP)/image-20230501142129361.png)

```python
bdata.select(".f_up em")
```

띄어쓰기는 내부요소를 찾을때

`.f_up`안에 있는 `em`을 찾아라

<br/>

+

```python
bdata.select(".f_up em")[0].txt
```

<br/>

<br/>

**<u3>이미지 수집 하기</u3>**

![image-20230501144109355](/../../images/2023-04-30-Web Crawer (AP)/image-20230501144109355.png)

```python
testimage = bdata.select("#imh_chart_area")
print(testimage)
```

<pre>
[&#60;img alt="이미지 차트" height="289" id="img_chart_area" onerror="this.src='https://ssl.pstatic.net/imgstock/chart3/world2008/error_700x289.png'" src="https://ssl.pstatic.net/imgfinance/chart/item/area/day/005930.png?sidcode=1682919827505" width="700"/	&#62;]
</pre>

<br/>

```python
testimage = bdata.select("#imh_chart_area")[0]
print(testimage)
```

<pre>
&#60;img alt="이미지 차트" height="289" id="img_chart_area" onerror="this.src='https://ssl.pstatic.net/imgstock/chart3/world2008/error_700x289.png'" src="https://ssl.pstatic.net/imgfinance/chart/item/area/day/005930.png?sidcode=1682919827505" width="700"/	&#62;
</pre>

<br/>

이미지 자체만 추출하고 싶으면 

```python
testimage = bdata.select("#imh_chart_area")[0]

print(testimage["src"])
```

<pre>
https://ssl.pstatic.net/imgfinance/chart/item/area/day/005930.png?sidcode=1682919993247
</pre>

<br/>

<br/>

<br/>

**<u3>이미지 URL을 가지고 파일로 저장 하는 방법</u3>**

```python
import requests             #<-------- 이 코드 추가
import urllib.request
from bs4 import BeautifulSoup


data = requests.get("https://www.upbit.com/trends")

bdata = BeautifulSoup(data.content, "html.parser") 

testimage = bdata.select("#img_chart_area")[0]

# urllib.request.urlretrieve("이미지URL", '파일명')     <----------- 추가

urllib.request.urlretrieve("https://ssl.pstatic.net/imgfinance/chart/item/area/day/005930.png?sidcode=1682919993247", "Chart.png")
```

<br/>

<br/>

<br/>

🚀 **for / def**

```python
testlist = ["가", "나", "다", "라",]

for i in range(4)
	print(i)
```

이거랑 밑에랑 똑같음 

```python
for i in testlist:       #<----- 이렇게 바로 리스트를 넣을 수 있음
    print(i)             #<----- i가 1,2,3,4 이렇게 변하는게 아니라 가, 나 , 다 ,라 이렇게 변함 
```

<br/>

<br/>

<br/>

📌 **무한 스크롤 데이터 수집(NAVER)**

<br/>

일반 적으로 page로 나뉘는 사이트는 page{번호} 만 바꿔주면 손쉽게 가능

이런거 말고

**<u2>네이버 검색 -> view</u2>**  처럼 무한스크롤 페이지 데이터 수집 하는 법

![image-20230501154518622](/../../images/2023-05-01-Web Crawer 2/image-20230501154518622.png)

```python
import requests            
from bs4 import BeautifulSoup


requests.get("https://s.search.naver.com/p/review/search.naver?rev=44&where=view&api_type=11&start=31&query=%EC%95%84%EC%9D%B4%EC%8A%A4%ED%81%AC%EB%A6%BC&nso=&nqx_theme=%7B%22theme%22%3A%7B%22main%22%3A%7B%22name%22%3A%22food_recipe%22%7D%7D%7D&main_q=&mode=normal&q_material=&ac=1&aq=0&spq=0&st_coll=&topic_r_cat=&nx_search_query=&nx_and_query=&nx_sub_query=&prank=31&sm=tab_jum&ssc=tab.view.view&ngn_country=KR&lgl_rcode=03121129&fgn_region=&fgn_city=&lgl_lat=35.2416&lgl_long=128.6265&abt=&_callback=viewMoreContents")

requests.get("https://s.search.naver.com/p/review/search.naver?rev=44&where=view&api_type=11&start=61&query=%EC%95%84%EC%9D%B4%EC%8A%A4%ED%81%AC%EB%A6%BC&nso=&nqx_theme=%7B%22theme%22%3A%7B%22main%22%3A%7B%22name%22%3A%22food_recipe%22%7D%7D%7D&main_q=&mode=normal&q_material=&ac=1&aq=0&spq=0&st_coll=&topic_r_cat=&nx_search_query=&nx_and_query=&nx_sub_query=&prank=31&sm=tab_jum&ssc=tab.view.view&ngn_country=KR&lgl_rcode=03121129&fgn_region=&fgn_city=&lgl_lat=35.2416&lgl_long=128.6265&abt=&_callback=viewMoreContents")
```

<br/>

![image-20230501154740878](/../../images/2023-05-01-Web Crawer 2/image-20230501154740878.png)

이렇게 규칙을 파악하면 데이터 수집 편하게 가능

<br/>

<br/>

**<u3>제목만 뽑아보기</u3>**

```python
import requests            
from bs4 import BeautifulSoup


data = requests.get("https://s.search.naver.com/p/review/search.naver?rev=44&where=view&api_type=11&start=31&query=%EC%95%84%EC%9D%B4%EC%8A%A4%ED%81%AC%EB%A6%BC&nso=&nqx_theme=%7B%22theme%22%3A%7B%22main%22%3A%7B%22name%22%3A%22food_recipe%22%7D%7D%7D&main_q=&mode=normal&q_material=&ac=1&aq=0&spq=0&st_coll=&topic_r_cat=&nx_search_query=&nx_and_query=&nx_sub_query=&prank=31&sm=tab_jum&ssc=tab.view.view&ngn_country=KR&lgl_rcode=03121129&fgn_region=&fgn_city=&lgl_lat=35.2416&lgl_long=128.6265&abt=&_callback=viewMoreContents")

a = BeautifulSoup(data.content, "html.parser")

print(a)
```

이렇게만 하면 출력물에 `\` 이게 들어 있음 ,  데이터 전송을 위해 가끔 있는데 이걸 지워줘야함

```python
# a = BeautifulSoup(data.content.replace("이거를", "이거로 바꿔주세요") "html.parser")

a = BeautifulSoup(data.content.replace("\\", ""),"html.parser")
```

<pre>
Error
</pre>

replace를 쓸려면 왼쪽이 text여야함

content는 뭐라고 알랴줬는데  까먹음 ㅋ

```python
a = BeautifulSoup(data.text.replace("\\", ""),"html.parser")
```

<br/>

```python
a = BeautifulSoup(data.text.replace("\\", "") "html.parser")

print(a.select("a.api_text_lines"))     #<------ findall 써도 ㄱㅊ 자기 선택
```

<br/>

```python
import requests            
from bs4 import BeautifulSoup


data = requests.get("https://s.search.naver.com/p/review/search.naver?rev=44&where=view&api_type=11&start=31&query=%EC%95%84%EC%9D%B4%EC%8A%A4%ED%81%AC%EB%A6%BC&nso=&nqx_theme=%7B%22theme%22%3A%7B%22main%22%3A%7B%22name%22%3A%22food_recipe%22%7D%7D%7D&main_q=&mode=normal&q_material=&ac=1&aq=0&spq=0&st_coll=&topic_r_cat=&nx_search_query=&nx_and_query=&nx_sub_query=&prank=31&sm=tab_jum&ssc=tab.view.view&ngn_country=KR&lgl_rcode=03121129&fgn_region=&fgn_city=&lgl_lat=35.2416&lgl_long=128.6265&abt=&_callback=viewMoreContents")

a = BeautifulSoup(data.text.replace("\\", ""), "html.parser")

b = a.select("a.api_txt_lines")

print(b[0].text)
print(b[1].text)
print(b[2].text)
```

<pre>
홈카페 레시피, 아이스크림 라떼 만들기 (w. 가찌아 아니마)
솔티드바닐라/네추럴킹덤 고구마큐브/머드스콘 말초칩/어른이날 널담 뚱카롱/메
가커피 로투스아이스크림
하동악양대봉곶감 아이스포장으로 든든히~ 부모님 간식으로 아이들 천연아이스크
림으로 시원 달콤한 맛...
</pre>

<br/>

<br/>

**<u3>URL도 뽑아보기</u3>**

![image-20230501161523845](/../../images/2023-05-01-Web Crawer 2/image-20230501161523845.png)

보니깐  `a`태그에 같이 들어 있음

```python
print(b[0]["href"])
print(b[1]["href"])
print(b[2]["href"])
```

<pre>
https://blog.naver.com/murum4/223045209324
https://blog.naver.com/jtu0323/223088325622
https://blog.naver.com/hhk520/223063509751
</pre>

<br/>

<br/>