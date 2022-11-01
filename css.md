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
> pseudo-class란 선택하고자 하는 html 요소의 특별한 상태를 명시할 때 사용한다
> 여러가지 pseudo-class가 존재한다
> http://ways2web.weebly.com/uploads/5/4/4/8/54485903/3112201_orig.png




box model
테두리를 만든다
border-width:5px;
border-color:red;
border-style:solid;

전체를 쓰는 element를 block level element
자신의 크기만큼을 쓰는 element를 inline element라고 한다
display:inline; 이라고 하면 inline element가 된다
display:block; 을 쓰면 block element가 된다
display:none; 을 쓰면 화면에서 사라진다
선택자에 ,를 사용하면 중복을 지울 수 있다
h1, a{
border-width:5px;
border-color:red;
border-style:solid;
}
더줄이면
h1, a{
border:5px solid red;
}
순서는 중요하지 않음
padding:20px; 을 사용하면 문자와 차지하는 크기 사이에 20px이 생김
margin:0;을 하면 요소 사이에 간격이 없어짐
margin:20px;을 하면 20px만큼 간격이 생긴다
width:100px;을 전체를 쓰던것의 가로 크기가 100px로 바뀐다
height도 마찬가지
검사를 이용하면 도움을 받을 수 있다

밑 테두리: border-bottom:1px solid gray;

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
