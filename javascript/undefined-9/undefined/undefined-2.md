# 함수의 호출

## apply 소

```javascript
function sum(arg1, arg2){
    return arg1+arg2;
}
//두개가 같은 뜻이다.
alert(sum(1,2)); //3
alert(sum.apply(null, [1,2])) //3
```

