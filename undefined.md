---
description: 핵심 33개!
---

# 노마드

1화  
콜스택 \(call stack\) : 자바스크립트가 함수를 실행하는 핸들 방법  
하나씩 차근차근 하는 것  
리스트가 존재하고 함수는 리스트에 추가된다. 실행이 완료되면 함수는 리스트에서 제거된다.

2화  
기초타입?\(Primitive type\)  
String : " " or ' '  
Number : 정수 or 소수점  
Undefined : 정의가 되지 않음  
Null : 존재하지 않음으로 정의 됨  
NaN \(Not A Number\) : 숫자와 문자\(?\)가 계산식 오류인 것

```text
console.log(hello === undefined)           ->  true
console.log(hello === null)                ->  false
```



3화  Value // reference

```text
Value   :string,number,boolean,NaN,undefined,null 에서 가

let a = 50;
let b = a;
a = 10;
console.log(b);           -> 50




reference : array,object,function 에서 사

const sexy = ["kimchi", "potato"]
const pretty = sexy;
sexy.push("hello");
console.log(pretty)                  -> "kimchi", "potato", "hello"


const sexy = ["kimchi", "potato"]
const pretty = sexy;
sexy.push("hello");
pretty.push("lalala");
console.log(sexy)                     ->"kimchi", "potato", "hello","lalala"
```

4화

```text
console.log(4 + "hello");            -> 4hello
console.log(4 + 4 + "hello");        -> 8hello
console.log("" == true);             -> false
console.log(1 == true);              -> true
console.log(66 + true);              -> 67
console.log(66 + false);             -> 0


type conversion -> 자바스크립트가 값을 강제적으로 변환시킨다
console.log(66 + true); 에서 true를 1로 변환시켜 값이 67이 된다.

=== : 문자열까지 같은지 비교
!== : 문자열까지 다른지 비교

===를 사용
```



5화 typeof  
자바스크립트는 항상 type를 체크해야함 boolean, string, number 등등  
사용법 : ex\)  console.log\(typeof "121212" \)   하지만 버그가 있음.  
그래서 typeof 대신 instance of 를 사용함 둘이 비슷하지만 instance of에선 primitive\(string, boolean, number 등\) 에서 작동을 안함 하지만 object, array에선 작동함  
ex\) console.log\({} instanceof Array\)  
  
\* primitive \(number,boolean,string,undefined,function,string\) 는 typeof를 사용  
\* object array 는 instanceof를 사용



6화  scope

```text
if(true){
    const hello = "hi";
}
console.log(hello);   

이것은 if안에서만 hellow가 존재하기 때문에 에러. 이것이 scope.

scope의 핵심 variable이 존재하는가, 접근할 수 있는가 
```



7화  Expression // Statement  
  
Expression : value가 되는것.\(?\)

```text
function add(a,b){
    return a + b;
}

const how = add(5,6);
console.log(how)

이것이 expression. 이유는 위에 있는 코드를 리턴해서.
```

statement는 명령 혹은 지시  
ex\) if, else, else if, for, while 등  
  
function expression // function declaration                       이해X

```text
const awesome = add(1.5);

function add(a,b){
    return a + b;
}

console.log(awesome)            -> 6

이것이 function declaration
```

8화 IIFE \(Immediately - Invoked Function Expressions\)  
IIFE : 자기 자신을 일으키는 함수  
  
.........

