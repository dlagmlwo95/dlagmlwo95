# arguments

## arguments란?

```javascript
function a(arg1){//arg1은 매개변
}
a(1);//여기서 1은 인자
```

```javascript
function sum(){
    var i, _sum = 0;    
    for(i = 0; i < arguments.length; i++){ //arguments = 4 (밑에 sum)
        document.write(i+' : '+arguments[i]+'<br />');
        _sum += arguments[i]; // 예) a=0; 일때 a+=1; 이것은 -> a=a+1; 이랑같
    }   
    return _sum;
}
document.write('result : ' + sum(1,2,3,4)); //10

//argument는 .length를 통해 몇개의 인자를 갖고있는지 알수있
```

## function length

```javascript
function one(arg1){
    console.log(
        'one.length', one.length, //arg1 이 1개이므로 1
        'arguments', arguments.length // one('val1','val2') 이게 2개이므로 2
    );
}
one('val1', 'val2');  // one.length 1 arguments 2  



function two(arg1, arg2){
    console.log(
        'two.length', two.length,
        'arguments', arguments.length
    );
}

two('val1');  // two.length 2 arguments 1
```

