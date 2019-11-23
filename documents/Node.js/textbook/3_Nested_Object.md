# 3 노드 기능 알아보기
노드는 DOM이나 BOM이 없어 window와 document 객체를 사용할 수 없다. 
## 1. 노드 내장 객체

#### 1.1 global 
전역 객체이다.
require를 사용할때 global.require 이 생략되어 있는 거다.

```
$ node
> global
```
다음 명령어를 사용하면 global의  속성들을 알 수 있음.


#### 1.2 console

+ console.time ('레이블명');   //timeEnd와 함께 쓰이며 사이의 시간 측정
+ console.timeEnd('레이블명');
+ console.log(내용) 
+ console.error(에러내용); 에러를 콘솔에 표시
+ console.dir(객체, 옵션);   // 객체를 콘솔에 표시
	 ```
	 const obj = {
	outside : {
		inside: {
			key: 'value',
		},
	}, 
	};  
	console.dir(obj, {colors:false, depth:2});
+ console.trace(레이블) : 에러가 어디에서 발생했는지 추적할 수 있음.

#### 1.3 타이머
+ setTimeout(콜백함수, 밀리초):
+ setInterval(콜백하무, 밀리초);
+ setImmediate(콜백함수) : 콜백 함수를 즉시 실행

+ clearTimeout(아이디) : setTimeout 취소
+ cleaerInterval(아이디) :setIntervval 취소
+ clearImmediate(아이디) : setImmediate 취소

#### 1.4 __filename, __dirname
+ console.log(__filename)
+ console.log(__dirname);


#### 1.4 module, exports
모듈을 만든다.

