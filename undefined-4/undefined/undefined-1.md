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

