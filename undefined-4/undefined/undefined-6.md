# 나머지 매개변수, 전개구문

### 인수 전달

```javascript
function showName(name){
    console.log(name);
}
showName('Mike'); //mike
showName('Mike','Tom'); // mike
showName(); //undefined
```

### arguments : 화살표함수에는 X 

함수로 넘어 온 모든 인수에 접근  
함수 내에서 이용 가능한 지역 변수  
length/index  
Array 형태의 객체  
배열의 내장 메서드없음\(forEach,map\)

```javascript
function showName(name){
    console.log(arguments.length);// 2
    console.log(arguments[0]);// m
    console.log(arguments[1]);// t
}
showName('m','t');
```

### 나머지 매개변수\(Rest parameters\) 

```javascript
function showName(...name){
    console.log(names);
}
showName(); // []
showName('m'); //['m']
showName('m','t'); //['m','t']



function add(...numbers){
    numbers.reduce((prev, cur) => prev + cur);
    console.log(result)
}
add(1,2,3);//6
add(1,2,3,4,5,6,7,8,9,10);//55
```

### 생성자함수 첫글자대문자 

```javascript
function User(name, age, ...skills){ // 나머지매개변수는 마지막에 있어야함.
    this.name = name;
    this.age = age;
    this.skills = skills;
}
const user1 = new User('m',30,'html','css');
const user2 = new User('t',20,'JS','React');
const user3 = new User('j',10,'English');

console.log(user1);
```

### 전개구문\(Spread syntax\) : 배열 

```javascript
let arr1 = [1,2,3];
let arr2 = [4,5,6];
let result = [...arr1,...arr2];
console.log(result); // [ 1,2,3,4,5,6]
```

