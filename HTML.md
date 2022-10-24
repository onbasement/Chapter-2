Learning HTML<br/>
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
