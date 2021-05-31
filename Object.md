## Object
### Variable types
* primitive type : 더이상 작은 단위로 나누어질 수 없는 single item (eg. number, string, boolean, null, undefined, symbol)
* object type : single item를 여러개 묶어서 관리
* function type : first-class fuction (함수의 파라미터로 전달, 변수로 할당, 리턴으로 사용가능)

### primitive type의 한계점
```javascript
const name = 'ellie';
const age = 4;
print(name, age);
fuction print(name, age){
  console.log(name);
  console.log(age);
}

```

### Class의 선언

```javascript
class Person{
  constructor(name, age){  // python의 init과 유사하게 사용가능
    this.name = name;
    this.age = age;
  }
  speak(){
    console.log('hi');
  }
}
```

### Class의 사용방법

```javascript
const ellie = new Person('ellie', 20);
console.log(ellie.name);
console.log(ellie.age);
```

### Getter와 Setter
* Class를 사용할 때 잘못된 입력이 들어오는 것이 방지하기 위해 Getter와 Setter 사용

```javascript
const ellie = new Person('ellie', -1);  // 나이를 -1로 입력함 (잘못된 코드의 예)
```
