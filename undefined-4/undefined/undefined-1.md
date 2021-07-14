# 생성자 함수

## 객체

```javascript
let user = {
    name : 'Mike',
    age : 30,
}
```

## 생성자함수

```javascript
function User(name,age){ //첫글자는대문자로!!! 
    this.name = name;
    this.age = age;
}

//new 연산자 사용 
let user1 = new User('Mike',30);
let user2 = new User('Jane',22);
let user3 = new User('Tom',17);

```

## 메소드

```javascript
function User(name,age){
    this.name = name;
    this.age = age;
    this.sayName = function(){
        console.log(this.name);
    }
}

let user5 = new User('Han',40);
user5.SayName(); // Han
```



```javascript
function Item(title,price){
    this.title = title;
    this.price = price;
    this.showPrice = function(){
        console.log(`가격은 ${price}입니다.`);
    };
}

const item1 = new Item("인형",3000);
const item2 = new Item("인형투",2000);
const item3 = new Item("인형",30);

console.log(item1);

```

