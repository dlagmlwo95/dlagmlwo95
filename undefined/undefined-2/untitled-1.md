# 15. 변수 primitive와 object

변수는 프로그래밍 언어에서 처리해야 되는 데이터를 담을 수 있도록 도와주는 것\(데이터를 담고있는 것\)



```javascript
// number, string, boolean, null, undefined
let number = 2;
let number2 = number;
console.log(number); // 2
console.log(number2); // 2

number2 = 3;
console.log(number); //2
console.log(number2); //3

```

## object

```javascript
let obj = {
    name : 'heejae',
    age: 2,
};
console.log(obj.name) //heejae

let obj2 = obj;
console.log(obj2.name) // heejae

obj.name = 'imheejae';
console.log('-----');
console.log(obj.name);//imheejae
console.log(obj2.name);//imheejae
```

## let,const

```javascript
//let은 변경 가능
let a = 2;
a = 5;


//const 는 변경 불가능
const num = 2;
num = 4 // x




//오브젝트는 오브젝트 자체가 담겨있는게 아니라 레퍼런스가 있기 때문에 안에 내용은 변경 가능.
const obj = {
    name: 'heejae',
    age: 2,
};
obj.name = 'imheejae'; 

```

