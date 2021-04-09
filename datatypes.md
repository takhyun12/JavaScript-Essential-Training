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
* block scope을 무시하는 문제가 있음

```javascript
console.log(name); // 변수선언 전 사용해도 오류가 발생하지 않음
var name = 'batman';
```

### Contants
* 한번 선언하면 절대로 값을 바꿀수 없는 상수 (immutable data type)
* 여러 개의 thread가 동시에 변수에 접근할때 safety를 보장함

```javascript
const daysInWeek = 7;
const softwareName = 'Test';
```

### Variable types
* primitive type : 더이상 작은 단위로 나누어질 수 없는 single item
(eg. number, string, boolean, null, undefined, symbol)
* object type : single item를 여러개 묶어서 관리
* function type : first-class fuction (함수의 파라미터로 전달, 변수로 할당, 리턴으로 사용가능)

### Data types for number
* 다른 언어와 달리 js의 number는 데이터의 크기를 고려할 필요가 없음
* 기본적인 number는 over (-2**53) ~ 2*53 이지만, 
* js에서는 type이 dynamic하게 설정되기 때문에 number로 선언할 필요는 없음

```javascript
// javascript
let a = 12;
let b = 1.2;
```
```typescript
// typescript
let a: number = 12;
let b: number = 1.2;
```

### Infinity, -Infinity and NaN
* 오류를 유발하므로 예외처리 시 확인 필요
```javascript
const infinity = 1 / 0;  // Infinity
const negativeInfinity = -1 / 0;  // -Infinity
const nAn = 'string' / 2;  // NaN
```
