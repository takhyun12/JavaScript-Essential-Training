## Backgrounds
* javascript의 class는 java 처럼 pure한 OOP가 아님
* javascript는 엄밀하게 보면 Procedural programming임
* javascript에서 function은 object 이므로, return이나 변수 등에 사용가능

## Function
### Fuction declaration
* 하나의 함수는 한가지의 일만 하는것이 좋음 (clean code)
* js의 naming은 verb를 통해 command의 형태로 하는것이 좋음 (eg. doSomething)

* javascript에서는 파라미터와 return의 타입을 알수가 없어서 난해함

```javascript
function printHello(message){
  console.log(message);
}
printHello('hello');
```

### Parameters
* premitive parameters : value가 전달됨
* object parameters : reference가 전달됨

```javascript
function changeName(obj){
  ojb.name = 'message';
}
const ellie = { name: 'ellie' };
changeName(ellie);
console.log(ellie);
```

### Default parameters (added in ES6)
* ES6부터 function에 default 값을 추가 가능

```javascript
function printHello(message, from = 'seoul'){
  console.log(message);
  console.log(from);
}
printHello('hello');
```

### Rest parameters (added in ES6)
* `...`을 사용하여 배열 형태로 입력받을 수 있다

```javascript
function printHello(...args){
  for (let 1=0; i < args.length; i++){
    console.log(args[i]);
  }
  
  for (const arg of args){
    console.log(arg);  // = python for in style
  }
  
  args.forEach((arg) ==> console.log(arg));  // foreach style
}
printHello('hello', 'there', '!');
```

### Scope
* Closure : 밖에서는 안이 보이지않고, 안에서는 밖을 볼 수 있다.
```javascript
let globalMessage = 'global';  // global variable
function printMessage(){
  let message = 'hello';
  
  function printAnother(){
    let child = '123';
  }
}
```

### Early rerurn
* invert if condition을 통해 빠른 리턴으로 예외처리
* 조건이 맞지 않는 경우에는 빠르게 리턴 (가독성을 높히기 위함)

```javascript
function badFunction(){
  if (user.pint > 10){
    // long logic
    return (x)
  }
}

function goodFunction(){
  if (user.pint <= 10){
    return 
  }
  // long logic
}
```

### Function expression
* 함수를 변수에 할당해서 사용하는 기법
* hoisting에 의해 선언부보다 윗단에서 코드 사용가능 (js engine이 위로 올려줌)

```javascript
print();  // hello
console print = function() {  // anonymous function (name x)
  console.log('hello');
}
print();  // hello
```

### Callback function
* 함수를 전달하여 콜백 수행

```javascript
function randomQuiz(answer, printYes, printNo){
  if (answer === 'love you'){
    printYes();
  }
  else{
    printNo();
  }
}
```

### Arrow function
* 코드를 간결하게 만들어주며, 무조건 anonymous function이다
```javascript
const simplePrint = function (){  // original
  console.log('test);
}

const simplePrint = () => console.log('test);  // arrow function
const add = (a, b) => a + b;
const simpleMultiply = (a, b) => {
  // do something 
  return a * b;  // block 사용 시 return 필수
}
```

### IIFE : Immediately Invoked Function Expression
* 함수의 선언을 괄호로 묶어서 뒤에 `()`를 사용하여 함수처럼 사용

```javascript
(function hello(){
  console.log('IIFE');
})();
```
