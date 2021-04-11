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
    let child = 'hello';
  }
}
printHello('hello', 'there', '!');
```


