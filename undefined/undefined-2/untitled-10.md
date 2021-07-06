# 17. 연산자, boolean



```javascript
//false : 0, -0, null, undefined
//true : -1, 'hello' 'false'
let num; //undefined
if (num){
    console.log('true');
} else {
    console.log('false');
} //false



let obj = {
    name:'heejae',
};
if (obj) {
    console.log(obj.name);
}

obj && console.log(obj.name); //heejae
```

