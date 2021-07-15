# 클래스

## Class

class문은 new를 무조건 써야함

class의 메서드는 forin문에서 제외됨.

```javascript
//생

const User = function (name,age){
  this.name = name;
  this.age = age;
  this.showName = function(){
    console.log(this.name);
  };
};
const mike = new User('mike',30);

//Class 클래스는 new가 무조건 
class User2 {
  constructor(name,age){  //constuctor 는 객체를 만들어주는 생성자 
    this.name = name;
    this.age = age;
  }
  showName(){
    console.log(this.name);
  }
}
const tom = new User2('tom');



//생성자함수에서 클래스와 동일하게 동작까지 만드는 식 
const User = function (name,age){
  this.name = name;
  this.age = age;
//  this.showName = function(){
//   console.log(this.name);
//  };
};
User.prototype.showName = function() {
  console.log(this.name);
};
const mike = new User('mike',30);
```

## class 상속: extends

```javascript
class car { 
  constructor(color){
    this.color = color;
    this.wheels = 4;
  }
  drive(){
    console.log('drive...');
  }
  stop(){
    console.log('stop')
  }
}

class Bmw extends Car {
  park() {
    console.log('park');
  }
}
const z4 = newBmw('blue');
```

## class 메소드 오버라이딩

```javascript
//위와 같음
class car { 
  constructor(color){
    this.color = color;
    this.wheels = 4;
  }
  drive(){
    console.log('drive...');
  }
  stop(){
    console.log('stop')
  }
}

class Bmw extends Car {
  park() {
    console.log('park');
  }
  stop(){
  console.log('off')
}

z4.stop(); //off 동일한 메서드를 정의하면 덮어쓰게됨.

//부모의 메서드를 그대로 사용하면서 확장하고 싶을땐 super.stop()
class Bmw extends Car {
  park() {
    console.log('park');
  }
  stop(){
  super.stop()
  console.log('off')
}
z4.stop(); // stop off
```

## class 오버라이딩

```javascript
//위와 같음
class car { 
  constructor(color){
    this.color = color;
    this.wheels = 4;
  }
  drive(){
    console.log('drive...');
  }
  stop(){
    console.log('stop')
  }
}

class Bmw extends Car {
constructor(){
super();
  this.navigation = 1;
  }
  park(){
    console.log('park');
  }
}
```

