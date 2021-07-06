# 함수의 호출

## apply 소개 

```javascript
function sum(arg1, arg2){
    return arg1+arg2;
}
//두개가 같은 뜻이다.
alert(sum(1,2)); //3
//null 이아닌 다른 속성을 사용할때 사용!!
alert(sum.apply(null, [1,2])) //3
```

## apply 사

```javascript
o1 = {val1:1, val2:2, val3:3}
o2 = {v1:10, v2:50, v3:100, v4:25}
function sum(){
    var _sum = 0;
    for(name in this){
        _sum += this[name];
    }
    return _sum;
}
alert(sum.apply(o1)) // 6
alert(sum.apply(o2)) // 185





function sum(){
    var _sum = 0;
    for(name in this){
        if(typeof this[name] !== 'function')
        _sum += this[name];
    }
    return _sum;
}
o1 = {val1:1, val2:2, val3:3, sum:sum}
o2 = {v1:10, v2:50, v3:100, v4:25, sum:sum}
alert(o1.sum());
alert(o2.sum());
```

