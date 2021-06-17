# 값으로서의 함수와 콜백

## 값으로서의 함

```javascript
//함수
function a(){} 
 
//메소드  b: function(){}
a = {
    b:function(){
    }
};


function cal(func, num){
    return func(num)
}
function increase(num){
    return num+1
}
function decrease(num){
    return num-1
}
alert(cal(increase, 1)); // 2
alert(cal(decrease, 1)); // 0



function cal(mode){
    var funcs = {
        'plus' : function(left, right){return left + right},
        'minus' : function(left, right){return left - right}
    }
    return funcs[mode];
}
alert(cal('plus')(2,1));   //3
alert(cal('minus')(2,1));   // 1




/* var process 가 총 3개 length : 0 1 2*/

var process = [
    function(input){ return input + 10;},  //1 + 10 = 11
    function(input){ return input * input;}, //11 * 11 = 121
    function(input){ return input / 2;} // 121 / 2 = 60.5
];
var input = 1;
for(var i = 0; i < process.length; i++){
    input = process[i](input);  //0 일때 return input + 10 이고, 1일때  input * input;, 2일때 input / 2 
}
alert(input); //60.5
```

## 콜백 함

```javascript
var numbers = [20,10,9,8,7,6,5,4,3,2,1];
var sortfunc = function(a,b){
    return a - b;
    /*if(a > b){
        return 1;
    } else if(a < b){
        return -1;
    } else {
        return 0;
    }*/
}
console.log(numbers.sort(sortfunc)); //sortfunc는 콜백함수.
// a - b   1 2 3 4 ... 20
// b - a   20 10 9 8 ... 1


//numbers.sort() //numbers는 객체,배열 sort()는 메소드라고함.
```



