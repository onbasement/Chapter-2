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

<br/><br/><br/>

2.&nbsp;Variables
----------------------------------------------
## 2.1 Create a Variable: var
> 변수선언코드는 다음과 같다
```javascript
var myName = 'Arya';
console.log(myName);
// Output: Arya
```
> var은 variable의 약자이다<br/>
> var은 새로운 변수를 만들거나 선언할때 사용한다<br/>
> myName자리에는 변수의 이름이 들어간다<br/>
> Arya자리에는 value값이 들어간다<br/>

<br/>

> variable 이름을 정할때는 몇가지 규칙이 있다<br/>
> * 숫자로 시작할 수 없다<br/>
> * 대문자,소문자가 구분된다<br/>
> * keyword와 같을 수 없다<br/>

## 2.2 Create a Variable: let
> let으로 새로운 variable을 생성할 수 있다<br/>
> let은 해당 value값을 재정의할 수 있다<br/>
> value값 없이 정의하면 undefined상태로 남아있는다<br/>
```javascript
let meal = 'Enchiladas';
console.log(meal); // Output: Enchiladas
meal = 'Burrito';
console.log(meal); // Output: Burrito
```

## 2.3 Create a Variable: const
> const도 새로운 variable을 생성할 수 있다<br/>
> const는 해당 value값을 재정의할 수 없다<br/>
> value값 없이 정의하면 syntaxerror가 발생한다<br/>
> value값을 재정의하면 TypeError가 발생한다<br/>
``` javascript
const myName = 'Gilberto';
console.log(myName); // Output: Gilberto
```

## 2.4 Mathematical Assignment Operators
> python이랑 비슷하게 변수를 재정의 할때 += 와 같은 기호를 사용한다<br/>
```javascript
let x = 20;
x -= 5; // Can be written as x = x - 5
console.log(x); // Output: 15
 
let y = 50;
y *= 2; // Can be written as y = y * 2
console.log(y); // Output: 100
 
let z = 8;
z /= 2; // Can be written as z = z / 2
console.log(z); // Output: 4
```

## 2.5 The Increment and Decrement Operator
> 덧셈기호나 뺄셈기호를 두번써서 value를 1만큼 더하거나 뺄 수 있다<br/>
```javascript
let a = 10;
a++;
console.log(a); // Output: 11

let b = 20;
b--;
console.log(b); // Output: 19
```

## 2.6 String Concatenation with Variables
> 문자열도 +를 통해 여러 문자들을 붙일 수 있다<br/>
```javascript
let myPet = 'armadillo';
console.log('I own a pet ' + myPet + '.'); 
// Output: 'I own a pet armadillo.'
```

## 2.7 String Interpolation
> 문자열 중간에 $를 사용하여 원하는 문자를 넣을 수 있다<br/>
> backticks를 이용해 문자를 작성해야 사용할 수 있다<br/>
```javascript
const myPet = 'armadillo';
console.log(`I own a pet ${myPet}.`);
// Output: I own a pet armadillo.
```

## 2.8 typeof operator
> typeof를 사용하면 해당 value의 type을 알아낼 수 있다<br/>
```javascript
const unknown1 = 'foo';
console.log(typeof unknown1); // Output: string
 
const unknown2 = 10;
console.log(typeof unknown2); // Output: number
 
const unknown3 = true; 
console.log(typeof unknown3); // Output: boolean
```



