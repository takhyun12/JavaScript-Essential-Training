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

* 이러한 문제를 해결하기 위한 Get/Set 적용 예시
* call stack size exceeded 예방하기 위한 naming 설정 필요(중요)

```javascript
class Person{
  constructor(name, age){  // python의 init과 유사하게 사용가능
    this.name = name;
    this.age = age;
  }
  
  get age(){
    return this._age;
  }
  
  set age(value){
    // if (value < 0{
    //   throw Error('age can not be negative!');
    // }
    this._age = value < 0 ? 0 : value;
  }
}
```

### Public, Private Fields
* 아무런 기호도 붙히지 않으면 Public, `#`을 사용하면 Private
* private fields는 class 외부에서는 읽거나 변경이 불가능 함

```javascript
class Experiment{
  publicField = 2;  // public field
  #privateField = 0;  // private filed
}
```

### Static
* static을 붙히면 Object 마다 할당되지 않고 class 자체에 정의하는 방법임
* object에 상관없이, 공통적인 것을 static으로 할당하면 메모리를 절약 가능

```javascript
class Article{
  static publisher = 'dream coding';
  constructor(articleNumber){
    this.articleNumber = articleNumber;
  }
  
  static printPublisher(){
    console.log(Article.publisher);
  }
}

const article1 = new Article(1);
const article2 = new Article(2);

console.log(article1.publisher);  // error (undefined)
console.log(Article.publisher);  // dream coding
```

### 상속과 다양성
* 공통적인 특징을 하나로 선언하여 재사용성, 유지보수성 그리고 다양성을 높히는 방법론

```javascript
class Shape{
  constructor(width, height, color){
    this.width = width;
    this.height = height;
    this.color = color;
  }
  
  draw(){
    console.log('drawing!');
  }
  
  getArea(){
    return width * this.height;
  }
}
```

* Javascript에서 Class를 상속받는 방법으로 부모 클래스의 함수와 필드를 사용 가능

```javascript
class Rectangle extends Shape {}

const rectangle = new Rectangle(20, 20, 'blue');
rectangle.draw();
```

* Overriding을 통해 필요한 함수만 재정의 해서 사용 가능

```javascript
class Rectangle extends Shape {}
class Triangle extends Shape {
  getArea(){  // overriding
    return (this.width * this.height) / 2;
  }
}
```

### instanceOf
* object가 해당 class를 통해 만들어진 것인지 확인하는 방법 (true / false)
* Javascript의 모든 ojbect는 Object로부터 상속받음

```javascript
console.log(rectangle instanceof Rectangle);
console.log(triangle instanceof Object);
}
```
