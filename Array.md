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

fruits.forEach((fruit, index, area) => console.log(fruit, index));
```

### addtion, deletion, copy
* Push : add an item to the end
* Pop : remove an item from the end

```javascript
fruits.push('melon');
fruits.pop()
```

* unshift: add an item from the beggining
* shift: remove an item from the beggining
* shift와 unshift는 push, pop에 비해 매우 느리다 (중요)
* 앞에서 데이터를 넣기 위해서는 기존 데이터들을 shifting 하는 과정이 있다

```javascript
fruits.unshift('melon');
fruits.shift();
```

* splice: remove an item by index position

```javascript
fruits.push('melon', 'lemon', 'kiwi');
fruits.splice(1, 1);  // 1번 인덱스부터 n개를 지움 (미지정 시 뒤에 모두를 다 지움)
```






