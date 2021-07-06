# 14. 자바스크립트 함수 기본

## 함수선언/

```javascript
function doSomething(){
    console.log('hello');
}
function add(a,b){
    const sum = a + b;
    return sum;
}

//호출
doSomething();

const result = add(1,2);
console.log(result);
```

```javascript
function doSomething(add){
    console.log(add);
    const result add(2,3);
    console.log(result)
}

function add(a,b){
    const sum = a + b;
    return sum;
}

//호출
doSomething(add);

const addFun = add;
console.log(add);
addFun(1,2);
```





