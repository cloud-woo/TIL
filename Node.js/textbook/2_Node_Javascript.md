# 노드와 관련된 자바

### 1. ES2015(ES6)
노드 버전 6부터 ES6 문법을 사용할 수 있음  

+ 1.1 CONST, LET
```
if(true) {
  const y = 3;
}
console.log(y);  //Uncaught ReferenceError: y is not defined
```
const와 let은 블록 스코프를 가지므로 블록 밖에서는 변수에 접근할 수 없음. 블록 범위 : __중괄호__ (if, whie, for, function)  
   const : 한 번 대입하면 다른 값을 대입할 수 없음
   let : 다른 값을 대입할 수 있음.  
  

+ 1.2 : 템플릿 문자열  
백틱(`)으로 문자열을 감쌈 + __문자열에 변수를 넣을 수 있음__ 

ex) __ES5__
```
var num1 = 1;
var num2 = 2;
var result =3;
var string1 = num1+'더하기'+num2+'는 \''+ result+ '\'';
console.log(string1);
```

__ES6__

```
const num1 = 1;
const num2 = 2;
const result = 3;
const string = `${num1} 더하기 ${num2}는 '${result}'`;
```
${변수} 형식으로 변수를 더하기 기호 없이 문자열에 넣을 수 있음.  
백틱을 사용해서 큰따옴표나 작은따옴표도 같이 사용할 수 있음.  

+ 1.3 : 객체 리터럴  
객체의 메서드에 함수를 연결할 때 콜론(:)과 function을 붙이지 않아도 됨  
속성명과 변수명이 겹치는 경우에 한 번만 쓸 수 있음.
```
{ name : name, age: age } //ES5  
{ name, age} //ES6
```
객체의 속성명을 동적으로 생성할 수 있음  
```
oldObject[es + 6]  //ES5
[es+6]  //ES6
```
익숙해지면 코드의 양을 많이 줄일 수 있음.  

+ 1.4 : 화살표 함수  
```
//function 1

function add(x,y) {
 return x+y;
 }

//function 2

const add2 = (x,y) => {return x + y;} 

// function 3

const add3 = (x,y) => x+y;  //매개변수 하나일 시

// function 4
const add4 = (x, y) => (x + y);
```

위는 모두 같은 기능의 함수

this 바인드 방식  
