# 7. Object

## Object란.

object는 key와 value의 집합체이다.

## 1. Literals and properties

```javascript
 const obj1 = {}; // object literal
  const obj2 = new Object(); // object constructor

  function print (person){
    console.log(person.name);
    console.log(person.age);
  }
  
  const ellie = {name:'ellie',age :5};
  print(ellie);
  
  //최댜한 ㅣ런식으론 하지말자.
  ellie.hasJob = true;
  console.log(ellie.hasJob); 
```

## 2. Computed properties

```javascript
console.log(ellie.name);
console.log(ellie['name']);
ellie['hasJob'] = true;
console.log(ellie.hasJob);

function printValue(obj,key){
    consloe.log(obj[key]);
}
printValue(ellie,'name');
printValue(ellie,'age');
```

## 3. Property value shorthand

## 4. Constuctor function

```javascript
//3Property value shorthand
const person1 = {name:'bob', age: 2 };
const person2 = {name:'st', age: 3 };
const person3 = {name:'da', age: 4 };
const person4 = new Person('ellie',5);
console.log(person4);
//4. Constuctor function
function Person(name, age){
    this.name = name;
    this.name = age;
    }

//function makePerson(name,age){
//    return {
//      name:name, // return { name   
//      age:age, //age  } 로 쓸수있다. 
//  }
//}
```

## 5. In operator

해당하는 속성 확인 하는 방법

```javascript
console.log('name' in ellie);  
console.log('age' in ellie);  
console.log('random' in ellie);  
//true - 확인 여부를 확인 할 수 있다. 
// 해당하는게 없을 시 undefined
```

## 6. for..in vs for..of

```javascript
//for (key in obj)
for(key in ellie){  
  console.log(key);
}
//for (value of iterable)
const array = [1,2,3,4,5];

for(let i =0; i < array.length; i++){
  console.log(array[i]);
}

//위 방식을 for of문으로 변경할 수 있다.(똑같은거) 
for(value of array){
  console.log(value);
};
```

## 7. Fun cloning

```javascript
const user = {name : 'ellie', age : '20'};
const user2 = user;
user2.name = 'coder';
console.log(user);

//old way
const user3 = {};
for (key in user) {
    user3[key] =  user3[key]
}
console.clear();
console.log(user3);

const user4 = Object.assign({},user);
console.log(user4);
```

