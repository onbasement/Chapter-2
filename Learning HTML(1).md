Learning HTML(1)
=============
Introduction to HTML & HTML Document Standards
----------------------------------------------
## HTML
#### HTML Anatomy
HTML은 Hyper Text Markup Language의 약자
HTML은 기본구조를 만드는것 나중에 CSS와 JavaScript로 꾸밀 수 있음
opening tag와 closing tag가 존재하고 그 사이에 content가 들어간다
An opening tag (<p>)
The content (“My name is onbasement” text)
A closing tag (</p>)
ex) <p>My name is onbasement</p>
이 코드 한줄이 하나의 html element
opening tag는 <>안에 들어가있음
closing tag는 opening tag에 front slash가 들어있는 모양

#### The Body
web page를 구축할때 가장 주요한 요소 <body>와 </body>사이에 다양한 유형의 content를 추가할 수 있음
```html
<body> 
  <h1>Hello World</h1>
  <p>This paragraph is a child of the body element</p>
  <div>
    <p>This paragraph is a child of the div element and a grandchild of the body element</p>  
  </div> 
</body>
```

#### HTML Structure
html은 가족구조로 형성되어 있음
```html
<body>
  <h1>Hello World</h1>
  <p>This paragraph is a child of the body element</p>
  <div>
    <p>This paragraph is a child of the div element and a grandchild of the body element</p>  
  </div> 
</body>
```
Heading
h1 ~ h6 까지 크기순서로 있음
텍스트 크기를 원하는크기로 만드는데 쓰는거 같음

div
페이지를 나눌때 사용 html의 요소를 그룹화하는 데 매우 유용함
div는 링크,이미지 또는 비디오와 같은 텍스트 또는 기타 html이 들어갈수 있음

attributes
오픈태그 안에 추가하여 정보제공, 스타일변경등에 사용가능하게 만들어줌
name과 value로 구성되어있음
일반적으로 id를 사용함
<div id="intro">
  <h1>Introduction</h1>
</div>

<p> paragraphs
<span> 을 사용하면 다른 텍스트와 분리해줌
<div>
  <h1>Technology</h1>
</div>
<div>
  <p><span>Self-driving cars</span> are anticipated to replace up to 2 million jobs over the next two decades.</p>
</div>

<em> <strong>
em 은 italic체로 강조해줌
strong은 bold체로 강조해줌

<br>
enter와 같은 역할을 함

<ul> <li>
<ul>을 사용하면 목록 구성가능
목록안의 요소앞뒤에는 <li>를 써줘야함
<ul>
  <li>Limes</li>
  <li>Tortillas</li>
  <li>Chicken</li>
</ul>

<ol> <li>
순서가 있는 목록을 구성할때 <ol>을 사용
1. 2. 이렇게 작성됨
<ol>
  <li>Preheat the oven to 350 degrees.</li>
  <li>Mix whole wheat flour, baking soda, and salt.</li>
  <li>Cream the butter, sugar in separate bowl.</li>
  <li>Add eggs and vanilla extract to bowl.</li>
</ol>

<img> src
이미지를 넣고 싶을때 사용
<img src="image-location.jpg" />
큰따옴표 안에 넣는거 잊지말기
src는 출처를 알림
img 태그는 self closing tag여서 마지막에 /를 입력

alt
alt는 사진에 대한 부가설명을 제공
사진위에 올려두고 볼수도 있고 시각장애인에게 도움 또한 검색엔진에서도 중요한 역할을 함

<video> width height controls
여는태그와 닫는태그가 모두 필요함
width height를 통해 브라우저에 표시되는 비디오의 크기를 설정함 controls는 기본 비디오 컨트롤을 포함하도록 브라우저에 지시함
여는태그 닫는태그 사이에 있는 텍스트는 브라우저가 비디오를 표시할수 없을때 표시됨


<!DOCTYPE html>
html의 첫 코드행이어야한다
문서에서 사용중인 버전과함계 예상되는 문서유형을 알려줌

<html>
html 구조와 콘텐츠를 생성하려면 여는태그 닫는태그를 추가해 주어야함

<head>
웹페이지 자체에 대한 정보를 제공
<html> 바로 밑에서 열고 바로 밑에서 닫음

<title>
<head>안에서 태그에 지정된 제목을 표시함
<!DOCTYPE html>
<html>
  <head>
    <title>My Coding Journal</title>
  </head>
</html>
이러면 site title에 우리가 설정한것이 나타남

<a> href
앵커요소
<a href="https://en.wikipedia.org/wiki/Brown_bear">Learn More</a>
해당된곳을 클릭하면 링크로 이동하게 할수 있음

target
링크가 열리는 방법을 바꿀수 있음
일반적으로는 원래 보던 탭에서 열리는데target="_blank"를 추가하면 새탭에서 열림
<a href="https://en.wikipedia.org/wiki/Brown_bear" target="_blank">Learn More</a>

내부 링크로 연결하는법
project-folder/
|—— about.html
|—— contact.html
|—— index.html
이런식으로 같은 폴더안에 있는데 이동하고싶을때 <a href="./contact.html">Contact</a> 원래url자리에 해당 파일명을 입력하면 이동할수 있음
<a href="./aboutme.html">About Me</a>
이렇게 코드를 작성하면 클릭하면 해당 카테고리로 이동할수 있는 About Me 라는 글자가 추가됨

이미지로 링크 연결하는법
<a href="https://en.wikipedia.org/wiki/Opuntia" target="_blank"><img src="https://www.Prickly_Pear_Closeup.jpg" alt="A red prickly pear fruit"/></a>
이미지를 링크로 변환함

같은화면에서 특정 부분으로 이동하는법
원하는 부분에 id를 제공해야함
<p id="top">This is the top of the page!</p>
<h1 id="bottom">This is the bottom! </h1>
그 뒤에 href가 해당 부분 id에 걸린 ol을 작성
<ol>
  <li><a href="#top">Top</a></li>
  <li><a href="#bottom">Bottom</a></li>
</ol>

공백
<body>
    <p>Paragraph 1</p>
    <p>Paragraph 2</p>
</body>
이런식으로 공백및 들여쓰기 해주기
W3C 표준에서는 space 2칸이 기준이 됨

주석처리
<!-- 으로 시작해서 -->로 끝남
그사이의 모든 문자가 주석처리

<table>
표형식의 데이터
<tr>로 row를 생성
<td>로 넣은 데이터의 개수만큼 column이 생성됨
<th> table head로 주로 맨위나 맨왼쪽에 사용됨
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
이코드의 결과는
           saturday sunday
temperature   73      81

scope는 해당 요소의 성질을 나타냄 column row 등

여러 column에 같은값을 넣을때 colspan="정수" 사용하면 해당정수의 개수만큼의 칸이 합쳐짐 그리고 나머지가 오른쪽으로 밀린다
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

row를 합치고 싶을때는 rowspan="정수" 사용하면 해당정수의 개수만큼 칸이 합쳐지고 나머지가 오른쪽으로 밀림
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

<tbody>
표가 길어질때 머리글을 제외한 모든데이터를 포함하는 tbody를 생성

<thead>
thead를 이용하여 표의 열 머리글을 분리함

<tfoot>
총 합계등 마지막열의 정보가 특별한 것일때 분리해줌
