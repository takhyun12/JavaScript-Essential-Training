# JavaScript Essential Training

#### Author: Tackhyun Jung

#### Status: ~ing

## References

* 자바스크립트 공식 사이트 : ecma-international.org
* 자바스크립트 문법 참조 사이트 : develpoer.mozilla.org

## Backgrounds

* ECMAScript 표준 : 브라우저 내 스크립트 엔진 표준
* SPA(Single page application) : 웹 사이트 내에서 필요한 부분만 업데이트 하는 기술
* React native(Mobile app), Ngular, nodeJS(Back-end) Electron(Desktop app)

## JavaScript 문법

### let variable (added in ES6)
* ES6 이상의 js에서 변수를 선언하는 유일한 방법 (var는 권장하지 않음)

```javascript
let globalName = 'superman'; // global scope
{  
  let name = 'batman';
  console.log(name);
} // block scope
```

### var variable
* ES6 이전의 js에서 사용하였고, 현재는 권장하지 않는 방법
* var hoisting issue가 있음 (선언부를 최상단으로 올림)
* block scope을 무시하는 문제가 있

```javascript
console.log(name); // 변수선언 전 사용해도 오류가 발생하지 않음
var name = 'batman';
```
