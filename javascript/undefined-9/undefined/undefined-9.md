# 유효범위

## 전역변수 지역변수

```javascript
var vscope = 'global';
function fscope(){
    var vscope = 'local';
    alert(vscope);
}
fscope();  //local

var vscope = 'global';
function fscope(){
    var vscope = 'local';
    vscope = 'local'
}
fscope();
alert(vscope); //global

//여기서 local은 지역변수, global은 전역변수
//지역변수는 그 지역(함수안)에서만 가능하다.
```

## 유효범위의 효

```javascript
function a (){
    var i = 0;
}
for(var i = 0; i < 5; i++){
    a();
    document.write(i);
} //0 1 2 3 4


function a (){
    i = 0;
}
for(var i = 0; i < 5; i++){
    a();
    document.write(i);
} // function a (){ i = 0 }에서 i는 전역변수가 되어 0이 됐음. 밑에꺼 실행하면 무한반복
```

## 전역변수를 사용하는 

```javascript
var MYAPP = {}
MYAPP.calculator = {
    'left' : null,
    'right' : null
}
MYAPP.coordinate = {
    'left' : null,
    'right' : null
}
 
MYAPP.calculator.left = 10;
MYAPP.calculator.right = 20;
function sum(){
    return MYAPP.calculator.left + MYAPP.calculator.right;
}
document.write(sum()); //30

//이런식으로 MYAPP.속성(소속)으로 사용한다.
```

#### 전역변수로 사용하고 싶지 않을 때

```javascript
// 감싸주고 맨밑에 ()바로 실행
(function(){
    var MYAPP = {}
    MYAPP.calculator = {
        'left' : null,
        'right' : null
    }
    MYAPP.coordinate = {
        'left' : null,
        'right' : null
    }
    MYAPP.calculator.left = 10;
    MYAPP.calculator.right = 20;
    function sum(){
        return MYAPP.calculator.left + MYAPP.calculator.right;
    }
    document.write(sum());
}())
```

