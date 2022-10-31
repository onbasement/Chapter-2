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



intro to css
처음엔 html만 존재 전자문서라는 정보를 만들 수 있었다
아름다우며 보기좋은 형태로 만들기 위한게 css
font 태그를 통해 다른색을 사용할 수 있다
font 태그는 정보를 담지 않기때문에 정보전달을 하기에 부적합한 코드가 되버림
또한 중복된 font 태그를 css를 통해 제거할 수 있다
가독성이 높아지고 유지보수가 편해진다

css를 사용한다는 것을 html 문법으로 이야기 해주어야 한다
<style> 태그 안쪽에 css를 작성하면 된다

<style>
a {
  color: red;text-decoration: none;
}
</style>

css 기본문법
html 코드 안에서도 style="color:red"를 사용가능
Selecter a{} 이게 selecter 누구에게 적용 할 것인지 정한다
declaration color:black; 이게 선언이고 무엇을 적용할 것인지
property는 color, value는 red
style태그를 사용하면 selecter가 포함됨
style 속성을 사용하면 해당 부분에 직접 추가하면 됨

css 선언 찾으면 다나옴
text-decoration: none; 을 사용하면 밑줄이 없어짐
text-align: center; 가운데 정렬
text-size: 45px; 텍스트 크기 설정

css 선택자 이것도 찾으면 다나옴
class를 이용해서 우리가 원하는 태그만을 바꿀수 있다
class="saw"라고 하면 해당 문장이 saw class에 속하게 된다
그리고 .saw라고 선택자를 쓰면 class가 saw인 모든 태그를 가리키게 된다
class는 띄어쓰기로 구분해서 여러개를 쓸 수가 있다 
이때 class가 여러개면 가장 마지막 명령을 따른다

이게 별로여서 id 태그를 이용한다
#active라고 하면 id가 active인 태그가 선택된다
#grid ol을 하면 부모가 grid ol만 선택된다
id선택자는 class 선택자를 이긴다
class선택자는 태그 선택자를 이긴다
id값은 유일무이한 값이기 때문에 중복하면 안된다

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
