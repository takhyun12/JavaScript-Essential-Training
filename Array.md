## Backgrounds
* 일반적인 자료구조 : 동일한 type의 object를 담는 구조
* JS의 자료구조(dynamically typed language) : 다른 type의 object를 한번에 담을수 있으나 비권장

## Array
* 배열의 핵심은 index이며, 이를 통해 삽입, 삭제, 갱신을 수행한다
* 문자열 + 숫자는 문자열로 변환됨

### Array 선언

```javascript
const arr1 = new Array();
const arr1 = [1, 2];
```

### index position

```javascript
const fruits = ['apple', 'banana'];
console.log(fruits.length);
console.log(fruits[0]);  # apple
console.log(fruits[fruits.length - 1]);  # banana
```

### loop with array

```javascript
for (let i = 0; i < fruits.length; i++){
  console.log(fruits[i]);
}

for (let fruit of fruits){
  console.log(fruit);
}

fruits.forEach()
```
