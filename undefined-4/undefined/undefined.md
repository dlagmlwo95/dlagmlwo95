# 변수

## 변수

* var는 한번 선언된 변수를 다시 선언할 수 있다.
* var는 선언하기 전에 사용할 수 있다.



```javascript
var name = 'mike';
console.log(name);

var name = 'jane';
console.log(name);
----------------------------
let name = 'mike';
console.log(name)

let name = 'jane';
console.log(name); //error
----------------------------
console.log(name); 
var name = 'mike'; 

var name;   // hoisting 호이스팅이라고 
console.log(name); //undefined
name = 'mike';
//선언(name)은 호이스팅 되지만 할당('mike')은 호이스팅이 되지 않는다
```

### 호이스팅

스코프 내부 어디든 변수 선언은 최상위에 선언된 것  처럼 행동

### TDZ : Temporal Dead Zone

```javascript
console.log(name) // TDZ영역
const name = 'Mike' // 힘수 선언 및 할당
console.log(name) // 사용 가능


//문제 없는 코
let age = 30;
function showAge(){
    console.log(age)
}
showAge();

// 문제 있는 드
let age = 30;
function showAge(){
    console.log(age); //TDZ
    let age = 20
}
showAge();
```

### 변수의 생성과정

* 1.선언단계
* 2.초기화단계
* 3.

var 1. 선언 및 초기화 단계  .2 할당 단계   
let 1.선언단계 2.초기화단계 3.할당단계  
const 1.선언 + 초기화 + 

### 함수 스코프\(function-scoped\) 

var

### 블록 스코프\(block-scoped\) 

let , const \(지역변수만\)

```javascript
const age = 30;
if(age>19){
    var txt = '희재'; // var는 안에서 선언했지만 밖에서도 가능.
}
console.log(txt); // 
```

