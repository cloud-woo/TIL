# 2 노드와 관련된 자바


## 1. ES6
노드 버전 6부터 ES6 문법을 사용할 수 있음  

#### 1.1 CONST, LET
```
if(true) {
  const y = 3;
}
console.log(y);  //Uncaught ReferenceError: y is not defined
```
const와 let은 <u>블록 범위</u>를 가진다. 즉,  블록 밖에서는 변수에 접근할 수 없다. 
블록 범위 : __중괄호__ (if, while, for, function)  
+ `const` : 한 번 대입하면 다른 값을 대입할 수 없음
+ `let` : 다른 값을 대입할 수 있음.      



#### 1.2  템플릿 문자열  
백틱(`)으로 문자열을 감싼다.  
문자열에 변수를 넣을 수 있음  

ES5와 ES6를 코드로 비교해보면 아래와 같다.

ES5
```
var num1 = 1;
var num2 = 2;
var result =3;
var string1 = num1+'더하기'+num2+'는 \''+ result+ '\'';
console.log(string1);
```

ES6
```
const num1 = 1;
const num2 = 2;
const result = 3;
const string = `${num1} 더하기 ${num2}는 '${result}'`;
```
${변수} 형식으로 변수를 더하기 기호 없이 문자열에 넣을 수 있다.
백틱을 사용해서 큰따옴표나 작은따옴표도 같이 사용할 수 있다.  



#### 1.3  객체 리터럴  
객체의 메서드에 함수를 연결할 때 콜론(:)과 function을 붙이지 않아도 됨  
속성명과 변수명이 겹치는 경우에 한 번만 쓸 수 있음.

ES5 : 
```
{ name : name, age: age } 
{ name, age} //ES6
```
ES6 :
```
oldObject[es + 6] 
[es+6]  //ES6
```
객체의 속성명을 동적으로 생성할 수 있음  
익숙해지면 코드의 양을 많이 줄일 수 있음.  

#### 1.4  화살표 함수  
```
function add(x,y) {  //function 1
	 return x+y;  }
 
const add2 = (x,y) => {return x + y;}  //function 2

const add3 = (x,y) => x+y;  // function 3

const add4 = (x, y) => (x + y);// function 4
```

위 4개의 함수는 모두 같은 기능을 하는 함수다.

#### 1.5 비구조화 할당

#### 1.6 프로미스
콜백 대신 프로미스 기반으로 재구성됨

1. 프로미스 객체를 생성
	```
	const condition = ture; //true면 resolve, false면 rejcect
		  const promise = new Promise((resolve, rejdct) => {
				  if(condition) {
					  resolve('성공');
					} else { 
					reject('실패');
					}
			});

#### 1.7 async/await

---

## 2 프런트엔드 자바스크립트
