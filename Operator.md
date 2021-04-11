## Backgrounds (Primitive type vs Object type)
* Primitive type : 값 자체가 메모리에 저장됨
* 값 변경시, 다른 문자열로 replace하는것이며, 메모리의 데이터 자체를 수정하는 것은 아님
```javascript
let a = 'bat man';
a = 'bat man1';
```

* Object : reference를 생성하고 이를 통해 실제 값을 포인팅함 
* 즉, Object 자체는 변경 불가하지만 attribute는 포인터를 통해 값 변경이 수행됨

## Operators
### string operations
* 문자열 + 숫자는 문자열로 변환됨

```javascript
console.log('hello' + 'world');
console.log('1' + 2);
console.log(`1 + 2 = ${1+2}`);
```

* single quote issue 처리는 `\`
```javascript
console.log('ellie\'s book');
```

### numeric operations
```javascript
console.log(1 + 1);  // add
console.log(1 - 1);  // substract
console.log(1 / 1);  // divide
console.log(1 * 1);  // multiply
console.log(1 % 1);  // remainder
console.log(1 ** 1);  // exponentiation
```

### Increment and decrement operaion
```javascript
let counter =2;
cost preIncrement = ++counter;
const postIncrement = counter++;
```

### Assignment operaion
```javascript
let x = 3;
let y = 6;
x += y;  // x = x + y;
```

### Logical operaion
* || (or), && (and), ! (not)
* or 연산자는 첫번째 조건이 True이면, 연산이 멈춘다. (중요)
* and 연산자는 첫번째 조건이 False이면, 연산이 멈춘다. (중요)
* 연산속도가 heavy한 연산이 앞 조건으로 가면 비효율적이다. (중요)

```javascript
console.log(`or: ${value 1 || value 2 || check()}`);
```

### Equality
* loose equality, 타입을 자동으로 맞춤 (`==`)

```javascript
const a = '5'
const b = 5
console.log(a == b);  // true
```

* strict equality, 타입을 엄격하게 체크함 (`===`)

```javascript
const a = '5'
const b = 5
console.log(a === b);  // False
```

* object equality, 오브젝트는 직접 참조하지 않는 이상 다름을 유의

```javascript
const ellie1 = { name: 'ellie' };
const ellie2 = { name: 'ellie' };
const ellie3 = ellie1;

console.log(ellie1 == ellie2);  // False
console.log(ellie1 === ellie2);  // False
console.log(ellie1 === ellie3);  // True
```
 
* data type quiz

```javascript
console.log(0 == false);  // True
console.log(0 === false);  // False
console.log('' == false);  // True
console.log('' === false);  // False
console.log(null == undefined);  // True
console.log(null === undefined);  // False
```

* Ternary operator: `?`

```javascript
console.log(name === 'ellie' ? 'yes' : 'no');  
```

* do while loop : block 내 코드를 먼저 실행하고 조건에 맞는지 검사

```javascript
let i = 0;
do {
    console.log('test');
    i--;
} while (i > 0);
```

