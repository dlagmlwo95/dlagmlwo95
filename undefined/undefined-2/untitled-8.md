# 19.  최신 문법 정리



```javascript
{
const ellie1 = {
    name: 'ellie',
    age : '18',
};
const name = 'ellie';
const age = '18';
```



```javascript
//array
const animals = ['고양이','개'];

{
const first = animals[0];
const first = animals[1];
console.log(first, second);
}

{
const [first, second] = animals;
console.log(first,second);
}
```



```javascript
//spread syntax

{
    const obj1 = {key:'key1'};
    const obj2 = {key:'key2'};
    const array = [obj1, obj2];
    
    //array copy
    const arrayCopy= [...array];
    console.log(array,arrayCopy);
    
    const arrayCopy2 = [...array, {key:'key3'}];
    console.log(array, arrayCopy, arrayCopy2);
}
```

