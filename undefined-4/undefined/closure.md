# 클로저\(Closure\)

## 클로저

함수와 렉시컬 환경의 조합  
함수가 생성될 당시의 외부 변수를 기억, 생성 이후에도 계속 접근  

## 어휘적 환경 \(Lexical Environment\)

```javascript
let one; //Lexical 환경   one:초기화x 사용불가
one = 1;

function addOne(num){ // Lexical 환경   addOne : function
    console.log(one+ num);
}

addOne(5) //num 5
//코드에서 변수를 찾을때 내부 -> 외부 -> 전역lexical환경
//addOne(5) 여기서 one이 없으니 외부에서 찾는다. 
```

![](../../.gitbook/assets/image%20%2839%29.png)



```javascript
function makeAdder(x){
    return function (y){
        return x + y
    }
}

const add3 = makeAdder(3);
console.log(add3(2));  // 5

const add10 = makeAdder(10);
console.log(add10(5)); // 15
console.log(add3(1)); // 4
```

