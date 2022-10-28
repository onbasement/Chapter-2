Learn HTML<br/>
=============
1.&nbsp;Introduction to HTML & HTML Document Standards
----------------------------------------------
## 1.1 About HTML
> HTML은 Hyper Text Markup Language의 약자<br/>
> HTML은 기본구조를 만드는것 나중에 CSS와 JavaScript로 꾸밀 수 있음<br/>
> opening tag와 closing tag가 존재하고 그 사이에 content가 들어간다<br/>
 ```html
 An opening tag (<p>)
 opening tag는 <>안에 들어가있음

 The content (My name is onbasement)

 A closing tag (</p>)
 closing tag는 opening tag에 front slash가 들어있는 모양

 <p>My name is onbasement</p>
 이 코드 한줄이 하나의 html element
 ```

## 1.2 The Body
> web page를 구축할때 가장 주요한 요소 <body>와 </body>사이에 다양한 유형의 content를 추가할 수 있다<br/>
```html
<body> 
  <h1>Hello World</h1>
  <p>This paragraph is a child of the body element</p> 
</body>
```

## 1.3 HTML Structure
> html은 가족구조로 형성되어 있다<br/>
```html
<body>
  <h1>Hello World</h1>
  <p>This paragraph is a child of the body element</p>
  <div>
   <p>This paragraph is a child of the div element and a grandchild of the body element</p>  
  </div> 
</body>
```

### 1.3.1 Headings
> h1 ~ h6 까지 크기순서대로 존재한다<br/>
> 텍스트 크기를 원하는크기로 만드는데 쓰는거 같다<br/>
```html
<h1>This is H1<h1>
<h2>This is H1<h2>
<h3>This is H1<h3>
<h4>This is H1<h4>
<h5>This is H1<h5>
<h6>This is H1<h6>
```

### 1.3.2 Divs
> 페이지를 나눌때 사용한다<br/>
> html의 요소를 그룹화하는 데 매우 유용하다<br/>
> div안에는 링크,이미지 또는 비디오와 같은 텍스트 또는 기타 html이 들어갈수 있다<br/>
```html
<div>
  <h1>Introduction</h1>
</div>
```

### 1.3.3 Attributes
> 오픈태그 안에 추가하여 정보제공, 스타일변경등에 사용가능하게 만들어준다<br/>
> name과 value로 구성되어있다<br/>
> 가장 흔히 id를 사용한다<br/>
```html
<div id="intro">
  <h1>Introduction</h1>
</div>
```

### 1.3.4 Text
> 문자를 추가하고 싶을때 사용한다<br/>
> span을 사용하면 다른 텍스트와 분리해준다<br/>
```html
<div>
  <p><span>Self-driving cars</span> are anticipated to replace up to 2 million jobs 
    over the next two decades.</p>
</div>
```
> em은 italic체로 강조해준다<br/>
> strong은 bold체로 강조해준다<br/>
```html
<p><strong>The Nile River</strong> is the <em>longest</em> river in the world, 
 measuring over 6,850 kilometers long (approximately 4,260 miles).</p>
```
> br은 한줄을 띄어준다<br/>
```html
<p>The Nile River is the longest river <br> in the world, 
  measuring over 6,850 <br> kilometers long (approximately 4,260 <br> miles).</p>
```

### 1.3.5 Lists
> ul을 사용하면 순서가 없는 목록을 구성하는게 가능하다<br/>
> 이때 li를 앞뒤로 써줘야한다<br/>
```html
<ul>
  <li>Limes</li>
  <li>Tortillas</li>
  <li>Chicken</li>
</ul>
```
> ol 사용하면 순서가 있는 목록을 구성하는게 가능하다<br/>
> 코드를 실행해보면 1. 2. 이런식으로 출력된다<br/>
> 이때 li를 앞뒤로 써줘야한다<br/>
```html
<ol>
  <li>Preheat the oven to 350 degrees.</li>
  <li>Mix whole wheat flour, baking soda, and salt.</li>
  <li>Cream the butter, sugar in separate bowl.</li>
  <li>Add eggs and vanilla extract to bowl.</li>
</ol>
```

### 1.3.6 Images
> 이미지를 넣고 싶을때 사용한다<br/>
> img와 src로 사용한다<br/>
> img 태그는 self closing tag이기 때문에 마지막에 /를 입력해주면된다<br/>
> src는 해당 이미지의 source를 알려준다<br/>
> src안에 주소를 넣을때 큰따옴표 안에 넣어야한다<br/>
```html
<img src="image-location.jpg" />
<img src="https://content.codecademy.com/courses/web-101/web101-image_brownbear.jpg" />
```
> alt는 사진에 대한 부가설명을 제공한다
> 사진위에 올려두고 볼수도 있고 시각장애인에게 도움 또한 검색엔진에서도 중요한 역할을 한다
```html
<img src="https://content.codecademy.com/courses/web-101/web101-image_brownbear.jpg" alt="bear" />
```

### 1.3.7 Videos
> video와 src를 통해 video를 넣을수 있다.
> width height를 통해 브라우저에 표시되는 비디오의 크기를 설정한다
> controls는 기본 비디오 컨트롤(재생,일시정지,볼륨,전체화면등)을 포함하는 비디오를 생성한다
> 여는태그 닫는태그 사이에 있는 텍스트는 브라우저가 비디오를 표시할수 없을때 표시된다
```html
<video src="myVideo.mp4" width="320" height="240" controls>
 Video not supported
</video>
```

<br/><br/><br/>

2.&nbsp;Introduction to HTML & HTML Document Standards
------------------------------------------------------
## 2.1 HTML Tags
### 2.1.1 DOCTYPE HTML
> ```<!DOCTYPE HTML>```<br/>
> html의 첫 코드행은 !DOCTYPE HTML이다<br/>
> 문서에서 사용중인 버전과 함께 예상되는 문서유형을 알려준다<br/>

### 2.1.2 html
> html 구조와 콘텐츠를 생성하려면 코드 처음과 끝에 여는태그 닫는태그를 추가해주어야한다<br/>
```html
<!DOCTYPE html>
<html>
 
</html>
```

### 2.1.3 head
> 웹페이지 자체에 대한 정보를 제공한다<br/>
```html
<!DOCTYPE html>
<html>
  <head>
  </head>
</html>
```

### 2.1.4 title
> ```title```<br/>
> head안에서 태그에 지정된 제목을 표시할때 사용한다<br/>
> title은 인터넷 탭에 표시된다<br/>
```html
<!DOCTYPE html>
<html>
  <head>
    <title>My Coding Journal</title>
  </head>
</html>
```

### 2.1.5 anchor
> **외부링크로 이동하고 싶을때 쓰는방법**<br/>
> 해당된곳을 클릭하면 링크로 이동하게 할 수 있다<br/>
> 아래 예시는 Learn More이라는 글자가 파랗게 변하고 클릭하면 해당 주소로 이동한다<br/>
```html
<a href="https://en.wikipedia.org/wiki/Brown_bear">Learn More</a>
```

> target을 사용하면 링크가 열리는 방법을 바꿀 수 있다<br/>
> 일반적으로 원래 보던 탭이 해당 페이지로 바뀌는데 ```target="_blank"```를 추가하면 새탭에서 열린다<br/>
```html
<a href="https://en.wikipedia.org/wiki/Brown_bear" target="_blank">Learn More</a>
```

<br/>

> **내부링크로 이동하고 싶을때 쓰는 방법**<br/>
```html
project-folder/
|—— about.html
|—— contact.html
|—— index.html
```
> 이런식으로 같은 폴더안에 있는데 이동하고싶을때 ```<a href="./contact.html">Contact</a>```을 사용하면 된다<br/>
> 원래 url자리에 해당 파일명을 입력하면 이동할수 있다<br/>
> 이렇게 코드를 작성하면 클릭하면 해당 카테고리로 이동할수 있는 About Me 라는 글자가 추가됨

<br/>

> **이미지로 링크 연결하는 방법**<br/>
> img 앞에 anchor를 사용하면 이미지 클릭시 해당 링크로 이동하게 만들 수 있다<br/>
```html
<a href="https://en.wikipedia.org/wiki/Opuntia" target="_blank">
 <img src="https://www.Prickly_Pear_Closeup.jpg" alt="A red prickly pear fruit"/></a>
```

<br/>

> **같은화면에서 특정 스크롤 부분으로 이동하는 방법**<br/>
> href에 해당 부분의 id를 적으면 된다<br/>
> 이때 이동하길 원하는 부분에 id를 제공하는 작업이 선행되어야 한다<br/>
```html
<p id="top">This is the top of the page!</p>
<h1 id="bottom">This is the bottom! </h1>
해당 부분에 id를 제공
```
```html
<ol>
  <li><a href="#top">Top</a></li>
  <li><a href="#bottom">Bottom</a></li>
</ol>
그 뒤에 href가 해당 부분 id에 걸린 ol을 작성
```

### 2.2 Whitespace & Indentation
> 공백은 html 문법에서도 중요하다<br/>
> W3C 표준에서는 space 2칸이 기준이다<br/>
```html
<body>
  <p>Paragraph 1</p>
  <div>
    <p>Paragraph 2</p>
  </div>
</body>
```

### 2.3 Comments
> 주석처리는 ```<!-- This is a comment that the browser will not display. -->``` 이런식으로 한다<br/>
```html
<!-- Favorite Films Section -->
<p>The following is a list of my favorite films:</p>
```

<br/><br/><br/>

3.&nbsp;HTML Tables
------------------------------------------------------
### 3.1 Introduction to Tables
> table은 표 형식의 데이터이다<br/>
> table을 이용하여 table을 생성할 수 있다<br/>
> 이때는 table이 만들어 졌으나 아무것도 보이지 않는다<br/>
```html
<table>
</table>
```
> row는 가로방향으로 같은 row이고, column은 세로방향으로 같은 column이다<br/>
> ex) row가 2이고 column이 3인 table은 이렇게 생겼다<br/>
<table>
 <tr>
  <td>row1column1
  <td>row1column2
  <td>row1column3
 </tr>
 <tr>
  <td>row2column1
  <td>row2column2
  <td>row2column3
 </tr>
</table>

### 3.2 Table Rows
> tr로 row를 생성 가능하다<br/>
> row를 추가하면 table이 밑으로 추가된다<br/>
> 이때까지도 table은 보이지 않는다<br/>
```html
<table>
  <tr>
  </tr>
  <tr>
  </tr>
</table>
```

### 3.3 Table Data
> td로 row에 데이터를 넣을 수 있다<br/>
> 이때 넣은 데이터의 개수만큼 column이 생성된다<br/>
```html
<table>
  <tr>
    <td>73</td>
    <td>81</td>
  </tr>
</table>
```
<table>
  <tr>
    <td>73</td>
    <td>81</td>
  </tr>
</table>

### 3.4 Table Heading
> th는 주로 table heading element에 사용된다<br/>
> scope는 해당 row 와column 에 있는 data가 represent하는것이 무엇인지 알려준다<br/> 
```html
<table>
  <tr>
    <th></th>
    <th scope="col">Saturday</th>
    <th scope="col">Sunday</th>
  </tr>
  <tr>
    <th scope="row">Temperature</th>
    <td>73</td>
    <td>81</td>
  </tr>
</table>
```
<table>
  <tr>
    <th></th>
    <th scope="col">Saturday</th>
    <th scope="col">Sunday</th>
  </tr>
  <tr>
    <th scope="row">Temperature</th>
    <td>73</td>
    <td>81</td>
  </tr>
</table>

### 3.5 Table Borders
> table에 테두리를 넣고 싶을때 사용한다<br/>
```html
<table border="3">
  <tr>
    <th></th>
    <th scope="col">Saturday</th>
    <th scope="col">Sunday</th>
  </tr>
  <tr>
    <th scope="row">Temperature</th>
    <td>73</td>
    <td>81</td>
  </tr>
</table>
```
<table border="3">
  <tr>
    <th></th>
    <th scope="col">Saturday</th>
    <th scope="col">Sunday</th>
  </tr>
  <tr>
    <th scope="row">Temperature</th>
    <td>73</td>
    <td>81</td>
  </tr>
</table>

### 3.6 Spanning Columns
> 여러 column을 하나로 합치고 싶을때 colspan="정수"를 사용하면 해당 정수만큼 칸이 합쳐진다<br/>
> 합쳐지고 남은요소들은 오른쪽으로 밀려난다<br/>
```html
<table>
  <tr>
    <th>Monday</th>
    <th>Tuesday</th>
    <th>Wednesday</th>
  </tr>
  <tr>
    <td colspan="2">Out of Town</td>
    <td>Back in Town</td>
  </tr>
</table>
```
<table>
  <tr>
    <th>Monday</th>
    <th>Tuesday</th>
    <th>Wednesday</th>
  </tr>
  <tr>
    <td colspan="2">Out of Town</td>
    <td>Back in Town</td>
  </tr>
</table>

### 3.7 Spanning Rows
> 여러 row를 합치고 싶을때는 rowspan="정수"를 사용하면 해당 정수만큼 칸이 합쳐진다<br/>
> 합쳐지고 남은 요소들은 오른쪽으로 밀려난다<br/>
```html
<table>
  <tr> <!-- Row 1 -->
    <th></th>
    <th>Saturday</th>
    <th>Sunday</th>
  </tr>
  <tr> <!-- Row 2 -->
    <th>Morning</th>
    <td rowspan="2">Work</td>
    <td rowspan="3">Relax</td>
  </tr>
  <tr> <!-- Row 3 -->
    <th>Afternoon</th>
  </tr>
  <tr> <!-- Row 4 -->
    <th>Evening</th>
    <td>Dinner</td>
  </tr>
</table>
```
<table>
  <tr> <!-- Row 1 -->
    <th></th>
    <th>Saturday</th>
    <th>Sunday</th>
  </tr>
  <tr> <!-- Row 2 -->
    <th>Morning</th>
    <td rowspan="2">Work</td>
    <td rowspan="3">Relax</td>
  </tr>
  <tr> <!-- Row 3 -->
    <th>Afternoon</th>
  </tr>
  <tr> <!-- Row 4 -->
    <th>Evening</th>
    <td>Dinner</td>
  </tr>
</table>

### 3.8 Table Element

<br/>

> **tbody**<br/>
> 표가 길어질때 머리글을 제외한 모든 데이터를 포함한다<br/>
> 이때 가장 첫 row는 제외하고 thead로 들어간다<br/>

<br/>

> **thead**<br/>
> th를 이용했던 element들 중에서 가장 첫 row를 thead로 설정한다<br/>
> 이때 다른 th들은 scope를 통해 heading 해준다<br/>

<br/>

> **tfoot**<br/>
> 해당 데이터의 합계등을 나타낼때 사용한다<br/>
> 이때 가장 마지막 row를 tfoot으로 설정한다<br/>
```html
<table>
  <thead>
    <tr>
      <th>Quarter</th>
      <th>Revenue</th>
      <th>Costs</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Q1</th>
      <td>$10M</td>
      <td>$7.5M</td>
    </tr>
    <tr>
      <th>Q2</th>
      <td>$12M</td>
      <td>$5M</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <th>Total</th>
      <td>$22M</td>
      <td>$12.5M</td>
    </tr>
  </tfoot>
</table>
```
<table>
  <thead>
    <tr>
      <th>Quarter</th>
      <th>Revenue</th>
      <th>Costs</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Q1</th>
      <td>$10M</td>
      <td>$7.5M</td>
    </tr>
    <tr>
      <th>Q2</th>
      <td>$12M</td>
      <td>$5M</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <th>Total</th>
      <td>$22M</td>
      <td>$12.5M</td>
    </tr>
  </tfoot>
</table>

<br/><br/><br/>

4.&nbsp;HTML Forms
------------------------------------------------------
## 4.1 HTTP request
> form이 있는 웹페이지에 방문을 해서 폼 내용을 입력하면 폼 안에 있는 데이터를 서버로 보내준다<br/>
> 이때 서버에서 폼 데이터를 처리후 html 페이지를 다시 보내준다<br/>
> form 태그 속성에는 name, action, method,target 등이 있다<br/>
> **name**은 폼을 식별하기 위한 이름을 지정한다<br/>
> **action**은 폼을 전송할 서버 쪽 스크립트 파일을 지정한다<br/>
> **method**는 폼을 서버에 전송할 http 메소드를 정한다(GET or POST)<br/>
> **GET**방식은 데이터가 외부에 노출되어 보안에 취약하여 주로 읽을 때 사용하는 method이다<br/>
> **POST**방식은 지정된 리소스에서 데이터를 수정,삭제할 때 사용한다<br/>
> **target**은 action에서 지정한 스크립트 파일을 현재 창이 아닌 다른 위치에 열도록 지정한다<br/>
```html
form action="/practice.html" method="POST">
<h1>Burger</h1>
<p>very delicious burger</p>
</form>
```

## 4.2 Text Input
> input은 정보를 입력하는 창을 만들때 사용한다<br/>
> type에 따라 입력창이 조금씩 달라진다<br/>
### 4.2.1 Type="text"
> 텍스트를 입력하는 한줄의 입력 필드를 만든다<br/>
> value를 통해 해당 빈칸에 텍스트를 채워놓을 수도 있다<br/>
```html
<form>
  First name:<br>
  <input type="text" name="firstname" value="write here"><br>
</form>
```

### 4.2.2 Type="password"
> password 필드를 만든다<br/>
> 이때 password 필드의 문자는 별표나 동그라미로 표시된다<br/>
```html
<form>
  User password:<br>
  <input type="password" name="psw">
</form>
```

### 4.2.3 Type="submit"
> form-handler에게 폼을 제출하는 버튼을 만든다<br/>
> form-handler는 폼의 action 속성에 명시되며 일반적으로 수신된 입력을 가지고 무언가를 수행한다<br/>
```html
<form action="action_page.php">
  First name:<br>
  <input type="text" name="firstname" value="Mickey"><br>
  Last name:<br>
  <input type="text" name="lastname" value="Mouse"><br><br>
  <input type="submit" value="Submit">
</form>
```

### 4.2.4 Type="radio"
> 오직 하나의 옵션만 선택 가능한 선택지들을 만든다<br/>
> name을 같게해서 같은 name을 가진 것 중에 오직 하나만 선택하게 만들 수 있다<br/>
```html
<form>
  <p>What is sum of 1 + 1?</p>
  <input type="radio" id="two" name="answer" value="2">
  <label for="two">2</label>
  <br>
  <input type="radio" id="eleven" name="answer" value="11">
  <label for="eleven">11</label>
</form>
```

### 4.2.5 Type="checkbox"
> 여러개의 요소를 체크할수 있는 창을 만든다<br/>
> value값을 써줘야 확인란의 속성값을 할당할 수 있다<br/>
> name이 같아도 id가 다르면 unique하게 저장된다<br/>
```html
<form>
 <label for="lettuce">Lettuce</label>
 <input id="lettuce" name="topping" type="checkbox" value="lettuce">
 <label for="tomato">Tomato</label>
 <input id="tomato" name="topping" type="checkbox" value="tomato">
</form>
```

### 4.2.6 Type="button"
> click할 수 있는 버튼을 만든다<br/>
```html
<form>
 <input type="button" onclick="alert('Hello World!')" value="Click Me!">
</form>
```

### 4.2.7 Type="number"
> 숫자를 입력하는 필드를 만든다<br/>
> 버튼으로 원하는 step만큼 +-할 수 있는 창을 생성 가능하다<br/>

```html
<form>
  Quantity (between 1 and 5):
  <input type="number" name="quantity" min="1" max="5">
</form>
```

### 4.2.8 Type="date"
> 날짜를 입력하는 필드를 만든다<br/>
> 브라우저에 따라 날짜 선택기가 입력 필드로 표시될 수도 있다<br/>
```html
<form>
  Birthday:
  <input type="date" name="bday">
</form>
```

### 4.2.9 Type="color"
> 색상을 입력하는 필드를 만든다<br/>
> 브라우저에 따라 색상 선택기가 입력 필드로 표시될 수도 있다<br/>
```html
<form>
  Select your favorite color:
  <input type="color" name="favcolor">
</form>
```

### 4.2.10 Type="range"
> 정해진 범위 안의 값을 입력하는 필드를 만든다<br/>
> 브라우저에 따라 슬라이드 컨트롤 필드가 표시될 수도 있다<br/>
```html
<form>
  <input type="range" name="points" min="0" max="10">
</form>
```

### 4.2.11 Type="month"
> 사용자가 월과 연도를 입력하는 필드를 만든다<br/>
> 브라우저에 따라 날짜 선택기 필드가 표시될 수도 있다<br/>
```html
<form>
  Birthday (month and year):
  <input type="month" name="bdaymonth">
</form>
```

### 4.2.12 Type="week"
> 사용자가 주와 연도를 입력하는 필드를 만든다<br/>
> 브라우저에 따라 날짜 선택기 필드가 표시될 수도 있다<br/>
```html
<form>
  Select a week:
  <input type="week" name="week_year">
</form>
```

### 4.2.13 Type="time"
> 사용자가 시간을 입력하는 필드를 만든다<br/>
> 브라우저에 따라 시간 선택기 필드가 표시될 수도 있다<br/>
```html
<form>
  Select a time:
  <input type="time" name="usr_time">
</form>
```

### 4.2.14 Type="datetime-local"
> 사용자가 날짜와 시간을 선택하는 필드를 만든다<br/>
> 브라우저에 따라 날짜 선택기 필드가 표시될 수도 있다<br/>
```html
<form>
  Birthday (date and time):
  <input type="datetime-local" name="bdaytime">
</form>
```

### 4.2.15 Type="email"
> email 주소를 입력하는 필드를 만든다<br/>
> 브라우저에 따라 폼이 제출 될 때 자동으로 email주소 유효성 검사를 실시한다<br/>
```html
<form>
  E-mail:
  <input type="email" name="email">
</form>
```

### 4.2.16 Type="search"
> 검색하는 필드를 만든다<br/>
```html
<form>
  Search Google:
  <input type="search" name="googlesearch">
</form>
```

### 4.2.17 Type="tel"
> 전화번호를 입력하는 필드를 만든다<br/>
```html
<form>
  Telephone:
  <input type="tel" name="usrtel">
</form>
```

### 4.2.18 Type="url"
> url주소를 포함하는 입력 필드를 만든다<br/>
> 브라우저에 따라 폼이 제출 될 때 자동으로 url 필드의 값 유효성 검사를 실시한다<br/>
```html
<form>
  Add your homepage:
  <input type="url" name="homepage">
</form>
```

## 4.3 Attribute
> 다양한 attribute로 input을 제한할 수 있다<br/>
> * **disabled**는 불리안 속성으로 속성을 명시하지 않으면 자동으로 false 값을 가지게 된다<br/>
> ```html
> <form action="/examples/media/action_target.php" method="get">
>   이름 : <input type="text" name="st_name"><br>
>   학번 : <input type="text" name="st_id"><br>
>   학과 : <input type="text" name="department" disabled><br>
>   <input type="submit">
> </form>
> ```
> * **min**은 허용되는 최솟값을 명시한다 이때 날짜를 입력하면 허용되는 최소 날짜를 명시한다<br/>
> * **max**는 허용되는 최댓값을 명시한다 이때 날짜를 입력하면 허용되는 최대 날짜를 명시한다<br/>
> ```html
> <form action="/examples/media/action_target.php" method="get">
>     생년월일 : <input type="date" name="bday" min="1900-01-01" max="2019-01-01"><br>
>     학년 : <input type="number" name="grader" min="1" max="4" ><br>
>     <input type="number">
> </form>
> ```
> * **maxlength**는 허용되는 최대 문자수를 명시한다<br/>
> ```html
> <form action="/examples/media/action_target.php" method="get">
>    이름 : <input type="text" name="st_name" maxlength="8"><br>
>    학번 : <input type="text" name="st_id" maxlength="12"><br>
>    학과 : <input type="text" name="department"><br>
>    <input type="number">
> </form>
> ```


## 4.4 label
> label 요소는 for 속성을 사용하여 다른요소와 결합할 수 있다<br>
> 이때 label 요소의 for 속성값은 결합하고자 하는 요소의 id 속성값과 같아야한다<br>
> label을 결합하고자 하는 요소 내부에 위치시키면 for 속성을 사용하지 않고 요소를 결합시킬 수 있다<br>
> label을 사용하면 마우스로 해당 text를 클릭하면 label요소와 연결된 요소를 곧바로 선택할 수 있다<br>
> label을 사용할 수 있는 요소는 button, input, meter, output, progress, select, textarea가 있다<br>
```html
<form action="/example.html" method="POST">
  <label for="meal">What do you want to eat?</label>
  <br>
  <input type="text" name="food" id="meal">
</form>
```

## 4.5 select
> select를 사용하면 여러 항목중에 고를수 있게할 수 있다<br>
> radio와 다른점은 옵션이 많아졌을때 버튼형식이 아닌 스크롤 형식으로 표시하여 더 깔끔하다<br>
```html
<select id="bun" name="bun">
  <option value="sesame">Sesame</option>
  <option value="potato">Potato</option>
  <option value="tomato">Tomato</option>
</select>
```

### 4.6 Datalist
> datalist는 input에서 type이 text일때 정해진 요소중 선택하는 필드를 생성한다<br>
> select와 다른점은 입력창에 검색을 하면 옵션을 찾을 수 있다<br>
```html
<datalist id="sauces">
  <option value="ketchup"></option>
  <option value="mayo"></option>
  <option value="choco"></option>
</datalist>
```

### 4.7 Textarea
> 자유롭게 작성할 수 있는 필드를 생성한다<br>
> 댓글창이나 블로그에 자주 사용된다<br>
> 여는코드와 닫는코드 사이에 문장을 작성하면 공백일때 해당문장이 출력된다<br>
> row와 col의 개수도 설정가능하다<br>
```html
<textarea id="extra" name="extra" rows="3" cols="40">Service
</textarea>
```

### 4.8 submit
> submit을 사용하면 양식을 서버에 보낼 수 있다<br>
> value값에 들어간 것이 보내는 버튼에 들어가고 누르면 제출된다<br>
```html
<form>
  <input type="submit" value="submit">
</form>
```

<br/><br/><br/>

5.&nbsp;Form Validation
------------------------------------------------------
## 5.1 Introduction to HTML Form Validation
> validation에는 여러가지 종류가 있다<br/>
> server-side validation은 서버에서 데이터가 전송될 때 발생한다<br/>
> 로그인 페이지에서 아이디와 비밀번호를 조합하여 엑세스 할때 사용된다<br/>
> client-side validation은 서버로 전송되기 전 브라우저에서 데이터를 확인한다<br/>
> 서버에서 정보를 확인하는데 걸리는 시간을 절약할 수 있다<br/>
> 또한 악성코드로 부터 서버를 보호하는데 도움이 된다<br/>


## 5.2 requiring an input
> 선택 사항이 아닌 필수 사항을 입력하는 창에 사용한다<br/>
> required를 사용하면 채우지 않고 제출할 때 경고메시지를 표시한다<br/>
```html
<form action="/example.html" method="POST">
  <label for="allergies">Do you have any dietary restrictions?</label>
  <br>
  <input id="allergies" name="allergies" type="text" required>
  <br>
  <input type="submit" value="Submit">
</form>
```

## 5.3 set min & max
> 입력 field가 number일때 최소값 또는 최대값을 할당할 수 있다<br/>
> 해당 값 범위를 벗어난 값을 제출할 때 경고메시지를 표시한다<br/>
```html
<form action="/example.html" method="POST">
  <label for="guests">Enter # of guests:</label>
  <input id="guests" name="guests" type="number" min="1" max="4">
  <input type="submit" value="Submit">
</form>
```

## 5.4 checking text length
> 입력 field가 text일때 최소 문자수 또는 최대 문자수를 할당할 수 있다<br/>
> 해당 길이 범위를 벗어난 값을 제출할 때 경고메시지를 표시한다<br/>
```html
<form action="/example.html" method="POST">
  <label for="summary">Summarize your feelings in less than 250 characters</label>
  <input id="summary" name="summary" type="text" minlength="5" maxlength="250" required>
  <input type="submit" value="Submit">
</form>
```

## 5.5 Matching a pattern
> 입력 field에 입력값을 제한 할 수 있다<br/>
> 설정된 정규 표현식이 아닌 값을 제출할 때 경고메시지를 표시한다<br/>
```html
<form action="/example.html" method="POST">
  <label for="payment">Credit Card Number (no spaces):</label>
  <br>
  <input id="payment" name="payment" type="text" required pattern="[0-9]{14,16}">
  <input type="submit" value="Submit">
</form>
```
> 다양한 정규 표현식이 존재한다<br/>
> 주로 사용되는 예시는 다음과 같다<br/>
> > 1. 숫자만
> > ```html
> > <input type="text" name="patternValue" pattern="\d*">
> > <input type="text" name="patternValue" pattern="^[0-9]+$">
> > ```
> > 2. 영문 대소문자만
> > ```html
> > <input type="text" name="patternValue" pattern="^[a-zA-Z]+$">
> > ```
> > 3. 영문 대소문자만(띄어쓰기 및 공백 가능)
> > ```html
> > <input type="text" name="patternValue" pattern="^[a-zA-Z\s]+$">
> > ```
> > 4. 숫자, 영문 대소문자만
> > ```html
> > <input type="text" name="patternValue" pattern="^[a-zA-Z0-9]+$">
> > ```
> > 5. 최소 8자리에서 최대 16자리 까지 숫자,영문,특수문자 각 1개 이상 포함(암호 유효성 검사)
> > ```html
> > <input type="text" name="patternValue" pattern="^(?=.*[A-Za-z])(?=.*\d)(?=.*[$@$!%*#?&])[A-Za-z\d$@$!%*#?&]{8,16}$">
> > ```

<br/><br/><br/>

6.&nbsp;Semantic HTML
------------------------------------------------------
## 6.1 Introduction to Semantic HTML
> semantic은 의미있는 의미론 이라는 뜻이다<br/>
> html 요소를 선택할 때 표시되는 방식이 아니라 의미에 따라서 선택하는 것이 semantic html이다<br/>
> 접근성, 검색엔진, 웹 개발자끼리의 협업 등에서 장점을 가진다<br/>
> 큰 마트에 표지판을 세우고 구역을 나누는 것과 비슷하다<br/>

## 6.2 header
> header는 도입부에 사용되며 nav 링크나 제목요소, 로고나 아이콘, 저자정보를 포함한다<br/>
> html 문서는 여러개의 header 요소를 포함할 수 있다<br/>
```html
<article>
    <header>
        <h3>날씨 정보</h4>
        <h4>2월 19일</h4>
        <p>- 기상청 제공 -</p>
    </header>
    <p>서울 : 맑음</p>
    <p>대전 : 흐림</p>
    <p>부산 : 비</p>
</article>
```

## 6.3 nav
> nav는 다른 페이지나 현재 페이지의 다른 부분과 연결되는 링크를 생성한다<br/>
> 보통 메뉴, 목차, 인덱스 등에 사용된다<br/>
```html
<nav>
    <a href="/html/intro">HTML</a> |
    <a href="/css/intro">CSS</a> |
    <a href="/javascript/intro">JavaScript</a>
</nav>
```

## 6.4 main
> main은 해당 문서의 main content를 정의할 때 사용한다<br/>
> main의 content는 문서의 중심 주제 또는 주요 기능과 직접적으로 관련되어 있어야한다<br/>
> 하나의 문서에는 단 하나의 main 요소가 존재해야 한다<br/>
> article aside footer header nav 요소의 자손 요소가 되어서는 안된다<br/>
```html
<main>
    <h1>바나나</h1>
    <p>바나나는 바나나는 파초과 바나나 속에 속하는 
     숙근성 영년생 열대과수를 총칭한다.</p>
    <article>
        <h2>다이어트 식품</h2>
        <p>바나나는 탄수화물이 약 27%이고 비타민 A와 C가 풍부하며, 
         100g당 87kcal의 열량을 갖는다.</p>
    </article>
    <article>
        <h2>다양한 섭취법</h2>
        <p>바나나는 열매를 주식으로 이용할 뿐 아니라 
         미성숙한 열매는 채소로 다양한 요리에 응용된다.</p>
    </article>
</main>
```

## 6.5 footer
> 문서나 특정 section의 footer를 정의할 때 사용한다<br/>
> 보통 저자, 저작권, 연락처, sitemap 등의 정보를 포함한다<br/>
```html
<footer>
    <p>Copyright © 2018 tcpschool.co.,Ltd. All rights reserved.</p>
    <address>Contact webmaster for more information. 070-1234-5678</address>
</footer>
```

## 6.6 section
> html 문서에 포함된 독립적인 section을 정의할 때 사용한다<br/>
> 관련있는 내용을 section 요소로 묶어 표시한다<br/>
> section 요소는 보통 제목 요소를 자식 요소로 포함하는 경우가 많다<br/>
```html
<section>
  <h2>Fun Facts About Cricket</h2> 
</section>
```

## 6.7 article
> 해당 문서나 페이지와 완전히 독립적으로 구성할 수 있는 요소를 정의할 때 사용한다<br/>
> 포럼포스트, 블로그포스트, 보도기사, 논평 등이 내용으로 포함된다<br/>
```html
<article>
    <h2>2월 19일 날씨 정보</h2>
    <h3>서울</h3>
    <p>맑음</p>
    <h3>대전</h3>
    <p>흐림</p>
    <h3>부산</h3>
    <p>비</p>
</article>
```

## 6.8 Aside
> main과 분리된 페이지 영역을 정의할 때 사용한다<br/>
> 주로 참고문헌, 미주, 코멘트, 인용문등이 포함된다<br/>
```html
<article>
  <p>The first World Series was played between Pittsburgh and Boston in 1903 and was a nine-game series.</p>
</article>
<aside>
  <p>
   Babe Ruth once stated, “Heroes get remembered, but legends never die.” 
  </p>
</aside>
```

## 6.9 Figure
> 사진이나 다이어그램과 같이 media를 text와 분리할 때 사용한다<br/>
> 해당 content를 제거해도 문서의 흐름에 영향이 없어야 한다<br/>
```html
<figure>
  <img src="overwatch.jpg">
</figure>
```

## 6.10 Figcaption
> figure요소의 caption을 정의할 때 사용한다<br/>
> media에 대한 부가 설명이 포함된다<br/>
> figure 요소의 첫번째나 마지막 자식 요소로만 위치할 수 있다<br/>
> p를 사용할때는 해당 설명이 figure과 독립적이지만 figcaption을 사용하면 의존하게 된다<br/>
```html
<figure>
  <img src="overwatch.jpg">
  <figcaption>This picture shows characters from Overwatch.</figcaption>
</figure>
```

## 6.11 Audio
> 음악이나 사운드를 정의 할 때 사용한다<br/>
> src에 파일 주소를 넣고 type에 파일 형식을 작성해주면 된다<br/>
> 현재 mp3, wav, ogg를 지원한다<br/>
> controls를 추가하면 play, mute와 같은 기능이 자동으로 지원된다<br/>
> autoplay를 추가하면 자동재생기능이 생성된다<br/>
```html
<audio controls>
  <source src="https://content.codecademy.com/courses/SemanticHTML/dogBarking.mp3" type="audio/mp3">
</audio>
```
