## Backgrounds (Primitive type vs Object type)
* Primitive type : 값 자체가 메모리에 저장됨
* 다른 문자열로 replace하는것이며, 메모리의 데이터 자체를 수정하는 것은 아님

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


