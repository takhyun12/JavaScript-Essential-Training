## Object
### Variable types
* primitive type : 더이상 작은 단위로 나누어질 수 없는 single item (eg. number, string, boolean, null, undefined, symbol)
* object type : single item(primitive type)를 여러개 묶어서 관리, Object = { key : value }의 형태로 관리
* function type : first-class fuction (함수의 파라미터로 전달, 변수로 할당, 리턴으로 사용가능)

### primitive type의 한계점
* 인자가 많아지면 추가해야할 작업이 많아서 관리의 효율성이 떨어짐. logical 하지 못함

```javascript
const name = 'ellie';
const age = 4;
print(name, age);
fuction print(name, age){
  console.log(name);
  console.log(age);
}
```

### Object type 사용 시 이점
* 호출과 관리가 간편해짐

```javascript
fuction print(person){
  console.log(person.name);
  console.log(person.age);
}

const ellie = { name: 'ellie'. age: 4 };
```

### Object의 선언

```javascript
const obj1 = {}; // object literal syntax
const obj2 = new Object(); // object constructor syntax
```

### Computed properties
* properties를 string type으로 object의 value에 접근가능 (=python)

```javascript
console.log(ellie.name);  // 코딩할때 사용하는것을 추천
console.log(ellie['name']);  // 동적으로 key/value를 받아올 때 사용하는것을 추천
```

```javascript
function printValue(obj, key){  // 동적으로 key/value 예시
  console.log(obj.key);  // X
  console.log(obj[key]);  // O
}
printValue(ellie, 'name');
```

### Property value shorthand
```javascript
const person1 = { name: 'bob', age: 2 };
const person2 = { name: 'steve', age: 3 };
const person3 = makePerson('ellie', 30);

function makePerson(name, age){  // Property value shorthand 예시
  return{
    name,
    age
  };
}
```

### Constructor Function
```javascript
const person1 = { name: 'bob', age: 2 };
const person2 = { name: 'steve', age: 3 };
const person3 = new Person('ellie', 30);

function Person(name, age){  // 첫글자 대문자
  // this = {} (생략가능)
  this.name = name;
  this.age = age;
  // return this (생략가능)
}
```

### in operator
* key가 object에 있는지 확인하는 operator
```javascript
console.log('name' in ellie);
}
```

### for in and for of
```javascript
for (key in ellie){  // for in
  console.log(key);
}
const array = [1, 2, 3, 4];
for (value of array){  // for of
  console.log(value);
}

```

### Cloning
* 아래와 같은 코드는 메모리 구조에서 reference를 copy할 뿐 데이터를 카피하지는 않음
```javascript
const user = { name: 'ellie', age: 20 };
const user2 - user
user2.name = 'coder';
console.log(user);  // { name: 'coder', age: 20}
```

* Object를 완전히 복제하는 방법
```javascript
const user = { name: 'ellie', age: 20 };

// method 1
const user2 = {};
Object.assign(user2, user);

// method 2 (one line)
const user2 = Object.assign({}, user);
```
