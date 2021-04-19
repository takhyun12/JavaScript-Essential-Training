## Class
### Class란? 조금 더 연관있는 데이터를 한곳에 묶어놓는 컨테이너(틀)을 만드는 프로그래밍 개념
* 쉽게말해, Class는 데이터가 들어올 틀을 의미하며, 이를 통해 생성된 instance가 Object이다.
* Javascript는 ES6에서 추가된 개념임. 이전에는 클래스 없이 Object를 생성했음
* 일반적으로 field나 method를 가짐, field만 가지고 있다면 데이터 클래스라고 함

```javascript
class Person{
  name;  // field
  age;   // field
  speak();  // method
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
### Class의 사용

```javascript
const ellie = new Person('ellie', 20);
console.log(ellie.name);
console.log(ellie.age);
```

