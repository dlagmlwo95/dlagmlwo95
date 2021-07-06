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

## spread syntax

```javascript
{
    const obj1 = {key:'key1'};
    const obj2 = {key:'key2'};
    const array = [obj1, obj2];
    
    //array copy
    const arrayCopy= [...array];
    console.log(array,arrayCopy);
    
    const arrayCopy2 = [...array, {key:'key3'}];
    console.log(array, arrayCopy, arrayCopy2);
    
    //object copy
    const obj3 = {...obj1};
    console.log(obj3);
    
    //array concatenation
    const fruits1 = ['복숭아','딸기'];
    const fruits2 = ['바나나','키위'];
    const fruits = [...fruits1, ...fruits2];
    console.log(fruits) //복숭아 딸기 바나나 키위
    
    //object merge
    const dog1 = {dog:'개1'};
    const dog2 = {dog:'개2'};
    const dog = {...dog1, ...dog2};
    console.log(dog) //개2
}
```

## Default parameters

```javascript
{
function printMessage(message = 'default message'){
    console.log(message);
    }
    
    printMessage('hello');
    printMessage();  //default message
}
```

## Ternary Operator

```javascript
{

const isCat = true;
{
    //x
    let component;
    if(isCat){
    component = '고양이';
    }else {
    component = '개';
    }
    console.log(component);
}

// o  간단히 
{
    const component = isCat ? '고양이' : '개';
    console.log(component);
    //or
    console.log(isCat ? '고양이' : '개')
}

}
```

## Template Literals

```javascript
{
const weather = '해';
const temparature = '16도';

// X
console.log(
'Today weather is ' + weather + 'and temparature is' + temparature + '.' 

//o 간단히 
console.log(`Today weather is${weather} and temparature is ${temparature} .`)
}
```

