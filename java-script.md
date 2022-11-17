Learn JavaScript<br/>
=============
1.&nbsp;Introduction to JavaScript
----------------------------------------------
## 1.1 Console
> Console이란 중요한 메시지를 표시해주는 곳이다<br/>
> Console keyword는 우리가 원하는 data나 action을 표시하는데 쓰인다<br/>
> semicolon(;)은 문장의 끝을 알려주는 부호이다<br/>
``` javascript
console.log(4);
console에 4가 표시된다
```

## 1.2 Comment
> slash두개를 이용해서 comment를 작성할 수 있다<br/>
```javascript
console.log(5);  // Prints 5
5만 출력된다

/*
This is all commented 
console.log(10);
None of this is going to run!
console.log(99);
*/
모두 주석처리된다

console.log(/*IGNORED!*/ 5);  // Still just prints 5
5만 출력된다
```

## 1.3 Data Types
> Number: 소수를 포함한 모든 숫자들이다<br/>
> String: 모든 문장부호를 포함한 문자들이다<br/>
> Boolean: true나 false로 표현되는 type이다<br/>
> Null: 의도적으로 value를 비울때 사용한다<br/>
> Undefined: 주어진 value가 없는것을 의미한다<br/>
> Symbol: unique한 식별자다<br/>
> Object: 관련된 data들의 집합이다<br/>
```javascript
console.log('headquarters: 575 Broadway, New York City');
console.log(40);
```

## 1.4 Arithmetic Operators
> 수학적 기호들을 사용할수 있다<br/>
> 덧셈, 뺄셈, 곱셈, 나눗셈, 나머지 표현이 가능하다<br/>
```javascript
console.log(3 + 4); // Prints 7
console.log(5 - 1); // Prints 4
console.log(4 * 2); // Prints 8
console.log(9 / 3); // Prints 3
console.log(11 % 3); // Prints 2
```

## 1.5 String Concatenation
> string도 +를 이용해 붙일 수 있다<br/>
> 이러한 작업을 concatenation이라 부른다<br/>
> 이때 띄어쓰기 없이 붙여준다<br/>
```javascript
console.log('I love to ' + 'code.')
// Prints 'I love to code.'
```

## 1.6 Properties
> .length를 사용하면 해당 문장의 길이가 출력된다<br/>
```javascript
console.log('Teaching the world how to code'.length);
```

## 1.7 Methods
> javascript구문은 3가지로 구성된다<br/>
> 'example string'.methodName() 형식이다<br/>
> example string 는 string instance라고 부른다<br/>
> .methodName은 method라고 부른다<br/>
> ()안에 들어가는 값은 argument라고 부른다<br/>
```javascript
console.log('hello'.toUpperCase()); // Prints 'HELLO'
console.log('Hey'.startsWith('H')); // Prints true
```

## 1.8 Built-in Objects
> javascript에는 built-in된 여러 함수들이 있다<br/>
> 그중에서 random한 값을 추출해내는 Math.random()함수가 있다<br/>
> 올림함수인 ceil과 내림함수인 floor가 있다<br/>
```javascript
console.log(Math.floor(Math.random() * 50)); // Prints a random whole number between 0 and 50
```


