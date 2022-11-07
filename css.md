Learn Css<br/>
=============
1.&nbsp;Setup and Syntax
----------------------------------------------
## 1.1 Intro to CSS
> css란 cascading style shhets의 약자이다<br/>
> html이 골격이라면 css는 보여지는 부분을 꾸미는데 사용한다<br/>
> 사실 html에서도 font 태그를 통해 font를 꾸밀 수 있었다<br/>
> 하지만 font태그가 중복되고 아무런 정보가 없는 코드가 들어가서 정보전달이 힘들어지자 css를 개발했다<br/>
> css를 사용하면서 유지보수가 편해졌다<br/>

## 1.2 CSS Anatomy
### 1.2.1 CSS Ruleset
> css에는 selecter declaration 이 있다<br/>
> declaration은 property와 value로 나뉜다<br/>
> selecter는 style하고 싶은 element를 target하는데 사용한다<br/>
> property는 바꾸고 싶은 내용이 포함된다<br/>
> value는 해당 element의 property를 어떤것으로 바꿀지에 대한 내용이다<br/>
```html
<style>
  p {
      color:blue;
  }
</style>
```

### 1.2.2 Inline Style
> css inline style이란 css코드를 html코드 사이사이에 넣어서 작성하는 방식이다<br/>
> opening tag안에 작성되며 attribute가 존재한다<br/>
> 여기서 attribute는 style이고 자체로 selecter의 역할을 한다<br/>
> css코드를 html코드 안에 바로 사용할 수 있는 장점이 있다<br/>
> 하지만 코드 수정이 어렵고 html의 목적인 정보전달에 불필요해서 잘 쓰지않는다<br/>
```html
<p style='color:blue;'>Hello world</p>
```

### 1.2.3 Internal Stylesheet
> internal stylesheet란 css코드를 head부분에서 style 태그와 함께 작성하는 방식이다<br/>
> 이때 style태그는 html이 css코드를 인식하는데 도움을 준다<br/>
```html
<head>
  <title>Vacation World</title>
  <style>
    p {
      color: green;
    }
  </style>
</head>
```

### 1.2.4 External Stylesheet
> html문서에는 오직 html 코드만 남겨두고 css코드를 다른파일에 저장하는 방식이다<br/>
> 현재 개발할때 가장 많이 사용하는 방식이다<br/>
> href와 rel을 통해 css파일을 html문서에 로드 해온다<br/>
> href='./style.css'는 relative URL로 css문서를 불러오는 것이다<br/>
> 이때 rel=stylesheet는 스타일 시트로 사용할 외부 리소스를 불러온다는 뜻이다<br/>
> 불러오는 링크는 다음과 같다<br/>
```html
<html>
<link href='./style.css' rel='stylesheet'>
```

<br/><br/><br/>

2.&nbsp;Selecter
------------------------------------------------------
## 2.1 Type
> type selecter는 가장 넓은 범위의 selecter이며 힘이 가장 약하다<br/>
> type selceter가 중복되면 가장 최근의 코드에 따라 style 된다<br/>
> 다음은 p tag에 style을 입히는 방법이다<br/>
```html
p {
  color: green;
}
```

## 2.2 Universal
> universal selecter는 모든 요소에 style을 적용시키는 selecter이다<br/>
```html
* { 
  font-family: Verdana;
}
```

## 2.3 Class
> class selecter는 중간 범위의 selecter이다<br/>
> 원하는 element의 opening tag에 class를 만들고 해당 class를 target하는 방식이다<br/>
> 꼭 class 설정이 선행되어야 한다<br/>
> 다음은 title class에 style을 입히는 방법이다<br/>
```html
<h1 class='title'> ... </h1>
```
```css
.title {
  color: teal;
}
```

## 2.4 Multiple Classes
> class selecter를 여러개 적용시킬 수 있다<br/>
> class를 만들어 줄때 여러개를 만들면 class를 원하는 개수만큼 가질 수 있다<br/>
> class는 띄어쓰기로 구분한다<br/>
```html
<h1 class='green bold'> ... </h1>
```
```css
.green {
  color: green;
}
 
.bold {
  font-weight: bold;
}
```

## 2.5 ID
> id selecter는 가장 좁은범위이고 힘이 가장 센 selecter이다<br/>
> 원하는 element의 opening tag에 id를 만들고 해당 id를 target하는 방식이다<br/>
> id는 유일무이하기에 id는 중복이 불가하고 하나의 element는 하나의 id만 가진다<br/>
```html
 <h1 class='title uppercase' id='article-title'>Top Vacation Spots</h1>
```
```css
#article-title {
  font-family: cursive;
}
```

## 2.6 Attribute
> href나 src같은 attribute를 target하여 적용시키는 selecter이다<br/>
> 특정 단어를 이용해 원하는 attribute를 target하여 적용시키기도 가능하다<br/>
```css
[href]{
   color: magenta;
}
```
```css
img[src*='winter'] {
  height: 50px;
}
이코드는 img src에 winter라는 단어가 포함된 이미지만 적용을 받는다
```

## 2.7 Pseudo-class
> pseudo-class란 선택하고자 하는 html 요소의 특별한 상태를 명시할 때 사용한다<br/>
> 여러가지 pseudo-class가 존재한다<br/><br/>
<img src="http://ways2web.weebly.com/uploads/5/4/4/8/54485903/3112201_orig.png" width="600px" height="450px" alt="Pseudo-class"></img><br/>
> 마우스 커서를 올리면 반응하는 hover를 이용한 예시이다<br/>
```css
a:hover {
  color: darkorange;
}
a 요소에 커서를 올리면 darkorange색으로 변한다
```

## 2.8 Chaining
> 특정 element에 한정하여 class들을 선택할 수 있다<br/>
> 다음 예시는 h1중 class가 special인 element를 선택하는 코드이다<br/>
```css
h1.special {
 
}
```

## 2.9 Descendant Combinator
> 다른 html element안에 들어있는 element를 선택할 때 사용한다<br/>
> 다음 코드는 description이라는 class를 가진 element를 먼저 찾고 그 하위에 있는 h5를 바꾼 예시이다<br/>
```css
.description h5 {
  color: blueviolet;
}
```
```css
질문
h5.description 랑 .description h5는 찾는순서외에 다른점은 없는건가?
```

## 2.10 Chaining and Specificity
> ul 내부의 li 안에 있는 요소를 접근할 수 있다<br/>
> li h4라는 코드를 작성하면 h4라는 element들중에서 li의 자손인 h4만 선택할 수 있다<br/>
```css
li h4 {
  color: gold;
}
```

## 2.11 Multiple Selectors
> 여러개의 특징을 가진 element들을 하나의 코드로 나타내고 싶을때 사용한다<br/>
> 코드의 중복을 방지해준다<br/>
```css
h1 {
  font-family: Georgia;
}
 
.menu {
  font-family: Georgia;
}
수정전 코드 (declaration이 두번 중복된다)
```

<br/>

```css
h1, 
.menu {
  font-family: Georgia;
}
수정후 코드 (훨씬 깔끔하다)
```

<br/><br/><br/>

3.&nbsp;Visual Rules
------------------------------------------------------
## 3.1 Introduction to Visual Rules
> CSS의 목적은 web page에 style을 입히는 것이다<br/>
> 기본적인 css visual rule들을 배워보는 단원이다<br/>

## 3.2 Font Family
> 글꼴을 바꾸는 property다<br/>
> font-family: ~~ 로 작성한다<br/>
> * font가 사용자의 컴퓨터나 site에 다운로드 되어있어야한다<br/>
> * 다수의 웹에서 지원하는 web safe fonts가 있다<br/>
> * 사용하는 font가 둘이상의 단어로 구성되어있다면 ;로 묶어주는것이 좋다<br/>
```css
h1 {
  font-family: 'Courier New';
}
```

## 3.3 Font Size
> 글꼴의 크기를 바꾸는 property다<br/>
> font-size: ~~ 로 작성한다<br/>
> px을 이용하여 바꿀 수 있다<br/>
```css
p {
  font-size: 18px;
}
```

## 3.4 Font Weight
> 글꼴의 굵기를 바꾸는 property다<br/>
> font-weight: ~~ 로 작성한다<br/>
> normal, bold 등의 value가 있다<br/>
```css
p {
  font-weight: bold;
}
```

## 3.5 Text Align
> 문자 정렬을 해주는 property다<br/>
> text-align: ~~ 로 작성한다<br/>
> left, center, right, justify(좌우에 딱맞게 간격조절)등의 value가 있다<br/>
```css
h1 {
  text-align: right;
}
```

## 3.6 Color and Background Color
> color를 바꿀때 사용하는 property다<br/>
> color은 foreground color와 background color의 영향을 받는다<br/>
> foreground color는 element의 색이다<br/>
> color: ~~ 로 작성한다<br/>
> background color는 글자 배경의 색이다<br/>
> background-color: ~~ 로 작성한다<br/>
```css
h1 {
  color: red;
  background-color: blue;
}
```

## 3.7 Opacity
> 투명도를 조절할때 사용하는 selecter다<br/>
> value는 0과 1 사이의 값이며 0에 가까워질수록 투명해진다<br/>
> opacity: ~~ 로 작성한다<br/>
```css
.overlay {
  opacity: 0.5;
}
```

## 3.8 Background Image
> background에 image를 넣을때 사용하는 selecter다<br/>
> value에는 url과 링크가 들어간다<br/>
> background-image: url(' 주소 ') 로 작성한다<br/>
> 주소에 external site 또는 relative file path를 통해 이미지를 불러온다<br/>
```css
.main-banner {
  background-image: url('https://www.example.com/image.jpg');
}
external site를 이용한 코드
```

<br/>

```css
.main-banner {
  background-image: url('images/mountains.jpg');
}
relative file path를 이용한 코드
```

## 3.9 Important
> 해당 declaration의 힘을 가장 세게 만들어주는 방법이다<br/>
> !important 를 사용하면 해당 코드의 target은 다른 declaration들을 무시한다<br/>
```css
p {
  color: blue !important;
}
 
.main p {
  color: red;
}
위 코드에서 main class의 p element도 모두 blue로 바뀐다
```

<br/><br/><br/>

4.&nbsp;The Box Model
------------------------------------------------------
## 4.1 Introduction to Box Model
> element가 box안에 들어있다<br/>
> borders, paddings, margins가 있다<br/>

## 4.2 The Box Model
> 가장 안쪽에 content가 있고 width, height로 크기를 조정할 수 있다<br/>
> content 바깥쪽에 padding이 있다<br/>
> padding 바깥쪽에 border이 있다<br/>
> 가장 바깥쪽에 margin이 있다<br/>
> <img src="https://content.codecademy.com/courses/updated_images/diagram-boxmodel_Updated_1-01.svg" width="600px" height="450px" alt="Box model"></img><br/>

## 4.3 Height and Width
> content의 가로 세로 크기를 조정할때 사용한다<br/>
> px로 설정하면 어디서 보든 똑같은 크기로 설정할 수 있다<br/>
```css
p {
  height: 80px;
  width: 240px;
}
```

## 4.4 Borders
> element를 감싸는 선이다<br/>
> width, style, color를 바꿀 수 있다<br/>
> 설정해주지 않은값은 default값으로 적용된다<br/>
```css
p {
  border: 3px solid coral;
}
```
```css
p {
  height: 80px;
  width: 240px;
  border: solid coral;
}
```

## 4.5 Border Radius
> Border의 모서리를 둥글게 만들 수 있다<br/>
> px을 이용하면 해당 픽셀만큼 둥글어진다<br/>
> %를 이용하면 해당 %만큼 둥글어진다<br/>
```css
div.container {
  height: 60px;
  width: 60px;
  border: 3px solid blue;
  border-radius: 50%;
}
```

## 4.6 Padding
> 사진의 frame과 비슷하다<br/>
> top, right, bottom, left를 이용해 다른값을 줄 수 있다<br/>
```css
p.content-header {
  border: 3px solid fuchsia;
  padding-bottom: 10px;
}
```
> value가 4개일때 top, right, bottom, left 순서<br/>
> value가 3개일때 top, left&right, bottom 순서<br/>
> value가 2개일때 top&bottom, left&right 순서<br/>
```css
p.content-header {
  padding: 6px 11px 4px 9px;
}
```

## 4.7 Margin
> 가장 바깥쪽의 공간이다<br/>
> top, right, bottom, left에 다른값을 줄 수 있다<br/>
```css
p {
  border: 3px solid DarkSlateGrey;
  margin-right: 15px;
}
```
> value가 4개일때 top, right, bottom, left 순서<br/>
> value가 3개일때 top, left&right, bottom 순서<br/>
> value가 2개일때 top&bottom, left&right 순서<br/>
```css
p {
  margin: 6px 10px 5px 12px;
}
```

## 4.8 Auto
> auto를 사용하면 browser에서 자동으로 가운데 정렬을 시켜준다<br/>
> width 설정이 선행되어야 한다<br/>
> 0 auto는 상하는 0으로 좌우는 자동으로 조정한다는 뜻이다<br/>
```css
div.headline {
  width: 400px;
  margin: 0 auto;
}
```

## 4.9 Minimum and Maximum Height and Width
> 해당 box의 최소, 최대 높이와 넓이를 설정할 수 있다<br/>
> text의 경우 브라우저 창이 너무 좁아지거나 확장되어 읽기 어려울때 유용하다<br/>
> 이때 max값이 box안의 content보다 작아지면 읽을 수 없는 내용이 될수도 있기에 주의해야한다<br/>
```css
p {
  min-width: 300px;
  max-width: 600px;
} 
너비조절
p {
  min-height: 150px;
  max-height: 300px;
} 
높이 조절
```

## 4.10 Overflow
> content가 box 바깥으로 넘칠때 overflow라는 property를 이용한다<br/>
> common value로 hidden, scroll, visible등이 있다<br/>
> overflow-x, overflow-y를 이용하여 horizontal과 vertical로 나눌수 있다<br/>
```css
p {
  overflow: scroll; 
}
```

## 4.11 Resetting Defaults
> 모든 browser는 각자의 default stylesheet가 있다<br/>
> clean한 slate에서 작업하기위해 해당 코드를 사용해주는 것이 좋다<br/>
```css
* {
  margin: 0;
  padding: 0;
}
```

## 4.12 Visibility
> 해당 element를 숨기거나 겹쳐지게 만들 수 있는 property다<br/>
> value값으로 hidden, visible, collapse를 가진다<br/>
> 해당 content만 없어지고 빈 box는 그대로 나오게된다<br/>
```css
<ul>
  <li>Explore</li>
  <li>Connect</li>
  <li class="future">Donate</li>
</ul>

.future {
  visibility: hidden;
}
Donate가 사라지게 만드는 코드
```

<br/><br/><br/>

5.&nbsp;Changing the box model
------------------------------------------------------
## 5.1 Box Model:Content-Box
> box model의 기본값은 content box이다<br/>
> 설정한 값에따라 그대로 크기가 커진다<br/>
> browser에서 사용하는 content-box는 다음과 같다<br/>
> <img src="https://content.codecademy.com/courses/updated_images/diagram-boxmodel_Updated_1-01.svg" width="600px" height="450px" alt="Content-Box"></img><br/>

## 5.2 Box Model:Border-Box
> box model을 border-box로 reset할 수 있다<br/>
> height와 width를 설정하면 content가 border, padding의 크기에 따라 자동으로 조정된다<br/>
> <img src="https://content.codecademy.com/courses/web-101/htmlcss1-diagram__borderbox.svg" width="600px" height="450px" alt="Border-Box"></img><br/>

<br/><br/><br/>

6.&nbsp;Display and Positioning
------------------------------------------------------
## 6.1 Position
> Block 요소는 자체적으로 공간을 차지해서 서로 겹치지 않는다<br/>
> element의 기본 위치는 position이라는 property를 이용해 변경할 수 있다<br/>
> position은 value값으로 static, relative, absolute, fixed, sticky를 가진다<br/>
> static은 기본값이다<br/>
```css
question {
  position: static;
}
```
## 6.2 Position: Relative
> relative를 이용해 box를 원하는 위치에 옮겨놓을 수 있다<br/>
> top, bottom, left, right를 이용하여 원하는 px만큼 이동한다<br/>
> top: 50px은 해당 box 위에 50px만큼 공간을 남긴다<br/>
```css
green-box {
  background-color: green;
  position: relative;
  top: 50px;
  left: 120px;
}
```

## 6.3 Position: Absolute
> absolute는 다른요소를 무시하고 옮겨진다<br/>
> box 가장 좌측 상단 모서리를 기준으로 옮겨진다<br/>
> box 바깥으로 element가 나갈 수도있다<br/>
```css
header {
position: absolute;
  width: 100%;
}
```

## 6.4 Position: Fixed
> fixed는 화면에서 고정된다<br/>
> 주로 navigation bar에 이용된다<br/>
> top, bottom, left, right를 이용해 위치를 고정시킬 수 있다<br/>
> <img src="https://static-assets.codecademy.com/Courses/Learn-CSS/Display-Position/Fixed.gif" width="600px" height="450px" alt="Border-Box"></img><br/>
``` css
.title {
  position: fixed;
  top: 0px;
  left: 0px;
}
```


## 6.5 Position: Sticky
> 정해진 범위를 벗어나면 해당 위치에 고정된다<br/>
> parent container의 가장 밑에 도달하면 다시 문서와 함께 scroll된다<br/>
> <img src="https://static-assets.codecademy.com/Courses/Learn-CSS/Display-Position/Sticky.gif" width="600px" height="450px" alt="Border-Box"></img><br/>
```css
.box-bottom {
  background-color: darkgreen;
  position: sticky;
  top: 240px;
}
```

## 6.6 Z-Index
> box끼리 겹쳐졌을때 어떤 element가 앞에 올지 정해준다<br/>
> z-index에 입력된 integer가 클수록 앞으로 오게된다<br/>
```css
.blue-box {
  background-color: blue;
  position: relative;
  z-index: 1;
}
 
.green-box {
  background-color: green;
  position: relative;
  top: -170px;
  left: 170px;
}
```

## 6.7 Display: Inline
> display라는 property는 해당 element의 horizontal space share여부를 결정한다<br/>
> display: none은 해당 element가 
> value값으로 inline, block, inline-block을 가진다<br/>
> inline element는 줄바꿈이 일어나지 않고 바로 전 element에 붙어서 시작한다<br/>
> 사용자가 크기를 지정할 수 없고 크기를 그대로 사용해야한다<br/>
> vertical-algin과 text-algin이 모두 작동한다<br/>
```html
To learn more about <em>inline</em> elements, read <a href="#">MDN documentation</a>.
<em>이나 <a>는 모두 inline element라서 줄바꿈이 일어나지 않는다
```
```css
h1 {
  display: inline;
}
```

## 6.8 Display: Block
> block element는 줄바꿈이 일어난다<br/>
> 사용자가 크기를 지정할 수 있다<br/>
> vertical-align과 text-align이 작동하지 않는다<br/>
```css
strong {
  display: block;
}
```

## 6.9 Display: Inline-Block
> Inline element와 Block element의 특징을 모두 갖고있다<br/>
> Inline element처럼 줄바꿈이 일어나지않는다<br/>
> Block element처럼 크기를 지정할 수 있다<br/>
```html
<div class="rectangle">
  <p>I’m a rectangle!</p>
</div>
<div class="rectangle">
  <p>So am I!</p>
</div>
<div class="rectangle">
  <p>Me three!</p>
</div>
```
```css
.rectangle {
  display: inline-block;
  width: 200px;
  height: 300px;
}
```
> 먼저 같은 class로 묶어준다<br/>
> 그다음 코드를 작성하면 다음과 같은 결과가 나온다<br/>
> <img src="https://static-assets.codecademy.com/Courses/Learn-CSS/Display-Position/display-inline-block.png" width="600px" height="450px" alt="Border-Box"></img><br/>

## 6.10 Float
> 원하는 방향으로 끝까지 이동시키고 싶을때 쓰는 property다<br/>
> text를 image주변에 wrapping할때 주로 사용한다<br/>
```css
.orange-section {
  background-color: orange;
  width: 50%;
  float: right;
}
```

## 6.11 Clear
> multiple element를 한번에 float하게 되면 layout이 깨질수 있다<br/>
> clear property는 element들이 bump 되었을때 어떻게 존재할지 결정해준다<br/>
> value로 left, right, both, none이 있다<br/>
> left,right: element의 left,right부분은 다른 element와 겹치지 않는다<br/>
> both: element끼리 서로 touch 하지 않는다<br/>
> none: element끼리 자유롭게 side로 빠진다<br/>
```css
div {
  width: 200px;
  float: left;
}
 
div.special {
  clear: left;
}
```

<br/><br/><br/>

7.&nbsp;Color
------------------------------------------------------
## 7.1 Foreground vs Background
> Foreground color는 element의 색상이다<br/>
> Background color는 배경의 색상이다<br/>
```css
h1 {
  color: red;
  background-color: blue;
}
```

## 7.2 Hexadecimal
> hex color는 code로 color를 나타낸다<br/>
> 16진법을 쓰고 0~9, A~F를 사용한다<br/>
```css
.italian {
  background-color: #000000;
}
```

## 7.3 RGB colors
> RGB value를 이용해 색을 표현한다<br/>
> red, gleen, blue 순서로 값이 높을수록 색이 많이 들어간다<br/>
```css
.green {
  background-color: rgb(143,188,143);
  }
```

## 7.4 Hex and RGB
> Hex color의 경우의수는 16^6 = 256^3 이다<br/>
> RGB또한 256^3으로 총 16777216개의 color를 표현할 수 있다<br/>
> Hex 에서 RGB로 변환할때 16진법을 이용하면 편하다<br/>
> 첫 두자리가 red 가운데 두자리가 green 마지막 두자리가 blue다<br/>
> 예) A8F184를 변환하면 R = 10x16+8, G=15x16+1 B=8x16+4 이므로 RGB값은 168,241,132다<br/>

## 7.5 Hue, Saturation, and Lightness
> 줄여서 HSL이라고 부른다<br/>
> hue는 색조, saturation은 채도, Lightness는 명도다<br/>
> hue는 0이 red, 120이 green, 240이 blue다<br/>
> saturation은 0%가 음영, 100%가 컬러 최대치이다<br/>
> lightness는 0%는 검은색, 100%는 흰색이다<br/>
```css
body {
  background-color: hsl(240, 100%, 80%);
}
```

## 7.6 Opacity and Alpha
> opacity는 element의 투명도를 조절하는 property다<br/>
> 숫자가 작을수록 투명해지며 0과1 사이의 value를 가진다<br/>
> hsla 또는 rgba로 네번째 값에 alpha가 추가되어 해당부분에 value를 넣어주면 된다<br/>
> hex color에서도 마지막 두자리에 00~FF의 값을 추가하여 투명도를 조절할 수 있다<br/>
```css
.midground {
  background-color: hsla(225, 100%, 25%, 0.4);
}
```















그리드
div, span 는 의미가없고 디자인 용도로만 쓰는 태그
block은 div
inline은 span을 사용
태그의 배치변경을 하고싶으면 grid를 사용하는데 이때 배치변경을 하고싶은 태그들을 다른 태그로 묶어주고 묶은 부모태그에 id를 부여해야한다
그 후 id가 부여된 부모태그에 대해 css를 적용한다
display:grid;
grid-template-columns; 150px 1fr;
이러면 앞에꺼는 150px 고정 뒤에꺼는 화면 전체에서 남은부분을 사용
grid-template-columns; 1fr 1fr;
이러면 반반
grid-template-columns; 3fr 1fr;
이러면 3:1

caniuse에서 해당 기술을 이용할 수 있는지 파악하는데 중요하다

반응형 디자인
수많은 화면에서 다르게 동작해야함

미디어쿼리
@media(min-width:800px) {
  div{
    display:none;
  }
}
800px 보다 크면 없어지게 만드는 코드
max를 사용하면 800px보다 작으면 없어지게 만들 수 있다

css 코드의 재사용
css코드가 중복되서 여러 페이지에서 등장할 때 중복제거가능
<link rel="stylesheet" href="style.css">
이렇게 쓰면 style.css 라는 파일을 만들어서
원래 style 자리에 써주면 된다
이때 style.css 파일이 cashing되면 네트워크 트래픽이 적어진다
