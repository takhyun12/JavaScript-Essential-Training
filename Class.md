## Backgrounds (Primitive type vs Object type)
* Primitive type : 값 자체가 메모리에 저장됨
* 값 변경시, 다른 문자열로 replace하는것이며, 메모리의 데이터 자체를 수정하는 것은 아님

```javascript
let a = 'bat man';
a = 'bat man1';
```

## Class
### Class : 조금 더 연관있는 데이터를 한곳에 묶어놓는 컨테이너와 같은 프로그래밍 개념
* 일반적으로 field나 method를 가짐, field만 가지고 있다면 데이터 클래스라고 함
```javascript
class person{
  name;  // field
  age;   // field
  speak();  // method
}

```
